# Dataset Description (Soil_Properties_CEH)

## Overview
- Describes soil physical and chemical properties across three land-use types in Sabah, Malaysia: unlogged tropical forest, logged tropical forest, and oil palm plantation.
- Collected March–April 2015 as part of the NERC-funded BALI project; analyzed at the Centre for Ecology & Hydrology, Lancaster, UK.
- The dataset in Soil_Properties_CEH.csv contains 15 columns covering sample identifiers, site, land use, plot and subplot details, horizon, and multiple soil properties (moisture, bulk density, pH, total C and N, inorganic P, C:N, C:P).

## Sampling Design and Methods
- 9 one-hectare plots across 3 sites representing the land-use types: DVCA, MBCA, and SAFE project.
- Stratified sampling: each 1 Ha plot subdivided into 25 subplots (20 m x 20 m); 5 subplots randomly sampled per plot.
- 5 samples collected from each sampled subplot using a gouge auger; organic layer separated from mineral soil.
- Bulk density determined from a separate sample taken with a bulk density ring; soils dried at 105°C for bulk density.
- Gravimetric soil moisture measured; pH measured on fresh soil with a calibrated pH meter.
- Total C and N measured on oven-dried, ground soil using a LECO Truspec Micro analyzer.
- Inorganic P extracted using Bray No. 1 extraction and analyzed with a SEAL AutoAnalyzer 3.

## Data Structure and Metadata
- 15 columns in the dataset: Identifier, Site, Land_Use, Plot_Name, Subplot, Horizon, Soil_Moisture, Horizon_Depth, Bulk_Density, Soil_pH, total_C, total_N, Inorganic_P, C:N, C:P.
- Metadata provides descriptions and units for each column (e.g., Soil_Moisture as gravimetric moisture; Horizon_Depth in cm; Inorganic_P in µg/g; C:N and C:P as numeric ratios).
- Missing data: 3 missing samples are from oil palm plots.

## Data Quality and Provenance
- Data verified and processed as part of standardized protocols; measurements aligned with referenced methods (Emmett et al. 2010; Bray & Kurtz 1945).
- Analyses conducted to ensure consistency across sites and land-use types, enabling comparability for monitoring purposes.

## Outputs and Accessibility
- Provides structured data suitable for reports, maps, and charts to monitor soil properties across land uses.
- Data intended for storage in appropriate data portals to enhance accessibility and reuse.

## Relevance to Environmental Monitoring (Analysts Perspective)
- Supports long-term monitoring of soil physical and chemical properties across land-use change gradients.
- Facilitates standardized outputs for assessing environmental health and the impacts of land-use change on soil carbon, nitrogen, phosphorus, and related soil properties.
- Aligns with the role of environmental monitoring analysts in verifying data quality, applying standardised methods, and providing clear, accessible outputs for policy evaluation and scientific scrutiny.

## References
- Bray, R.H. and Kurtz, L.T. 1945. Determination of total organic and available forms of phosphorus in soils. Soil Science 59, 39-45.
- Emmett, B.A. et al. 2010. Countryside Survey: Soils Report from 2007. Technical Report No. 9/07 NERC/CEH.
- Riutta, T. et al. 2018. Logging disturbance shifts net primary productivity and its allocation in Bornean tropical forests. Global Change Biology.