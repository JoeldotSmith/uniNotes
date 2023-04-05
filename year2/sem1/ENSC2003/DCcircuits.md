# DC Cicuits including storafe elements
---
#### Long term bs short term energy storage
- Long term
  - Chemical battery
  - super conducting batteries
  - hydro potential engery
  - melted sald
We are now covering a group of elemets that can prove some degree of energy stores, 
- for a short amount of time
- within an electrical cicuit

#### Time varying electrical sources

##### Background 
- most electrical/ electronic engineering deals with time-varying voltages/currents
##### Switching on and off DC sources
- Very common function in electrical engineering switch turned on at $t = 0$

##### Define **Unit Step Function**
![](/assets/USF1.png)

- Express $v_o(t)$ as 
$$
v_o(t) = 2u(t)
$$

- Note, irrespective of what the argument ($x$) is , $u(x)$ is zero when $x<0$, and 1 when $x \geqslant 0$
- Let us consider what happs when $x = t-5$ ie. $v_o(t) = 2u(t-5)$

![](/assets/USFDiagram.png)

- This is a *shifted unit step*, ie. switch is turned ON at $t = 5$ so $u(t-T)$ provides switch ON behaivor at $t = T$


- A *negative step function* provides a step down
  - eg. $v_o(t)=2(u(t)-u(t-5))$
  - ![](/assets/USFDiagram2.png)


#### Stores in electric fields

$$
E(t)= \int P(t) dt = \frac{1}{2}C(V_c(t))^2
$$

- Capacitance relates to the voltage $v$ applied to the chage $q$ generated
  
$$
C = \frac{q}{v}
$$
$$
q = Cv
$$

##### Symbol

- Commom implimentation of a capacitor is a pair of paralell plates.
![](/assets/pPlates.png)
- Symbol is some varient of a pair of parralell plates

![](/assets/CapacitorTypes.png)

##### Series combinations of capacitors
$C_r$: Effective total capacitance of combination
$\frac{dv}{dt} = v$
$$
i = C_r \frac{dv}{dt}\\
\rArr i = C_r (\frac{dv_1}{dt} + \frac{dv_2}{dt})\\
\rArr i = C_r(\frac{i_1}{C_1} + \frac{i_2}{C_2})
$$
But $i_1 = i_2 = i$
$$
\rArr \frac{1}{C_r} = \frac{1}{C_1} + \frac{1}{C_2} 
$$

**Capacitors in series combine like resistors in parralel**

Therefore N capacitors in series:
$$
\frac{1}{C_r} = \sum_{i = 1}^{N} \frac{1}{C_i}
$$

#### First order RC Cicuits

**DC Steady state all voltage and current sources**

When we insert a capacitor into a simple circuit: