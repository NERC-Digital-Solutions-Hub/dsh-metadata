# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain: weather@home2 (climate model) driving data [MaRIUS-G2G-WAH2-daily]

- Background and aim
  - MaRIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity) funded by NERC (2014-2017) to develop a risk-based approach to drought and water scarcity.
  - Provides Grid-to-Grid (G2G) model estimates of daily mean river flow for 260 NRFA gauging stations across Great Britain.
  - Data enable assessment of environmental health and drought risk over historical and future periods, using standardized formats suitable for monitoring and policy evaluation.

- What is included
  - River flow (m3 s-1) as daily mean from G2G at 1 km x 1 km grid cells corresponding to NRFA stations.
  - Time periods:
    - Historical Baseline (HISTBS): 1900-2006
    - Baseline (BS): 1975-2004
    - Near-Future (NF): 2020-2049
    - Far-Future (FF): 2070-2099
  - 100-member ensembles for each period (100 G2G simulations per period).

- Hydrological model and driving data
  - Grid-to-Grid (G2G) hydrological model at 1 km grid, 15-minute time-step; uses soils, land cover, and other spatial datasets.
  - Forcing data: MaRIUS weather@home2 (WAH2) regional climate model (RCM) dataset, providing multiple climate ensembles (historical and future) under RCP8.5.
  - Snow module not used; precipitation treated as rain.
  - PE (potential evaporation) derived via Penman-Monteith; for historical periods uses stomatal resistance from MORECS; future periods use adjusted values to reflect CO2 effects on stomata.
  - Precipitation bias-corrected for historical baselines; PE not bias-corrected.

- Data processing and re-gridding
  - WAH2 precipitation and PE re-projected from ~25 km grid to 1 km G2G grid.
  - Within each RCM box, precipitation distributed using spatial weights based on average annual rainfall patterns.
  - Calendar uses 360-day year (12 months of 30 days) to align with model data; 30-day months.

- Output data format and naming
  - CSV files, one per catchment, with a single header line.
  - Columns: Date, then 100 ensemble members (1–100).
  - File naming:
    - HISTBS: G2G_WAH2_flow_HISTBS_*.csv (1900-2006; 1900 and 1901 spin-up)
    - BS: G2G_WAH2_flow_BS_*.csv (1975-2004)
    - NF: G2G_WAH2_flow_NF_*.csv (2020-2049; 2020-2021 spin-up)
    - FF: G2G_WAH2_flow_FF_*.csv (2070-2099; 2070-2071 spin-up)
  - Related station info file: MaRIUS_NRFAStationInfo.csv with station metadata (ID, river, location, G2G coordinates, catchment area, data issues).

- How to use for monitoring and analysis
  - Baseline comparisons (HISTBS/BS) should be against long-term statistics, not direct time-series matching to observations.
  - Future slices (NF/FF) should be compared to Baseline, not to observed real-time data.
  - Impacts analyses should compare scenarios to Baseline rather than to observed real-world outcomes.
  - Individual ensemble members are plausible realizations; focus on differences in distributions between historical and future periods, not direct one-to-one ensemble member comparisons.
  - The 1 km G2G grid cell is chosen to best represent each NRFA site; catchment areas are within 8% of NRFA catchments, but small catchments may show discretisation-driven errors.

- Model performance and caveats
  - G2G does not explicitly model abstractions or discharges; performs well for low flows and drought identification.
  - Calibration is not done at the catchment level; preference for physically based, high-resolution inputs over parameter calibration.
  - For future periods, using adjusted stomatal resistance in PE moderates projected low-flow declines.

- Data quality, provenance and accessibility
  - Dataset produced under the MaRIUS project with acknowledgement of contributors.
  - Data are intended to support standardized environmental monitoring and policy evaluation over time.
  - Users should consider biases in WAH2 driving data and model structure when interpreting results.
  
- References and related work
  - Key methodological and validation sources listed, including development of high-resolution grid-based river flow modeling, use of soil data, drought analyses, and the WAH2 climate dataset construction.

- Acknowledgements
  - Thanks to contributors for advice and data availability; funded under the UK Drought and Water Scarcity programme.