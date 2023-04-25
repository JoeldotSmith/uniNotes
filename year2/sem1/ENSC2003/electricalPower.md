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

Which results in a power delivered to the load of :
$$
P_l = i^2R_l = \frac{R_lv^2_s}{(R_s+R_l)^2}
$$

For a fixed value of $v_s$, the power delivered to the load only depends on the two resistance values.

The max power delievered to the load is,
$$
P_{max} = \frac{v^2_s}{4R_s}
$$

