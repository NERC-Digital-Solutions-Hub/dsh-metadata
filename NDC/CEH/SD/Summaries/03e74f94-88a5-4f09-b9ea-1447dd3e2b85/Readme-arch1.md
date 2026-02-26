# Simulated winter wheat and maize above-ground dry matter, soil organic matter and soil water at a site near Changwu, China, 19832015 and future climate scenarios to 2049

- Overview
  - Model-generated dataset using the SPACSYS model applied to a historic site on the Loess Plateau in China (35.52°N, 107.68°E).
  - Validation: observed wheat yields (1993–2004) and maize yields (1983–2015) used to validate the model.
  - Simulation scope: historical period 1983–2015 and future climate scenarios to 2049, producing daily predictions of above-ground dry matter, soil water, and soil organic carbon stocks.
  - Management assumptions: ploughing timing (wheat in September; maize in April) and fertiliser rate (20.7 g N/m^2 for winter wheat; 14.7 g N/m^2 for maize) using urea.

-Location and model details
  - Site: Loess Plateau, China.
  - Model: SPACSYS (integrates root architecture with carbon, nitrogen, and water cycling).
  - Simulation authors: K Gongadze and H Yang.
  - Purpose: quantify daily dynamics of crop growth, soil water, and soil organic carbon under different climate futures to inform decision-making.

- Data content and variables
  - Outputs include:
    - Above-ground dry matter (DM) by organ: leaves (leaf_DM), stems (stem_DM), grains (grain_DM); total above-ground DM (DM).
    - Yield: grain yield (dry) in g/m^2 (Yield).
    - Soil water content: proportions of water content by depth layers (SW) across multiple layers (e.g., 0–10 cm, 10–20 cm, ..., 180–220 cm).
    - Soil organic carbon stocks: topsoil and subsoil layers (SOM) at 0–40 cm and 40–100 cm.
  - Temporal resolution: daily data; for DM and yield, summaries are provided at daily or per-date granularity; for SW and SOM, daily values across depth layers.

- Data structure and file organization
  - Dataset comprises 248 CSV files.
  - Naming convention: crop name + 'sim' + weather data name + variable name.
    - Crop: 'wheat' or 'maize'.
    - Weather data name: 'historic' or a future SSP-RCP scenario.
    - SSP-RCP scenarios: SSP119, SSP126, SSP245, SSP370, SSP434, SSP585.
    - Ensemble members: r1i1p1f1, r2i1p1f1, r3i1p1f1, r4i1p1f1, r8i1p1f1.
  - Variable names include 'Yield', 'DM', 'SW', and 'SOM'.
  - Example file contents:
    - wheat sim historic DM: wheatsimhistoricDM.csv
    - maize sim SSP245 Yield: maize sim SSP245Yield.csv
  - File-type details:
    - *Yield.csv: harvest_date (dd/mm/yyyy) and yield (g/m^2).
    - *DM.csv: date (dd/mm/yyyy); leaf_DM, stem_DM, grain_DM (daily DM per organ in g/m^2).
    - *SW.csv: date; depth-specific columns such as 0_10_cm, 10_20_cm, 20_40_cm, 40_60_cm, 60_80_cm, 80_100_cm, 100_140_cm, 140_180_cm, 180_220_cm (proportion of soil water content by layer, with layer thickness indicated in headers).
    - *SOM.csv: date; 0_40_cm and 40_100_cm (daily soil organic carbon stocks in g C/m^2).

- Climate scenarios and ensemble context
  - Future climate scenarios used: six SSP-RCP combinations (SSP119, SSP126, SSP245, SSP370, SSP434, SSP585).
  - Each scenario includes five ensemble members to capture internal variability (r1i1p1f1, r2i1p1f1, r3i1p1f1, r4i1p1f1, r8i1p1f1).

- Validation, outputs, and interpretation notes
  - Validation relies on observed yields for wheat (1993–2004) and maize (1983–2015).
  - The dataset provides complete simulation results across historical and future periods, enabling analyses of climate impact on DM production, grain yield, soil moisture distribution by depth, and soil organic carbon stocks.
  - Focused on daily dynamics to support correlation analyses, model validation, and predictive assessments of management and climate interactions at a local scale.

- Reference to model origin
  - SPACSYS model described in Wu et al. 2007 (integration of a 3D root architecture component to carbon, nitrogen and water cycling). https://doi.org/10.1016/j.ecolmodel.2006.08.010

- Potential analysts’ uses
  - Identify correlations between climate scenario factors and yields/DM/SOM/SW across depths and time.
  - Develop predictive insights on how different SSP-RCP futures may influence crop performance and soil moisture regimes.
  - Compare ensemble variability to assess uncertainty in climate-driven predictions.
  - Inform local management decisions by linking daily DM and soil conditions to agronomic outcomes.