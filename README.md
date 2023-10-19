# OP-LAMP

**Contributors: Dokyu Lee, Yejun Jang, Seungyeon Jung, Jaejun Kim (Professor)**

OP-LAMP is a project that synthesizes the voltages of two RC circuits to draw various curves in Lissajous figures. This includes the Cardioid, Epicycloid, and Epitrochoid curves.

## Overview

- **Cardioid Curve**: This curve is generated when a pink circle rotates around a yellow circle with a radius ratio of 1:1 or 2:1. The angular speed ratio between the two is 1:2. The resulting motion is represented by the equation:
  $$(cos(ωt) + 0.5cos(2ωt), sin(ωt) + 0.5sin(2ωt))$$

<img width="682" alt="Screenshot 2023-09-26 at 1 06 10 AM" src="https://github.com/codingJang/OP-LAMP/assets/56782623/5086cb85-f8df-44b3-9b35-26613a9d08f9">


- **Epicycloid & Epitrochoid Curves**: These curves are generated based on the size ratio of the two circles and the position of the tracing point on the pink circle.

<img width="1078" alt="Screenshot 2023-09-26 at 1 07 22 AM" src="https://github.com/codingJang/OP-LAMP/assets/56782623/c2315984-6011-433e-ae24-67c1d6a8529d">


## Experiments & Findings

During the breadboard demonstration, the following observations were made:
- The voltage of the first RC circuit corresponds to '1' and the voltage of the second RC circuit corresponds to '2'.

![Picture1](https://github.com/codingJang/OP-LAMP/assets/56782623/c1c30397-fc97-4f83-be2e-947d578ce599)

- When the input frequency of the second circuit was doubled, unexpected results were observed. This was due to the impedance of the capacitor decreasing with the increase in frequency, leading to a decrease in voltage across the capacitor.
  $$|R| = \left| \frac{1}{j\omega C} \right| \implies f \times R = \frac{1}{2πC}$$
  This led to a change in the circuit design.

## Final Design

The design was modified to allow for free changes in resistance. This made it possible to represent both the Epicycloid and Epitrochoid curves.

![Picture3](https://github.com/codingJang/OP-LAMP/assets/56782623/8a462b67-cf97-4e0f-91d9-18fab7461341)

![Picture5](https://github.com/codingJang/OP-LAMP/assets/56782623/e54a8605-d394-400c-ae18-780ac2be6c44)

## Conclusion

Using the RC circuit and the inverting summing amplifier circuit, we successfully constructed and implemented a circuit that can freely express the Cardioid curve, including the Epicycloid and Epitrochoid curve families, as Lissajous figures. Although currently limited to the Epicycloid/Epitrochoid curve families, theoretically, by adding countless circular motions of different frequencies, we can always represent a curve of finite length. To implement this, we are considering using devices that generate high frequencies, like a modified oscillator, and then using counter circuits to downscale and convert to sinusoidal waves for synthesis.

