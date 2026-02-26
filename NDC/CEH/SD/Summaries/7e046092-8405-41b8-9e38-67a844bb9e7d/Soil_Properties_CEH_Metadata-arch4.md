# Dataset Description (Soil_Properties_CEH)

## Overview
- Describes soil physical and chemical properties across unlogged tropical forest, logged tropical forest, and oil palm plantation in Sabah, Malaysia.
- Collected March–April 2015; part of the NERC-funded BALI project; analyzed at Centre for Ecology & Hydrology, Lancaster, UK.
- Data stored in Soil_Properties_CEH.csv with 15 columns; metadata provides column descriptions.

## Sampling Design
- Sites: Danum Valley Conservation Area (DVCA), Maliau Basin Conservation Area (MBCA), and SAFE project in Sabah.
- A stratified design using 9 one-hectare plots across the three land-use types.
- Each 1 Ha plot subdivided into 25 subplots (20 x 20 m); 5 subplots randomly sampled per plot.
- 5 samples collected from each sampled subplot using a gouge auger; organic layer depth measured and separated from mineral soil.
- Bulk density determined with a ring; soil moisture gravimetrically.
- pH measured on fresh soil with a calibrated pH meter.
- Total carbon and nitrogen measured on oven-dried, ground soil (LECO Truspec); inorganic phosphorus extracted with Bray No. 1 and analyzed.
- Sampling yields 100 samples per forest type and 25 samples from oil palm (per the description).

## Data Columns and Metadata
- 15 columns: Identifier, Site, Land_Use, Plot_Name, Subplot, Horizon, Soil_Moisture, Horizon_Depth, Bulk_Density, Soil_pH, total_C, total_N, Inorganic_P, C:N, C:P.
- Metadata provides detailed descriptions and units for each column (e.g., Soil_Moisture gravimetric; Horizon_Depth in cm; Inorganic_P in µg/g).

## Data Quality and Missing Data
- Three missing data points are from oil palm samples (missing samples).

## Methods and References
- Bray, R.H. & Kurtz, L.T. (1945) for inorganic phosphorus extraction.
- Emmett et al. (2010) for soil moisture, bulk density, and related methods.
- Riutta et al. (2018) related to logging disturbance effects in Bornean tropical forests.

## Relevance for Data Leaders
- Demonstrates跨-site, cross-land-use data collection with clear metadata to support discoverability and reuse.
- Highlights importance of documenting sampling design, measurement methods, and units to enable data integration across networks.
- Identifies data gaps (e.g., missing oil palm samples) and the need for consistent data standards and provenance for effective data governance and collaboration within the wider data community.