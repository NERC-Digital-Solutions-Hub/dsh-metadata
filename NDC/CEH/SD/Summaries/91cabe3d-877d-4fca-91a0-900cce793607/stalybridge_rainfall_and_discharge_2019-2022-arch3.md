# Stalybridge Rainfall and Discharge 2019-2022

## Overview
- Dataset of rainfall and runoff from ten experimental microcatchments (A–J) on Stalybridge Moor, upland peatland, UK.
- Collected to assess how different gully blocking methods influence storm flow response.
- Study design employs Before-After-Control-Intervention (BACI) with four unrestored controls (A, D, G, J) and six intervention microcatchments implementing various dam types.
- Data period spans 2019–2021 for pre/post comparisons, with records continuing through early 2022 for some adjustments.

## Experimental design and sampling regime
- Microcatchments named A–J from west to east; A, D, G, J serve as unrestored controls.
- Intervention methods include:
  - B: 22 standard cobblestone dams
  - C: 7 cobblestone dams (lower gully) + 13 peat dams (upper/mid)
  - E: 10 piped-peat dams
  - F: 6 standard peat dams
  - H: 6 standard peat dams
  - I: 20 timber dams
- Pre-intervention period: May 2019–March 2020.
- Gully blocking conducted 16–25 March 2020; post-restoration records begin April 2020 for affected microcatchments.
- Post-restoration design changes included modifications to dam configurations (e.g., open pipe diameters and slot widths) in microcatchments E and I, implemented 2020–2021.
- Study focuses on how dam type and post-restoration adjustments affect stormflow generation.

## Data collection, processing, and methods
- Continuous measurements at 5-minute timesteps (May 2019–Feb 2022) using:
  - Discharge: v-notch weirs with pressure transducers in stilling wells; barometric correction applied using above-water sensor data.
  - Rainfall: tip bucket rain gauges (0.2 mm per tip).
- Data download and calibration:
  - Manual stageboard readings used to calibrate depth measurements to v-notch height.
  - Discharge computed with: Q = 0.01678 × (100 × h)^2.4331 (Q in L/s, h in meters).
- Data gaps:
  - Instrument failures caused irregular gaps; rainfall gaps filled by patching with observations from the nearest microcatchment when a gauge failed.
  - Some periods identified as spurious (e.g., vegetation blocking the V-notch) were flagged and omitted.

## Instrumentation and calibration
- Discharge monitoring: HOBO U20-001-04 pressure transducers; v-notch weirs with stage readings for calibration.
- Rainfall monitoring: HOBO RG3-M rain gauges with 186 cm² orifice; resolution 0.2 mm per tip.
- Calibration:
  - Temperature/pressure readings used to derive water depth; manual readings at download used for depth-to-height calibration.
  - Barometric compensation applied to convert absolute pressure to water depth.

## Data structure, units, and file organisation
- Data arranged per calendar year for each microcatchment in CSV format.
- Filename convention: [site name]_[microcatchment name]_[year]_rainfall_discharge.csv
  - Example: stalybridge_e_2021_rainfall_discharge.csv
- Columns (in order):
  - DateTime (GMT): timestamp (YYYY-MM-DD HH:MM:SS)
  - Rainfall (mm): rainfall observations (float64)
  - Discharge (L/sec): discharge observations (float64)

## Data quality, accessibility, and governance
- Quality control:
  - Visual checks of discharge against rainfall context to detect anomalies (e.g., obstructions causing spurious high readings); erroneous periods removed and marked as no data.
- Data completeness:
  - Record gaps due to instrument failure; rainfall data patched with nearby microcatchment observations when possible.
- Metadata and provenance:
  - Detailed description of site locations (UK grid references) and equipment.
  - Documentation of design changes to dam configurations and their dates.
- Data sharing and standards:
  - Clear data structure, units, and calibration methods facilitate reuse and reproducibility; alignment with project reporting needs (Protect-NFM, Shuttleworth et al. 2019).

## Notable references
- Shuttleworth, E.L. et al. (2019). Restoration of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge. Journal of Hydrology X, 2, 100006.