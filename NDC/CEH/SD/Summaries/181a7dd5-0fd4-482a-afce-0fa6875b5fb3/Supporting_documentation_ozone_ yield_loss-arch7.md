# Modelled average percentage yield loss due to ozone damage for four global staple crops (20102012)

## Overview
- Describes a GIS-based data product: modeled average yield loss percentages due to ozone for maize, rice, soybean, and wheat during 2010–2012.
- Outputs four 1° by 1° grid-based shapefiles (one per crop) with yield loss estimates and associated climate/zone metadata.

## Data sources and collection
- Crop production data: FAO Global Agro-Ecological Zones (GAEZ) dataset (year 2000; 0.0833° resolution) used to derive grid-level production, distinguishing irrigated vs non-irrigated production.
- Spatial grid construction: Aggregation to 1° by 1° cells; cells with >500 tonnes production included in mapping.
- Climate and zone classification:
  - Hemisphere and climate zone assigned per grid cell.
  - Climate zones derived from the ES DAC JRC European Soil Data Centre GIS raster.
- Growing period definitions:
  - For each hemisphere/climate zone combination, a 90-day growing period was set for each crop, based on USDA/FAO data.
  - Detailed 90-day start/end days per crop and climate zone are provided (Table S1 in source).
- Ozone data and modeling:
  - Wheat yield loss calculated using POD3IAM (phytotoxic ozone dose above 3 nmol m^-2 s^-1) from the EMEP MSC-W model (v4.16) for 2010–2012.
  - For all crops, POD3IAM is accumulated over the principal 90-day growing period per grid cell.

## Crop-specific yield loss methodology
- Wheat:
  - Yield loss computed directly from POD3IAM using CLRTAP dose–response: Percent Yield Loss = (POD3IAM − 0.1) × 0.64.
  - 0.1 mmol/m^2 represents a baseline (pre-industrial/near-natural ozone).
- Maize, Rice, Soybean:
  - Since species-specific flux–yield relationships are not available for these crops, their yield losses are derived by adjusting wheat losses.
  - Compute wheat yield loss from POD3IAM; multiply by the crop’s relative ozone sensitivity, defined as the ratio of that crop’s M7 (7-hour mean ozone) slope to the wheat slope (from published functions).
  - The crop-specific relative sensitivity uses M7-based response functions to scale wheat results (see source figures for functions).
- Output:
  - Final percentage yield loss per grid cell for each crop, stored in four separate GIS shapefiles.

## Data products and structure
- Four shapefiles (one per crop): maize, rice, soybean, wheat.
- Grid resolution: 1° by 1° cells.
- Attribute columns (5 per shapefile):
  - ID: Unique grid cell identifier.
  - Zone: Climate zone for the grid cell.
  - Long_Lat: Center coordinates of the grid cell (decimal degrees).
  - Hemisphere: Northern, Southern, or Far South classification.
  - Yield loss: Average percentage yield loss due to ozone for 2010–2012.

## Quality control and validation
- EMEP model validation:
  - Comparisons of modeled vs. observed ozone from Global Atmosphere Watch (GAW) sites show good agreement in daily maximum ozone and seasonal metrics (Dmax and M7) with R^2 values typically in the 0.88–0.93 range, after outlier handling.
  - Additional evaluation of stomatal uptake proxies (AET/PET) supports the model’s representation of ozone uptake.
- Limitations acknowledged:
  - Maize, rice, and soybean lack extensive direct flux–response data; reliance on wheat-based flux relationships introduces uncertainty.
  - Data are most robust for climates with a single major growing season; multi-season regions (e.g., India) use only the primary growing period.
  - Differences in ozone uptake across crops and environments may not be fully captured; model improvements possible with species-specific data.

## Limitations and caveats
- Absence of crop-specific ozone flux relationships for maize, rice, and soybean; results depend on scaling by relative M7 slopes to wheat.
- Uncertainty is higher for maize due to limited variety-specific data.
- In regions with multiple growing seasons per year, only the dominant growing period was used.
- Recommendations: update with species-specific flux data when available; re-evaluate using multiple growing seasons where appropriate.

## Data sources and references
- EMEP MSC-W chemical transport model (v4.16) for POD3IAM ozone uptake.
- CLRTAP 2017 dose–response methodology for wheat.
- M7 ozone response functions and relative sensitivity assessments (crop-specific vs wheat).
- FAO/GAEZ crop production data and calibration factors (1999–2001 to 2010–2012).
- Climate zones from ES DAC JRC (ESDAC) GIS layer.
- Validation and supporting analyses detailed in Mills et al. 2018a, 2018b (Global Change Biology), including supplementary information and figures.

## Practical use for GIS specialists
- Create map-based analyses of ozone-related yield risk by crop at 1° resolution; overlays with policy, climatic, or agricultural data are straightforward using the provided shapefiles.
- Integrate with regional datasets to identify hotspots of yield loss and to support risk assessment, adaptation planning, or agricultural policy discussions.
- Potential for refinement by incorporating new species-specific ozone flux data and expanding to higher-resolution grids if data permit.