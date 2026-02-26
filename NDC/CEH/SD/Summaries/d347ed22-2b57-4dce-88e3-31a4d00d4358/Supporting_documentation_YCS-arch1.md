# Yield Constraint Score (YCS) for the effect of five crop stresses on global production of four staple food crops.

## Overview
- Purpose: Derive Yield Constraint Scores (YCS) for five stresses (ozone, pests and diseases, soil nutrients, heat, aridity) affecting global production of maize, rice, soybean, and wheat.
- Output: Four 1° by 1° GIS shapefiles (one per crop) with YCS per stress and a total YCS per grid cell.
- Scale: Global, grid-based assessment integrating multiple data sources and models to estimate potential yield losses and classify them into a 1–5 scale.

## Data sources and grid construction
- Grid system and crops
  - 1° by 1° grid cells created; crop production data at 0.0833° (GAEZ FAO) for 2000, with irrigated/non-irrigated production per crop.
  - Grid cells with >500 tonnes production included; 2010–2012 average production estimated via conversion factors from FAO national data.
- Irrigation and climate context
  - Cells classified as irrigated if >75% irrigated production; otherwise non-irrigated.
  - Hemisphere (North/South) and climate zone assigned using GIS layers (ESDAC climate zones).
  - For each crop, a 90-day growing period defined per climate zone/hemisphere (based on USDA/FAO data) to tailor stress calculations.
- Data sources for stresses
  - Ozone: EMEP MSC-W model (POD3 IAM) for 2010–2012; hourly ozone-related inputs (Dmax, M7) from model outputs.
  - Pests and diseases: literature-based regional yield losses (Oerke 1994, 2006) applied to 2002–2004 period data.
  - Soil nutrients: HWSD-derived soil nutrient availability and retention (GAEZ v3) with topsoil and subsoil classifications; combined to yield constraint scores.
  - Heat stress: Temperature data from ECMWF (1990–2014); 30-day thermal sensitive period (days 40–70) with crop-specific critical and limiting temperatures.
  - Aridity: Global Aridity Index (Trabucco & Zomer 2009) averaged 1950–2000; aridity climate classes per UNEP (1997) used for scoring.

## Stress-specific YCS methodologies

- Ozone Yield Constraint Score (YCS)
  - Compute 90-day growing period ozone dose (POD3 IAM) per grid cell; convert to yield loss using CLRTAP-based dose–response for wheat: Percent Yield Loss = (POD3IAM − 0.1) × 0.64.
  - For non-wheat crops (maize, rice, soybean), derive relative ozone sensitivity by dividing each crop’s M7 slope by wheat’s M7 slope; multiply wheat yield loss by this relative sensitivity to obtain crop-specific yield loss.
  - Convert yield loss to YCS categories (1: 0–5%, 2: 5–10%, 3: 10–25%, 4: 25–40%, 5: >40%).

- Pests and Diseases YCS
  - Use mean regional yield losses (2002–2004) from Oerke et al. to assign YCS in 1–5 categories (0–5%, 5–10%, 10–25%, 25–40%, >40%).

- Soil Nutrients YCS
  - Combine soil nutrient availability and nutrient retention classes (HWSD-derived) to five stress classes.
  - Assign grid-cell YCS based on the majority soil class within each cell; note substantial uncertainty due to data and expert judgement.

- Heat Stress YCS
  - Define heat stress using a daily heat-stress index over a 30-day thermal-sensitive period (TSP) with crop-specific critical (Tcrit) and limiting (Tlim) temperatures.
  - Calculate daily fHSd from hourly/ daily temperature data; average over the 30-day TSP to obtain fHS per grid cell.
  - Categorize into YCS: 1 = 0, 2 = <0.05, 3 = 0.05–0.15, 4 = 0.15–0.3, 5 = >0.3.

- Aridity YCS
  - Use mean Aridity Index (1950–2000) from Trabucco & Zomer; classify into aridity climate classes (humid to hyper-arid) per UNEP scheme.
  - Translate aridity class into YCS (1–5) corresponding to increasing constraint.

## YCS calculation and outputs
- Per grid cell, sum the five stress scores (ozone, pests, nutrients, heat, aridity) to produce a Total YCS.
- Outputs: four shapefiles (one per crop: maize, rice, soybean, wheat) with 1° by 1° resolution.
- Shapefile attributes (8 columns per grid cell)
  - ID: unique grid cell identifier
  - Long_Lat: center coordinates
  - Ozone: YCS for ozone
  - Nutrient: YCS for soil nutrients
  - Aridity: YCS for aridity
  - Heat: YCS for heat
  - Pests: YCS for pests and diseases
  - Total: sum of all five stress YCS

## Model validation and quality control
- Ozone model validation
  - Mills et al. (2018b): comparison of modelled vs. observed ozone (GAW sites) showing good correlation (Dmax and M7) with r2 ~ 0.88–0.93.
  - Demonstrated plausibility of stomatal uptake via AET/PET proxy (r2 = 0.63 for wheat scenario).
- General caveats
  - First global attempt using ozone flux (POD3 IAM) rather than concentration to estimate crop impacts; recognition of uncertainties, especially for maize, rice, and soybean due to lacking species-specific flux datasets.
  - Maize data limited to a small number of older varieties, increasing uncertainty for maize yield loss estimates.
  - Seasonal multiple cropping in some regions not explicitly modeled; only the primary growing period used per climate.
  - Pest/disease losses based on regional historical data (2002–2004) and may overestimate modern losses due to improved crop protection.
  - Soil nutrient YCS relies on expert judgement and HWSD data; potential cross-regional reliability issues and data scale differences.
  - Heat and aridity results depend on chosen temperature datasets and time windows; aridity comparison across periods may introduce uncertainty.

## Data structure and sources
- Data structure
  - 4 GIS shapefiles (maize, rice, soybean, wheat), each with 1° × 1° gridded cells and 8 attribute columns plus a total score.
- Key data sources and tools
  - FAO Global Agro-Ecological Zones (GAEZ) for crop production (2000)
  - EMEP MSC-W model for ozone flux
  - WorldClim and PET estimates; ECMWF IFS data for temperature
  - Oerke et al. for pest/disease loss estimates
  - HWSD (Harmonized World Soil Database) via GAEZ v3 for soil nutrient constraints
  - Trabucco & Zomer aridity index (CGIAR-CSI) and UNEP climate classes
  - GAZEA/USDA inputs for crop growing periods
  - CLRTAP dose–response framework for yield loss from ozone
- References for methods and validation
  - Mills et al. 2018a; Mills et al. 2018b (global ozone yield gap, model validation)
  - Supporting model and data sources cited throughout (EMEP MSC-W, GAW, CLRTAP, HWSD, GAEZ, etc.)

## Practical considerations for analysts
- The approach provides a harmonised, spatially explicit framework to compare multiple stressors on global crop yields at a common 1° grid, enabling cross-stressor prioritisation and scenario analysis.
- Important to consider uncertainties and data timeliness when applying the YCS in policy or research contexts, particularly for species-specific ozone responses and nutrient stress assessments.
- The datasets are designed to be discoverable and usable with metadata, aiding reproducibility and reuse in further analyses.