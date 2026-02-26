# Project Carbon Storage in Intertidal Environments (C-SIDE)

## Overview
- A dataset describing three pools of organic matter (labile, recalcitrant, refractory) and carbon reactivity in UK saltmarsh soils, collected from 2018 to 2021.
- Aims to support consistent representation of environmental condition and enable monitoring of soil organic matter dynamics over time.

## Dataset scope and contents
- Contains 1211 down-core soil samples from UK saltmarsh sites.
- Measured variables include: labile OM (%wt), recalcitrant OM (%wt), refractory OM (%wt), total OM (%wt), and carbon reactivity index (CRI).
- Includes core metadata and a CRI-based reactivity continuum.

## Sampling locations and design
- Geographic extent covers UK saltmarsh regions with sites chosen to represent diverse but comparable conditions along the coastline.
- Locations provided as decimal degrees (WGS84) with four corner coordinates listed: 
  - 60.973491, -8.019200
  - 60.973491, 2.176113
  - 49.844006, -8.019200
  - 49.844006, 2.176113
- Data include site saltmarsh name and precise lat/long for each sub-sample.

## Observed variables
- Core identification (Core_ID)
- Saltmarsh name
- Latitude (Lat_dec_deg)
- Longitude (Long_dec_deg)
- Depth interval of sub-sample (cm)
- Depth interval mid-point (cm)
- Labile organic matter (%wt)
- Recalcitrant organic matter (%wt)
- Refractory organic matter (%wt)
- Total organic matter (%wt)
- CRI (Carbon reactivity index)

## Laboratory methods and data processing
- Thermogravimetric Analysis (TGA) of freeze-dried, milled samples (~20 mg) in crucibles.
- Heating from 40°C to 1000°C at 10°C/min under nitrogen.
- Thermograms adjusted to a common temperature scale and clipped to 200–650°C; values normalized to mass.
- OM fractions defined thermally: labile (200–400°C), recalcitrant (400–550°C), refractory (550–650°C); updated ranges used for CRI calculation.
- CRI calculated as CRI = %OM_R / %OM_total, representing a continuum from fully biodegradable (0) to non-biodegradable (1).
- Calibration performed with standard substances; QA includes equipment calibration per University of St Andrews guidelines.

## Calibration and quality control
- Thermogravimetric analyses calibrated against known standards.
- Laboratory equipment calibrated to standard practices; data checks align with QA procedures.

## Data format and file details
- Primary dataset file: C_SIDE_organic_matter_pools_and_reactivity.csv
- Key fields include: Core_ID, Saltmarsh name, Lat_dec_deg, Long_dec_deg, Depth_interval_cm, Depth_midpoint_cm, Labile_OM_Perc, Recalcitrant_OM_Perc, Refractory_OM_Perc, Total_OM_Perc, CRI
- File format: CSV
- Metadata supports integration with environmental data portals and standardised analyses.

## Data usage and accessibility
- Dataset is prepared to support standardized reporting of environmental condition and carbon storage potential in intertidal saltmarsh soils.
- Accompanied by methodological details and references to enable reproducibility and cross-study comparisons.

## References
- Kristensen, E. (1990). Characterization of biogenic organic matter by stepwise thermogravimetry (STG). Biogeochemistry, 9(2), 135-159.
- Smeaton, C., & Austin, W.E.N. (2022). Quality not quantity: Prioritizing the management of sedimentary organic matter across continental shelf seas. Geophysical Research Letters, 49(5), p.e2021GL097481.