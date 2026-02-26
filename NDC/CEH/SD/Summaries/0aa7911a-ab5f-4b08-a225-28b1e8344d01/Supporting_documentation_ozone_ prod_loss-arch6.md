# Modelled annual average production loss due to ozone damage for four global staple crops, 20102012

## Summary
- Assesses annual average production loss due to ozone for maize, rice, soybean, and wheat using a global 1° by 1° grid for 2010–2012.
- Combines climate-zone and hemisphere classification, irrigation status, and growing-period timing to estimate losses.
- Uses ozone uptake (POD3IAM) from the EMEP MSC-W chemical transport model and a dose–response relationship to derive yield loss, with crop-specific adjustments based on relative sensitivity to wheat.
- Produces four GIS shapefiles (one per crop) with gridded production-loss estimates, enabling spatial analysis of ozone-related impacts on staple-crop production.
- Validates model performance against GAW observations, showing good correlations, and discusses key uncertainties and caveats.

## Data sources and collection
- Crop production data: FAO Global Agro-Ecological Zones (GAEZ) dataset (year 2000) at 0.0833° resolution; aggregated to 1°×1° grid cells.
- Climate zones: Global Climate Zone GIS raster from the European Soil Data Centre (ESDAC), JRC.
- Growing periods: 90-day growing windows per climate zone and hemisphere (sourced from USDA/FAO data; table of start/end days per crop and zone).
- Irrigation: Grid cells classified as irrigated if >75% irrigated production; otherwise non-irrigated.
- Ozone modelling: EMEP MSC-W model (version 4.16) used to compute daily ozone flux (POD3IAM) for 2010–2012, with separate irrigated vs non-irrigated flux outputs.

## Modelling approach
- Wheat: uses POD3IAM to estimate yield loss via CLRTAP 2017 dose–response relationship; subtracts a pre-industrial reference POD3IAM = 0.1 mmol/m2; applies slope 0.64 to convert to percent yield loss.
- Maize, rice, soybean: lack crop-specific flux–yield data; estimate yield loss by applying the relative ozone sensitivity of each crop to wheat’s yield-loss, using their M7 (7-hour mean ozone concentration) response functions to derive crop-specific slopes.
- For each grid cell:
  - Compute 90-day POD3IAM based on the cell’s climate/hemisphere growing period.
  - Apply wheat-based yield loss, then scale by crop-specific relative sensitivity to obtain final yield loss.
  - Convert to production loss using grid-cell crop production (2010–2012 average) and aggregate into the 1° grid.
- Outputs: production loss (thousand tonnes) per grid cell; results stored in four shapefiles (one per crop).

## Data structure and outputs
- Four GIS shapefiles (one per crop): maize, rice, soybean, wheat.
- Grid resolution: 1° by 1°.
- Attribute fields (5 per grid cell):
  1) ID: Unique grid cell identifier
  2) Zone: Climate zone
  3) Long_Lat: Center coordinates (decimal degrees)
  4) Hemisphere: Northern, Southern, or Far South (for wheat/maize in Cool temperate)
  5) ProdLoss: Annual average production loss (thousand tonnes) for 2010–2012
- Outputs enable spatial analysis of ozone-driven production losses for major global crops.

## Quality control and validation
- Model validation using Global Atmosphere Watch (GAW) observations shows good correlation for Dmax and M7 (r2 ≈ 0.88–0.93) across sites.
- Additional validation linked stomatal conductance proxies: ratio of actual to potential evapotranspiration (AET/PET) versus POD3IAM/M7 shows a notable correlation (r2 = 0.63).
- The methodology represents a first-use of ozone flux (POD3IAM) rather than concentration alone to assess crop-wide impacts; results include caveats and call for species-specific flux data as it becomes available.

## Caveats and limitations
- For maize, rice, and soybean, there are no dedicated flux–response relationships; estimates rely on wheat-derived flux data scaled by relative sensitivity, introducing uncertainty.
- Maize data are based on only three older varieties, increasing uncertainty for that crop.
- Only the most important growing period per crop is used in multi-season climates (e.g., India); multi-season crops may be underrepresented in some regions.
- Differences in ozone uptake due to species or environment are assumed to be less influential than concentration differences (captured via M7), but this remains a source of uncertainty until species-specific data are available.

## References and data access
- Primary methodology and validation papers:
  - Mills et al. (2018a, 2018b) on global ozone yield impacts and model validation.
- Data sources:
  - FAO Global Agro-Ecological Zones (GAEZ) dataset
  - EMEP MSC-W chemical transport model (version 4.16)
  - CLRTAP 2017 dose–response framework
  - Global Atmosphere Watch (GAW) measurements for validation
  - ES DAC/JRC climate zone raster layer
- Additional details and supplementary information available in the cited Mills et al. papers.