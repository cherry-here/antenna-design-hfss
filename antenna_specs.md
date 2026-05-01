# Microstrip Patch Antenna Design - ANSYS HFSS

## Design Specifications
| Parameter | Value |
|-----------|-------|
| Operating Frequency | 2.4 GHz (WiFi/Bluetooth band) |
| Substrate | FR4 Epoxy |
| Dielectric Constant (er) | 4.4 |
| Substrate Height (h) | 1.6 mm |
| Loss Tangent (tan d) | 0.02 |
| Patch Material | Copper (sigma = 5.8e7 S/m) |

## Calculated Dimensions (Transmission Line Method)

### Effective Dielectric Constant
ereff = (er+1)/2 + (er-1)/2 * [1 + 12h/W]^(-0.5)
ereff = 4.09

### Patch Width (W)
W = c/(2f) * sqrt(2/(er+1))
W = 38.0 mm

### Effective Length
Leff = c/(2f*sqrt(ereff))
Leff = 29.5 mm

### Length Extension (DeltaL)
DeltaL = 0.412h * (ereff+0.3)(W/h+0.264) / (ereff-0.258)(W/h+0.8)
DeltaL = 0.74 mm

### Final Patch Length (L)
L = Leff - 2*DeltaL
L = 28.0 mm

## Ground Plane Dimensions
- Length: 60 mm (L + 6h each side)
- Width: 48 mm (W + 6h each side)

## Feed Method
- Coaxial probe feed
- Feed point: (L/4, W/2) from edge
- Feed location optimized for 50 ohm impedance match

## HFSS Simulation Results
| Parameter | Simulated | Target |
|-----------|-----------|--------|
| Resonant Frequency | 2.41 GHz | 2.4 GHz |
| Return Loss (S11) | -28.5 dB | < -10 dB |
| Bandwidth (-10dB) | 48 MHz | > 30 MHz |
| VSWR | 1.08 | < 2 |
| Gain | 6.2 dBi | > 5 dBi |
| Efficiency | 87% | > 80% |

## Radiation Pattern
- E-plane (phi=0 deg): Broadside radiation, 3dB beamwidth = 74 deg
- H-plane (phi=90 deg): Symmetric, 3dB beamwidth = 82 deg
- Front-to-back ratio: 14 dB

## HFSS Setup Notes
- Solution type: Modal
- Frequency sweep: 2.0-2.8 GHz, 801 points
- Mesh: Auto + manual refinement at feed point
- Radiation boundary: lambda/4 from patch on all sides
- Convergence: DeltaS < 0.01

## Author
**Mothi Charan Naik Desavath** - RF and Antenna Design