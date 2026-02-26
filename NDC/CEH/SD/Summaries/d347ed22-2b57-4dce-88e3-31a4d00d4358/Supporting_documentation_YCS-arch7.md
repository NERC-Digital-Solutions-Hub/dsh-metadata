# Yield Constraint Score (YCS) for the effect of five crop stresses on global production of four staple food crops

- Purpose: Develop a global, map-based assessment of yield constraints on maize, rice, soybean, and wheat due to five stresses (ozone, pests and diseases, soil nutrients, heat, aridity) to support spatial analysis of crop vulnerability.
- Outputs: Four GIS shapefiles (one per crop) at 1° by 1° resolution, with per-cell yield constraint scores and a total score.

## Data and grid construction

- Grid cells: 1° by 1° global grid created in ArcMap (v10.3); crop production data at 0.0833° (GAEZ FAO) for 2000, separated into irrigated and non-irrigated production, summed per 1° cell.
- Temporal adjustment: For each crop, average production for 2010–2012 estimated using a conversion factor from FAO national data, based on 1999–2001 vs 2010–2012 differences. Cells with >500 tonnes production included.
- Irrigation classification: Cells with >75% irrigated production labeled irrigated; others non-irrigated.
- Climate context: Each cell assigned to hemisphere (North/South) and climate zone using a GIS layer from ESDAC/JRC.
- Growing period: 90-day growing period defined per climate zone and hemisphere (based on USDA/FAO data) to drive stress calculations.

## Stress-specific Yield Constraint Score (YCS) methods

- Ozone YCS
  - Used POD3IAM (daily ozone uptake proxy) from the EMEP model to estimate ozone flux and crop-specific yield loss over the 90-day growing period.
  - Wheat-based dose–response used as the reference; other crops scaled by their relative ozone sensitivity to wheat.
  - Yield loss converted to a 1–5 YCS category (0–5%, 5–10%, 10–25%, 25–40%, >40% loss).

- Pests and diseases YCS
  - Based on literature-based regional yield losses (Oerke 1994, 2006) for maize, rice, soybean, and wheat (2002–2004 data).
  - Assigned to 1° grid cells by country/region; yields translated into five-category YCS (0–5%, 5–10%, 10–25%, 25–40%, >40%).

- Soil nutrients YCS
  - Nutrient availability and retention classifications drawn from HWSD-based GAEZ v3 data (0–30 cm and 30–100 cm layers).
  - Combined into five stress classes via a fixed table; per-cell dominant soil nutrient class used to assign YCS (no/ slight to very severe constraints).

- Heat YCS
  - 30-day thermal-sensitive period (TSP) within the 90-day growing period; critical temperatures per crop (e.g., soybean 35/40°C, wheat 25/35°C, rice 35/45°C, maize 32/45°C).
  - Daily heat stress fHSd calculated from daily effective temperature (hourly data averaged to daily) and aggregated to a 0–1 index over the 30-day window; then categorized into five YCS levels (0, <0.05, 0.05–0.15, 0.15–0.3, >0.3).

- Aridity YCS
  - Global Aridity Index per cell derived from mean annual precipitation and potential evapotranspiration (1950–2000 basis).
  - Aridity climate classes mapped to five YCS levels (humid to hyperarid).

## Data integration and scoring

- For each grid cell and crop:
  - Compute individual YCS values for ozone, pests, nutrients, heat, and aridity.
  - Total YCS = sum of the five stress scores (range depends on per-stress categorization).
- Output: Four shapefiles (one per crop) with 1° grid cells and attributes.

## Data structure and attributes

Each crop shapefile includes 8 main attributes per grid cell:
- ID: Unique cell identifier
- Long_Lat: Center coordinates (longitude, latitude)
- Ozone: YCS for ozone (1–5)
- Nutrient: YCS for soil nutrients (1–5)
- Aridity: YCS for aridity (1–5)
- Heat: YCS for heat stress (1–5)
- Pests: YCS for pests and diseases (1–5)
- Total: Sum of all five stress YCS

## Quality control and validation

- EMEP model validation (2010–2012 data) against Global Atmosphere Watch (GAW) observations showed good correlation for Dmax and M7 (r2 about 0.88–0.93) with minimal scatter.
- Model performance checks included stomatal uptake proxy (AET/PET ratio) versus POD3IAM/M7, showing a strong relationship (r2 = 0.63).
- Uncertainties discussed:
  - Absence of crop-specific ozone flux–yield relationships for maize, rice, and soybean; reliance on wheat baseline and relative sensitivities.
  - Limited and dated pests/diseases data (2002–2004) and regional aggregation; potential mismatch with current practices.
  - Soil nutrient stress data rely on expert judgment and HWSD/GAEZ integration; possible regional inconsistencies.
  - Heat and aridity calculations depend on chosen climate data and timelines; potential differences with other studies.

## Uncertainty and limitations (summary)

- Species-specific ozone uptake data are lacking for some crops; results depend on relative sensitivity to wheat.
- Pest/disease losses are historical and regionally generalized; current protection measures may change actual losses.
- Soil nutrients: reliance on global soil databases with varying regional reliability and resolution.
- Heat and aridity indices depend on data choices and timeframes; co-occurrence and interaction effects may be complex.

## References and data sources (selected)

- Climate/zonal data: Climate Zone GIS layer (ESDAC/JRC)
- Crop production: FAO Global Agro-Ecological Zones (GAEZ)
- Soil data: Harmonized World Soil Database (HWSD) and GAEZ v3
- Ozone model and validation: EMEP MSC-W model; CLRTAP dose–response framework
- Temperature/heat stress methods: Challinor et al. (2005), Deryng et al. (2014), Teixeira et al. (2013)
- Pests/diseases losses: Oerke (1994, 2006)
- Aridity index: Trabucco & Zomer (2009); WorldClim PET data

## How GIS specialists can use this work

- Integrate per-crop YCS shapefiles into regional or global risk assessments for policy, planning, or communication.
- Overlay with additional GIS layers (crop distributions, irrigation, land use, climate projections) to explore alternative scenarios.
- Use the 1° grid framework to compare spatial patterns of stress and identify hotspots of yield constraint.