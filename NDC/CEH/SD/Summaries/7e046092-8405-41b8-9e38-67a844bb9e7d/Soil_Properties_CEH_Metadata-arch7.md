# Dataset Description (Soil_Properties_CEH)

## Overview
- Describes soil physical and chemical properties across unlogged tropical forest, logged tropical forest, and oil palm plantation in Sabah, Malaysia.
- Collected March–April 2015 as part of the NERC-funded BALI project; analyzed at the Centre for Ecology & Hydrology, Lancaster, UK.

## Data structure and columns
The CSV contains 15 columns:
- Identifier: Unique sample identifier (text)
- Site: Geographical site (e.g., Danum Valley Conservation Area, Maliau Basin Conservation Area, SAFE project) (text)
- Land_Use: Land use category – Unlogged tropical forest, Logged tropical forest, or Oil palm plantation (text)
- Plot_Name: Name of the 1 ha plot (text)
- Subplot: Subplot number within each 1 ha plot (numeric)
- Horizon: Soil horizon sampled (text)
- Soil_Moisture: Gravimetric soil moisture (numeric)
- Horizon_Depth: Depth of the organic horizon sampled (cm) (numeric)
- Bulk_Density: Bulk density of soil sample (g/cm3) (numeric)
- Soil_pH: pH of the soil sample (numeric)
- total_C: Total carbon content of the soil sample (numeric)
- total_N: Total nitrogen content of the soil sample (numeric)
- Inorganic_P: Inorganic/soluble phosphorus concentration (µg/g) (numeric)
- C:N: Carbon to nitrogen ratio (numeric)
- C:P: Carbon to inorganic phosphorus ratio (numeric)

- Metadata provides descriptions and units/formats for each field.

## Sampling design and data collection
- 9 one-hectare plots across 3 sites representing forest and oil palm: Danum Valley Conservation Area (DVCA), Maliau Basin Conservation Area (MBCA), and SAFE project in Sabah.
- Stratified sampling: Each 1 ha plot subdivided into 25 subplots (20 m x 20 m); 5 subplots sampled per plot.
- For each sampled subplot, 5 samples were collected (via gouge augur) plus an organic layer depth measurement; samples sealed for lab analysis.
- Additional bulk density sample collected with a bulk density ring; moisture determined gravimetrically.
- pH measured on fresh soil with calibrated pH meter.
- Total C and N measured on oven-dried, ground soil using a LECO analyser.
- Inorganic P extracted with Bray No. 1 extractant and analysed with SEAL AutoAnalyser.
- 100 samples per forest type; 25 samples from oil palm (this yields 125 samples per site-category across all plots).
- Sampling protocol referenced: Emmett et al. 2010; Bray & Kurtz 1945; Riutta et al. 2018.

## Metadata, units and data quality notes
- Metadata provides explicit descriptions and units for each field (e.g., Horizon_Depth in cm; Soil_Moisture gravimetric or percentage; Bulk_Density in g/cm3).
- 3 missing data points occur in the oil palm dataset (unavailable samples).

## Spatial and GIS applicability
- GIS-ready dataset suitable for map-based analyses of soil properties by plot, subplots, and land-use type.
- Potential uses:
  - Create thematic maps of soil moisture, pH, carbon, nitrogen, and phosphorus across sites and land uses.
  - Join to spatial plot boundaries or subplots to visualize spatial patterns and gradients.
  - Compare soil properties by Land_Use (unlogged forest, logged forest, oil palm) and by Site.
  - Integrate with other spatial layers (topography, vegetation, disturbance) to explore drivers of soil property variation.
- Considerations for GIS workflows:
  - Use Identifier to join with spatial plot shapefiles or survey data.
  - Align units and ensure consistency across properties (e.g., C, N, P values in appropriate percent or concentration units per metadata).
  - Account for limited spatial density (9 plots) and the timepoint (2015) when interpreting spatial patterns.

## Data quality, limitations and considerations
- Sample density is modest (9 plots across 3 sites); results are indicative at plot-level resolution.
- Oil palm data has three missing samples; absence should be noted in analyses.
- Data reflect a single timepoint; temporal variability not captured.
- Methods and references provided indicate standardized protocols, aiding comparability with other soil datasets.

## References
- Bray, R.H. and Kurtz, L.T. 1945. Determination of total organic and available forms of phosphorus in soils.
- Emmett, B.A. et al. 2010. Countryside Survey: Soils Report from 2007.
- Riutta, T. et al. 2018. Logging disturbance shifts net primary productivity in Bornean tropical forests. Global Change Biology.