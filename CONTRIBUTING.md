# Contributing Guidelines

Thank you for your interest in contributing to the FlashForge ADV5M Pro slicer profiles collection! This document outlines how to properly add new profiles and improvements.

## File Naming Convention

All profile files must follow this naming convention:

```
{NOZZLEWIDTH}_{MATERIAL}_{DESCRIPTION}.fcfg
```

### Components:

- **NOZZLEWIDTH**: The nozzle diameter in millimeters without unit (e.g., `025`, `04`, `06`, `08`)
  - Format: Use zero-padded three digits (e.g., `0.25mm` → `025`)
  
- **MATERIAL**: The primary material this profile is for (e.g., `PLA`, `PETG`, `TPU`, `ASA`)
  - Use uppercase material abbreviation
  
- **DESCRIPTION**: Brief characteristic or use case of the profile (e.g., `HighPresicion`, `ECO`, `Fast`, `Draft`)
  - Use CamelCase for readability
  - Should be descriptive but concise (max 20 characters)

### Examples:

- `025_PLA_HighPresicion.fcfg` - Fine detail PLA profile with 0.25mm nozzle
- `06_PETG_ECO.fcfg` - Economical PETG profile with 0.6mm nozzle
- `04_TPU_Flexible.fcfg` - Flexible TPU profile with 0.4mm nozzle

## Adding a New Profile

### Step 1: Create and Test
1. Create your profile in FlashSlicer with optimized settings
2. Export the profile following the naming convention
3. Thoroughly test the profile on multiple prints
4. Document your findings

### Step 2: Update README

When adding a new profile, add an entry in the **Available Profiles** section of `README.md` with the following information:

```markdown
### {FILENAME_WITHOUT_EXTENSION}
- **Material:** {Material name}
- **Nozzle Diameter:** {Nozzle size}mm ({nozzle type})
- **Layer Height:** {Layer height in mm}
- **Dimensional Accuracy:** XY: ±{nozzle size}mm, Z: ±{layer height/2}mm
- **Purpose:** {Brief one-line purpose}
- **Best for:** {Target use cases}
- **Key Features:** {Comma-separated list of notable settings or characteristics}
```

Example:
```markdown
### 04_TPU_Flexible
- **Material:** TPU
- **Nozzle Diameter:** 0.4mm (standard nozzle)
- **Layer Height:** 0.15mm
- **Dimensional Accuracy:** XY: ±0.4mm, Z: ±0.075mm
- **Purpose:** Flexible and elastic prints with good layer adhesion
- **Best for:** Phone cases, gaskets, flexible hinges
- **Key Features:** Higher extrusion ratio (1.15), lower speeds (30-40 mm/s), enhanced retraction settings
```

### Step 3: Submit

- Place the `.fcfg` file in this directory
- Update `README.md` with profile information
- Consider submitting additional notes about:
  - Material brand/grade tested with
  - Bed and nozzle temperature ranges
  - Speed recommendations
  - Known limitations or special considerations

## Profile Documentation Standards

When describing profiles in README.md, include in this order:

1. **Material**: The filament material type
2. **Nozzle Diameter**: The size and type of nozzle this profile uses
3. **Layer Height**: The configured layer height in mm
4. **Dimensional Accuracy**: XY accuracy (±nozzle width) and Z accuracy (±layer height/2)
5. **Purpose**: What the profile is optimized for (one clear statement)
6. **Best for**: Target use cases and applications
7. **Key Features**: 3-5 important configuration notes

### Dimensional Accuracy Formula

- **XY-axis accuracy**: ±(nozzle width / 2) - accounts for nozzle extrusion width
- **Z-axis accuracy**: ±(layer height / 2) - accounts for layer stacking tolerance

Examples:
- 0.25mm nozzle with 0.1mm layers → XY: ±0.25mm, Z: ±0.05mm
- 0.3mm nozzle with 0.2mm layers → XY: ±0.3mm, Z: ±0.1mm

Example of a well-documented profile:
```
### 06_PETG_ECO
- **Material:** PETG
- **Nozzle Diameter:** 0.6mm (standard nozzle)
- **Layer Height:** 0.2mm
- **Dimensional Accuracy:** XY: ±0.6mm, Z: ±0.1mm
- **Purpose:** Economical PETG printing with reduced material usage
- **Best for:** Large prints, prototypes, when material cost is a concern
- **Key Features:** Fewer start and end layers, reduced infill density, lower shell count, maintains structural integrity while minimizing material waste
```

## Testing Requirements

Before submitting a profile, ensure:

- ✅ Profile has been tested on actual FlashForge ADV5M Pro hardware
- ✅ At least 3+ successful test prints completed
- ✅ Print quality meets intended purpose
- ✅ No adhesion, extrusion, or layer separation issues
- ✅ First layer adheres correctly
- ✅ No stringing or excessive oozing problems
- ✅ Profile name follows naming convention exactly

## Quality Standards

Profiles should demonstrate:

- Consistent extrusion and layer bonding
- Appropriate surface finish for the intended use case
- Reliable bed adhesion without plate damage
- No jams or nozzle clogs during prints
- Print times within reasonable expectations

## Profile Variations

When creating variations of existing profiles (e.g., optimized for speed, draft quality, or specific material brand):

1. Use descriptive suffix in the description component
2. Example: `06_PETG_ECO`, `06_PETG_Fast`, `06_PETG_Draft`
3. Document differences in README relative to the base profile

## Questions or Issues?

If you have questions about:
- **File naming**: Review the convention examples above
- **What to document**: See the Profile Documentation Standards section
- **Testing requirements**: Check the Testing Requirements section

## Important Notes

- All profiles must be compatible with **FlashForge ADV5M Pro** printer
- Profile files must be in **FlashSlicer .fcfg format**
- Only well-tested, stable profiles are accepted
- Profiles that reduce print quality for marginal speed gains will not be accepted
- Always test on actual hardware, not just simulations

---

Thank you for contributing to better printing experiences for the FlashForge ADV5M Pro community!
