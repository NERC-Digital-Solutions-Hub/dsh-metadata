# Yield Constraint Score (YCS) for the effect of five crop stresses on global production of four staple food crops.

## Objective and scope
- Quantifies yield constraint scores (YCS) for five stresses (ozone, pests and diseases, soil nutrients, heat, aridity) on four crops (maize, rice, soybean, wheat) at a global scale.
- Produces gridded data products (GIS shapefiles) at 1° by 1° resolution, with per-grid-cell YCS for each stress and a total YCS.
- Data product intended for cross-cector data exploration and decision-support.

## Data sources and preprocessing
- Crop production data: FAO Global Agro-Ecological Zones (GAEZ); grid cells 1°×1°; 0.0833° resolution production data; irrigated/non-irrigated classification; 2010–2012 period; grid cells with >500 tonnes included.
- Ozone data and modelling: EMEP MSC-W chemical transport model (v4.16) producing POD3 IAM (phytotoxic ozone dose above 3 nmol m-2 s-1); hourly inputs (ozone, temperature, VPD, irradiance, soil moisture); 2010–2012 period; model validation against GAW measurements.
- Heat stress: daily heat stress index based on a 30-day thermal-sensitive period (TSP), using daily hourly temperature data (1990–2014) and crop-specific Tcrit/Tlim values.
- Aridity: Global Aridity Index (1950–2000) from Trabucco & Zomer; precipitation (WorldClim 1950–2000) and PET (Global-PET) to compute index; UNEP 1997 climate classifications used for categories.
- Pests and diseases: regional mean yield losses from Oerke et al. (1994, 2006) for maize, rice, soybean, wheat; 2002–2004 data; region/country-based mapping to 1°×1° cells.
- Soil nutrients: HWSD (Harmonized World Soil Database) v1.1 via GAEZ v3; soil nutrient availability and retention (topsoil 0–30 cm and subsoil 30–100 cm) with weighting by active roots; five stress classes derived by combining availability and retention.
- Summary data: Tables and supplementary information from Mills et al. (2018a,b) used for method references and classification schemes.

## Stress-specific YCS calculation approaches
- Ozone YCS
  - For each grid cell, determine 90-day growing period by climate zone/hemisphere and irrigated status.
  - Compute percentage yield loss from POD3 IAM, relative to wheat-dose-response; convert to 1–5 YCS categories (0–5%, 5–10%, 10–25%, 25–40%, >40% loss).
  - Adjust using crop-specific relative ozone sensitivity (ratio to wheat) to obtain final ozone-induced loss per crop; YCS 1–5 accordingly.
- Pests and diseases YCS
  - Use regional mean yield losses (0–40+%) and map to five-class YCS (0–5% = 1, 5–10% = 2, 10–25% = 3, 25–40% = 4, >40% = 5).
- Soil nutrients YCS
  - Combine soil nutrient availability and retention classes (topsoil and subsoil) per grid cell; map to five YCS classes per a defined matrix; if multiple countries influence a cell, the dominant crop area governs the cell’s class.
- Heat stress YCS
  - Calculate daily heat stress for the 30-day TSP using crop-specific critical/limiting temperatures; derive daily stress values and average across the 30 days.
  - Categorize final heat stress into five YCS classes using defined thresholds (0, <0.05, 0.05–0.15, 0.15–0.3, >0.3).
- Aridity YCS
  - Assign aridity class (Humid to Hyper-arid) from UNEP/UNEP climate categories based on mean aridity index (1950–2000); convert to five YCS classes (None to Very Severe) accordingly.

## Output products and data structure
- Four YCS GIS shapefiles, one per crop (maize, rice, soybean, wheat), each at 1°×1° resolution.
- Each shapefile contains 8 attributes per grid cell:
  - ID: unique cell identifier
  - Long_Lat: center coordinates (lon, lat)
  - Ozone: YCS for ozone (1–5)
  - Nutrient: YCS for soil nutrient stress (1–5)
  - Aridity: YCS for aridity stress (1–5)
  - Heat: YCS for heat stress (1–5)
  - Pests: YCS for pests and diseases (1–5)
  - Total: sum of the five stress YCS values (per grid cell)
- Outputs provide a per-crop total YCS plus individual stress components to enable self-serve analysis.

## Validation, quality control, and uncertainties
- Validation: EMEP model performance evaluated against GAW observations; good spatial-temporal fit; r^2 for Dmax and M7 between 0.88 and 0.93; stomatal uptake proxy supported by AET/PET comparison.
- Key uncertainties and caveats
  - Lack of species-specific ozone flux relationships for maize, rice, and soybean; reliance on wheat flux as baseline with crop-specific sensitivity adjustment.
  - Maize, rice, and soybean data for flux relationships have higher uncertainty due to limited experimental data.
  - Pest/disease losses derived from 2002–2004 regional data; may overestimate current losses due to changes in crop protection.
  - Soil nutrient YCS based on HWSD-derived classifications with potential regional inconsistencies and lack of crop-specific nutrient requirements.
  - Heat stress methodology differs from other studies; regional climate and crop-growth window variability; aridity and heat often co-occur.
  - Aridity index based on 1950–2000 climate data; potential mismatch with 2010–2012 ozone impact period.
- Overall, product emphasizes global-scale patterns with acknowledged uncertainties at grid and crop-specific levels; designed for cross-crop comparison and data-driven decision support.

## References and data sources (highlights)
- Mills et al. (2018a, 2018b) for ozone yield loss methodology and model validation.
- Challinor et al. (2005), Teixeira et al. (2013), Deryng et al. (2014) for heat stress approaches.
- Oerke et al. (1994, 2006) for pests and diseases losses.
- HWSD (2011, FAO/IIASA/ISRIC/ISS-CA) and GAEZ data for soils and production.
- ECMWF IFS data for hourly temperature; GAW for model validation.
- Trabucco & Zomer (2009) and WorldClim for aridity and climate data.
- CLRTAP (2017) dose–response framework; UNEP climate classifications.

## Notes for data users
- Outputs are designed for exploration and integration with other data products; the per-grid-cell breakdown enables cross-stress analysis and scenario assessment.
- Users should consider the stated uncertainties when interpreting results, especially for crops with limited flux data (maize, rice, soybean) and historical pest/disease loss estimates.