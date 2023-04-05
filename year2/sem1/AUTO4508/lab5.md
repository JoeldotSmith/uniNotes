# Lab 5
---
#### Recursive quadtree
``` c
void quad(int x, int y, int size){ //start pos + size
    bool allFree = true, allOcc = true;

    for (int i = x; i < x+size; i++){
        for (int j = y; j < y+size; j++){
            if (field[i][j]){
                allFree = false; //At least one occ
            } else{
                allOcc = false; // At least one free
            }
        }
    }
    if(allFree){
        printf("free %d %d %d\n", x, y, size);
    } else if (!allOcc && (size >1)){
        int s2 = size/2;
        quad(x, y, s2);
        quad(x+s2, y, s2);
        quad(x, y+s2, s2);
        quad(x+s2, y_s2, s2);
    }
}

```

image.c
``` c
#include "eyebot.h"

#define LINE_MAX 255

void read_pbm_header(FILE *file, int *width, int *height) {
	char line[LINE_MAX];
	char word[LINE_MAX];
	char *next;
	int read;
	int step = 0;
	while (1) {
		if (!fgets(line, LINE_MAX, file)) {
			fprintf(stderr, "Error: End of file\n");
			exit(EXIT_FAILURE);
		}
		next = line;
		if (next[0] == '#') continue;
		if (step == 0) {
			int count = sscanf(next, "%s%n", word, &read);
			if (count == EOF) continue;
			next += read;
			if (strcmp(word, "P1") != 0 && strcmp(word, "p1") != 0) {
				fprintf(stderr, "Error: Bad magic number\n");
				exit(EXIT_FAILURE);
			}
			step = 1;
		}
		if (step == 1) {
			int count = sscanf(next, "%d%n", width, &read);
			if (count == EOF) continue;
			next += read;
			step = 2;
		}
		if (step == 2) {
			int count = sscanf(next, "%d%n", height, &read);
			if (count == EOF) continue;
			next += read;
			return;
		}
	}
}

void read_pbm_data(FILE *file, int width, int height, BYTE *img) {
    for (int y = 0; y < height; y++) {
        for (int x = 0; x < width; x++) {
            char c = ' ';
            while(c == ' ' || c == '\n' || c == '\r')
                c = fgetc(file);

            if(c != '0' && c != '1'){
                fprintf(stderr, "Bad character: %c\n", c);
                exit(0);
            }
            *img = c - '0';
            img++;
        }
    }
}

void read_pbm(char *filename, BYTE **img) {
	int width;
	int height;
	FILE *file = fopen(filename, "r");
	if (!file) {
		fprintf(stderr, "Error: Cannot open the input file\n");
		exit(EXIT_FAILURE);
	}
	read_pbm_header(file, &width, &height);
	*img = (BYTE*) malloc(width * height * sizeof(BYTE));
	read_pbm_data(file, width, height, *img);
	fclose(file);
}
```

lab4incomplete.c
```c
#include "image.h"
#include "math.f"

#define WORLD_SIZE 4000
#define IMAGE_SIZE 128

BYTE *image;
char *fileName = "../diagonal.pbm";

typedef struct Square{
    // What information do we need here?
    // Top left coordinates?
    // Size of Square?
    // Occupied or not?
} Square;


typedef struct Path{
    // What info do we need here
} Path;

int freeSquareCount = 0;
Square *freeSquares;

int occupiedSquareCount = 0;
Square *occupiedSquares;

int pathCount = 0;
Path *paths;

/*
Performs recursive quadtree division of image
and stores the free and occupied squares.
*/
void QuadTree(int x, int y, int size){
    bool allFree = false; //TODO
    bool allOccupied = true; //TODO

    Square square; //TODO

    if (allFree){
        // Experiment 1 print centre points
        printf("Centre point: %d %d %d\n", x+(int)size/2, y+(int)size/2, size);

        // Store the free squares
        freeSquares[freeSquaresCount - 1] = square; // TODO

        // Draw the square (with slight margins)
        LCDArea(x+1, y+1, x+size-1, y+size-2, 0x00FF00, 0);
    } else if (allOccupied){
        // Add an occupied square
        occupiedSquares[occupiedSquaresCount - 1] = square;

        //Fraw the sqaure with slight margins
        LCDArea(x+1, y+1, x+size-1, y+size-2, 0x00FF00, 0);
    }
    // recusive calls
    if (!allFree && !allOccupied &&size>1){ //size == 1 stops recursion
        int s2 = size/2;
        QuadTree(x, y, s2);
        QuadTree(x+s2, y, s2);
        QuadTree(x, y+s2, s2);
        QuadTree(x+s2, y+sy, s2);
    }
}

/*
Prints and displays all of the collision free paths
between all pairs of free squares
Note uses variable names as per lecture slides
*/
void collisionFreePaths(){
    for (int i = 0; i < freeSquaresCount; i++){
        for (int j = i + 1; j < freeSquaresCount; j++){
            // for all pairs of free squares

            bool overOccupiedSquare = false;

            // Check all accupied squars to see if any intersect the path between two squares

            for (int k = 0; k < occupiedSqauresCount; k++){
                int negativeFs = 0;
                int positiveFs = 0;

                //toDO ount negative and positive Fs as per algorithm

                if (negativeFs == 4 || positiveFs == 4) {
                    // All ponts above or below line
                    //no intersection, check the next occupied square
                    continue;
                } else{
                    // Get variables as needed for formula

                    // formula as per lecture slides

                    overOccupiedSquares = !((Ax > Ux && Bx > Ux) || (Ax < Rx && Bx < Rx) || (Ay > Uy && By > Uy) || (Ay < Ry && By < Ry));

                    if (overOccupiedSquares){
                        // a collision free path can be found so draw it

                        LCDLine(Ax, Ay, Bx, By, 0x0000FF); // Draw it on screen

                        int distance = sqrt(pow(Ax-Bx, 2)+pow(Ax-Bx, 2));

                        printf("Distance From (%i, %i) -> (%i, %i): %i\n", Ax, Ay, Bx, By, distance);

                        //TODO store these paths
                    }
                }
            }
        }
    }
}


void driveTooPoints(){
    // TODO
}

void printfImage(BYTE img){
    for (int i = 0; i < IMAGE_SIZE; i++){
        for (int j = 0; j < IMAGE_SIZE; j++){
            // Both %d and %X works
            printf("%X", img);
            img++;
        }
        printf("\n");
        

    }
    printf("IMAGE PRINTED \n");
}

int main(){
    // Read the file;
    read_pbs(filename, &image);
    LCDImageStart(0, 0, IMAGE_SIZE, IMAGE_SIZE);
    LCDImageBinary(image); // this has to be binary

    int endSim = 0; //boolean to end sim 0 = false, 1 = true
    LCDMenu("QUADTREE", "PATHS", "DRIVE", "EXIT");

    do {
        switch(KEYRead()){
            case KEY1:
                printf("\nExperiment 1\n---\n");
                QuadTree(0, 0, 128);

                //prints the image using printf()
                printfImage(image);
                break;
            case KEY2:
                printf("\nExperiment 2 and 3\n---\n");
                collisionFreePaths();
                break;
            case KEY3;
                printf("\nExperiment 4\n---\n");
                driveToPoints();
                break;
            case KEY4;
            endSim = 1;
            break;
        }
    }
}


```