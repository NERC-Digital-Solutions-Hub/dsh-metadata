# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain: weather@home2 (climate model) driving data [MaRIUS-G2G-WAH2-daily]

- Overview
  - Provides Grid-to-Grid (G2G) model estimates of daily mean river flow (m3 s-1) for 260 NRFA gauging stations across Great Britain.
  - Outputs correspond to daily flows (midnight–midnight) from 1km x 1km G2G grid cells, aligned with the GB national grid.
  - Based on MaRIUS (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity) with weather@home2 (WAH2) climate driving data.

- Model and driving data
  - Hydrological model: Grid-to-Grid (G2G), parameterised with spatial datasets (soil, land cover, topography) and run at 1km grid with 15-minute time steps.
  - Driving meteorology: MaRIUS weather@home2 (WAH2) regional climate model data providing multiple climate ensembles (historical and future).
  - Periods and ensembles:
    - HISTBS: 1900–2006 (Historical Baseline) – 100 ensemble members
    - BS: 1975–2004 (Baseline) – 100 ensemble members
    - NF: 2020–2049 (Near-Future) – 100 ensemble members
    - FF: 2070–2099 (Far-Future) – 100 ensemble members
  - Data processing details:
    - Precipitation bias-corrected with monthly multiplicative factors (historical and future).
    - Potential evaporation (PE) derived via Penman-Monteith; for historical, uses monthly stomatal resistance from MORECS; for future, uses adjusted r_s values.
    - Snow module not used; precipitation treated as rain.
    - WAH2 data re-projected from ~25 km grid to 1 km, with within-grid distribution weights.
    - 360-day year calendar used (12 x 30 days).
  - Spin-up considerations:
    - Initial two years of HISTBS, NF, and FF should be ignored or treated as spin-up in analyses.

- Data coverage and outputs
  - 260 NRFA gauging stations across Britain; each station associated with a corresponding 1km grid cell.
  - Outputs are daily natural flows (no abstractions/discharges) for each ensemble member and period.
  - File structure:
    - CSV per catchment with a header line; columns: Date, then 1–100 for ensemble members.
    - File naming:
      - G2G_WAH2_flow_HISTBS_*.csv (1900–2006)
      - G2G_WAH2_flow_BS_*.csv (1975–2004)
      - G2G_WAH2_flow_NF_*.csv (2020–2049)
      - G2G_WAH2_flow_FF_*.csv (2070–2099)
    - Related file: MaRIUS_NRFAStationInfo.csv including station IDs, river names, locations, G2G coordinates, catchment areas, and data issues.
  - Data limitations:
    - G2G aims to represent a 1km catchment but may not perfectly align with observed NRFA catchment areas (within 8% difference in catchment area).
    - G2G captures natural flows; does not account for abstractions or discharges.

- Format and interpretation guidance
  - Data are meant for statistical comparisons over multi-decadal periods rather than direct time-series matching to observations.
  - When comparing to observations or Oudin-driven runs, focus on statistics (e.g., distributions, low-flow frequencies) rather than exact time series.
  - For future assessments (NF/FF), compare to the Baseline (BS) rather than to observed data.
  - Ensemble members are plausible realizations for each period; do not directly link ensemble numbers across periods (e.g., BS1 should not be compared to NF1).

- Use recommendations for data governance
  - Clear provenance: dataset derived from MaRIUS project and WAH2 climate model with documented bias corrections and PE treatment.
  - Metadata and discoverability: NRFA station mapping and description included; CSV format with consistent naming and headers facilitates data discovery and reuse.
  - Data quality considerations: notes on calibration approach (grid-based over parameter calibration), bias correction for precipitation, and potential impacts of catchment discretisation on small catchments.
  - Reproducibility: detailed methodological notes enable replication of analyses, including the need to treat the first two years of certain ensembles as spin-up.

- Provenance and acknowledgments
  - Part of the MaRIUS project (UK NERC funding) under the UK Drought and Water Scarcity programme.
  - Acknowledges contributions and supporting references related to the G2G model, WAH2 climate data, and hydrological analyses.

- References (selected)
  - Foundational papers on G2G, rainfall/evaporation computations, and drought/hydrology analyses across Britain.
  - Key methodological sources for bias correction, PE formulation, and hydrological drought assessment.