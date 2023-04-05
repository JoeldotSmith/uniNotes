# Examples
---
![](/assets/COMexamples1.png)
#### Question
Find the forces and moment at D and E

#### Know
Provided with diagram of a compound beam w/supports dimensions and loads.

#### Find
Internal forces at D and E


#### Diagram
Note: important to split at compound beam joint in this case @ B
![](/assets/COMexamples2.png)


#### Analysis
##### Assumptions
- Rigid Body
- Static Equilibrium
- Massless Beams

##### Stategy
1. Solve for support reactions
2. Solve for the internal forces at D
   - Cut at D and use LHS
3. Solve for internal forces at E
   - Cut at E and use LHS

##### Working
Step 1
From (b)
$$
+\rightarrow \sum F_x = 0 = B_x
$$
$$
+(ac)\sum M_C = 0 = -200 -B_y(4)\\
B_y = -50N
$$
$$
+\uparrow \sum F_y = 0 = B_y + C_y\\
C_y =50N 
$$

from (a)
$$
+\rightarrow \sum F_x = 0 = A_x
$$
$$
+\uparrow \sum F_y = A_y -B_y - 800\\
A_y = 800+ (-50)\\
\therefore A_y = 750N 
$$
$$
+(ac)\sum M_A = 0 = A_m - 800(4)-B_y(8)\\
A_m = 3200 + (-50*8)\\
\therefore A_m = 2800Nm
$$

Step 2
![](/assets/COMexamples3.png)

$$
+\rightarrow \sum F_x = 0= N_D
$$
$$
+\uparrow \sum F_y = 0 = A_y - V_D\\
V_D = A_y = 750N
$$
$$
+(ac)\sum M_D = 0 = A_m -V_D(2) + M_D\\
M_D = (750)(2)-2800\\
\therefore M_D = -1300Nm
$$

Step 3

![](/assets/COMexamples4.png)

$$
+\rightarrow \sum F_x = 0 = N_E\\
$$
$$
+\uparrow \sum F_y = - = B_y - V_E\\
V_E = -50N
$$
$$
+(ac)\sum M_E = 0 = -V_E(2)+M_E\\
M_E = V_E(2) = (-50)(2)\\
\therefore M_E = -100Nm
$$