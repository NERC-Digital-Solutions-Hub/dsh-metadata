# Operation Manual HYPROP

## Overview
- HYPROP is a fully automated system to determine soil hydraulic properties (water retention curve pF/WC and unsaturated hydraulic conductivity Ku) via evaporation.
- Uses two tensio shafts at different depths to measure matrix tensions as soil sample dries.
- Mass change (via a balance) and tensions are combined to generate data points, which HYPROP-FIT then analyzes.
- Two operating modes: multi balance (one balance per sensor unit) and single balance (one balance for multiple sensor units).
- Software tools: HYPROP-VIEW for data logging/management and HYPROP-FIT for data evaluation and exporting.

## What’s Included and Safety
- Included components: sensor unit with tensio shafts, HYPROP balance, saturation plate, refilling attachments, syringes, reservoirs, cables, and related accessories.
- Intended use: measure water retention and hydraulic conductivity as a function of water tension/content in soil samples.
- Safety: electrical safety per country codes; handle tensio shafts and ceramic tips with care; avoid introducing air/contaminants; ensure proper grounding and EMC compliance.

## How HYPROP Works
- Measures water tension at two depths in a saturating soil sample during evaporation.
- Whole-sample evaporation is tracked via mass loss; tensions are converted to a pF/WC curve and Ku curve.
- Tensions are transmitted through degassed water in tensio shafts to pressure sensors; proper degassing is essential to avoid air bubbles.
- The air entry point, water vapor pressure, and boiling delay influence the measuring range; typical ranges and boiling behavior are described.
- Output data points are processed to derive θ(h) (water content vs. tension) and K(h) (hydraulic conductivity vs. tension) curves.

## Measuring Process and Setup
- Preparation steps:
  - Saturate the soil sample in a sample ring using controlled water and ventilation.
  - Degas water for tensio shafts and sensor unit (two methods: HYPROP Refill Unit or syringes).
  - Implement tensio shafts into the sensor unit, ensuring air-free connections and monitored pressure rise.
  - Attach dirt protection and ensure all connections are bubble-free.
- Initial software setup:
  - Install HYPROP-VIEW and HYPROP-FIT; connect HYPROP balance to computer; ensure unique device IDs to avoid conflicts.
  - Configure measurement via wizard or manually; choose multi or single balance mode.
- Measuring sequence:
  - Saturate soil sample, prepare and fill the device, install tensio shafts, and connect to balance.
  - Start the measuring campaign; HYPROP records tensions at two depths and mass changes over time.
  - In multi balance mode, each sensor unit is paired with a balance; in single balance mode, weigh each sample manually as instructed.
- Optimal measuring curve phases (all four if air-free filling achieved):
  - Phase 1: regular measurement range (tensions rise toward boiling point).
  - Phase 2: boiling delay (ideal but not always present).
  - Phase 3: cavitation (water vapor formation; tension drops).
  - Phase 4: air entry (tensions drop toward zero as air enters; used for evaluation in some cases).
- Finishing a measurement:
  - Stop at cavitation for upper shaft, or, if using air entry point, wait until both shafts provide usable data; HYPROP-FIT can compute medial values when appropriate.
- Dry weight determination (post-measurement):
  - Weigh the dry soil after removing the sample ring; account for tare and any soil sticking to the sensor unit; adjust as needed for clayey soils.

## Data Generation and Analysis
- HYPROP produces time-series data: tensions at two depths and sample mass (depending on mode).
- HYPROP-VIEW handles data logging and device management; HYPROP-FIT performs parameter estimation and curve fitting.
- Data processing steps:
  - Interpolate raw data using Hermitian splines to create consistent time points.
  - Compute medial water content θi from mass data and sample volume.
  - Compute h i as the average tension from h1 and h2; derive θ(h) and K(h) via methods based on Darcy’s law and the Evaporation method.
  - Apply non-linear regression to fit standard soil hydraulic models (van Genuchten, Brooks-Corey, Kosugi, etc.) and optionally Peters-Durner-Iden (PDI) variants.
  - Use integral fitting where appropriate to avoid bias in coarse or structured soils.
- Output:
  - Discrete data points for retention and conductivity functions.
  - 100 time-point data set by default; adjustable by user.
  - Options to export results and, if applicable, add WP4 data points (wet/dry masses and corresponding pF values) with equal weighting in fitting.
- Data quality and workflow:
  - Ensure complete degassing and bubble-free sampling to maintain data validity.
  - Verify device connections and avoid interruptions during measuring to prevent data gaps.

## Modes: Multi Balance vs Single Balance
- Multi balance mode:
  - One balance per sensor unit; reduced manual weighing workload.
- Single balance mode:
  - One balance for multiple sensor units; manual sample weighing required (typically twice daily per sample).
- Setup considerations:
  - Properly connect balances and sensor units; ensure magneto cables are managed to avoid interference.
  - Prepare measurement data for each sample; in multi-mode, balances and sensor units appear in the device tree for management.

## Finishing a Measurement and Post-Processing
- Finishing options depend on data quality and phase completion:
  - Stop at end of phase 1 or 2 for simpler datasets, or include phase 3/4 when data quality allows.
  - HYPROP-FIT can use data points to fit retention and conductivity curves and export parameters.
- Dry weight data is essential for converting mass-based water content to volumetric water content; ensure accurate drying (105°C) and complete material collection.
- WP4 data integration:
  - If WP4 measurements are performed, combine WP4 dry mass and pF data with HYPROP data in HYPROP-FIT for enhanced fitting.

## Maintenance, Troubleshooting, and Care
- Common issues and remedies:
  - Tensio shaft remains dry: degas/fill shafts with degassed water; re-check connections.
  - Bubbles in tensio shafts: re-run filling procedure; inspect for leaks or damaged O-rings.
  - Tension values capped or erratic: verify air-free filling and seal integrity; inspect sensors and O-rings.
  - Pressure readings beyond acceptable range: reduce pressure via degassing; check for leaks or damaged shafts.
  - Data not recording: check USB connection and computer power settings (set to continuous operation for laptops).
  - Sensor unit cleaning: rinse with running water while keeping it upside-down; avoid disassembly of tensio shafts; dry thoroughly.
  - O-ring replacement: replace red O-rings if leakage is detected; use proper tool to avoid sensor damage.
- Routine upkeep:
  - Clean sensor unit and tensio shafts after use.
  - Store and protect from algae growth if unused for extended periods.
- Documentation and references:
  - HYPROP-FIT manual for evaluation details and fitting options.
  - Technical data and recommended models for curve fitting.

## Additional Notes and References
- Typical measuring ranges, units, and conversion notes (pF, hPa, kPa, MPa, %rF, etc.) provided for reference.
- Theoretical background and literature cited describe the evaporation method, model fitting, and validation (Wind, Schindler, Peters, Durner, Van Genuchten, Kosugi, etc.).
- For citation, use HYPROP Manual references as listed (UMS, 2015) and HYPROP-FIT/ZIP manuals.

## Technical Data (Selected)
- Tensio shafts: two depths; ceramic tips; degassed water required.
- Pressure range: approximately -0.3 to 3000 hPa (-0.3 to 300 kPa); temperature range -30 to 70 °C.
- Balance: 2200 g weighing range; 0.01 g readout; 0.01 g reproducibility; internal linearity.
- IP65 rated sensor unit; protect against water ingress during cleaning.
- Connectivity: USB to computer; device IDs must be unique to avoid collisions.