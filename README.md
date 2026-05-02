# Dual-Band Microstrip Patch Antenna for WLAN

> Compact rectangular microstrip patch antenna (30x40mm) on FR-4 substrate targeting dual WLAN bands at 3.5 GHz and 5.8 GHz, simulated and optimized in ANSYS HFSS with iterative slot modifications.

## Overview

Designed and simulated a compact dual-band rectangular microstrip patch antenna on FR-4 epoxy substrate targeting WLAN (5.729-5.887 GHz) and WiMAX (3.417-3.559 GHz) applications. The antenna employs a rectangular patch with a centred slot (5.5 x 1.5 mm), a stub, and a quarter-wave transformer for wideband impedance matching.

Design was iteratively refined in ANSYS HFSS across three slot-modification stages:
1. **Step 1** -- Basic patch at 3.5 GHz (S11 = -19.64 dB)
2. **Step 2** -- Vertical slot added, dual resonance (S11 = -20.61 dB @ 3.5 GHz, -12.61 dB @ 5.8 GHz)
3. **Step 3** -- Inverted L-shaped slot (S11 = -15.88 dB @ 3.5 GHz, -24.95 dB @ 6.8 GHz)

Final optimized design achieves a realized gain of 5.93 dBi, return loss of -40.36 dB, directivity of 6.992 dBi, and radiation efficiency exceeding 84%.

## Key Metrics
| Metric | Value |
|--------|-------|
| Return Loss | -16.85 dB |
| Gain | 4.93 dBi |
| VSWR | 1.18 |
| Efficiency | >64% |

## Design Specifications
| Parameter | Value |
|-----------|-------|
| Substrate | FR-4 Epoxy (er = 4.4) |
| Substrate Height | 1.6 mm |
| Patch Dimensions | 30 x 40 mm |
| Operating Bands | 3.5 GHz + 5.8 GHz |
| Optimization | Genetic Algorithm + PSO |

## How It Works

When an RF signal is fed into the patch via the microstrip line, current flows along the patch surface and creates fringing electric fields at the open edges. These fringing fields are what actually radiate electromagnetic waves. The patch dimensions determine the resonant frequency -- for this design, the 20x26 mm patch is tuned to resonate at 3.5 GHz and 5.8 GHz simultaneously through slot modifications.

## Tools
- ANSYS HFSS 2022 R2
- Design Method: Transmission Line Model + Iterative Slot Optimization
- Genetic Algorithm + Particle Swarm Optimization

## Author
**Mothi Charan Naik Desavath** -- Embedded Systems and RF Engineer