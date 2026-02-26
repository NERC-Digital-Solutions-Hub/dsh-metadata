# Modelled average percentage yield loss due to ozone damage for four global staple crops (20102012)

## Overview
- Estimates average yield loss due to ozone for maize, rice, soybean, and wheat during 2010–2012.
- Combines global ozone modelling with crop production data to produce 1°x1° grid estimates.
- Outputs four GIS shapefiles (one per crop) with yield-loss values by grid cell.

## Data collection and inputs
- Crop production data: FAO Global Agro-Ecological Zones (GAEZ) dataset (year 2000; 0.0833° resolution), separated into irrigated and non-irrigated production.
- Grid construction: 1° by 1° grid cells; total production summed per cell; only cells with >500 tonnes included in mapping.
- Irrigation classification: Irrigated if >75% of crop production is irrigated; otherwise non-irrigated.
- Geospatial tagging: Each grid cell assigned to hemisphere (Northern/Southern) and climate zone using the ESDAC climate-zone GIS layer.
- Growing periods: 90-day growing periods per crop per climate zone/hemisphere, derived from USDA/FAO data (see detailed Table S1 in Mills et al. 2018a).

## Modelling approach and calculations (by crop)
- Wheat (reference model and dose–response)
  - Ozone flux (POD3IAM) calculated with the EMEP MSC-W chemical transport model (version 4.16) using hourly ozone concentration, temperature, vapour pressure deficit, irradiance, and soil moisture.
  - POD3IAM integrated over the 90-day growing period; irrigated vs. non-irrigated fluxes used accordingly.
  - Yield loss for wheat computed with the CLRTAP dose–response: Percent Yield Loss = (POD3IAM − 0.1) × 0.64.
  - 0.1 mmol/m² represents a pre-industrial ozone baseline; 0.64 is the slope of the dose–response.

- Maize, Rice, Soybean (indirectly linked to wheat via relative sensitivity)
  - Initial step: compute wheat-like yield loss using the same equation for the grid cell (based on POD3IAM for that cell).
  - Relative ozone sensitivity: determine each crop’s sensitivity relative to wheat by dividing that crop’s M7 (7-hour mean ozone concentration) slope by the wheat slope (from published response functions).
  - Final yield loss for each crop = wheat-based yield loss × crop’s relative ozone sensitivity.
  - Note: for maize, rice, and soybean, flux–yield relationships are less well characterised; the method uses wheat-based flux as a proxy with crop-specific sensitivity adjustments.

- Data handling and aggregation
  - For each grid cell, accumulate the 90-day yield losses per crop and save as GIS shapefiles (one file per crop).
  - Growth-period and climate-zone specifics govern which POD3IAM values are used per cell.

## Quality control and validation
- Model validation for the EMEP model described in Mills et al. (2018b): comparison of modelled vs. observed ozone at Global Atmosphere Watch (GAW) sites shows good correlation (r² between 0.88 and 0.93) with acceptable scatter.
- Additional checks:
  - Modelled Dmax and M7 values validated against GAW data.
  - AET/PET proxy validation indicates reasonable estimation of stomatal uptake (r² = 0.63).
- Caveats
  - Ozone flux–yield relationships are well established for wheat; for maize, rice, and soybean, the approach is more uncertain due to limited species-specific flux data.
  - Only the most important growing period per crop/climate is used in climates with multiple seasons.
  - Uncertainties are higher for maize due to limited varietal data (only three older varieties used for the maize flux relationship).

## Outputs and data structure
- Four yield-loss GIS shapefiles (one per crop: maize, rice, soybean, wheat).
- Each shapefile contains 1° by 1° grid cells with five attribute fields:
  - ID: Unique grid cell identifier.
  - Zone: Climate zone for the cell.
  - Long_Lat: Centre coordinates (decimal degrees).
  - Hemisphere: Northern, Southern, or Far South (for Cool temperate in the South).
  - Yield loss: Average percentage yield loss due to ozone for 2010–2012.
- Growth period and climate data sources embedded in the methodology (GAEZ, ESDAC climate zones, CLRTAP, EMEP model).

## Key caveats and considerations for analysts
- Global-scale results rely on a proxy (wheat flux–based approach) for crops other than wheat; regional/local applications should account for crop-specific flux data when available.
- Data quality is constrained by uncertainties in ozone flux–yield relationships, especially for maize, rice, and soybean.
- Some regions with multiple cropping seasons may require more granular seasonal data to refine estimates.
- The approach emphasizes detecting broad spatial patterns and potential co-benefits, rather than precise local yields.

## References and supplementary information
- Mills, G. et al. (2018a). Closing the global ozone yield gap: Quantification and co-benefits for multi-stress tolerance. Global Change Biology, 24, 4869–4893.
- Mills, G. et al. (2018b). Ozone pollution will compromise efforts to increase global wheat production. Global Change Biology, 24, 3560–3574.
- Supporting data and methodological details: supplementary information and figures in the cited Mills et al. papers; input datasets from FAO/GAEZ and ESDAC.