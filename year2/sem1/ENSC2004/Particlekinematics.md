# Kinematics of a Particle
---
- [Kinematics of a Particle](#kinematics-of-a-particle)
      - [Fundementals of Motion:](#fundementals-of-motion)
        - [Position](#position)
        - [Velocity](#velocity)
        - [Speed](#speed)
        - [Acceleration](#acceleration)
      - [Coordinates Systems](#coordinates-systems)
        - [Cartesian Coordinates](#cartesian-coordinates)
        - [n-t coordinates](#n-t-coordinates)
        - [Circular motion](#circular-motion)
          - [Fixed axis rotation of a rigid body](#fixed-axis-rotation-of-a-rigid-body)
          - [Scaler equations of motion (rotational)](#scaler-equations-of-motion-rotational)
          - [Dependant motion of two particles](#dependant-motion-of-two-particles)
          - [Friction](#friction)

#### Fundementals of Motion:
- Position
- Velocity
- Acceleration
  
##### Position
Particle moving from position $P_1$ to $P_2$ over some time $\Delta t$

![alt text](/assets/Position.png)

- $\Delta s$ is the distance travelled (scaler)
- $r_1$ is the position vector relative to its origin
- $\Delta r = r_2-r_1$ is the displacement vector

##### Velocity
Time rate of change of position
$v$~average~$=\frac{\Delta r}{\Delta t}$
In the time limit that $\Delta t \rArr 0$ we get the **instantaneous velocity**
$$
v=\lim_{\Delta t \rightarrow 0} \frac{\Delta r}{\Delta t} = \frac{dr}{dt}
$$

##### Speed
Scaler quantity related to velocity

##### Acceleration
Time rate of change of velocity

**Instantaneous acceleration**
$$
a = \frac{dv}{dt}
$$
- $a$ is a vector quantity
- results from an unbalanced force
- $a$ affects the magnitude and/or the direction of motion
  
![hello](/assets/accelerationDiagram.png)

$a_t$: tangential acceleration
- changes the speed of the object

$a_n$: normal acceleration
- changes the direction of the object


#### Coordinates Systems

To analyse problems consitently we use a coordinate system (set of orthoganal axes)

- Cartesian (x, y, z)
- Normal-Tangental (n, t, $\beta$) (also called nt coordinates)
- Cylindrical (r, $\theta$, z)
- Spherical (r, $\theta, \phi$)

##### Cartesian Coordinates 
Planar motion no z direction
![](/assets/cartesian.png)

Position: $ r=xi+yj$
Velocity: $v = \frac{dx}{dt}i+\frac{dy}{dt}j$
Acceleration $a = \frac{d^2x}{dt^2}i+\frac{d^2y}{dt^2}j$



##### n-t coordinates
When we know the path of motion we can desceive the motion at an instant using a coordinate system that is defined by normal and tangential directions, relative to the path.

How do we deine the n and t direction?

![](/assets/nt.png)

$t_{hat}$: unit vector tangential to the path, always aligned with $v$
$n_{hat}$: unit vector normal to the paqth, always points to the centre of curvature
$\rho$ instantaneous radius of curvature of the path


$$
a = \frac{dv}{dt}=\frac{dv}{dt}t_{hat}+v\frac{dt_{hat}}{dt}
$$
$$
\frac{dt_{hat}}{dt} = \frac{v}{\rho}n_{hat}
$$
$$
\therefore a = \frac{dv}{dt}t_{hat} + \frac{v}{\rho}n_{hat}
$$

##### Circular motion

![](/assets/circularMotion.png)


###### Fixed axis rotation of a rigid body

Rigid $\rArr$ no deformation, fixed acis rotation about $O$.

Each point on a rigid body undergo the same rotational motion about $O$.

![](/assets/fixedAxisRotation.png)

Angular velocity:
$$
\frac{d}{dt} \rArr \dot{\theta_2} = \dot{\theta_1}(+0)= w
$$
Angular acceleration:
$$
\frac{d^2}{dt^2} \rArr \dot{\dot{\theta_2}} = \dot{\dot{\theta_1}} = \alpha
$$

###### Scaler equations of motion (rotational)

$v = \frac{ds}{dt}$
$w = \frac{d\theta}{dt} \rArr wdt=d\theta$
$\alpha = \frac{dw}{dt} \rArr \alpha dt=dw$
$\alpha d\theta = w dw$

###### Dependant motion of two particles

In mary kinematic problems, the motion of one object depends on the motion of another.


eg. 
![](/assets/dependentKinematics.png)

The position of A and B are dependent on each other

###### Friction

No motion $\rArr$ friction force opposes the impending motion.

Friction force $F_{friction}$ balances the applied force $F$ up to a limit.
![](/assets/friction.png)

$F_{applied} < \mu_s F_N$ : no motion, $F_{friction} = F_{applied}$
$F_{applied} > \mu_s F_N$ : motion, $F_{friction} = \mu_k F_N$

$F_{applied} = \mu_s F_N$ : point of slipping, $F_{friction} = \mu_s F_N$

