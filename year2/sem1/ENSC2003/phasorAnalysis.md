# Phasor analysis
---
**Can ONLY be aplied to Sinusoidal Steady State**


#### Phasor analysis
- Assumes the enture curcuit operates at a single (fixed) angular frequency $\omega$.
- The parameters allowed to change are the amplitude, and the phase angle.
- The beaty of pahsor representation is that we are actually representing something physical by the imaginary part of the complex number.

#### The phasor
- A sunusoidal varying parameter can generally given by:
  - $v(t) = V_o\cos(\omega t+\phi)$
- Represented by the quantity
  - $V=V_oe^{j(\omega t +\phi)} = V_o\cos(\omega t+\phi)+jV_o\sin(\omega t+\phi)$
    - With $v(t)=$Re{V}

##### Representation on the complex plane
- $V_oe^{j(\omega t +\phi)} = V_oe^{j\omega t}e^{j\phi}$ is the *Rotating phasor*
- $\bar{V} = V_oe^{j\phi}$ is the *Phasor* (ommiting $e^{j\omega t}$ term)


- Alternative representation of a phasor
  
  1. $\bar{V} = V_o \angle \phi$ (Polar form)
  2. $\bar{V} = V_o\cos\phi+jV_o\sin\phi$ (cartesian form)
   
Note, there is no time dependant term remaining in the expression of a phasor. It has been completely removed.
The only information remaining in the phasor is the amplitude $V_o$ and the phase $\phi$.
However, angular frequency $\omega$ is assumed. So time-domain signal can always be recovered:
$v(t)=$ Re{$\bar{V}e^{j\omega t}$}

There is a one to one correspondence between a time-domain sinusoid and its phasor representation.

Given one, you can always obtain the other. You can transfer from one to the other.
![](/assets/phasorRep.png)
![](/assets/phasorRes.png)
![](/assets/phasorCap.png)
![](/assets/phasorInd.png)


##### Generalized "impedance"
- Above analysis shows that in the phasor-representaion, resistance, capacitance and inductance all behave as if they were a *resistance-like* entity.
- We use the term *impedance* when referring to this resistace like quantity
- Similar to conductance, the inverse of impedance is admittance.
- Impedance has units of Ohms($\Omega$) and us generally given the phasor symbol $\bar{Z}$
- Admittance has units of Mho($\mho$) or Siemens(S) and is given the phasor symbol $\bar{Y}$

| Type  |  $\bar{Z}$ |$\bar{Y}$|
|---|---|---|
| Resistor, R  | $R$  |$1/R$|
| Capacitor, C  | $1/j\omega C$  | $j\omega C$ |
| Inductor, L  |  $j\omega L$ | $1/j\omega L$ |
