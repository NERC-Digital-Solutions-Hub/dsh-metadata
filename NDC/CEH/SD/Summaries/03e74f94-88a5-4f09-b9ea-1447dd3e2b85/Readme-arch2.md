# Simulated winter wheat and maize above-ground dry matter, soil organic matter and soil water at a site near Changwu, China, 19832015 and future climate scenarios to 2049

## Overview
- Model-generated dataset using the SPACSYS model applied to a historic site on the Loess Plateau, China (35.52°N, 107.68°E) near Changwu.
- Validation with observed crop yields: winter wheat (1993–2004) and maize (1983–2015).
- Simulates daily above-ground dry matter (leaves, stems, grains), daily soil water content across layers, and soil organic carbon stocks in topsoil and subsoil, under climate scenarios up to 2049.
- Management practices in simulations include crop-specific ploughing timing and nitrogen fertilizer application.

## Data and methods
- SPACSYS model used to integrate carbon, nitrogen, and water cycling, with a 3D root component.
- Climate scenarios: six SSP-RCP scenarios for near- to mid-term (SSP119, SSP126, SSP245, SSP370, SSP434, SSP585) each with five ensemble members (r1i1p1f1, r2i1p1f1, r3i1p1f1, r4i1p1f1, r8i1p1f1).
- Outputs include daily measurements of above-ground dry matter by organ, soil water content by depth, and soil organic carbon stocks.

## Outputs and file structure
- 248 CSV files in total.
- File naming convention: crop name + 'sim' + weather data name + variable name.
  - Crop: 'wheat' or 'maize'
  - Weather data: 'historic' or a named future scenario
  - Variable: 'Yield' or 'DM' (daily above-ground dry matter) or 'SW' (soil water content) or 'SOM' (soil organic carbon stocks)
- Examples:
  - wheatsimhistoricDM.csv: daily leaf_DM, stem_DM, grain_DM, etc.
- Yield files: include harvest_date and yield (dry grain yield in g/m^2).
- DM files: date and daily DM for leaf, stem, and grain (g/m^2).
- SW files: date and soil water proportion for layers (0–10 cm, 10–20 cm, 20–40 cm, 40–60 cm, 60–80 cm, 80–100 cm, 100–140 cm, 140–180 cm, 180–220 cm).
- SOM files: date and soil organic carbon stocks for 0–40 cm and 40–100 cm.

## Management and inputs
- Ploughing performed in September before the wheat season; in April for maize in each year.
- Nitrogen fertiliser rate: winter wheat 20.7 g N/m^2; maize 14.7 g N/m^2; fertiliser assumed as urea.
- Simulation period spans 1983–2049, with 2015–2049 covered for future scenarios.
- Simulation work conducted by K Gongadze and H Yang.

## Validation and reference
- Model validation used observed yields for wheat (1993–2004) and maize (1983–2015).
- SPACSYS model described in Wu et al. 2007 (Ecological Modelling) for integration of root architecture with carbon, nitrogen, and water cycling.

## Potential uses for environmental monitoring
- Enables consistent temporal assessment of environmental health and policy performance related to crop production, soil carbon, and soil moisture under climate change.
- Can be combined with other environmental datasets to increase value and support broader analyses beyond single-use outputs.
- Provides underlying process-level data to support transparency and scrutiny of environmental monitoring efforts.

## Access and reuse notes
- The dataset is a comprehensive, model-generated collection suitable for ongoing monitoring and scenario analysis.
- Data quality assurance includes validation against historical yields; outputs are organized in a uniform file structure for reuse and integration into monitoring portals.