# Description

- Objective: Assess how climate, socioeconomic conditions, and population growth affect the Mekong River basin and the nutrient fluxes entering the Vietnamese Mekong Delta (VMD), using the INCA model to predict future flow and nutrients from 2018 to 2098 under eight scenario combinations.

- Modeling framework: Integrated Catchment (INCA) model is a dynamic daily simulator of water quantity and quality in rivers and catchments.
  - INCA-N: predicts daily channel discharge, nitrate-N, and ammonium-N.
  - INCA-P: predicts daily channel discharge, depth, suspended sediment concentration, total phosphorus, and soluble reactive phosphorus.
  - Outputs are generated for 24 subcatchments via two independent INCA modelling pathways.

- Data inputs and generation:
  - Requires river network topology, reach characteristics, subcatchment areas, land use, rainfall, temperature, hydrologically effective rainfall (HER), and soil moisture deficit (SMD).
  - HER and SMD produced by the PERSiST hydrological model, designed to feed INCA models.
  - Baseline calibrations use observed discharge and water quality data for 1980–2017; validations conducted for 1985–1990.

- Calibration and validation:
  - Generalized Likelihood Uncertainty Estimation (GLUE) used for parameter uncertainty analysis.
  - Model performance assessed with Nash-Sutcliffe Efficiency (NSE) and R²; both INCA-N and INCA-P achieved R² > 0.63 in calibration.

- Future climate, socioeconomics, and population scenarios:
  - Climate inputs from a regional climate model downscaled from GCMs.
  - Binary scenarios: climate (RCP 4.5 or 8.5), socioeconomic growth (medium or high), population growth (low or high).
  - Combining these yields eight future scenarios for discharge and nutrient flux across the Mekong basin.

- Outputs and interpretation:
  - Channel water quantity and nutrient flux predictions for the Mekong River system, focusing on nitrate-N, ammonium-N, depth, SSC, TP, and SRP across 24 subreaches (M01–M24).
  - Outputs support evaluation of nutrient delivery to the VMD under changing climate, economy, and population conditions.

- Data products and file formats:
  - Baseline and future scenario CSV files with standardized naming:
    - C_GFDLXX_YYYY-YYYY_baseline_Reach_MDD.csv (constituent N or P)
    - C_GFDLXX_YYYY-YYYY_ZZWW_Reach_MDD.csv (future scenario)
  - Constituents coded as:
    - C: N for nitrate-N (INCA-N) or P for total phosphorus (INCA-P)
  - XX denotes climate scenario (GFDL45 = RCP 4.5; GFDL85 = RCP 8.5)
  - YYYY-YYYY denotes simulation years
  - ZZ, WW denote economic (HG or MG) and population (HP or LP) growth scenarios
  - Reach_MDD enumerates M01–M24 subreaches (e.g., M01 Source, M05 Jinghong, M18 Pakse, M24 Delta)

- Quality assurance and reference:
  - Model calibration and validation described in Whitehead et al. (2019), including GLUE-based uncertainty assessment and performance metrics.
  - Provides a reproducible dataset framework for monitoring environmental flows and nutrient fluxes to the Mekong Delta.

- Context and relevance:
  - Highlights how upstream water and sediment nutrients (nitrate and phosphorus) drive Delta agriculture, enabling standardized monitoring outputs for policy evaluation and environmental health assessments over time.