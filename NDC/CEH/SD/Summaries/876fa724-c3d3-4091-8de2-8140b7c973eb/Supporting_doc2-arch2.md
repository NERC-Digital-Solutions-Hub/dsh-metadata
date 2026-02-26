# Supporting documentation

## Overview
- Simulation results for the red soil region of China using the Global ECOSSE model.
- Outputs include carbon dioxide emissions and soil organic carbon from soil pools.
- The study covers 2016–2100 under the IPCC A2_MG1 (business as usual) climate scenario with agricultural and forest land uses.

## Model and data
- Global ECOSSE is a spatial application of the ECOSSE soil model; carbon and nitrogen exist in multiple pools in 5 cm soil layers. Turnover rates depend on environmental drivers; carbon input comes from land use and simulated net primary productivity.
- Key input datasets:
  - Soils: Harmonised World Soil Database (HWSD), resolution 0.083 degrees.
  - Land cover: Copernicus land monitoring service.
  - Climate: CRU high-resolution gridded datasets (0.5 degrees) from the University of East Anglia.
- Study area and soils:
  - Regions selected by predominant soil types: Acrisols, Alisols, Luvisols, Lixisols, Nitisols.
  - Land uses simulated: agricultural and forest.
- Outputs of the model:
  - Simulated CO2 emissions from soil (under agriculture and forest).
  - Soil organic carbon dynamics.

## Simulation workflow
- Stage 1: Prepare national/province boundaries for CookieCut; reduce boundary points by thinning polygons.
- Stage 2: CookieCut; create bounding boxes using GADM shapefiles and the Countries utility to identify country/province extents.
- Stage 3: Build a JSON file specifying one or more provinces and one or more land cover types; each line includes coordinates, HWSD mu_global identifier, and land cover index.
- Stage 4: GlblEcosse; read the _hwsd.csv AOI file, generate ECOSSE input file sets for each entry, and skip adjacent entries on the same latitude with the same HWSD mu_global identifier; a unique manifest file records adjacent relationships.

## Quality control
- Input data are checked for accuracy to ensure reliable model outputs.

## Outputs and data files
- Agri_RS_co2.txt — simulated CO2 emissions from soil under agriculture.
- For_RS_co2.txt — simulated CO2 emissions from soil under forest.
- The documentation implies structured outputs (and accompanying inputs) suitable for reproducibility and data sharing.