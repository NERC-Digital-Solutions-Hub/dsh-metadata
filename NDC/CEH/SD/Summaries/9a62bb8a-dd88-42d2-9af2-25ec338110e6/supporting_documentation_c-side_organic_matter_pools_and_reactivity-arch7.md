# Project Carbon Storage in Intertidal Environments (C-SIDE)

## Overview
- Funding: NERC (NE/R010846/1)
- Purpose: Dataset detailing three pools of soil organic matter (labile, recalcitrant, refractory) and a carbon reactivity index (CRI) for UK saltmarshes (2018–2021)
- Spatial scope: Observations across UK saltmarsh sites with coordinates in WGS84; approximate bounding box includes lat/longs around UK coast
- Output format: CSV data file with accompanying data dictionary

## Spatial Data & Geography
- Location data: Site coordinates as decimal degrees (lat/long) in WGS84
- Spatial coverage: Sites selected to span UK saltmarsh habitats and to enable comparability across similar environmental regions
- Data granularity: Point-level observations linked to core samples; depth information included for sub-samples

## Data Content & Variables
- Core information: Core_ID, Saltmarsh name, Latitude (Lat_dec_deg), Longitude (Long_dec_deg), Depth interval (Core_depth_cm), Depth midpoint (Core_mid-depth_cm)
- Organic matter pools: Labile_OM_Perc, Recalcitrant_OM_Perc, Refractory_OM_Perc, Total_OM_Perc
- Reactivity metric: CRI_Carbon (CRI)
- Data dictionary: Details the variable names, formats, units, and descriptions; file: C_SIDE_organic_matter_pools_and_reactivity.csv
- Observational scope: 1211 down-core soil samples from across UK saltmarsh sites

## Methods & Quality Assurance
- Laboratory method: Thermogravimetric Analysis (TGA) on ~20 mg samples; heated 40–1000°C at 10°C/min under N2
- Data processing: Thermograms aligned to a common temperature scale; clipped to 200–650°C; normalized to mass loss
- OM fractions by temperature: Labile (200–400°C), Recalcitrant and Refractory (400–650°C)
- CRI computation: CRI = %OM_R / %OM_total; conceptually ranges from 0 (fully biodegradable) to 1 (non-biodegradable)
- Calibration & QA: Thermogravimetric calibration with standards; equipment calibrated per University of St Andrews practices
- Site selection rationale: Sites chosen to represent UK coastline diversity while maintaining comparable environmental regions

## File Formats & Access
- Main data file: C_SIDE_organic_matter_pools_and_reactivity.csv
- Data types: Core and location metadata plus numeric OM pool percentages and CRI
- Data quality notes: NA indicates missing data in cells as applicable

## Data Dictionary Highlights
- Key fields and formats:
  - Core Identification (Text), Core_ID
  - Saltmarsh name (Text)
  - Latitude (Lat_dec_deg, Number), Longitude (Long_dec_deg, Number)
  - Depth interval (Core_depth_cm, Number), Depth interval mid-point (Core_mid-depth_cm, Number)
  - Labile_OM_Perc, Recalcitrant_OM_Perc, Refractory_OM_Perc, Total_OM_Perc (Number)
  - CRI_Carbon (Number)

## GIS Applications & Use Cases
- Create thematic maps of OM pool distributions and CRI across UK saltmarshes
- Link with other geospatial layers (coastlines, tidal zones, climate surfaces) for integrated analyses
- Assess spatial patterns of organic matter reactivity in relation to depth or site characteristics

## Considerations & Limitations for GIS work
- Data scope: UK-focused, saltmarsh environments; not a global dataset
- Resolution: Point-based core sampling; may require spatial aggregation for broader analyses
- Temporal dimension: Observations span 2018–2021; cross-year analyses may be limited without additional time-series data
- Data quality: Laboratory calibration and QA procedures documented; cross-site comparability supported by consistent methodology

## References
- Kristensen, E. (1990). Characterization of biogenic organic matter by stepwise thermogravimetry (STG). Biogeochemistry, 9(2), 135-159.
- Smeaton, C. & Austin, W.E.N. (2022). Quality not quantity: Prioritizing the management of sedimentary organic matter across continental shelf seas. Geophysical Research Letters, 49(5), p.e2021GL097481.