# OpenStint Loop Preamplifier Board

The **OpenStint Loop Preamplifier Board** is an optional front-end module, designed for the [OpenStint Laptimer System](https://github.com/zsellera/openstint).  
It provides signal conditioning and amplification for the inductive loop sensor, ensuring clean, stable, and maximized signal transfer to the timing receiver.

## 🔧 Features

- Fully compatible with the OpenStint timing receiver interface. Operated from the bias-tee available on HackRF One and RTLSDR.
- Output is matched to 50 Ohm.
- +12 dB gain low-noise amplifier
- Fits Hammond's 1590L-style aluminium cases
- Power pin available for 1S batteries (remove `L6` or `FB2` in this case, or add DC-block capacitor before the SDR).
- Open hardware design – schematics and PCB available under permissive license
- Directly manufacturable at JLCPCB (LCSC part codes provided).

## ✳️  Overview

The loop preamplifier is built around 4 key functional stages:

1. **Balanced–Unbalanced Conversion**  
   Converts the differential loop input into a single-ended signal. It has some input protection that can also clamp the input signal in case of close transmitters.

2. **Matching Network**  
   Optimizes impedance matching between the loop and the amplifier for maximal power transfer and improved sensitivity.

3. **+12 dB Low-Noise Amplifier (LNA)**  
   Boosts the signal with minimal added noise, ensuring reliable lap detection even under low signal conditions.

4. **Band-pass filter**
   SDRs unfortunatelly downconvert out-of-band signals to basebands (like harmonics of LO). This filter does some justice, and is probably the most important contribution of this preamp board.

## Schematics
<img width="1156" height="345" alt="image" src="https://github.com/user-attachments/assets/7bbb96dc-14c6-4cbb-804f-48a8de589aaa" />


---
Part of the OpenStint Laptimer System – open, modular, and precise RC timing.

