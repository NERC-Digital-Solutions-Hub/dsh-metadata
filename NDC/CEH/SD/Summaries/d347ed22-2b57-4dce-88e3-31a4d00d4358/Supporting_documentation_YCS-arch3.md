# Yield Constraint Score (YCS) for the effect of five crop stresses on global production of four staple food crops.

## Summary
- Purpose: Quantify global crop yield losses from five stresses (ozone, pests/diseases, soil nutrients, heat, aridity) for maize, rice, soybean, and wheat, to support monitoring and policy evaluation.
- Outputs: Four GIS shapefiles (one per crop) at 1°×1° resolution, each with per-cell YCS for each stress and a total YCS; data structured for clear visualization (maps, charts, dashboards).
- Data scope: Global grid-based assessment using historical data (mostly 1990–2014 temperature data, 2010–2012 ozone data, and 2002–2004 pest/disease losses), integrated with global soil and climate datasets.
- Key approach: Combine multiple stress indicators into a standardized 1–5 YCS per stress, then sum to a total score per grid cell.

## Methodology overview by crop stress

- Ozone yield constraint score (YCS)
  - Compute for each 1°×1° cell using a 90-day growing window by hemisphere/climate zone; classify cells as irrigated or non-irrigated.
  - Use POD3IAM (phytotoxic ozone dose above 3 nmol m⁻² s⁻¹) with baseline 0.1 mmol/m²; convert to relative yield loss via a 0.64 slope (wheat reference).
  - Derive percent yield loss per cell, assign to YCS categories (1–5).
  - Adjust maize, rice, and soybean yield loss by crop-specific relative ozone sensitivity compared to wheat (based on M7 responses); apply to wheat baseline to obtain final crop-specific losses.
  - Outputs: Ozone YCS per crop per grid cell.

- Pests and diseases YCS
  - Use regional yield loss estimates from Oerke (1994, 2006) for maize, rice, soybean, wheat (2002–2004).
  - Map regional losses to 1–5 YCS classes (0–5%, 5–10%, 10–25%, 25–40%, >40%).
  - Assign to grid cells based on majority-crop region; if multiple countries, assign by dominant crop area in cell.

- Soil nutrients YCS
  - Derived from GAEZ v3; HWSD v1.1 data for nutrient availability and retention (topsoil 0–30 cm, subsoil 30–100 cm).
  - Combine availability and retention into five classes; assign per grid cell by majority soil class in cropped areas.
  - Note: NA for permafrost or water bodies; acknowledged uncertainties due to cross-dataset inconsistencies.

- Heat stress YCS
  - Follow Challinor et al. approach with a 30-day thermal-sensitive period (TSP) during the crop’s reproductive phase.
  - Use daily effective temperature (T_eff) from hourly ECMWF data (1990–2014) to compute daily heat stress f_HSd, then average over 30-day TSP to yield f_HS.
  - Categorize into five YCS levels (0, <0.05, 0.05–0.15, 0.15–0.3, >0.3).

- Aridity YCS
  - Use mean Aridity Index (1950–2000) from Trabucco & Zomer with precipitation (WorldClim) and PET (Global-PET).
  - Assign aridity climate classes (Humid, Dry sub-humid, Semi-arid, Arid, Hyper-arid) mapped to 1–5 YCS categories.

- Total YCS
  - Sum the per-stress YCS values for each grid cell across ozone, pests, soil nutrients, heat, and aridity to produce a total YCS per crop.

## Data inputs, processing, and structure

- Grid and crop data
  - Grid: 1°×1° cells; crop production data from FAO GAEZ (year 2000 baseline) rescaled to 2010–2012 using national production changes.
  - Irrigation: cells classified as irrigated or non-irrigated based on a 75% threshold for irrigated production.
  - Climate zoning: cells assigned to hemisphere and climate zone (ESDAC/JRC layer).
  - Growing periods: 90-day windows per climate zone/hemisphere defined (based on USDA/FAO data) for calculating ozone and heat exposures.

- Data sources and technologies
  - Ozone model: EMEP MSC-W (v4.16) and CLRTAP dose–response frameworks.
  - Temperature/heat: ECMWF hourly data (1990–2014).
  - Pests/diseases: Oerke (1994, 2006) syntheses; regional losses.
  - Soil nutrients: HWSD v1.1; GAEZ v3.
  - Aridity: Trabucco & Zomer (1950–2000 means); WorldClim precipitation; Global-PET PET data.
  - Validation: Model evaluation against GAW data; Dmax and M7 comparisons; stomatal uptake proxy correlations.

- Outputs and files
  - Four GIS shapefiles (maize, rice, soybean, wheat), each with 1°×1° grid cells and eight attributes: ID, Long_Lat, Ozone, Nutrient, Aridity, Heat, Pests, Total.
  - Summary table (Table 3 in the source) detailing YCS category mappings and stress definitions.

## Quality control and validation

- Model validation for ozone flux and yield loss
  - Comparison of model outputs with Global Atmosphere Watch (GAW) observations; good spatial/temporal alignment in 2012 data.
  - r² values for modelled vs observed Dmax and M7 between about 0.88 and 0.93 with modest scatter.
  - Strong correlation (r² ≈ 0.63) between proxy stomatal conductance (AET/PET) and POD3IAM/M7 as a check on uptake estimation.

- Uncertainty and caveats
  - No crop-specific ozone flux–response data for maize, rice, or soybean; relied on wheat flux with crop-specific sensitivity adjustments, introducing species-specific uncertainty.
  - Maize data limited (only three older varieties), increasing uncertainty for that crop.
  - Pest/disease losses based on 2002–2004 regional data; may overstate current losses due to improved practices; regional scale with within-region variability.
  - Soil nutrient YCS relies on HWSD-derived classifications and expert judgment; potential inconsistencies across regions and scales.
  - Heat stress methodology differs from some prior studies due to data choices and climate-zone windows; results broadly align with other wheat-focused analyses but differ in regional risk patterns.
  - Aridity index uses 1950–2000 means, introducing potential mismatch with 2010–2012 ozone impacts; co-occurrence with heat stress acknowledged.

## Data governance and accessibility

- Data handling emphasizes openness and transparency (public sharing of underlying data where possible) but notes potential barriers related to metadata gaps and dataset sharing.
- The approach includes clear documentation of methods, uncertainties, and validation to support reproducibility and governance.

## Key references and data sources

- Ozone and crop yield modeling: Mills et al. (2018a, 2018b); Global Change Biology
- EMEP/CLRTAP framework and ozone flux methodology
- GAEZ and HWSD soil resources (FAO/IIASA/ISRIC/ISS-CAS/JRC)
- Pests and diseases yield losses: Oerke (1994, 2006)
- Aridity and climate datasets: Trabucco & Zomer (2009); WorldClim
- Temperature/heat stress: Challinor et al. (2005); Deryng et al. (2014); Teixeira et al. (2013)

## Practical takeaways for Monitoring Framework Authors

- The YCS framework provides a reproducible, grid-based (1°×1°) method to quantify and compare multiple stressors affecting global staple crops, suitable for monitoring policy impacts and identifying hot spots.
- It integrates ozone exposure, pests/diseases, soil nutrient constraints, heat stress, and aridity, with a transparent scoring system (1–5 per stress) and a total stress burden per grid cell.
- Outputs are ready for visualization in dashboards and GIS-based policy analyses, with explicit data sources, validation steps, and acknowledged uncertainties to inform decision-making and data governance considerations.