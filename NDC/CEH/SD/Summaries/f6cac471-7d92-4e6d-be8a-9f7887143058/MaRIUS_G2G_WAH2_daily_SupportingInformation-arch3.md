# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain: weather@home2 (climate model) driving data [MaRIUS-G2G-WAH2-daily]

- Purpose and scope
  - Provides Grid-to-Grid (G2G) model estimates of daily mean river flow for 260 NRFA gauging stations across Great Britain.
  - Driven by weather@home2 (WAH2) climate model data as part of the MaRIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity).
  - Supports drought and water scarcity risk assessment under historical and future climate scenarios.

- What the dataset contains
  - Daily river flow (m3 s-1) for 260 NRFA locations on a 1 km x 1 km grid, for historical (1900–2006), near-future (2020–2049), and far-future (2070–2099) periods.
  - 100 ensemble members for each period, capturing climate uncertainty.
  - A companion file with details for the 260 NRFA gauging stations.

- Model and data inputs
  - Hydrological model: Grid-to-Grid (G2G), 1 km grid, 15-minute time-step; accounts for land cover/soil effects on runoff but excludes abstractions and discharges.
  - Forcing data: precipitation and potential evaporation (PE) from MaRIUS WAH2 regional climate model.
  - Climate model specifics: HadRM3P nested in HadAM3P; five NF/FF ensemble sets exist, with the study using the median-pattern NF/FF sets based on RCP8.5.
  - Precipitation bias-correction: applied (monthly multiplicative factors); PE derived via Penman-Monteith with stomatal resistance (rs) values; two PE variants exist, with here the adjusted-rs version used for future periods.
  - Data processing: re-projection from ~25 km to 1 km grid; 360-day year and 30-day months used.

- Temporal and ensemble structure
  - Periods and samples:
    - HISTBS: Historical Baseline, 1900–2006
    - BS: Baseline, 1975–2004
    - NF: Near-Future, 2020–2049
    - FF: Far-Future, 2070–2099
  - Each period has 100 ensemble members.
  - Spin-up caveats:
    - The first two years of HISTBS, NF, and FF should be ignored for analyses or used only for spin-up.
  - Ensemble guidance:
    - Do not directly compare ensemble members with the same index across periods (e.g., HISTBS1 vs NF1).
    - Analyses of future changes should compare distributions across periods, not individual ensemble-member time series.

- Spatial coverage and outputs
  - 260 NRFA gauging stations mapped to corresponding 1 km grid cells; catchment areas may slightly differ from NRFA delineations (within ~8%).
  - Outputs per catchment: CSV file with a header row; first column = date, followed by 1–100 ensemble member columns.
  - File naming conventions:
    - HISTBS: G2G_WAH2_flow_HISTBS_*.csv (1900–2006;  spin-up years excluded as noted)
    - BS: G2G_WAH2_flow_BS_*.csv (1975–2004)
    - NF: G2G_WAH2_flow_NF_*.csv (2020–2049; spin-up years)
    - FF: G2G_WAH2_flow_FF_*.csv (2070–2099; spin-up years)
  - Supporting station information: MaRIUS_NRFAStationInfo.csv detailing station IDs, river names, locations, G2G coordinates, catchment area, and data issues.

- How to use and interpret
  - Use for statistical comparisons rather than direct time-series matching to observations or to other G2G runs.
  - Baseline (BS) and Historical (HISTBS) can be contrasted with NF/FF to assess potential changes in river flows under climate change.
  - When evaluating impacts (economic, ecological, agricultural), compare impact-model results driven by NF/FF against those based on BS, not against observed time series.
  - Treat each ensemble as a plausible realisation of its period’s climate; focus on differences in distributions between periods rather than single-member streams.
  - Be mindful of potential biases from the driving climate data and the discretisation to a 1 km grid, especially for small catchments.

- Data quality, limitations, and caveats
  - G2G does not simulate abstractions or discharges; real-world flows may be affected by such human influences not captured here.
  - PE bias correction exists for historical baselines; future PE uses adjusted stomatal resistance, which moderates projected low-flow declines.
  - Precipitation is bias-corrected; PE is not bias-corrected in future periods.
  - The 360-day year and 30-day months are non-standard; users should account for this in time-based analyses.
  - Spatial mapping to NRFA stations can produce slight mismatches in catchment area; overall, discrepancies are within ~8%.

- Acknowledgements and references
  - Funded by the UK Natural Environment Research Council (NE/L010208/1) as part of the UK Drought and Water Scarcity programme.
  - References include key methodological papers on the G2G model, rainfall/evaporation calculations, and drought analyses relevant to this dataset.