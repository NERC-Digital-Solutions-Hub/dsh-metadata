# Modelled average percentage yield loss due to ozone damage for four global staple crops (20102012)

## Objective and outputs
- Estimate average yield loss due to ozone for maize, rice, soybean, and wheat during 2010–2012.
- Produce four GIS shapefiles (one per crop) enabling spatial exploration and self-service analysis.

## Data sources and collection
- Ozone exposure and uptake modeling:
  - Wheat: POD3IAM metric (phytotoxic ozone dose above 3 nmol m-2 s-1) derived from the EMEP MSC-W chemical transport model (version 4.16).
  - Other crops: use relative ozone sensitivity derived from wheat-based flux results.
  - Model outputs include irrigated and non-irrigated POD3IAM values.
- Crop production data:
  - FAO Global Agro-Ecological Zones (GAEZ) dataset (year 2000), 0.0833° resolution; used to compute grid-cell production and irrigation classification.
- Spatial and climate classification:
  - Climate zones from ESDAC GIS layer (JRC).
  - Hemisphere classification (Northern, Southern, and Far South for Cool temperate).
- Growing period framing:
  - 90-day growing periods per climate zone and hemisphere, informed by USDA/FAO data.
- Data processing references:
  - Main methodological sources: Mills et al. (2018a, 2018b) for yield loss calculation and model validation.

## Spatial-temporal framework
- Grid structure:
  - 1° by 1° global grid; crop production mapped to grid cells.
- Irrigation and climate context:
  - Each grid cell classified as irrigated if >75% of crop production is irrigated; otherwise non-irrigated.
  - Grid cells assigned to climate zones and hemispheres to define crop growing periods.
- Yield loss calculation period:
  - Focused on 2010–2012 for averaging yield losses.

## Calculation workflow
- Wheat baseline and yield-loss calculation:
  - Yield loss for wheat: Percent Yield Loss = (POD3IAM − 0.1) × 0.64, where 0.1 mmol/m2 represents pre-industrial ozone uptake.
- Cross-crop adjustment via relative sensitivity:
  - Relative sensitivity for maize, rice, and soybean computed from M7 (7-hour mean ozone) dose-response slopes relative to wheat.
  - Slopes used (from published data): soybean, wheat, rice, maize with respective linear relationships; relative sensitivity = crop slope / wheat slope.
  - Final crop yield loss = wheat yield loss × relative sensitivity.
- Data products:
  - For each crop, compute grid-cell yield loss and save as GIS shapefiles (1° by 1°).

## Output data structure
- Four GIS shapefiles (one per crop: maize, rice, soybean, wheat).
- Each shapefile contains 1° by 1° grid cells with 5 attributes:
  - ID: Unique grid cell identifier.
  - Zone: Climate zone for the cell.
  - Long_Lat: Central coordinates of the grid cell.
  - Hemisphere: Northern, Southern, or Far South classification.
  - Yield loss: Average percentage yield loss for 2010–2012.

## Quality control and validation
- Model validation approach:
  - Comparison of EMEP model outputs with Global Atmosphere Watch (GAW) observations to assess spatial and temporal performance during peak ozone episodes.
  - Strong correlation between modeled and observed metrics for Dmax and M7 (r2 approximately 0.88–0.93) with low scatter.
- Stomatal uptake proxy validation:
  - Correlation between Actual Evapotranspiration (AET)/Potential Evapotranspiration (PET) and POD3IAM/M7 proxy (r2 ≈ 0.63), suggesting reasonable estimation of stomatal conductance.
- Uncertainties and caveats:
  - No direct ozone flux–yield data for maize, rice, and soybean; flux-based adjustments rely on wheat flux as a proxy.
  - Maize data limited to three older varieties, increasing uncertainty for maize-specific yield losses.
  - Some climates have multiple growing seasons; this study uses only the most important growing period per crop per climate.
  - Global-scale uncertainties acknowledged; future work recommended when species-specific flux data become available.

## Data and methodological caveats (summary)
- Ozone flux approach supersedes concentration-only methods but remains contingent on limited species-specific flux data beyond wheat.
- The approach assumes concentration differences (captured by the M7 metric) drive uptake variability more than species-specific uptake differences.
- Results are most robust where data coverage and crop-specific flux data are strongest; uncertainties are higher for poorly represented crops or climates.

## References and supporting materials
- Mills et al. (2018a, 2018b) for methodology, model validation, and flux-based yield-loss framework.
- Related data sources: CLRTAP guidelines; FAO GAEZ; ESDAC GIS climate zones; GAW network observations.