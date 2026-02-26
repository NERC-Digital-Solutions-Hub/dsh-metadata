# Dataset Description (Soil_Nutrients)

## Overview
- Describes soil nutrient availability across unlogged tropical forest, logged tropical forest, and oil palm plantation in Sabah, Malaysia.
- Collected March–April 2016 as part of the NERC-funded BALI project.
- Data file Soil_Nutrients.csv contains 21 columns with various nutrient measurements.

## Sampling Design
- 9 one-hectare plots across 3 sites representing different land uses: Danum Valley Conservation Area (unlogged), Maliau Basin Conservation Area (logged), and SAFE project (oil palm).
- Stratified design: each 1 Ha plot subdivided into 25 subplots (20 x 20 m); 3 subplots selected per plot for sampling.
- At 3 locations within each subplot, 4 pairs of PRS ion exchange membranes (one pair = 1 cation + 1 anion) buried to ~10 cm for 2 weeks.
- Membranes pooled per location, eluted with 0.5 M HCl for 1 hour.
- Analytes:
  - NO3- and NH4+ measured colorimetrically via flow injection analysis (FIA).
  - Other elements analyzed by ICP-OES.
- Results reported as supply rates per 10 cm2 area over the burial period (µg/10 cm2/14 days).

## Measurements and Outputs
- 21 measured variables per sample:
  - Identifier, Site, Land_Use, Plot_Name, Subplot
  - NO3_N, NH4_N, Total_N
  - Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd
- NO3_N, NH4_N, Total_N, and all element concentrations are expressed as µg/10 cm2/14 days.

## Metadata and Data Structure
- Metadata fields described with data types (e.g., Identifier, Site, Land_Use, Plot_Name as text; Subplot as numeric).
- Units standardized as µg/10 cm2/14 days for nutrient measurements.
- Data stored in Soil_Nutrients.csv with 21 columns.

## Data Quality, MDL, and Reporting
- MDL (Method Detection Limits) provided for each element; zeros indicate non-detectable levels.
- Reported data are measurements even if below MDL, preserving potentially informative low-level values.

MDL highlights:
- NO3_N: 2
- NH4_N: 2
- Ca: 2
- Mg: 4
- K: 4
- P: 0.2
- Fe: 0.4
- Mn: 0.2
- Cu: 0.2
- Zn: 0.2
- B: 0.2
- S: 2
- Pb: 0.2
- Al: 0.4
- Cd: 0.2

## Access, Use, and Reuse
- Data produced using standardised methods suitable for monitoring and comparison across land-use types.
- Outputs can be presented as reports, maps, and charts; datasets are stored and can be uploaded to appropriate portals.
- Potential to enhance monitoring value by combining with other relevant environmental datasets.

## References
- Qian, P. & J. J. Schoenau (2002) Practical applications of ion exchange resins in agricultural and environmental soil research. Canadian Journal of Soil Science, 82, 9-21.
- Riutta, T. et al. (2018) Logging disturbance shifts net primary productivity and its allocation in Bornean tropical forests. Global Change Biology.
- Western Ag (www.westernag.ca)