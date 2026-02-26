# Supporting documentation

## Overview
- Simulation results for the red soil region of China using the Global ECOSSE model, a spatial application of the ECOSSE soil carbon-nitrogen model.
- Model outputs include carbon dioxide emissions from soil and soil organic carbon.

## Model and outputs
- Global ECOSSE is a pool-based soil model with carbon and nitrogen distributed across multiple pools in 5 cm soil layers.
- Carbon turnover is base-rate driven and modified by environmental drivers.
- Inputs drive carbon addition via land use and a simulated net primary productivity.
- Outputs produced: CO2 emissions from soil and soil organic carbon stocks.

## Data inputs and sources
- Soil data: Harmonised World Soil Database (HWSD) at 0.083-degree resolution.
- Land cover: Copernicus land monitoring service.
- Climate: University of East Anglia Climatic Research Unit high-resolution gridded data at 0.5-degree resolution.
- Study grid cells include predominant soil types Acrisols, Alisols, Luvisols, Lixisols, and Nitisols.
- Simulation period: 2016–2100.
- Climate scenario: IPCC A2_MG1 (business-as-usual, CO2 emissions continue to rise).
- Land uses simulated: Agricultural and Forest across the entire region.

## Study region and period
- Red soil region of China (specific geographic focus inferred from text).

## Simulation workflow (Stage 1–4)
- Stage 1: Prepare national/province boundaries for CookieCut; thinning polygons to reduce boundary points.
- Stage 2: CookieCut. Create bounding boxes from the prepared shapefiles; use Countries utility to determine bounding boxes for countries/provinces.
- Stage 3: Create/select a JSON file specifying one or more provinces and one or more land cover types (as defined in table 1). Each line includes a coordinate set, HWSD mu_global identifier, and land cover index.
- Stage 4: GlblEcosse. Read the _hwsd.csv AOI file from Stage 2 and produce ECOSSE input file sets for each entry, skipping adjacent entries on the same latitude with the same HWSD mu_global identifier. Adjacent entries are recorded in a manifest file.

## Quality control
- Input data are checked for accuracy.

## Data files
- Agri_RS_co2.txt – Simulated CO2 emissions from soil under agriculture.
- For_RS_co2.txt – Simulated CO2 emissions from soil under forest.