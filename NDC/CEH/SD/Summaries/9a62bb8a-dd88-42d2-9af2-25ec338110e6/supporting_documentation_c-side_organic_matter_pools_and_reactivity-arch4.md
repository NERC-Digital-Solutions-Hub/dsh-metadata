# Project Carbon Storage in Intertidal Environments (C-SIDE)

## Overview
- Project: Carbon Storage in Intertidal Environments (C-SIDE)
- Funded by: NERC (NE/R010846/1)
- Objective: quantify three pools of organic matter (labile, recalcitrant, refractory) in UK saltmarsh soils
- Scope: 1211 down-core soil samples collected across UK saltmarsh sites (2018–2021); includes a measure of organic matter reactivity via the Carbon Reactivity Index (CRI)

## Data assets

- Dataset title: C_SIDE_organic_matter_pools_and_reactivity.csv
- Content: observations of core-level organic matter pools and CRI
- Observations: 1211 down-core samples from UK saltmarsh sites; site selection aimed to represent UK saltmarsh habitat diversity
- Variables/parameters observed:
  - Latitude (decimal degrees)
  - Longitude (decimal degrees)
  - Core depth (cm)
  - Labile organic matter (%wt)
  - Recalcitrant organic matter (%wt)
  - Refractory organic matter (%wt)
  - Total organic matter (%wt)
  - CRI (carbon reactivity index)
- Site metadata: Saltmarsh name; Core_ID
- Location data: Site coordinates provided in WGS84
- Data format: CSV
- Data quality: Calibration and QA procedures described; laboratory practices followed at University of St Andrews

## Methods and quality

- Analytical technique: Thermogravimetric Analysis (TGA) using Mettler Toledo TGA2
- Sample prep: approximately 20 mg, freeze-dried and milled; placed in 70 mL crucibles
- Thermal program: 40°C to 1000°C at 10°C/min under N2
- Data processing: thermograms adjusted to a common temperature scale; clipped to 200–650°C; normalized to mass loss for comparability
- OM fraction definition (thermally defined):
  - Labile OM: 200–400°C
  - Recalcitrant OM: 400–650°C
  - Refractory OM: 550–650°C
- CRI calculation: CRI = %OM_R / %OM_total (interpreted as a continuum from highly biodegradable (CRI near 0) to non-biodegradable (CRI near 1))
- Calibration: analyses performed with standard substances of known thermal characteristics
- Quality control: laboratory equipment calibrated according to University of St Andrews practices

## Data structure and metadata

- File: C_SIDE_organic_matter_pools_and_reactivity.csv
- Core Identification: Core_ID (text)
- Spatial data: Saltmarsh name (text); Latitude (decimal degrees); Longitude (decimal degrees)
- Depth data: Depth interval of sub-sample (cm); Depth interval mid-point (cm)
- Observed variables (percent mass): Labile_OM_Perc; Recalcitrant_OM_Perc; Refractory_OM_Perc; Total_OM_Perc
- Reactivity: CRI (dimensionless)
- Data dictionary notes: Units and formats provided (e.g., Lat/Long in decimal degrees, OM percentages as %wt, CRI as a reactivity index)

## Access, usage, and reuse

- Data format: CSV with clearly defined columns and units
- Site coverage: UK saltmarsh environments, selected to capture environmental diversity and enable cross-site comparability
- Temporal coverage: Samples collected 2018–2021
- Documentation: includes methodological details, calibration procedures, and references to foundational work

## References

- Kristensen, E. (1990). Characterization of biogenic organic matter by stepwise thermogravimetry (STG). Biogeochemistry, 9(2), 135-159.
- Smeaton, C. & Austin, W.E.N. (2022). Quality not quantity: Prioritizing the management of sedimentary organic matter across continental shelf seas. Geophysical Research Letters, 49(5), e2021GL097481.