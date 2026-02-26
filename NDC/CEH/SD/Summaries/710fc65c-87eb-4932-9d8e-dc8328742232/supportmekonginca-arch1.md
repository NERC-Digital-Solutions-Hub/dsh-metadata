# Water quality modelling of the Mekong River basin: Climate change and socioeconomics drive flow and nutrient flux changes to the Mekong Delta

- Objective
  - Evaluate how climate, socioeconomic development, and population growth impact the Mekong River basin and the nutrient fluxes entering the Vietnamese Mekong Delta (VMD), focusing on nitrate and phosphorus as key upstream nutrients.

- Modeling framework
  - Use the integrated catchment (INCA) model, a dynamic daily simulator of water quantity and quality in rivers and catchments.
  - Two INCA submodels: INCA-N (discharge, nitrate-N, ammonium-N) and INCA-P (discharge, depth, suspended sediment, total P, soluble reactive P).
  - Two independent INCA modelling pathways (N and P) run in parallel for robustness.

- Spatial and temporal setup
  - 24 subcatchments (reaches M01–M24) along the Mekong River basin.
  - Daily timestep projections spanning 2018–2098.
  - Baseline calibration/validation using observed data from 1980–2017 (separate baselines for nitrate and phosphorus).

- Inputs and data generation
  - River network topology, reach characteristics, subcatchment areas, land use.
  - Hydrological inputs: rainfall, temperature, hydrologically effective rainfall (HER), soil moisture deficit (SMD).
  - HER and SMD derived by the PERSiST hydrological model, designed for coupling with INCA.
  - Climate projections: downscaled regional climate model outputs from global climate models to drive future scenarios.
  - Economic and population scenarios combined with climate to create eight future scenarios (two climate pathways × two economic growth levels × two population growth levels).

- Future scenarios
  - Climate: RCP 4.5 and RCP 8.5.
  - Economic growth: Medium (MG) and High (HG).
  - Population: Low (LP) and High (HP).
  - Combined into eight distinct scenarios for both INCA-N and INCA-P.

- Outputs and units
  - Nitrate data: Date, Flow (cms), Nitrate (mg/L as nitrate-N), Ammonium (mg/L as ammonium-N).
  - Phosphorus data: Date, Flow (cms), Depth (m), Suspended Sediment Concentration (SSC, gm/L), Total Phosphorus (TP, mg/L), Soluble Reactive Phosphorus (SRP, mg/L).

- Calibration, validation, and quality control
  - Baseline models calibrated and validated against historical discharge and water quality data (1980–2017; 1985–1990 validation window mentioned).
  - Uncertainty analysis using GLUE to identify key controlling parameters.
  - Model performance assessed with Nash–Sutcliffe Efficiency (NSE) and R²; both INCA-N and INCA-P baseline calibrations achieved R² values greater than 0.63, indicating reasonable skill in reproducing downstream flow and nutrient fluxes.

- Data organization and accessibility
  - File naming conventions for outputs:
    - C_GFDLXX_YYYY-YYYY_baseline_Reach_MDD.csv (baseline outputs)
    - C_GFDLXX_YYYY-YYYY_ZZWW_Reach_MDD.csv (future scenario outputs)
  - CSV files encode constituent (C = nitrate; P = phosphorus) and climate scenario (GFDL45/85) with year spans and reach identifications (M01–M24).

- Implications
  - The integrated INCA modelling framework enables projection of how climate change, economic development, and population growth could alter river discharge and nutrient fluxes to the Mekong Delta.
  - Outputs support assessment of potential impacts on agriculture and aquatic ecosystems, informing management and policy decisions to mitigate nutrient transport and protect VMD water quality.

- Reference
  - Whitehead, P.G. et al. 2019. Water quality modelling of the Mekong River basin: Climate change and socioeconomics drive flow and nutrient flux changes to the Mekong Delta. Sci. Total Environ. 673, 218-229.