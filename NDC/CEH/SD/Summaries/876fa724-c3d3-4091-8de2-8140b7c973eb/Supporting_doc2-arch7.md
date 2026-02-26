# Supporting documentation

## Overview
- Presentation of simulation results for the red soil region of China using the Global ECOSSE model, a spatial application of ECOSSE.
- Outputs include carbon dioxide and soil organic carbon from a pool-based soil model with 5 cm soil layers and carbon/nitrogen in different pools.
- Inputs come from multiple data sources at different resolutions, with outputs suitable for map-based analysis.

## Data sources and resolutions
- Soil input: Harmonised World Soil Database (HWSD) at 0.083-degree resolution.
- Land cover: Copernicus land monitoring service.
- Climate: University of East Anglia Climatic Research Unit high-resolution gridded data at 0.5-degree resolution.
- Soil types considered: Acrisols, Alisols, Luvisols, Lixisols, Nitisols.
- Study period and scenario: 2016–2100 under IPCC scenario A2_MG1 (business-as-usual CO2 emissions growth).
- Land uses modeled: Agricultural and Forest land uses across the region.

## Simulation design
- Model outputs: CO2 emissions from soil and soil organic carbon changes.
- Spatial focus: Red soil region of China.
- Layering: 5 cm soil layers with carbon and nitrogen pools and their turnover driven by environmental drivers.
- Data integration: Combines data across resolutions and sources for GIS-ready outputs.

## Processing workflow (Stage-by-stage)
- Stage 1: Prepare national or province boundaries for reuse in CookieCut.
  - Start from a GADM country/province shapefile and reduce boundary points (thinning) to simplify polygons.
- Stage 2: CookieCut
  - Use ReformShapes-generated shapefile and define a bounding box (lower-left and upper-right coordinates).
  - Employ Countries utility to determine bounding boxes for countries and provinces.
- Stage 3: JSON specification
  - Create or select a JSON file listing one or more provinces and one or more land cover types (per Table 1).
  - Each line contains: coordinate set, HWSD mu_global identifier, and land cover index.
- Stage 4: GlblEcosse processing
  - Read the _hwsd.csv AOI file from Stage 2 and generate ECOSSE input file sets for each entry.
  - Skip adjacent entries on the same latitude with the same HWSD mu_global identifier.
  - Record adjacent entries in a unique manifest file.

## Quality control
- Input data are checked for accuracy as part of the workflow.

## Outputs and data products
- ECOSSE input files generated for processing.
- Data files documenting simulated soil CO2 emissions:
  - Agri_RS_co2.txt — simulated CO2 emissions from soil under agriculture.
  - For_RS_co2.txt — simulated CO2 emissions from soil under forest.

## Relevance to GIS practice
- Involves GIS-ready data preparation: boundary thinning, bounding-box specification, and AOI handling.
- Uses standard GIS data sources (GADM, HWSD, Copernicus, CRU) and transforms them into ECOSSE inputs for spatially explicit simulations.
- Produces outputs suitable for map-based visualization of soil carbon dynamics and CO2 emissions across defined provinces and land-cover types.