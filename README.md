# High-Fidelity-Audio-Amplifier-Design
---

This repository contains the design, simulation, and implementation details for a high-fidelity audio amplifier, developed as a project for the Department of Electronic and Telecommunication Engineering at the University of Moratuwa, Sri Lanka (EN2111). The amplifier is designed for home audio applications, providing clear, distortion-free sound by balancing performance and efficiency.

---

### Project Overview

<img src="https://github.com/user-attachments/assets/d7a64af2-820e-4f88-bbdb-3457a6baac7d" alt="Team Pixie Bots" width="600"/>

The project focuses on a **Class AB power amplifier** that aims to deliver optimal audio quality. The system is divided into several key stages:

* **Pre-Amplifier Stage:** This initial stage takes weak audio signals from sources like smartphones or audio players and boosts them to a suitable level for further processing. It uses a non-inverting operational amplifier configuration, specifically the **NE5532 op-amp**, known for its low noise and high fidelity. The gain is adjustable, ranging from 30 to 40, to accommodate various input signal strengths.
* **Tone Control Stage:** This stage provides users with manual control over the audio signal's bass, midrange, and treble frequencies. It incorporates low-pass, band-pass, and high-pass filters, each carefully designed with an NE5532 op-amp to ensure precise tonal adjustments across the audio spectrum. This allows for sound customization based on personal preference or the listening environment.
* **Power Amplifier Stage:** The core of the system is a **Class AB power amplifier**, responsible for driving an 8-ohm, 10-watt speaker. This topology was chosen for its balance of efficiency and linearity, minimizing crossover distortion while maintaining good power efficiency (around 78.5% maximum). The design incorporates complementary transistors (**2SD1047** and **2SB817**) suitable for audio applications, capable of handling the required power dissipation and current. Diodes (**1N4148**) and specific resistor and capacitor values are used for biasing and emitter degeneration to optimize performance.
---
### Pre Amplifier
<img src="https://github.com/user-attachments/assets/caabf5f3-b9e4-410e-b289-9c3265eca4f9" alt="Pre Amp" width="600"/>

---
### Tone Controller
<img src="https://github.com/user-attachments/assets/971d1a95-7232-4b01-9c22-736b5f88dbfc" alt="Tone Controller" width="600"/>

---
### Power Amplifier
<img src="https://github.com/user-attachments/assets/a4805fbd-fa30-46de-ab7f-4ec2790d5275" alt="Power Amp" width="600"/>

---

### Features

* **Adjustable Tone Control:** Independent control over bass, midrange, and treble frequencies.
* **Low-Noise Pre-Amplifier:** Ensures clean amplification of weak input signals.
* **Class AB Power Amplification:** Provides high fidelity with efficient power delivery, minimizing distortion.
* **Standard Speaker Compatibility:** Designed to drive 8-ohm speakers.
* **Regulated Power Supply:** Operates on a stable $\pm15V$ supply.
* **Negative Feedback Implementation:** Incorporated to reduce distortion and improve linearity across the full frequency range.
* **Robust Component Selection:** Utilizes high-performance audio-grade components like the NE5532 op-amp and specific power transistors.

<img src="" alt="Team Pixie Bots" width="600"/>

---

### Implementation and Validation

The amplifier system underwent a comprehensive design and validation process:

* **Circuit Design:** The circuits were designed with a focus on optimal performance for high-fidelity audio.
* **Simulation:** Extensive simulations were conducted using **LTspice** and **Proteus** software to verify circuit functionality, gain ranges, frequency responses, and distortion characteristics. For instance, the pre-amplifier's adjustable gain was confirmed, and the tone control's frequency response was analyzed across different settings. Maximum power dissipation for the power amplifier was calculated using **Maxima**.
* **Prototyping:** The designs were physically implemented on a breadboard to test their real-world performance.
* **Testing and Analysis:** Thorough testing evaluated key parameters such as gain, frequency response (20 Hz – 20 kHz), and output power (10W). **Total Harmonic Distortion (THD)** was a critical metric, with the goal of keeping it below 1%. Detailed analysis of harmonic and crossover distortion was performed, demonstrating how the Class AB topology and biasing techniques minimize these effects. Real-time THD measurements were compared against simulated values, validating the design and identifying areas for practical considerations.



The project successfully delivers a high-performance audio amplifier, achieving high fidelity output with THD typically below 0.1% under nominal operating conditions by minimizing both harmonic and crossover distortions through careful design choices, including local feedback loops and a VBE-multiplier bias network.


