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


##### Ohm's law

Based on the previous discussion we can simple re-state Ohm's law in the phasor representation in terms of imedance($\bar{Z}$), as
$$
\bar{V}= \bar{I}\bar{Z}
$$
Power()$\bar{P}$ can also be expressed in a phasor form:
$$
\bar{P} = \bar{V}\bar{I}
$$

Note, current voltage and power expressed here will have a phsae (which may be zero) and a time-dependance associated with it. While the time-dependence is hidden here, we are still evaluating instantaneous quantities. It is important to not confuse phasor quantities of voltage, current and power with average quantities.

![](/assets/phasorCurrenteg.png)

$\bar{V} = \bar{I}\bar{Z}$
$\bar{I}= \frac{\bar{V}}{\bar{Z}}$
$\bar{Z}= 2+j1 \space\Omega$
$\bar{V} = 10(\cos(0)+j\sin(0))= 10V$

$\bar{I}= \frac{\bar{V}}{\bar{Z}}=\frac{10}{2+j1}$
$$
\bar{I}= \frac{10}{2+j1}=\frac{10}{2+j1}*\frac{2-j1}{2-j1}=\frac{10(2-j1)}{(2+j1)(2-j1)}=\frac{10(2+j1)}{4+1}
$$
$$
\bar{I} =2(2-j1)=(4-2j)A
$$
$$
\bar{I} = 4-2j = |I|e^{j\theta} = \sqrt{4^2+-2^2}e^{j\arctan(\frac{-2}{4})}
$$
$$
\bar{I} = 4.47e^{j(-26.6°)}
$$

##### Combining impedances
Impedance has the same functional dependence to voltage and current as does resistance. Therefore, their combinations will happen in exactly the same way:

**Series combinations of N impedances:**
$$
\bar{Z_r} = \sum_{i=1}^{N} \bar{Z_i}
$$
**Parralel combinations of N impedances:**
$$
\frac{1}{\bar{Z_r}} = \sum_{i=1}^{N} \frac{1}{\bar{Z_i}}
$$

##### Componants of impedance
- Consider impegance looking into two terminals A-B of the circuit shown
  
![](/assets/impedanceEg.png)

$$
\bar{Z} = j\omega L+R_1+R_2 = (R_1+R_2)+j(\omega L)
$$
Therefore $\bar{Z}$ = Re{$\bar{Z}$} + jIm{$\bar{Z}$}

- WE say that the impedance consists of a resistive part and a reactive part.
- Alternatively: R is the resitance and X is the reactance.. Both have units of Ohms($\Omega$)

##### Concept of Admittance
- Remember conductance, $G=1/R$, the inverse parameter of resistance, which makes the inverse form of Phm's law easier to work with: $i = vG$
- Conductance in parallel also simply add:
$$
G_{r, parallel} = \sum_{n=1}^{N}G_n
$$

- Similarly we can define the inverse parameter of impedance as Admittance: ($\bar{Y}$)
- Which allows the inverse forms of Ohm's law to be written as:
$$
\bar{I} = \bar{Y}\bar{V}
$$
- and admittances sum as:
$$
\bar{Y_{T, parallel}} = \sum_{n=1}^{N} \bar{Y_n}
$$
##### Componants of Admittance
- Consider impedance looking into two terminals A-A' of the circuit shown:

![](/assets/admittanceEG.png)

$$
\bar{Y} = j\omega C + G_1+G_2 = (G_1+G_2)+j(\omega C)
$$
Therefore, $\bar{Y} =$ Re{Y} + j Im{Y} = $G + jB$

- Alternatively: G is the coductanve and B is the susceptance. Both have units of Mho($\mho$) or Siemens(S).
- Note, $\bar{Y} = G+jB = |Y|e^{j\phi_Y}$
  - $\bar{Y}$ is the phasor quantity,
  - $|Y|, \phi_Y, G$ and $B$ are all real-valued quantities and not phasors.
  - $|Y|$ is the magnitude of the phasor $\bar{Y}$
    - $|Y| = \sqrt{G^2+B^2}$
  - The phase angle $\phi_Y$ is obtained by,
    - $\tan(\phi_Y)=\frac{B}{G}$
  - Note also,
    - $G = \frac{R}{R^2+X^2}$
    - $B = \frac{-X}{R^2+X^2}$

#### Circuit analysis using phasors

We have used various techinques in past chapters in particuler they were:
- Ohm's law
- KCL
- KVL
- Nodal Analysis
- Mesh Analysis
- Superposition
- Thevenin's theorem
- Norton's theorem
- source transformations
- voltage divider.

All of these techniques can be used to solve for phasor potential differences and currents in a circuit, by treating the impedances in a similar way we treated resistances.

However, we must remeber we are only looking at the sinusoidal steay state solution. Furthermore, when we solve for phasors in the circuit we are doing so only at the specific frequency of the source, $\omega$. Additionally all sources need to be of the same frequency $\omega$ when solving for a particular phasor.

##### Example node to datum analysis
- Similar to the time-domain representation, we define one node as the datum with $\bar{V_D} = 0$
-  All other nodes voltages are then defined with respect to $\bar{V_D}$
-  Note, all node voltafes are ohasor quantities and the voltage are generally complex valued
-  Working with impedances is perfectly possible in NTD analysis
-  However working with admittances may make the algebra somewhat less difficult, particulary with complex number in the mix.
-  Compare: $\bar{I} = \frac{\bar{V}}{\bar{Z}} $ with $\bar{I} = \bar{V}\bar{Y}$

##### Source transformation
- Phasor-domain circuits may be simplified using source transformation, in much the same way as in the time-domain
- A voltage source with an output impedance can be replaced witha current source and an output admittance, as shown, without an attached circuit experiencing a difference in source behaivour

![](/assets/phasorST.png)
- Be careful you remember phasors are complex quantities and the algebra is adjusted accordingly