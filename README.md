# FlashForge ADV5M Pro Slicer Profiles

This repository contains optimized FlashSlicer configuration profiles for the **FlashForge ADV5M Pro** 3D printer.

## Overview

These profiles are carefully tuned to deliver consistent print quality and performance across various materials and use cases. Each profile is named following a standardized convention and is documented with its specific characteristics and recommended applications.

## Available Profiles

### 025_PLA_HighPresicion
- **Material:** PLA
- **Nozzle Diameter:** 0.25mm (fine detail nozzle)
- **Layer Height:** 0.1mm
- **Dimensional Accuracy:** XY: ±0.125mm, Z: ±0.05mm
- **Purpose:** High-precision prints with excellent detail and surface finish
- **Best for:** Miniatures, intricate designs, models requiring fine features
- **Key Features:** Reduced layer height, optimized speeds for detail retention, lower temperatures for dimensional accuracy

### 025_PLA_HighPresicion_FORSMALL
- **Material:** PLA
- **Nozzle Diameter:** 0.25mm (fine detail nozzle)
- **Layer Height:** 0.1mm
- **Dimensional Accuracy:** XY: ±0.125mm, Z: ±0.05mm
- **Purpose:** High-precision printing of small models
- **Best for:** Small miniatures, jewelry, tiny decorative objects
- **Key Features:** Fine layer height, conservative speeds, enhanced bridge capabilities for tiny spans, raft enabled for stability

### 06_PETG
- **Material:** PETG
- **Nozzle Diameter:** 0.6mm (standard nozzle)
- **Layer Height:** 0.2mm
- **Dimensional Accuracy:** XY: ±0.6mm, Z: ±0.1mm
- **Purpose:** Standard PETG printing with balanced quality and speed
- **Best for:** Functional parts, mechanical models, general-purpose printing
- **Key Features:** Moderate temperatures for PETG, reliable extrusion settings, optimized for strength

### 06_PETG_ECO
- **Material:** PETG
- **Nozzle Diameter:** 0.6mm (standard nozzle)
- **Layer Height:** 0.2mm
- **Dimensional Accuracy:** XY: ±0.3mm, Z: ±0.1mm
- **Purpose:** Economical PETG printing with reduced material usage
- **Best for:** Large prints, prototypes, when material cost is a concern
- **Key Features:** Fewer start and end layers, reduced infill density (15% vs 25%), lower shell count, maintains structural integrity while minimizing material waste

## Getting Started

1. Download the desired `.fcfg` profile file
2. In FlashSlicer, import the profile through **File > Load Profile** or drag-and-drop
3. Adjust model orientation and placement as needed
4. Review print settings before sending to printer
5. Send to FlashForge ADV5M Pro

## Profile Selection Guide

| Requirement | Recommended Profile |
|---|---|
| Maximum detail and surface quality | `025_PLA_HighPresicion` |
| Small miniature objects | `025_PLA_HighPresicion_FORSMALL` |
| Functional parts / general printing | `06_PETG` |
| Material efficiency / fast prints | `06_PETG_ECO` |

## Contributing

We welcome contributions to improve these profiles! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on submitting new profiles or improvements.

## Notes

- Always verify bed leveling before printing
- Ensure build plate is clean and properly adhered
- Temperature calibration may be needed based on your specific material batch
- Test first with smaller models before committing to large prints

## License

These profiles are provided as-is for use with FlashForge ADV5M Pro printers.
