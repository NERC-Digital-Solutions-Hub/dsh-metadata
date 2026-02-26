# Modelled annual average percentage yield loss due to ozone damage for four global staple crops, 2010-2012 version 2.

## Purpose and scope
- Presents methodology and data for estimating annual average percentage yield loss due to ozone for maize, rice, soybean, and wheat during 2010-2012.
- Outputs consist of geospatial yield-loss estimates at a 1° by 1° grid for global analysis.

## Data collection and generation
- Grid construction: 1° by 1° grid; crop production data from FAO Global Agro-Ecological Zones (GAEZ) at 0.0833° resolution (year 2000) used to derive per-grid production totals.
- Data classification: each grid cell labeled as irrigated or non-irrigated (irrigated if >75% irrigated production).
- Spatial attributes: each cell assigned to hemisphere (Northern/Southern) and climate zone (ESDAC JRC layer).
- Growing periods: for each hemisphere/climate zone, a 90-day growing period defined per crop using USDA/FAO guidance; detailed start/end days tabulated (Table 1 in Mills et al. 2018a).
- Crop-specific data handling:
  - Maize, rice, soybean: ozone flux-based estimates derived from POD3 IAM values (hourly ozone flux proxy for stomatal uptake).
  - Wheat: uses POD3 IAM with a dose-response relationship (POD3 IAM minus 0.1, then multiplied by slope 0.64).
- Output per crop: four GIS shapefiles (maize, rice, soybean, wheat) with 1° grid cells and a Yloss value.

## Methodology for yield-loss estimation
- Ozone exposure metric:
  - Wheat: POD3 IAM is used with baseline subtraction (0.1 mmol/m²) and a dose-response slope (0.64) to compute percent yield loss (Eqn 1).
  - Other crops: relative ozone sensitivity to wheat is applied. Crop-specific M7 (7-hour mean ozone) response slopes are used to compute a relative sensitivity; wheat yield loss is scaled by these relative values to yield crop-specific losses.
- Flux-based approach: emphasizes ozone flux (POD3 IAM) rather than concentration alone; wheat-derived dose-response is scaled for other crops due to limited species-specific flux data.
- Data integration: crop-specific yield losses are added to the 1° grid and saved as separate shapefiles.

## Quality control and validation
- EMEP MSC-W model validation:
  - Compare model results to Global Atmosphere Watch (GAW) ozone observations; assessment shows spatial and temporal consistency, including peak ozone periods.
  - Model performance: Dmax and M7 correlations with observations at 2012 GAW sites show r² ≈ 0.88–0.93 with low scatter.
- Stomatal uptake verification:
  - Correlation between Actual Evapotranspiration (AET)/Potential Evapotranspiration (PET) and POD3 IAM divided by M7 (proxy for growing-season stomatal conductance) shows r² ≈ 0.63.
- Caveats:
  - No crop-specific flux-response data for maize, rice, soybean; maize data limited to three older varieties, increasing uncertainty for maize.
  - Only most important growing period per climate used; multiple seasons in some climates (e.g., India) are simplified.
  - Global-scale limitations acknowledged; when species-specific flux data become available, a species-specific flux approach is recommended.

## Data structure and outputs
- Four yield-loss GIS shapefiles (one per crop) at 1° by 1° resolution.
- Each shapefile includes 5 attributes:
  - ID: unique grid square identifier
  - Zone: climate zone
  - Long_Lat: center coordinates (decimal degrees)
  - Hemisphere: Northern, Southern, or Far South (for Cool temperate)
  - Yloss: annual average percentage yield loss due to ozone (2010–2012)
- Data provenance:
  - EMEP MSC-W model (v4.16) for ozone flux and POD3 IAM
  - FAO GAEZ for production baseline data
  - ES DAC/JRC climate zone layer
- Output delivery:
  - Shapefiles with per-grid yield-loss estimates for each crop

## Key caveats and interpretation notes
- The approach uses ozone flux (POD3 IAM) rather than concentration alone to estimate global crop yield impacts.
- Species-specific flux-response data are incomplete (notably for maize, rice, soybean); relies on wheat-based dose-response and cross-crop sensitivity ratios.
- Model validation indicates good overall agreement with observed ozone patterns but uncertainties remain due to data limitations, crop diversity, and climate variability.
- In regions with multiple cropping seasons, only the primary growing period was used; this may under- or over-estimate losses in multi-season contexts.
- Future work suggested: incorporation of species-specific flux data as they become available to refine crop-specific yield-loss estimates.

## References and data sources
- Mills et al. (2018a) and Mills et al. (2018b) for methodology, model validation, and supplementary analyses.
- CLRTAP (2017) modelling and mapping practices.
- FAO FAO GAEZ dataset for crop production baselines.
- ES DAC/JRC Climate Zone GIS raster layer for climate zoning.
- GAW network observations for model validation.