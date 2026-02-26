# Water quality modelling of the Mekong River basin: Climate change and socioeconomics drive flow and nutrient flux changes to the Mekong Delta

## Purpose and scope
- Evaluate climate, socioeconomic, and population impacts on the Mekong River basin and assess nutrient fluxes entering the Vietnamese Mekong Delta (VMD).
- Apply the integrated catchment (INCA) model to predict future flow and nutrient flux for 2018–2098 under eight combined scenarios.

## Modelling framework and data inputs
- INCA-N and INCA-P: daily-timestep models predicting channel discharge and nutrient/constituent fluxes.
  - INCA-N: nitrate-N and ammonium-N with discharge.
  - INCA-P: total phosphorus and soluble reactive phosphorus with discharge and sediment-related metrics.
- Spatial and temporal scope:
  - 24 subreaches across the Mekong River system (M01–M24).
  - Daily outputs for each subreach.
- Input data and data lineage:
  - River network topology, reach characteristics, subcatchment areas, land use.
  - Hydrological inputs: rainfall, temperature, hydrologically effective rainfall (HER), soil moisture deficit (SMD) from PERSiST.
  - Calibration/validation using observed flow and water quality data (1980–2017 baseline).
  - Future climate projections downscaled from regional climate models (RCMs) based on GCMs.
- Calibration and validation:
  - Baseline model outputs generated for nitrate and phosphorus data (1980–2017).
  - Model performance assessed with Nash-Sutcliffe efficiency (NSE) and R²; R² > 0.63 indicates reasonable fit.

## Scenarios and outputs
- Eight future scenarios created by combining:
  - Climate: RCP 4.5 and RCP 8.5.
  - Economy: Medium (MG) and High (HG) growth.
  - Population: Low (LP) and High (HP) growth.
- Outputs include:
  - INCA-N: daily channel discharge, nitrate-N, ammonium-N.
  - INCA-P: daily channel discharge, depth, suspended sediment concentration (SSC), total phosphorus (TP), soluble reactive phosphorus (SRP).

## Data formats, naming conventions, and units
- File naming conventions (examples):
  - C_GFDLXX_YYYY-YYYY_baseline_Reach_MDD.csv (baseline, nitrate or phosphorus)
  - C_GFDLXX_YYYY-YYYY_ZZWW_Reach_MDD.csv (scenario outputs)
- Climate code:
  - GFDL45 = RCP 4.5; GFDL85 = RCP 8.5
- Economic and population codes:
  - HG = High economic growth; MG = Medium economic growth
  - HP = High population growth; LP = Low population growth
- Spatial reference: 24 Mekong subreaches (M01–M24) along the delta region.

## Data quality, provenance, and documentation
- Uncertainty and sensitivity analysis:
  - Generalized Likelihood Uncertainty Estimation (GLUE) used to estimate parameters.
  - Validation period: 1985–1990.
  - Performance metrics indicate good alignment with observed discharge and water quality (R² > 0.63).
- Provenance:
  - Methodology documented in Whitehead et al. (2019) with detailed flow paths and processing details for INCA-N and INCA-P.

## Data availability, sharing, and governance considerations
- Data are prepared to support discovery and reuse, with explicit metadata and clear naming conventions.
- Potential need for data portal uploads and ongoing updates as new data or scenarios arise.
- Documentation cues (units and column descriptions) facilitate interoperability and reuse.

## Practical considerations for Data Stewards
- Manage multiple large, time-series datasets (daily outputs for 24 subreaches across several scenarios).
- Maintain clear versioning, metadata completeness (model versions, calibration period, scenario definitions, spatial extent, units).
- Ensure consistent data formats across INCA-N and INCA-P products.
- Track data lineage from observed inputs through calibration to future projections.
- Address licensing, access, and potential embargoes, and provide citation guidance (e.g., reference to Whitehead et al. 2019).