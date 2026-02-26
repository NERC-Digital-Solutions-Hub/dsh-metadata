# Historical (1950-2014) and projected (2015-2100) hydrological model (HMF-WA) estimates of monthly mean and annual maximum river flows across West Africa driven by CMIP6 projected climate data

## Purpose and context
- Provides ensemble hydrological estimates of river flows across West Africa at 0.1° × 0.1° (approx. 10 km) resolution for historical and future periods.
- Driven by bias-corrected CMIP6 climate variables to support climate-impact planning, water resources management, and policy monitoring.
- Part of AMMA-2050; designed to explore how monsoon-related hydrology may change under different climate and water-use scenarios to inform climate-compatible development.

## Data, modelling approach, and scenarios
- Hydrological Model: Hydrological Modelling Framework for West Africa (HMF-WA); physically-based, grid-based, including anthropogenic water use, wetlands, and endorheic regions.
- Domain and resolution: West Africa and Sahel, 3°–26° N and -18°–25° E, on a 0.1° × 0.1° grid.
- Temporal coverage: Historical 1950–2014; Future 2015–2100.
- Climate inputs: Bias-corrected CMIP6 daily precipitation and near-surface temperature (and daily max/min temperature where available); Potential Evaporation estimated from temperature data.
- Ensemble and scenarios: 44 CMIP6 members across three SSP-RCP pathways (SSP126, SSP245, SSP585); two water-use scenarios for future periods:
  - Population-change–driven water use (envelope of possible increases)
  - Present-day water use (WO)
- Hydrological outputs: Monthly mean river flows and annual maximum daily river flows (both in m3 s-1).
- Data format: NetCDF4; three calendar options (365/366, or 360-day year) with a single, consistent gridded dataset.

## Data structure, access, and file naming
- Outputs include:
  - Monthly Mean Flows (MMFLOW) and Annual Maximum Flows (AMFLOW)
  - Bias-corrected BC versions (driven by CMIP6 data) and WO versions (without population-driven water-use changes)
- File naming examples:
  - HMF-WA_MMFLOW_BC_<model>_HIST_195001-201412.nc
  - HMF-WA_MMFLOW_BC_<model>_<SSP-RCP>_201501-210012.nc
  - HMF-WA_AMFLOW_BC_<model>_HIST_1950-2014.nc
  - HMF-WA_AMFLOW_BC_WO_<model>_<SSP-RCP>__2015-2100.nc
- Spatial and temporal metadata are included; data suitable for regional analysis but not for small catchments.

## Model performance and limitations
- Validation: Compared with observed daily river discharge from 20 GRDC stations (1981–2010) using CHIRPS precipitation and GLEAM PE for driving data.
- Performance: Median NSE = 0.62 and NSE log = 0.82, indicating good capture of high flows and reasonable low-flow representation; smaller, upland, or flashy catchments showed weaker performance.
- Not calibrated to individual catchments; designed for spatially consistent gridded estimates across ungauged locations.
- Baseline simulations rely on climate model realizations rather than observed climate data, so outputs are best used for relative comparisons and scenario analysis rather than exact reproduction of past flows.
- Key assumptions:
  - Future per-capita water use remains at present-day levels per country (population-driven changes only via population growth).
  - River networks, lakes, reservoirs, and wetlands are assumed not to change significantly from present day to 2100.

## Guidance for monitoring and decision-making
- Use the full CMIP6 ensemble; no single model is considered preferred or most reliable.
- Outputs are not directly comparable to observed historical flows; suitability is for assessing spatial patterns, relative changes, and extremes under different climate and water-use scenarios.
- Spatial resolution limits: cannot resolve rivers below ~5000 km²; suitable for regional planning rather than fine-scale catchment management.
- Extreme-flow analysis: AMFLOW enables flood-frequency assessment (e.g., Gringorten plotting positions and L-moment fits) under stationarity assumptions.
- Climate- and scenario-aware planning: compare across SSP126, SSP245, and SSP585 to bound potential hydrological changes and to inform adaptation strategies.

## Data sources and governance considerations
- Driving data and inputs:
  - Climate: CMIP6 bias-corrected outputs; compared to CMIP5-based analyses for context.
  - Observations: GRDC discharge records for validation.
  - Water use: AQUASTAT (FAO) current use data; population projections (UN).
- Metadata and openness: data come with metadata in NetCDF headers; transparency around bias correction and scenario assumptions is provided, with guidance on uncertainty and interpretation.

## Practical takeaways for Monitoring Frameworks
- The HMF-WA dataset offers a spatially consistent, ensemble-based view of how West African river flows could respond to climate change and population-driven water use.
- Useful for evaluating policy questions related to floods, drought risk, and water resource planning under multiple climate futures.
- Requires careful interpretation of ensemble spread, non-calibration at catchment level, and the coarse resolution when applying to local monitoring or enforcement decisions.