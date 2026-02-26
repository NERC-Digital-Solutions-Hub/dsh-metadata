# Supporting documentation

## Scope and purpose
- Presents simulation results for the red soil region of China using the Global ECOSSE model, a spatial application of ECOSSE.
- Produces outputs on carbon dynamics, including carbon dioxide emissions and soil organic carbon.
- Describes data sources, inputs, model structure, and the step-by-step workflow used to generate ECOSSE inputs and outputs.

## Model and data context
- Global ECOSSE is a pool-based soil carbon and nitrogen model with 5 cm soil layers; carbon turnover rates are modified by environmental drivers and inputs include net primary productivity.
- Inputs and data types:
  - Soil data: Harmonised World Soil Database (HWSD) at 0.083-degree resolution.
  - Land cover: Copernicus land monitoring service.
  - Climate: CRU high-resolution gridded datasets at 0.5-degree resolution.
  - Target soil types: Acrisols, Alisols, Luvisols, Lixisols, Nitisols.
  - Timeframe: 2016–2100.
  - Scenario: IPCC A2_MG1 (business-as-usual CO2 emissions trajectory).
  - Land uses modelled: agricultural and forest land across the entire region.

## Simulation outputs
- Outputs include:
  - CO2 emissions from soil under agricultural land (Agri_RS_co2.txt).
  - CO2 emissions from soil under forest land (For_RS_co2.txt).

## Simulation workflow (Stage 1–Stage 4)
- Stage 1: Prepare boundaries for CookieCut by thinning GADM shapefiles to manage polygon complexity.
- Stage 2: CookieCut. Use ReformShapes-generated shape file to define a bounding box; determine bounding boxes for countries/provinces.
- Stage 3: Create and select a JSON file specifying one or more provinces and one or more land cover types; each line includes coordinates, HWSD mu_global identifier, and land cover index.
- Stage 4: GlblEcosse. Read the _hwsd.csv AOI file from Stage 2 and generate ECOSSE input files for each entry; skip adjacent entries on the same latitude with identical HWSD mu_global identifier. Record adjacencies in a unique manifest file.

## Quality control
- Input data are checked for accuracy to ensure reliability of the simulations.

## Data and file inventory
- Agri_RS_co2.txt — Simulated CO2 emissions from soil under agriculture.
- For_RS_co2.txt — Simulated CO2 emissions from soil under forest.
- Supporting processing steps reference related files such as _hwsd.csv AOI inputs and a manifest file to track adjacencies.