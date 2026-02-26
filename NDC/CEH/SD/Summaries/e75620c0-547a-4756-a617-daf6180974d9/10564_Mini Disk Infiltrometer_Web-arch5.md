# Mini Disk Infiltrometer

## Overview
- Instrument to measure soil unsaturated hydraulic conductivity using a tension infiltrometer.
- Suitable for field measurements, labs, and classrooms to demonstrate and quantify infiltration and hydraulic properties.
- Data collected feed into calculations of hydraulic conductivity, sorptivity, and related soil properties.

## Key Specifications
- Total length: 32.7 cm; tube diameter: 3.1 cm
- Sintered disk: 4.5 cm diameter, 3 mm thick
- Suction regulation tube: 10.2 cm
- Suction range: 0.5 to 7 cm
- Water reservoir: 21.2 cm; Mariotte tube: 28 cm
- Water required to operate: 135 mL

## How It Works
- Upper chamber (bubble chamber) controls suction; lower chamber infiltrates water into the soil.
- Water in the lower chamber infiltrates at a rate defined by the applied suction and soil properties.
- A porous disk at the bottom prevents air leakage; measurements are taken as water volume in the lower chamber decreases over time.
- Data are used to calculate hydraulic conductivity, typically via a spreadsheet macro.

## Preparation and Setup
- Fill the bubble chamber to three-quarters with non-distilled water (soil water preferred to avoid ionic balance changes).
- Fill the reservoir after setting suction and ensure zero suction offset (adjust mariotte tube position if needed).
- Refit the bottom elastomer and disk firmly; check for leaks with the device upright.
- For smooth contact, place the infiltrometer on a flat spot; use a thin layer of fine silica sand or diatomaceous earth if needed.
- Optional: use a ring stand and clamp to secure.

### Choosing the Suction Rate
- Default suction: 2 cm for most soils.
- For sandy soils with rapid infiltration, 6 cm can help.
- For compact soils with slow infiltration, 0.5 cm may be preferable.
- Adjustments beyond 2 cm should be done by experienced users.

## Placement and Data Collection
- Ensure solid contact with a smooth soil surface.
- Record starting water volume, then volumes at regular intervals.
- Interval timing depends on soil type and suction rate (e.g., sand: every 2–5 seconds; silt loam: every 30 seconds; tight clay: 30–60 minutes).
- Ensure at least 15–20 mL infiltrates per measurement for accuracy.
- Data are typically tabulated with time, volume, and infiltration depth.

## Data Processing and Infiltration Calculations
- 5.1 Use the Spreadsheet Macro: download from Decagon, input volumes, and use the auto-updating sqrt(time) and infiltration graphs to compute slope.
- 5.2 Calculate Infiltration:
  - I = C1 t + C2 sqrt(t) (Zhang 1997 method; good for dry soil infiltration)
  - Hydraulic conductivity k = C1 / A
  - A depends on van Genuchten parameters (n, α) and disk geometry (r0, ho)
  - For Mini Disk Infiltrometer: suction −0.5 to −6 cm, disk radius 2.25 cm
  - A values provided in Table 2 for 12 soil texture classes and various ho
  - If C1 is negative, data are inconsistent (likely due to shallow flow restrictions or movement during measurement)
  - For soils with n < 1.35, use Dohnal et al. (2010) modification to Zhang equation for improved k estimates

## Additional Calculations: Water Repellency Index
- Se and Sw are sorptivities derived from cumulative infiltration versus sqrt(time) for ethanol and water, respectively.
- Steps:
  - Fill reservoir with ethanol for ethanol sorptivity; keep bubble chamber with water; suction rate at 2 cm
  - Measure ethanol infiltration and compute Se from I = Se sqrt(t)
  - Repeat with water for Sw
  - Repellency index R = 1.95 × Se × Sw
- Cautions:
  - Ethanol can damage certain reservoir types; use only polycarbonate reservoirs produced after 2005
  - Ethanol/water measurements should be spatially separated to prevent interference

## Maintenance and Cleaning
- Clean all parts with mild soap and water.
- Disk is dishwasher-safe.
- If the suction tube is stiff, apply a small amount of vacuum grease to ease movement.

## Support and References
- Customer support: contact by email, phone, or fax with instrument serial number and problem description.
- Warranty: 1 year on parts and labor; coverage excludes ordinary wear, misuse, or external damage.
- References include foundational works on soil physics and methods for analyzing infiltration and sorptivity.

## Practical Considerations for Data Stewards
- Ensure measurement protocols and data formats are consistent across datasets (units, time intervals, volumes).
- Capture metadata: soil type, texture class, suction rate used, disk radius, ambient conditions, and instrument serial number.
- Maintain data provenance: document any calibration or offset adjustments (e.g., zero suction offset) and maintenance history.
- Integrate data with proper quality checks (look out for negative C1 values; flag anomalous infiltration curves).
- When sharing datasets, include methodological notes and the specific calculation approach (Zhang 1997 with or without Dohnal modification) and the A values used for the relevant soil texture.