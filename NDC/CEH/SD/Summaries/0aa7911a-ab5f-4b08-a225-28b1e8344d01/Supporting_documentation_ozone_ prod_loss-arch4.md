# Modelled annual average production loss due to ozone damage for four global staple crops, 20102012.

## Overview
- Document detailing full methodology to calculate crop production loss due to ozone for maize, rice, soybean, and wheat during 2010-2012.
- Uses EMEP MSC-W chemical transport model and a flux-based approach to estimate yield loss and production impact on a global 1° by 1° grid.
- Produces four GIS shapefiles (one per crop) with grid-level production loss figures.

## Data sources and collection
- Crop production data: FAO Global Agro-Ecological Zones (GAEZ) dataset (year 2000 baseline, 1° by 1° grid; 0.0833° resolution for production; irrigated vs non-irrigated).
- Climate zones and geography: Climate Zone GIS layer from European Soil Data Centre (ESDAC) at JRC; hemisphere classification (Northern/Southern) and irrigation status per grid cell.
- Growing periods: 90-day growing periods per climate zone and hemisphere derived from USDA/FAO data.
- Threshold for grid inclusion: only cells with >500 tonnes production included in analysis.
- Model framework references: Mills et al. (2018a, 2018b) for methodology, validation, and interpretation.

## Modelling methodology
- Wheat (POD3 IAM): Used EMEP MSC-W model to compute daily ozone flux (POD3 IAM) for 2010-2012; separates irrigated vs rain-limited conditions. Yield loss calculated using a CLRTAP-adopted dose-response: Percent Yield Loss = (POD3IAM − 0.1) × 0.64.
- Other crops (maize, rice, soybean): Since crop-specific ozone flux-response data are limited, apply wheat-based yield loss and scale by crop-specific relative ozone sensitivity. Relative sensitivity = slope of crop’s M7 (7-hour mean ozone) response function divided by wheat’s slope.
- Final production loss: Production loss per grid cell = (annual mean production for 2010-2012) × (percent yield loss/100). Computed separately for each crop and aggregated into 1° grids.
- Output: Four GIS shapefiles (one per crop) with grid-level production loss values.

## Data processing and structure
- Grid framework: 1° by 1° cells; only cells with sufficient production used.
- Shapefile attributes (per crop):
  - ID: Unique grid cell identifier.
  - Zone: Climate zone.
  - Long_Lat: Center coordinates (decimal degrees).
  - Hemisphere: Northern, Southern, or Far South (for wheat/maize in Cool temperate climates).
  - ProdLoss: Annual average production loss (thousand tonnes) for 2010-2012.

## Validation and quality assurance
- Model validation against Global Atmosphere Watch (GAW) data shows good temporal and spatial performance; seasonal max ozone captured well across regions.
- Correlation between modelled Dmax/M7 and observations at GAW sites: r^2 between 0.88 and 0.93 with low scatter.
- Stomatal uptake proxy validation: strong correlation (r^2 = 0.63) between AET/PET and POD3IAM/M7 ratio, indicating reasonable estimation of stomatal uptake.
- Noted caveats:
  - Lack of crop-specific ozone flux-response data for maize, rice, and soybean leads to reliance on wheat-based flux with relative sensitivity adjustments.
  - Maize data limited to a few older varieties; introduces greater uncertainty for maize.
  - In some climates with multiple growing seasons, only the dominant season was used.
  - Calls for future species-specific flux data as it becomes available.

## Assumptions, limitations, and considerations for data governance
- Assumes that differences in ozone concentration (captured by M7) drive uptake variability more than species-specific uptake differences beyond the relative sensitivity adjustment.
- Provides a transparent framework for updating when species-specific flux-response data become available.
- Outputs are static for 2010-2012; future work could explore updates orScenario analyses with new ozone data or climate projections.
- Data lineage is documented (FAO/GAEZ for production, ESDAC for climate zones, and EMEP for atmospheric chemistry modelling).

## Relevance for data leadership and use
- Demonstrates end-to-end data workflow: data discovery, integration of diverse data sources, spatial aggregation, modelling, validation, and production of dissemination-ready GIS outputs.
- Highlights data discovery challenges (scattered data, gaps in species-specific flux relationships) and governance implications (need for standardized metadata, documentation, and ongoing data updates).
- Provides a replicable model for evaluating environmental stress impacts on agricultural production at a global scale, with clear data outputs and quality controls.
- Points to opportunities for improved data coordination and partnerships to obtain more species-specific flux-response data and enhance model fidelity.