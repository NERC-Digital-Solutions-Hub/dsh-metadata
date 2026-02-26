# Yield Constraint Score (YCS) for the effect of five crop stresses on global production of four staple food crops.

## Overview
- A global, grid-based (1° by 1°) set of Yield Constraint Scores (YCS) assessing the impact of five stresses (ozone, pests and diseases, soil nutrients, heat, aridity) on four staple crops (maize, rice, soybean, wheat).
- For each grid cell and crop, YCS values (1–5) are produced per stress and summed to a total YCS.
- Outputs are GIS shapefiles with per-cell stress scores and totals to support data-driven decision making and prioritisation.

## Data sources and collection
- Ozone yield constraint
  - Data: POD3 IAM ozone flux (POD3IAM) from the EMEP MSC-W model (2010–2012).
  - Processing: convert daily ozone uptake to yield loss using CLRTAP dose–response with a pre-industrial reference (0.1 mmol/m²) and a slope of 0.64; adjust crop-specific sensitivity relative to wheat using published 7-hour mean ozone response functions (M7) to derive crop-specific yield losses; categorize into YCS 1–5.
  - Notes: no species-specific flux data for maize, rice, soybean; wheat-based flux scaled by relative sensitivity.

- Pests and diseases yield loss
  - Data: regional mean yield losses (2002–2004) from Oerke et al., compiled in CABI/Global datasets.
  - Processing: assign 1–5 categories (0–5%, 5–10%, 10–25%, 25–40%, >40% losses) and map to grid cells by country/region; grid cells with multiple countries use majority crop area.
  - Notes: potential overestimation due to vintage and regional aggregation.

- Soil nutrients yield loss
  - Data: soil nutrient availability and retention from HWSD-based classifications via GAEZ v3.
  - Processing: combine topsoil and subsoil assessments (with weighting by active root prevalence) to five stress classes; assign to grid cell majority constraint.
  - Notes: expert judgement used where numerical scores are unavailable; HWSD-based data are extensive but come with regional reliability variations.

- Heat stress yield loss
  - Data/Method: heat stress following Challinor et al. (2005), Deryng et al. (2014), Teixeira et al. (2013).
  - Processing: define a 30-day thermal-sensitive period (TSP) within the 90-day growing window; compute daily heat stress f HSd from daily effective temperature; average to get final f HS per grid cell; categorize into YCS 1–5.
  - Temperature data: hourly ECMWF reanalysis (1990–2014).

- Aridity yield loss
  - Data: Global Aridity Index (Trabucco & Zomer 2009) at 0.083° resolution; mean precipitation (WorldClim 1950–2000) and PET (Global-PET).
  - Processing: compute Aridity Index per 1° cell and map climate classes to YCS 1–5.
  - Notes: aridity values averaged over 1950–2000; potential co-occurrence with heat stress acknowledged.

## Growth periods and climate stratification
- Cells are classified as irrigated vs non-irrigated (based on >75% irrigated production).
- Grid cells are assigned to hemispheres (North/South) and climate zones (ESDAC JRC layer).
- A 90-day growing period per crop-climate-hemisphere combination defines the temporal window for stress calculations; detailed start/end day ranges are provided per crop and climate zone.

## Data processing and outputs
- Per-crop processing culminates in four YCS GIS shapefiles (one per crop: maize, rice, soybean, wheat).
- Each grid cell includes eight attributes:
  - ID, Long_Lat, Ozone, Nutrient, Aridity, Heat, Pests, Total.
- Total YCS is the sum of the five stress scores per cell; outputs support spatial prioritisation and cross-stress analysis.

## Quality control and validation
- Model validation for ozone-related flux and yield loss incorporates:
  - Model–observation comparisons (Global Atmosphere Watch data) showing good spatial/temporal alignment.
  - Strong correlations (r² typically 0.88–0.93) between model outputs (Dmax, M7) and observations at multiple GAW sites.
  - Additional validation linking modeled POD3IAM to stomatal conductance proxies (AET/PET).
- Uncertainty considerations highlighted:
  - Cross-crop flux relationships for maize, rice, soybean due to lack of species-specific flux data.
  - Pest/diseases data are from 2002–2004 and may overstate current losses; regional granularity vs. country-level variation.
  - Soil nutrient stress relies on expert judgement and HWSD/GAEZ data with known reliability caveats.
  - Heat and aridity indices rely on historical climate data; potential co-occurrence effects and methodological choices explained.

## Data governance, stewardship and reuse
- Data lineage: multiple established datasets (EMEP, GAW, FAO GAEZ, HWSD, WorldClim, ECMWF, Trabucco & Zomer) integrated to derive per-stress YCS.
- Data format and accessibility: shapefiles per crop with clearly defined attributes enabling interoperability with standard GIS workflows.
- Reproducibility and updates: methodology references detailed; structure supports re-running with updated datasets (e.g., newer flux data, revised climate inputs) as data become available.
- Limitations to consider in reuse: cross-crop sensitivity assumptions, vintage limitations of pest data, and regional variability in underlying soil and climate data.

## Practical implications for Data Leaders
- Demonstrates end-to-end data pipeline from diverse sources to a harmonised, policy-relevant, spatially explicit product.
- Highlights the importance of cross-disciplinary data integration (climate, soil, agronomy, pests) and the need for transparent uncertainty articulation.
- Provides a scalable framework for expanding to additional crops, stresses, or finer spatial resolution as data quality improves.
- Useful as a governance case for data provenance, metadata richness, and stakeholder-aligned data products (e.g., informing resilience and adaptation planning).