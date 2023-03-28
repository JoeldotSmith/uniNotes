# Powered and Non Linear Circuit Elements
---
- [Powered and Non Linear Circuit Elements](#powered-and-non-linear-circuit-elements)
    - [Basics](#basics)
    - [Abstraction](#abstraction)
    - [Non Linear Cicuit elements](#non-linear-cicuit-elements)
      - [Incremental/Dynamic resistance](#incrementaldynamic-resistance)
      - [Non linear sources](#non-linear-sources)
        - [Diodes](#diodes)
          - [Types](#types)
          - [The diode model equation](#the-diode-model-equation)

### Basics

  
|Linear   | Non linear |
|---|---|
|  Linear circuits comprise completely of linear circuit elements. Linear components described by linear I-V relationships. Described by linear Eqations| Non linear circuits consist of at least one non linear circuit elements.  Non linear components have non linear I-V relationships. Described by non linear equations |

### Abstraction
Can allow non linear circuits to be described by a seperate sets of linear equations in different regions of operation.

### Non Linear Cicuit elements
#### Incremental/Dynamic resistance
- If relationship is a straight line passing through origin, 
$$
R =\frac{v}{i}
$$
- In a non linear domain, 
$$
R(i) = \frac{dv(i)}{di}
$$

- For small changes $\Delta i$(i.e. $\Delta i << i$), we can estimate the resulting change in voltage as:
$$
\Delta v = R(I)\Delta i,\\
v = v_o+R(I)(i-i_o)
$$ 
- This a quazi-linear relationship, around the biasing point ($i_o, v_o$)

#### Non linear sources
All sources are in reality non linear although we use them in their linear range.

##### Diodes
###### Types
- Signal
- Power
- Special purpose diodes

###### The diode model equation
Ideal diodes characterized by the diode model equation

At room temperature, for silicon-based diodes, diode model equation becomes,
$$
u = \frac{v_d}{0.025}\\
v  = e^u-1\\
i_D = (I_s)^v
$$
$I_s$ is termed the *"saturation current"*, and is a function of temperature.
![](/assets/nonLinearElements1.png)

- $v_d>0 \rArr$ diode "forward baised"
- $v_d<0 \rArr$ diode "reverse baised"