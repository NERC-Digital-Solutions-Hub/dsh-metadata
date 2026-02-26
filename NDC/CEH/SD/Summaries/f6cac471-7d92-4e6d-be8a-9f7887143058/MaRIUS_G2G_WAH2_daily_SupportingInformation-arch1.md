# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain: weather@home2 (climate model) driving data [MaRIUS-G2G-WAH2-daily]

- Purpose of dataset
  - Provides Grid-to-Grid (G2G) model estimates of daily mean river flow (m3 s-1) for 260 NRFA gauging stations across Great Britain.
  - Covers historical (1900–2006), near-future (2020–2049), and far-future (2070–2099) periods.

- Data products and variables
  - Primary variable: daily mean river flow (midnight–midnight) for each NRFA site.
  - Output format: one CSV per catchment with a date column followed by 100 ensemble member columns (1–100).

- Hydrological model and driving data
  - Hydrological model: Grid-to-Grid (G2G) on a 1 km x 1 km grid with a 15-minute time-step.
  - Model inputs: precipitation and potential evaporation (PE) from MaRIUS weather@home2 (WAH2) regional climate model (RCM).
  - Snow module not used; precipitation treated as rain.

- Driving data characteristics (WAH2)
  - Climate model: HadRM3P nested in HadAM3P; runs many ensembles via volunteer computing.
  - Scenarios: future periods use RCP8.5 with five NF/FF ensemble sets; this dataset uses the median pattern/magnitude sets.
  - Bias correction: applied to precipitation (monthly multiplicative factors); PE derived via Penman-Monteith.
  - PE specifics: historical period uses stomatal resistance values from MORECS; future periods use adjusted r_s values to reflect CO2 effects (accounts for stomatal closure; moderates projected low-flow decreases). PE is not bias-corrected.

- Time slices and ensembles
  - Historical Baseline (HISTBS): 1900–2006
  - Baseline (BS): 1975–2004 (subset of HISTBS; first two years in HISTBS, NF, FF are spin-up and should be ignored in analyses)
  - Near-Future (NF): 2020–2049
  - Far-Future (FF): 2070–2099
  - Each period has 100 ensemble members (1–100); same-number ensembles across periods are not directly related.

- Spatial setup and site mapping
  - 260 NRFA gauging sites are mapped to corresponding 1 km x 1 km G2G grid cells.
  - Catchment area in the G2G cell may differ slightly from the NRFA catchment; typically within 8%.
  - Locations are checked to ensure the correct river tributary is represented.

- Data format and accessibility
  - Files named as G2G_WAH2_flow_<period>_*.csv (e.g., HISTBS, BS, NF, FF).
  - Each CSV includes a header; first column is the date, followed by 100 ensemble columns.
  - Related file MaRIUS_NRFAStationInfo.csv provides NRFA station details (ID, river, location, G2G coordinates, catchment area, data issues).

- How to use and interpretation guidance
  - Comparisons:
    - Use statistical comparisons between periods (e.g., baseline vs future) rather than direct time-series matching to observations.
    - When comparing with observations or observation-driven G2G runs, interpret biases in the driving data and model structure; assess effects on long-term statistics rather than exact series.
  - Future projections:
    - Compare NF/FF results to BS, not to observed time series.
    - Assess changes in distributions rather than individual ensemble members; ensemble member 1 is not related to NF1, NF2, etc.
  - Ensemble interpretation:
    - Each ensemble member represents a plausible realisation of the climate for the given period.
    - Analyses should focus on differences between historical and future distributions.
  - Model limitations to consider:
    - G2G emphasizes natural flow; it does not include abstractions and discharges in its default configuration.
    - Calibration is largely dataset-driven rather than catchment-specific parameter fitting.
    - The 1 km routing may introduce small catchment-area differences for some small basins.
    - Meteorological inputs are re-projected from a coarser grid and pre-distributions are spatially weighted within RCM boxes.

- Acknowledgments and references
  - Funded by the UK Natural Environment Research Council (MaRIUS project) as part of the UK Drought and Water Scarcity programme.
  - References include key methodological and validation studies on G2G, MaRIUS WAH2 data, and associated hydrological analyses.