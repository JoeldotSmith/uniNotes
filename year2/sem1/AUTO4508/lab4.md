# Lab 4
---
#### Distbug

- Garentees Convergence
- Similar to wandering stand point algorith but boundary-following stops only if goal is directly reachable or if future hit point witht next obstable would be closer to goa. This information together with detection of unreachable goal if robot has turned 360° garentees convergence.

- Requires positioning accuracy


##### Algorithm

0. initialize i = 0 and STEP
1. Increment i and **move toward the target** until:
   - The target is reached, Stop.
   - An obstacle is hit. Denote this point $H_i$. Go to step 2.
2. Turn left and follow the obstacle boundary whilst continuously updating freespace to target F and min. value of $d(x, T)(=d\scriptscriptstyle min$$(T))$. Repeat until the following occurs:
   - The target has been reached. Stop
   - The target is visable, $F \geqslant d(x, T)$ **F in target dir.** Mark this as point $L_i$. Go to step 1.
   - A position closer to the goal can be reached: $$d(x, T)-F \leqslant d\scriptscriptstyle min  - STEP$$ **F in target dir** denote this point $L_i$. Go to step 1.
   - The robot reached $H_i$ The target is unreachable. Stop



##### Code
Distbug written "pretty clearly" in text book.


```c
int DistBug(int x, int y);
//desired relative goal coord. [mm] x in rob's forward dir.
//return true when goal is reached; false if goal is unreach
```

obstacles.sim
```text
world obstacles6k.wld

marker 500 500 0 255 0
marker 5500 5500 255 0 0

S4 500 500 0
```

drive.py
```python
from eye import *

def main():
    for i in range(0, 2):
        VWStraight(500, 50)# 0.5m is 5s
        while (not VWDone()):
            x, y, p = VWGetPosition()
            LCDPrintF("X:%4d; Y:%4d; P:%4d\n;", x, y, p)
            if (PSDGet(2)<100):
                VWSetSpeed(0, 0) # Stop if obstacle in front
                VWTurn(180, 60)# Turn 180° in 3s
                VWWait()
```



distbug_incomplete.py
``` python
from eye import *
import math

GOAL_X = 3000
GOAL_Y = 3000

STEP = 1000

def get_relative_goal_location(x, y) -> (int, int):
    # As per lecture slides
    distance = 0 = TODO # can use math.sqrt() to figuire out distance to point
    rot = 0 = TODO # use atan2 function

    return distance, rot

def check_at_point(x, y, goal_x, goal_y) -> bool:
    return False # TODO 

def dist_bug(x, y):
    while True:
        # Drive towards goal
        # TODO
        # Get curent position
        currentXPosition, currentYPosition, currentAngle = VWGetposition()

        # Check if at goal
        if check_at_point(currentXPosition, CurrentYPosition, x, y):
            return True
        
        # Obstacle collision
        obstacle_detected = False # TODO
        if obstacle_detected:
        VWSetspeed(0, 0)
        # Store hit position
        hit_x, hit_y, hit_angle = VWGetPosition()

        hit_point = [currentXPosition, currentYPosition]

        minimum_distance = math.inf
        left_hit_point = False

        # Turn left so that wall can be followed

        while True:
            # boundary following
            # TODO: follow the boundary (adjust direction each time this loop executes)
            # Remember make this non-blocking

            # If back at hit point return False
            at_hit_point = False # TODO
            if at_hit_point:
                return False

            distace, angle = get_relative_goal_location(x, y)

            # Store minimum distance to goal
            if distance < minimum_distance:
                minimum_distance = distance
            
            # Space in direction to Goal
            angle_to_goal = 0 # TODO calculate the angle in the direction of the goal

            lidar_values = LIDARGet() # returns [100, 998, ....., 700, ... 99]

            # angle to the goal is 90° to the right 
            # Then straight ahead, is the 180th index, need to check the 180+90th = 270th element
            free_space_to_goal = lidar_values[angle_to_goal] # index 180 is straight ahead

            if distance = free_space _to_goal <= minimum_distance - Step:
                #leave the obstacle
                break # Go back to driving towoards the goal

dist_bug(GOAL_X, GOAL_Y)
VWSetSpeed(0, 0)
```