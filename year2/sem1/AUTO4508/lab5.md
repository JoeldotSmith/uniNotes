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
    }
}

```