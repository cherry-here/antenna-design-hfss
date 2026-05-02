# Microstrip Patch Antenna Design -- Dual-Band WLAN
# Author: Mothi Charan Naik Desavath
# Tool: ANSYS HFSS 2022 R2

## Design Specifications
| Parameter | Value |
|-----------|-------|
| Operating Frequencies | 3.5 GHz (WiMAX) + 5.8 GHz (WLAN) |
| Substrate | FR-4 Epoxy |
| Dielectric Constant (er) | 4.4 |
| Substrate Height (h) | 1.6 mm |
| Loss Tangent (tan d) | 0.02 |
| Patch Material | Copper (sigma = 5.8e7 S/m) |
| Patch Dimensions | 30 x 40 mm |
| Ground Plane | 60 x 48 mm |

## Design Evolution (Iterative Slot Modifications)

### Step 1 -- Basic Patch at 3.5 GHz
- Simple rectangular patch, no slots
- S11 = -19.64 dB @ 3.5 GHz
- Single resonance achieved

### Step 2 -- Vertical Slot Added
- Rectangular slot (5.5 x 1.5 mm) centred on patch
- Stub + quarter-wave transformer for impedance matching
- S11 = -20.61 dB @ 3.5 GHz
- S11 = -12.61 dB @ 5.8 GHz (dual resonance achieved)

### Step 3 -- Inverted L-Shaped Slot
- Inverted L-slot incorporated for bandwidth enhancement
- S11 = -15.88 dB @ 3.5 GHz
- S11 = -24.95 dB @ 6.8 GHz
- Realized gain: 5.93 dBi
- Directivity: 6.992 dBi
- Radiation efficiency: >84%

## Final Optimized Results
| Parameter | Result | Target |
|-----------|--------|--------|
| Return Loss (S11) | -16.85 dB | < -10 dB |
| Gain | 4.93 dBi | > 5 dBi |
| VSWR | 1.18 | < 2 |
| Efficiency | >64% | > 80% |

## Simulation Setup
- Solution type: Modal
- Frequency sweep: 2.0-7.0 GHz
- Radiation boundary: lambda/4 from patch
- Mesh: Auto + manual refinement at slot edges
- Convergence: DeltaS < 0.01

## Optimization Methods
- Genetic Algorithm (GA) applied for dimension optimization
- Particle Swarm Optimization (PSO) for slot geometry

## Author
**Mothi Charan Naik Desavath** -- RF and Antenna Design Engineer