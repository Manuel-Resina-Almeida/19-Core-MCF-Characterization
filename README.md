# 19-Core Multicore Fiber (MCF) Characterization

This repository contains the technical report and experimental data for the laboratory characterization of a 19-core Multicore Fiber (MCF). The project evaluates the viability of MCFs as a solution for Space Division Multiplexing (SDM) to overcome the theoretical capacity limits of traditional single-mode fibers.

## 🔬 Overview

The physical characterization of the 20 km fiber was divided into two main activities:
1. **Attenuation Measurement:** Bidirectional evaluation of the attenuation coefficient across the C-band (~1550 nm) and O-band (~1310 nm) using an Optical Time-Domain Reflectometer (OTDR).
2. **Chromatic Dispersion Measurement:** Phase delay analysis using the **Modulation Phase Shift Method** across the C-band.

## 📊 Key Findings

* **Attenuation:** The O-band (1310 nm) exhibited higher propagation losses compared to the C-band (1550 nm). The experimental setup successfully isolated the Fan-In/Fan-Out (FIFO) insertion losses, which were calculated at approximately **1.8 dB per interface** (3.68 dB total).
* **Chromatic Dispersion:** The MCF demonstrated a linear growth in dispersion across the C-band. Experimental values ranged from **18.54 ps/nm/km** (at 1525 nm) to **21.28 ps/nm/km** (at 1570 nm).
* **Dispersion Slope:** Through linear regression, the dispersion slope was estimated at **0.061 ps/nm²/km**.

## 📡 Laboratory Setup & Equipment

The experimental setup utilized high-end telecommunications and photonics equipment to guarantee signal integrity and measurement precision.

### Activity 1: Attenuation (OTDR)
* **OTDR:** EXFO MaxTester 720C
* **Optical Power Meter:** VIAVI OLP-3x
* **Fiber:** 20 km 19-core MCF with FIFO interfaces

### Activity 2: Chromatic Dispersion (Modulation Phase Shift)
To accurately measure the phase delay, a 2 GHz RF sinusoidal signal was generated and modulated onto a tunable optical carrier. The signal's phase shift was then captured at the receiver.

* **Tunable Laser Source:** HP 8168E (Optical Carrier)
* **RF Signal Generator:** Keysight E8257D/67D (2 GHz modulating signal)
* **Electrical Amplifier:** PSPL5865 (12.5 Gb/s Driver)
* **Optical Modulator:** JDSU X5 Series (10 Gbit/s LN Intensity Modulator)
* **Optical Amplifier (EDFA):** JDSU Multiple Application Platform (Output: 17.850 dBm)
* **Photodetector (PIN):** Discovery Semiconductors DSC 30S/40S/50S
* **Oscilloscope:** Keysight Infiniium UXR-B Series (Real-Time Phase Delay Analysis)

*Note: An optical filter (Waveshaper 500B) was initially tested but bypassed after determining it had negligible impact on the high-power, low-noise received signal.*

## ⚙️ Methodology

### Modulation Phase Shift Method
The chromatic dispersion $D(\lambda)$ was calculated by measuring the time delay variation ($\Delta\tau$) of the 2 GHz modulated signal as the laser wavelength ($\lambda$) was swept in 0.2 nm increments. The system was successfully validated using a Standard Single-Mode Fiber (SSMF) before testing the MCF.

$$D(\lambda) = \frac{1}{L} \frac{d\tau}{d\lambda}$$
*(Where $L$ is the fiber length, $20 km$)*

## 📁 Repository Structure

* `/Report`: Full scientific report (Portuguese) detailing the procedures, theoretical background, and extended data tables.

## 👥 Authors & Acknowledgements

**Researchers:**
* Manuel Almeida
* Miguel Raamsdonk
* Rafael Custódio

**Supervision:**
* Dr. João Rebola
* Dr. Tiago Manuel Alves 

*Instituto Universitário de Lisboa (Iscte-IUL) - Telecommunications Networks Engineering*
