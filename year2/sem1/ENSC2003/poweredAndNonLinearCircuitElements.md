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
        - [Operational Amplifiers](#operational-amplifiers)
          - [Ideal operation amplifier model](#ideal-operation-amplifier-model)
          - [Negative feedback](#negative-feedback)
          - [Inverting configuration](#inverting-configuration)
          - [Non inverting configuration](#non-inverting-configuration)

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

##### Operational Amplifiers
###### Ideal operation amplifier model

The name came from the analogue computer industry where they were used to perform mathematical opertations.

![](/assets/nonLinearElements2.png)

Open loop systems has no feedback
Closed looped systems have feedback

###### Negative feedback

The gain of the op-amp circuit is generally denoted by $A_v$;
$$
A_v = \frac{v_o}{v_i}
$$
Rules for ideal op-amps in negative feedback:
1. The two input terminals are at the same voltage eg. $V_+=V_-$
2. The inputs draw zero current eg. $I_+=I_-=0$

###### Inverting configuration

KLC at inverting input:
$$
\frac{v_- -v_i}{R_1}=\frac{v_o - v_-}{R_f}=0\\
V_- = V_+=0\\
\rArr v_o=-\frac{R_f}{R_1}v_i
$$
So the circuit gain:
$$
A_v = \frac{v_o}{v_i}=-\frac{R_f}{R_1}
$$

**$A_v$ is determined by the ration of $R_f$ and $R_1$ instead of A, which removes the signal distortion!**

###### Non inverting configuration

KLC at inverting input:
$$
\frac{v_- - 0}{R_1} = \frac{v_o-v_-}{R_f}\\
V_- = V_+ = V_i
\rArr v_o=(1+\frac{R_f}{R_1})v_i
$$
So, the circuit gain:
$$
A_v = \frac{v_o}{v_i}= 1+\frac{R_f}{R_1}
$$