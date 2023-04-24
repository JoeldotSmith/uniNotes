# Sinusoidal Steady State
### Sinusoidal sources
- Anysignal that can be represented as sinusoid:
  - wave like

- A very common type of signals - "harmonic signals", have a range of applications 
  - power transmission
  - communications
  - acoustic signals
  - any other signal that can be decomposed as a harmonic series

A harmonic signal $s(t)$ is mathematically represented as a function of time, $t$, as:
$$
s(t) = A\sin(\omega t+ \phi)
$$
Where:
  - $A$, Amplitude
  - $A_{pp} = 2A$, peak to peak amplitude
  - $\omega = 2\pi f$, angular frequency
  - $f = \frac{1}{T}$, frequency
  - $T$, period
  - $\phi$, phase shift
  
##### Example: mains AC power (single phase)
- Mains power in Australia is defined as 240V RMS, at 50Hz, what does this mean?
  - sinusoidal waveform
  - frequency $f = 50$Hz
  - period of 20ms
  - RMS amplitude of 240V. So waveform amplitude of $240\sqrt{2}\approx340V$

##### Basic relationships of relavance
###### Sine-Cosine relationship
$ A\cos(\omega t) = A\sin(\omega t+\frac{\pi}{2})$
###### Derivatives
$$s(t) = A\sin(\omega t+\phi) \rArr \frac{ds(t)}{dt} = A\omega \cos (\omega t + \phi)$$
$$
s(t) = A\cos(\omega t +\phi) \rArr \frac{ds(t)}{dt} = -A\omega \sin(\omega t+\phi)
$$

###### Integrals
$$s(t) = A\sin(\omega t +\phi) \rArr \int s(t)dt = -(\frac{A}{\omega})\cos(\omega t+\phi)+C$$
$$s(t) = A\cos(\omega t +\phi) \rArr \int s(t)dt = (\frac{A}{\omega})\sin(\omega t+\phi)+C$$

##### Phase lead and lag
The cosine curve is the same as the sine curve but shifted to the left .
In other words the trace of the cosine curve begins "earlier".
For time-varying signals as shown, we can say the phase of the cosine is ahead or leading the sine curve.

The phase pf the cosine leads the sine bu $\pi/2$. Alternatively, the phase of sine lags cosine by $\pi/2$.

Since this is a repetitive signal, you could equivalently say sine leads consine by $3\pi/2$.

