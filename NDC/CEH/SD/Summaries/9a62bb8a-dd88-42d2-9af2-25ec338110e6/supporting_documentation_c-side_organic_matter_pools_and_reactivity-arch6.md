# Project Carbon Storage in Intertidal Environments (C-SIDE)

## Overview
- Funded by NERC (NE/R010846/1).
- Dataset documents three pools of soil organic matter (labile, recalcitrant, refractory) and a carbon reactivity index (CRI) for UK saltmarshes.
- 1211 down-core soil samples collected across UK saltmarsh sites between 2018 and 2021.
- Data enables assessment of organic matter composition and reactivity in intertidal environments to support carbon storage research.

## Data content and structure
- Data file: C_SIDE_organic_matter_pools_and_reactivity.csv.
- Core information: Core_ID, Saltmarsh name, Latitude (WGS84), Longitude (WGS84), Depth interval (cm), Depth interval mid-point (cm).
- Organic matter measurements (percent by weight): Labile OM (%wt), Recalcitrant OM (%wt), Refractory OM (%wt), Total OM (%wt).
- Carbon reactivity: CRI (Carbon Reactivity Index) value.
- Notes: All values are structured for cross-site comparisons and reusability as a data product.

## Variables and data dictionary
- Core Identification: Core_ID (text).
- Saltmarsh name: Saltmarsh name (text).
- Latitude: Lat_dec_deg (decimal degrees, WGS84).
- Longitude: Long_dec_deg (decimal degrees, WGS84).
- Depth interval of sub-sample: Core_depth_cm (cm).
- Depth interval mid-point: Core_mid_depth_cm (cm).
- Labile organic matter: Labile_OM_Perc (%wt).
- Recalcitrant organic matter: Recalcitrant_OM_Perc (%wt).
- Refractory organic matter: Refractory_OM_Perc (%wt).
- Total organic matter: Total_OM_Perc (%wt).
- CRI Carbon: CRI (dimensionless reactivity index).

## Methods and data processing
- Observation/simulation procedures: Thermogravimetric Analysis (TGA).
- Sample preparation: Freeze-dried, milled ~20 mg samples placed in 70 mL crucibles.
- Instrumentation: Mettler Toledo TGA2.
- Heating protocol: 40°C to 1000°C at 10°C/min under N2.
- Data processing: Thermograms adjusted to a common temperature scale; clipped to 200°C–650°C to remove water and non-organic material; thermograms normalized to mass loss for comparability.
- OM fraction definitions (thermally defined): Labile OM (200°C–400°C); Recalcitrant + Refractory OM (400°C–650°C).
- CRI calculation: CRI = %OM_R / %OM_total, where OM_R represents the combined recalcitrant+refractory fraction.
- Calibration: Thermogravimetric analyses calibrated with standards (Smeaton & Austin 2022; Kristensen 1990 underpinning approach).
- Quality control: Laboratory equipment calibrated according to University of St Andrews practices.

## Data quality and provenance
- Site selection aims to reflect UK saltmarsh environmental diversity for comparability.
- Latitude/longitude provided for precise site localization.
- Calibration and quality practices documented to support data reliability and reproducibility.

## File formats and access
- Data format: CSV (.csv).
- Data dictionary included within the dataset description to support interpretation and reuse.
- Metadata notes indicate standard handling of missing cells (NA where applicable).

## Geographical scope
- Location coordinates cover UK saltmarsh environments, with observations distributed to represent coastal saltmarsh diversity.
- Coordinates provided in decimal degrees (WGS84): illustrative corners include (60.973491, -8.019200), (60.973491, 2.176113), (49.844006, -8.019200), (49.844006, 2.176113).

## Relevance for data support practice
- Produces a ready-to-analyze data product enabling self-serve exploration of organic matter pools and reactivity across multiple UK saltmarsh sites.
- Clear data dictionary and standardized processing steps facilitate data integration with other environmental datasets (e.g., location, depth, site metadata).
- Supports cross-site comparisons, regional carbon storage assessments, and synthesis work for policy or management contexts.

## Potential uses
- Cross-site comparison of labile, recalcitrant, and refractory organic matter fractions in saltmarsh soils.
- Analysis of carbon reactivity (CRI) in relation to depth, location, and environmental conditions.
- Integration with other site-level or environmental datasets for carbon cycling research and conservation planning.
- Development of dashboards or reports to communicate organic matter composition and reactivity to diverse stakeholders.

## References
- Kristensen, E. (1990). Characterization of biogenic organic matter by stepwise thermogravimetry (STG). Biogeochemistry, 9(2), 135-159. https://doi.org/10.1007/bf00692169
- Smeaton, C. & Austin, W.E.N. (2022). Quality not quantity: Prioritizing the management of sedimentary organic matter across continental shelf seas. Geophysical Research Letters, 49(5), p.e2021GL097481. https://doi.org/10.1029/2021GL097481