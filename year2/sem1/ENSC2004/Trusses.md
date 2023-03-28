# Trusses
- [Trusses](#trusses)
      - [Lab 1](#lab-1)
      - [Beam Bending](#beam-bending)
        - [Internal forces](#internal-forces)
      - [Shear force and bending moment diagrams.](#shear-force-and-bending-moment-diagrams)

#### Lab 1

Weeks 5 and 6
first week calculations and predictions
second week testing

Assessment

- Group submission(recorded powerpoint and pdf with calculations)
- Individual quiz

![alt text](/assets/truss_example.png)

#### Beam Bending

##### Internal forces

Unlike trusses, beams dont just stretch and compress under load, they bend under transverse loads.

###### eg. 1
![alt text](/assets/BeamBendingeg.png)
![alt text](/assets/BeamBendingCont.png)

$$
\sum F_x = 0 = -30(3)+B_y(6)\\B_y = 15kN
$$

$$
\sum F_y = 0 = A_y + B_y -30\\A_y = 15kN
$$

Cut the beam into a section.

![alt text](/assets/cutSection.png)

There is a missing vertical force which is a **internal shear force** on the cut section donoted V.

$$
\therefore+\uparrow \sum F_y = 0= A_y -5 +V\\\therefore+\uparrow \sum F_y= 0=(15)-5+V\\\therefore+\uparrow \sum F_y= 0=10+V\\\therefore V = -10
$$

Similarly for the cut section there will be an **internal bending moment** (M).

$$
+(ac)\sum M = 0=(-10)(1)=5(0.5)+M\\M = 12.5kNm
$$

For RHS you will get the same result but opposite direction for static equilibrium.

#### Shear force and bending moment diagrams.

Consider the example above but for an arbitary cut at x.
![alt text](/assets/sheerForce.png)
![alt text](/assets/bendingMoment.png)

$$
V(x)=\frac{d}{dx}M(x)
$$


###### eg.2

1. Solve the reaction forces at the supports

![alt text](/assets/trussesEg2.png)

$$
+\rightarrow \sum F_x = 0 = A_x\\
\therefore A_x = 0
$$
$$
+(ac) \sum M_A = -F_L(6)+B_y(9)\\
\therefore B_y = 19kN
$$
2. Take a cut through the beam at position x

![alt text](/assets/trussesEg2_1.png)

$$
+\uparrow \sum F_y = 0 = A_y -V-F_L1\\
V = A_y - F_L1x\\
V = 9-\frac{x^2}{3}
$$

$$
 +(ac)\sum M_c = 0 = -A_y(x)+F_l1x(\frac{x}{3})+M\\
 M=A_yx-F_l1x(\frac{x}{3})\\
 \therefore M = 9x - \frac{x^3}{9}
$$
![](/assets/trussesEg2_2.png)
![](/assets/trussesEg2_3.png)