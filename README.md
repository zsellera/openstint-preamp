# OpenStint Loop Preamplifier Board

The **OpenStint Loop Preamplifier Board** is an optional front-end module, designed for the [OpenStint Laptimer System](https://github.com/zsellera/openstint). It provides signal conditioning and amplification for the parallel-wire "antenna", ensuring clean, stable, and maximized signal transfer to the timing receiver.

<img width="800" alt="openstint preamp, rev 1." src="https://github.com/user-attachments/assets/124f38fc-45e9-4060-b4db-2ab19285af84" />


## 🔧 Features

- Fully compatible with the OpenStint timing receiver interface. Operated from the bias-tee available on HackRF One and RTLSDR.
- Output is matched to 50 Ohm.
- +12 dB gain low-noise amplifier
- Fits Hammond's 1590L-style aluminium cases
- Power pin available for 1S batteries (remove `L6` or `FB2` in this case, or add DC-block capacitor before the SDR).
- Open hardware design – schematics and PCB available under permissive license
- Directly manufacturable at JLCPCB (LCSC part codes provided).

## ✳️ Measurement Results

The following measurements were made at the `VNA_IN` port (after the balun).

**POWER GAIN**
<img width="954" height="885" alt="image" src="https://github.com/user-attachments/assets/e1d99bb5-b01f-4508-aae7-5364899a0f6a" />

**INPUT MATCHING**
<img width="1640" height="726" alt="image" src="https://github.com/user-attachments/assets/c65f61b1-97e2-4e6c-9c82-a492dd5fa86e" />


## Schematics
<img width="1156" height="345" alt="image" src="https://github.com/user-attachments/assets/7bbb96dc-14c6-4cbb-804f-48a8de589aaa" />

## 🗺 Roadmap / Project ideas

Add an optional 75 Ohm output as well, or add a separate 50 to 50+75 splitter. This hardware change should have a software counterpart, which reads both the OpenStint and MyLaps decoders, and merges the results into a single stream for laptiming applications. We could keep both open and commercial transponders to co-exists on the same track this way. Also, upgrading post-4.4 firmware won't be such a headache neither.

Automatic gain control: even a simple one could increase the dynamic range of the decoders.





---
Part of the OpenStint Laptimer System – open, modular, and precise RC timing.

