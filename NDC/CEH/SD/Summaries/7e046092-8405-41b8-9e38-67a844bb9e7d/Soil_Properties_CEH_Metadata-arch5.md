# Dataset Description (Soil_Properties_CEH)

## Overview
- Describes soil physical and chemical properties across unlogged tropical forest, logged tropical forest, and oil palm plantation in Sabah, Malaysia.
- Data collection: March–April 2015; part of the NERC-funded BALI project; analyzed at Centre for Ecology & Hydrology, Lancaster, UK.
- File Soil_Properties_CEH.csv contains 15 columns: Identifier, Site, Land_Use, Plot_Name, Subplot, Horizon, Soil_Moisture, Horizon_Depth, Bulk_Density, Soil_pH, total_C, total_N, Inorganic_P, C:N, C:P.
- Metadata provides descriptions and units for each column to support discoverability and reuse.

## Sampling Design
- 9 one-hectare plots across 3 sites representing unlogged forest, logged forest, and oil palm plantation: Danum Valley Conservation Area (DVCA), Maliau Basin Conservation Area (MBCA), and SAFE project in Sabah.
- Stratified design: each 1 Ha plot subdivided into 25 subplots (20 x 20 m); 5 subplots randomly selected per plot for sampling.
- 5 samples per subplot collected with gouge auger; organic layer depth measured and samples sealed in bags.
- Bulk density measured from a separate bulk density ring sample; samples dried and prepared for analyses.
- Laboratory analyses:
  - Soil moisture: gravimetric
  - pH: measured on fresh soil with calibrated pH meter
  - Total C and N: oven-dried, ground soil analyzed with LECO
  - Inorganic P: Bray No. 1 extractant, analyzed with SEAL AutoAnalyser
- Sample counts: 100 samples per forest type; 25 samples from oil palm.

## Data Columns and Metadata
- Identifier: Unique sample identifier
- Site: Geographical site of sampling (text)
- Land_Use: Land use category (Unlogged tropical forest, Logged tropical forest, Oil palm plantation)
- Plot_Name: Name of the 1 Ha plot
- Subplot: Subplot number within each plot
- Horizon: Soil horizon sampled
- Soil_Moisture: Gravimetric moisture (1) or percentage (2)
- Horizon_Depth: Depth of organic horizon sampled (1) or cm (2)
- Bulk_Density: Bulk density (1: g/cm3) or (2: numeric)
- Soil_pH: pH value (numeric)
- total_C: Total carbon content (1: %; 2: %)
- total_N: Total nitrogen content (1: %; 2: %)
- Inorganic_P: Inorganic/soluble phosphorus (1: µg/g; 2: numeric)
- C:N: Carbon-to-nitrogen ratio (1: numeric; 2: numeric)
- C:P: Carbon-to-inorganic phosphorus ratio (1: numeric; 2: numeric)

## Missing Data
- Three missing data points occur in oil palm samples.

## Provenance and References
- Bray, R.H. & Kurtz, L.T. 1945. Determination of total organic and available forms of phosphorus in soils.
- Emmett et al. 2010. Countryside Survey: Soils Report (CEH Technical Report).
- Riutta et al. 2018. Logging disturbance shifts net primary productivity in Bornean tropical forests.

## Governance and Use Considerations
- Dataset adheres to a structured 15-column schema with defined units to support interoperability and reuse.
- Sampling design supports representativeness across land-use types, though note the three oil palm missing samples.
- Metadata provides clear variable definitions and units to enable proper interpretation and integration with other datasets.
- Users should be aware of missing oil palm observations and potential limitations in cross-site comparability due to site-specific conditions.