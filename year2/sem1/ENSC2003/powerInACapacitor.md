# Power in a capacitor
---
#### Instantaneos power/energy in a capacityor

- Knowing v-i relationship for a capacitor

$$
i = C\frac{dv}{dt}
$$
$$
P = vi = Cv\frac{dv}{dt}
$$

- Note $Cv = Q$ we get back to electrostatic term in original derivation of power

$$
P = Q\frac{dv}{dt}
$$

$$
\rArr Pdt = Cvdv
$$

Energy store in electric fielf of capacitor by increasing voltage from zero to $v$:

$$
E = \int_0^t Pdt
$$

$$
\rArr E = \frac{1}{2}Cv^2
$$
Consider voltage applied to capacitor

$$
v(t) = V\sin(\omega t)
$$


Energy stored in capacitor varies with voltage waveform:

from $E = 0 \rightarrow E = \frac{1}{2}CV^2$
Energy is independant of sign (direction) of voltage

Note in a single complete voltage cycle the energy change in the capacitor is zero.

Energy cycles twice for a single cycle in voltage

What can w say about power in this case

**Energy stored and released (cycled) per half cycle in voltage**
$$
E_{cycle} = \frac{1}{2}CV^2
$$

**Average energy cycled per unit time(power)**

$$
E_{avg} = \frac{1}{2T}CV^2
$$

#### Instantaneous power/energy in an inductor

Knowing i - v relationship for an inductor
note implicit time dependance for convenience

$$
v = L\frac{di}{dt}
$$
$$
P = vi = Li\frac{di}{dt}
$$

Note $Li = \lambda \rArr$ is the equivalent magneto-static term to the electrostatic term
$$
P = \lambda \frac{di}{dt}
$$
$$
\rArr Pdt = Lidi
$$

Energy stored in a magnetic dield of inductor by increasing current from zero to i

$$
E = \int_0^t Pdt
$$

$$
E = \frac{1}{2} Li^2
$$

Consider current applied to inductor $i(t) = I\sin(\omega t)$

Energy stored in inductor varies with current waveform from $e = 0 \rArr e = 1/2Li^2$

Energy is independant of sign direction of current

$$
E_{cycle} = \frac{1}{2}Li^2
$$
$$
E_{avg} = \frac{1}{2T}Li^2
$$

# Power in the AC steady state.
---
Now consider the phase difference $\phi$ between the voltage and current signals within a circuit or circuit element.

$$
v(t) = \sqrt{2}V_{RMS}\cos(\omega t)
$$
$$
i(t) = \sqrt{2}I_{RMS}\cos(\omega t - \phi)
$$

Average power dissipated is
$$
P_avg = \frac{1}{T}\int_0^T v(t)i(t)dt \rArr = V_{RMS}I_{RMS}\cos(\phi)
$$

#### Complex power
Lets consider the general case: phasor $\hat{V} = V\angle\theta,$ phasor $\hat{I} = I\angle\phi$

Define complex power **S** as
$$
S = \hat{V}_{RMS}*\hat{I}_{RMS} = \frac{VI}{2}\angle(\theta - \phi) = P+jQ
$$

S has the units of Volt amperes, VA.

P=Re(S) = |S|cos($\theta - \phi$) is called the active power or real power and has the unit of Watt. Here , P equals to the $P_{avg}$ discussed before

Q = Im(S) = |S|sin($\theta - \phi$) is called the reactive power and has units of Volt Emperes, reactive (VAR)

The magnitude |S| of the complex power is called the apparent power, and the unit of Volt amperes VA

The ratio of active power to apparent power in a circuit is called the power factor


NOTE:

S = Complex power
P = Real power
|S| = Apparent power
Q = Reactive power

