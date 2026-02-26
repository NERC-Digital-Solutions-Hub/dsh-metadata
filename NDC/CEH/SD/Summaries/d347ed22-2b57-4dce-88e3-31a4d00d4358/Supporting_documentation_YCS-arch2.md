# Yield Constraint Score (YCS) for the effect of five crop stresses on global production of four staple food crops.

## Overview
- Global, grid-based assessment of how five stresses constrain yields for maize, rice, soybean, and wheat.
- Produces 4 GIS shapefiles (1° x 1° grid) with per-cell scores for each stress and a total score.
- Uses standardized data sources and methods to support environmental monitoring and policy evaluation.

## Data collection and grid setup
- 1° by 1° grid created in ArcMap; crop production data at 0.0833° resolution from FAO GA Ez (year 2000) with irrigated and non-irrigated breakdown.
- Total production summed per grid cell; 2010–2012 average production estimated per cell using a conversion factor from FAO national data (based on 1999–2001 vs 2010–2012 changes).
- Only grid cells with >500 tonnes production included for mapping.
- For each cell, irrigated vs non-irrigated classified (>75% irrigated production deemed irrigated).
- Cells assigned to hemisphere (North/South) and to a global climate zone (ESDAC JRC climate zones).

## Yield Constraint Scores by stress

### Ozone Yield Constraint Score (YCS)
- 90-day growing period per climate zone/hemisphere based on main growing season (crop-specific windows in Table 1 of the source).
- Ozone flux model: EMEP MSC-W (POD3 IAM) using hourly ozone, temperature, VPD, irradiance, and soil moisture to produce daily POD3IAM; separate irrigated vs rain-limited (non-irrigated) pathways.
- Yield loss estimated using CLRTAP 2017 dose–response: Percent Yield Loss = (POD3IAM − 0.1) × 0.64, with 0.1 representing pre-industrial ozone uptake.
- Relative ozone sensitivity for each crop (compared to wheat) derived from M7 response functions; final crop yield loss = wheat-based loss × crop’s relative sensitivity.
- YCS categories: 1 = 0–5%, 2 = 5–10%, 3 = 10–25%, 4 = 25–40%, 5 = >40% loss.

### Pests and Diseases YCS
- Based on literature-derived regional mean yield losses for 2002–2004 (pre-harvest losses with crop protection applied) from Oerke sources.
- Assigned to 1° x 1° cells by country/region; if multiple countries in a cell, majority crop area country used.
- Five-category scale as for ozone (1–5).

### Soil Nutrients YCS
- Nutrient availability and nutrient retention classes from GAEZ v3, derived from HWSD v1.1 soil data (texture, organic carbon, pH, bases; retention from texture, CEC, pH).
- For each cell, average of topsoil (0–30 cm) and subsoil (30–100 cm) combined by rooting prevalence.
- Five-class mapping (No/slight, Moderate, Severe, Very Severe, etc.) collapsed into five YCS levels via a crosswalk (Table S2 in the supplement).

### Heat Stress YCS
- Heat stress follows Challinor et al. (2005) approach; daily heat stress (fHSd) calculated during a 30-day thermal-sensitive period (TSP): days 40–70 of the 90-day growing window.
- Critical and limiting temperatures per crop sourced from Deryng et al. (2014) and Teixeira et al. (2013).
- Daily effective temperature (Teff) computed from hourly data (daily mean + daily max)/2; hourly data from ECMWF IFS (1990–2014).
- Daily fHSd aggregated over 30-day TSP; converted to 0–1 index (Teixeira et al. approach).
- Final YCS for heat stress categorized into five levels: 1 = 0; 2 = <0.05; 3 = 0.05–0.15; 4 = 0.15–0.30; 5 = >0.30.

### Aridity YCS
- Global Aridity Index calculated from mean annual precipitation (WorldClim 1950–2000) and potential evapotranspiration (Global-PET model; Trabucco & Zomer 2009).
- Mean Aridity Index per cell for production areas; climate-class mapping used to assign five YCS levels (1 = Humid, 5 = Hyper-arid).

## YCS calculation and outputs
- For each grid cell and each crop, the five stress YCS values are calculated and stored.
- Total YCS per cell is the sum of the five stress scores.
- Outputs are four GIS shapefiles (one per crop) with 1° x 1° grid cells and 8 attributes:
  - ID, Long_Lat, Ozone, Nutrient, Aridity, Heat, Pests, Total.

## Quality control and validation
- EMEP model validation against Global Atmosphere Watch (GAW) data showed good spatial and temporal performance; r^2 for Dmax and M7 between 0.88–0.93 in 2012 after outlier handling.
- Stomatal uptake proxy correlation (AET/PET) with POD3IAM/M7 showed r^2 = 0.63, supporting reasonable estimation of stomatal uptake.
- Uncertainties acknowledged:
  - No crop-specific ozone flux data for maize, rice, and soybean; relative crop sensitivities used instead of species-specific flux-response data.
  - Maize data limited to three older varieties, increasing uncertainty for that crop.
  - Pests/diseases data come from 2002–2004; practices since then may reduce losses, introducing regional uncertainty.
  - Soil nutrient YCS relies on expert judgment to map HWSD-derived classes to five-score categories; potential regional inconsistencies.
  - Heat stress uses a 1990–2014 hourly dataset and climate-zone windows; differences with other studies reflect methodological choices.
  - Aridity index based on 1950–2000 data; potential mismatch with 2010–2012 ozone impact patterns; aridity and heat stress co-occurrence complicates attribution.

## Data sources and references
- Main methodology references: Mills et al. (2018a) and Mills et al. (2018b).
- Data sources: FAO GA Ez (2000 data), GAEZ dataset, HWSD, EMEP/MSC-W model, CLRTAP dose–response, GAW observations, WorldClim, Global-PET, ESDAC climate zone layer.
- Supplementary information documents provide detailed validation, uncertainty analyses, and data processing steps.