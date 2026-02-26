# Stalybridge Rainfall and Discharge 2019-2022

## Overview
- Dataset of rainfall and runoff records from ten experimental microcatchments (A–J) on Stalybridge Moor, upland peatland, UK.
- Microcatchment sizes range from 0.4 to 3.9 hectares.
- Time period: 2019–2022 (pre-, during-, and post-gully blocking interventions).
- Purpose: evaluate the impact of different gully blocking methods on storm flow response.
- Data collection methods: v-notch weirs with pressure transducers for discharge; tip bucket rain gauges for rainfall.
- Data gaps occurred due to instrument failures.

## Experimental design and sampling
- BACI design: Before-After-Control-Intervention.
- Controls: microcatchments A, D, G, J (no gully blocking).
- Interventions:
  - B: 22 cobblestone dams.
  - C: 7 cobblestone dams (lower gully) + 13 peat dams (middle/upper reach).
  - E: 10 piped-peat dams.
  - F: 6 peat dams.
  - H: 6 peat dams.
  - I: 20 timber dams.
- Pre-intervention period: May 2019–March 2020.
- Gully blocking conducted 16–25 March 2020.
- Post-intervention period (records after March 2020) reflect gully blocking effects.
- Post-restoration design changes:
  - E (pipeds): 25/03/2020–22/02/2021 open pipes (diameter 150 mm; lower dam 64 mm); from 22/02/2021 all piped-peat dams capped at 64 mm.
  - I (timber): 25/03/2020–27/01/2021 timber dam slots 150 × 40 mm; 27/01/2021 lower dam slot narrowed to 50 × 40 mm; 29/03/2021 remaining timber dam slots reduced to 50 × 40 mm.
- Continuous measurements: May 2019–February 2022 (discharge and rainfall at 5-minute timesteps).
- Data gaps: due to instrument failures; rainfall gaps patched from nearest available microcatchment when a gauge failed.

## Collection, generation and transformation methods
- Discharge: v-notch weirs across erosional gullies; pressure transducers in stilling wells; barometric compensation using an above-water sensor for depth-to-height calibration.
- Rainfall: HOBO RG3-M rain gauges (186 cm² orifice; 0.2 mm resolution per tip).
- Calibration: manual stageboard readings and depth-to-height calibrations during data downloads.
- Data loggers downloaded monthly; field observations used to flag spurious readings (e.g., vegetation blocking the V-notch).
- Depth-to-discharge conversion: Q = 0.0167 × (100h)^(2.4331), where Q is in litres per second and h is water depth above the V-notch (in metres).

## Locations and spatial details
- Microcatchment outfalls and V-notch weirs located at specific UK grid references:
  - A: SE 00827 02191
  - B: SE 01024 02020
  - C: SE 01129 02063
  - D: SE 01252 02025
  - E: SE 01317 01925
  - F: SE 01386 01869
  - G: SE 02051 01444
  - H: SE 02421 01344
  - I: SE 02750 01345
  - J: SE 03111 01431
- Rain gauge locations (UK grid references):
  - B: SE 01022 02011
  - E: SE 01317 01913
  - G: SE 02040 01437
  - I: SE 02748 01339

## Data structure and units
- Recording cadence: 5-minute timesteps.
- Files: rainfall and discharge data provided per calendar year for each microcatchment.
- Filename convention: [site name]_[microcatchment name]_[year]_rainfall_discharge.csv
  - Example: stalybridge_e_2021_rainfall_discharge.csv
- CSV columns (same order in all files):
  - DateTime (GMT): YYYY-MM-DD HH:MM:SS (string)
  - Rainfall (mm): rainfall observations (float64)
  - Discharge (L/sec): discharge observations (float64)

## Quality control and data handling
- Discharge data visually reviewed for spurious values; cross-checked against rainfall context (e.g., vegetation blocking V-notch causing inflated readings).
- Periods with erroneous data omitted and flagged as no data.
- Rainfall data gaps were filled from nearest available microcatchment when a gauge failed.

## Analytical context
- The dataset supports analysis of how gully blocking and dam type influence stormflow and peak discharge in upland peat landscapes.
- Referenced methodology: Shuttleworth et al. (2019) on restoration delaying stormflow and reducing peak discharge.

## References
- Shuttleworth, E.L. et al. (2019) Restoration of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge, Journal of Hydrology X, 2, p. 100006. Available at: https://doi.org/10.1016/j.hydroa.2018.100006