# Electrical Power
---
#### Definition
The power supplied to or dissipated by the charges is the time rate of change of work.

$$
W = Qv
$$
$$
P = \frac{dW}{dt} = \frac{d}{dt}Qv = v\frac{dQ}{dt}+Q\frac{dv}{dt} = vi+q\frac{dv}{dt}
$$

$vi$: is the electrodynamic term, power imparted by virtue of moving changes, relevant to circuits
$Q\frac{dv}{dt}$: electrostatic term, power imparted on a fixed charge due to a change in voltage.

Ignoring the static term (we are talking about currents), we can write the power relevant to moving charge as:

$$
P = vi
$$
#####
Power in a resister (dissipation)
$$
P = i^2R
$$
$$
P = \frac{v^2}{R}
$$

#### Maximum power transfer theorem (resistive-only circuits)

- It is valuable to examine the transfer of power from one network to another.
- Under what conditions will maimum power be transferred from network S to network L?
- For this analysis, simplify the two networks:
  - Network S: replace with equivalent source voltage($v_s$) and equivalent resistance ($R_s$)
  - Network L: replace with equivalent resistance ($R_l$)

![](/assets/powerTransferTheorum.png)

The current through the circuit is then,
$$
i = \frac{v_s}{(R_s+R_l)}
$$







**IMPORTANT** $R_S = R_L$










Which results in a power delivered to the load of :
$$
P_l = i^2R_l = \frac{R_lv^2_s}{(R_s+R_l)^2}
$$

For a fixed value of $v_s$, the power delivered to the load only depends on the two resistance values.

The max power delievered to the load is,
$$
P_{max} = \frac{v^2_s}{4R_s}
$$

##### Practical applications
- This is a very low efficiency
- When a source can only supply very small power levels, we would accept this.
- We do not aim for maximum power transfer with large DC generators.
  - Very low efficiency of power transfer
  - Also potential for heating and damage to generator
- Large power applications value effiency over maximum power transfer

![](/assets/powerTransferQuestion.png)

a. For maximum power transfer $R_O = R_T = 2\Omega$
b.
$$
P_{max} = \frac{V^2_T}{4R_T} = \frac{10^2}{4*2}= 12.5W 
$$

c. $P_{RT} = 12.5W$, $\eta = \frac{P_{R_o, max}}{P_{R_o, max} + P_{RT}} = 50\%$

#### Instantaneous, peak, and average power.
- The current and/or voltage time varying - power is also a function of time.
- Instantanous power ($P(t)$) is defined as the power at a given moment in time.

$$
P(t) = v(t)i(t)
$$

- For a resistor
$$
P(t) = \frac{1}{R}v^2(t) = Ri^2(t)
$$

#### Root-mean-square (RMS)
- the RMS is a measure of *average signal*
- Sinusoidal signals spend as much time below zero as they do above
- Leads to potential illusion that the signal carries zero net power
- Consider power into a resistive load

$$
P(t) = \frac{v^2(t)}{R}
$$
- So power is proportional to the square of the voltage.
  - if voltage is a sinusoid power goes as
    - $v^2(t)= V^2\sin^2(\omega t +\phi)$
    - always above zero therefore non zero net power.


##### Instantaneous Power, of a squared sinusoid:
$$
P(t) = \frac{v^2(t)}{R} = \frac{V^2\sin^2(\omega t +\phi)}{R} = V^2(\frac{1-\cos(2\omega t+2\phi)}{2R})
$$

##### Peak Power:
$$
P_{pk}(t) = \frac{V^2}{R}
$$

##### Average power integrates over an entire period
$$
\rArr P_{avg} = \frac{1}{T}\int_{t =0}^T
 V^2(\frac{1-\cos(2\omega t+2\phi)}{2R}) = \frac{V^2}{2RT}(t|^T_0) = \frac{V^2}{2R}
 $$

- Let us define a new amplitude $V_{avg}$ such that $P_{avg} = \frac{V^2_{avg}}{R}$, (as for the DC signal case)

$$
V_{abg} = \sqrt{P_{avg}R} =\frac{V}{\sqrt{2}}
$$

- This gives a better measure of average power in the signal, and was obtain by taking the square-root of the mean of the square. i.e. Root mean square.

Define the Root Mean Square (RMS) amplitude, $V_{RMS}$ that is related to signal amplitude $V$, by:
$$
V_{RMS} = \frac{V}{\sqrt{2}}
$$

- Back to average power definition: average of power over a single period of oscillation
$$
P_{avg} = \frac{1}{T}\int_{t=0}^{T} P(t)dt
$$

- In a similar way, we can calculte RMS voltage and current (the root of the mean of the square)

$$
V_{RMS} = \sqrt{\frac{1}{T}\int_{t=0}^{T} v^2(t)dt}
$$
$$
I_{RMS} = \sqrt{\frac{1}{T}\int_{t=0}^{T} i^2(t)dt}
$$

- Note the above definitions of RMS apply for any periodic signal (not just sinusoid) and are ultimatly tied to power in a wave form.



Generalized circuit including reactive elements:

![](/assets/generalizedPower.png)

Where $$
I = \frac{\hat{V_S}}{\hat{Z_S}+\hat{Z_L}}
$$

without loss of generality we assume $\hat{V_S} = V_S \angle 0$

where $$
\tan(\alpha) = \frac{X_S+X_L}{R_S+R_L}
$$


So:
$$
P=\frac{V^2_SR_L}{(R_S+R_L)^2+(X_S+X_L)^2}
$$
To maximize $P$ with respect to $R_L$, we ned to maximize the numerator and minimize the denominatpr

1. Maximize $R_L$ whilst minimizing $(R_S+R_L)^2$ for only positive values of $R_S$ and $R_L$ for only positive values of $R_S$ and $R_L$
2. Minimize $(X_S+X_L)^2$, for any real valye of $X_S$ and $X_L$

Condition 2 is satisfied eg $(X_S+X_L)^2$ is minimized (zero) when $X_L = -X_S$

Resulting in $$
P = \frac{V_S^2R_L}{(R_L+R_S)^2}
$$

This is the same as the purely resistive case and is maximized when $R_L=R_S$

#### MAXIMUM POWER TRANSFER THEOREM (PHASOR FORM)

Power to load is maximized when $\hat{Z_L}= \hat{Z^*_S}$

And maximum power transferred to load is:

$$
P_{max} = \frac{V_S^2}{4R_S}
$$

Note this is only the resistive case when $X_L = X_S = 0$

#### Impedance matching

Consider a voltage source $\hat{V_S}$ with internal impedance $\hat{Z_S}$, supplying power to a load $\hat{Z_L}$

If the maximum power transfer condition is not satisfied we can surmise that the power delivered to the load with be lower than what is possible - lower power factor.

If we cannot change either the source or load impedance, how do you maximize power transfer

The question then arises can we improve power transfer by inserting a "matching network" between the source and load?

ie can we make the load and matching network together mimic the impedance required to satisfy maximum power transfer?

if matching network can be designed to be non-lossy (ie purely reactive), we could conclude that

- maximum power is supplied
- all that power must be dissapated in the load

![](/assets/matchingNetwork.png)

Examine the practival example of a radio transmitter with
- Deliverable maximum power of 10kW
- Frequency of 1000kHz
- Resistance of 50$\Omega$
- Supplying a radio antenna of impedance 250$\Omega$ (also purely reactive)

![](/assets/radioTransmitter.png)

The equivalent circuit is then 

![](/assets/equivalentCircuit.png)

What is $\hat{V_s}$
- max poewr delivered when $Z_L=Z_S^*$
- Max power delievered of 10kW implies 20kW generated (50% loss in $\hat{Z_S}$)

$$
P = \frac{V_S^2}{R}
\rArr 20000 = \frac{V_S^2}{100}
\rArr V_S = 1414V_{RMS}
$$

Now insert a proposed matching network 
- purely reactive 
- containing two reactive components $X_1$ and $X_2$

![](/assets/proposedMatchingNetwork.png)

Evaluate $\hat{Z_{in}}$

$$
\hat{Z_{in}} = jX_1 + jX_2 || 250 = jX_1 + \frac{j250X_2}{250+jX_2} = \frac{jX_1(250+jX_2)}{250+jX_2} + \frac{j250X_2}{250+jX_2}
$$$$
\hat{Z_{in}} = \frac{j250X_1+j250X_2-X_1X_2}{250+jX_2}
$$

Max power transfer $Z_{in} = Z^*_S = 50\Omega$

$$
\rArr j250X_1+j200X_2 -X_1X_2 = 12500
$$

Split real and imaginary parts and solve

$X_1 = \plusmn100$
$X_2 = \mp 125$

Say $X_1 = 100, X_2 = -125$

$$
f = 100kHz \rArr \omega  = 2\pi f = 6.28*10^6 rads/s
$$

$X_1>0 \rArr$ inductor: $X_1 = \omega L \rArr L = \frac{X_1}{\omega} = 100/6.28*10^6 = 16 \mu H$
$X_2 < 0 \rArr$ capacitor : $X_2 = -1/\omega C \rArr C = -1/\omega X_2 = 1/(6.28*10^6 * 125) - 1.27nF$

So the matched circuit is 
![](/assets/matchedCircuit.png)

