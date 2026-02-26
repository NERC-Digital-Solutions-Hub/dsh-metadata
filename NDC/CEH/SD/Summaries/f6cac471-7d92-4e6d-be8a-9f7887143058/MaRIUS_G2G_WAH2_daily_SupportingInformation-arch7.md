# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain: weather@home2 (climate model) driving data [MaRIUS-G2G-WAH2-daily]

- Purpose: Provides Grid-to-Grid (G2G) model estimates of daily mean river flow for 260 NRFA gauging stations across Great Britain, driven by weather@home2 climate model data.
- Time periods: Historical (1900-2006), Near-Future (2020-2049), Far-Future (2070-2099); each period has 100 ensemble members.
- Related file: Includes details of the 260 NRFA gauging stations.

- Hydrological model (Grid-to-Grid, G2G)
  - Resolution and timing: 1 km x 1 km grid, 15-minute time-step; parameterised with soil and land-cover data; accounts for urban/suburban runoff effects.
  - Output: Daily mean river flow (m3 s-1) for each NRFA station location.
  - Calibration: Largely based on distributed spatial data; national-typical parameters; no catchment-by-catchment calibration.
  - Inputs: Precipitation and potential evapotranspiration (PE) from MaRIUS WAH2 regional climate model dataset.
  - Snow module: Not used in this dataset; precipitation treated as rain.
  - Ensemble structure: 100 ensemble members per period; five NF/FF ensemble sets exist but only the median-pattern sets are used here.
  - Climate driving data: MaRIUS WAH2 uses HadRM3P nested in HadAM3P; RCP8.5 for future periods; includes bias correction for precipitation only.

- Data processing and re-projection
  - Climate data re-projected from ~0.22° rotated lat-lon grid to the 1 km G2G grid.
  - Within each climate box, spatial weights produce a non-uniform distribution of precipitation.
  - Year length: 360-day calendar (12x30-day months) as per WAH2 data.
  - Spatial matching: Each G2G flow is assigned to the 1 km grid cell that best represents the NRFA station’s location and catchment, with checks to ensure correct tributary. In some cases, derived catchment area differs from the NRFA catchment area; all G2G catchments are within 8% of NRFA catchment areas.

- Format and structure of the MaRIUS-G2G-WAH2-daily dataset
  - File format: CSV per catchment; one line header; first column is date; subsequent columns are ensemble members (1–100).
  - File naming conventions:
    - Historical Baseline: G2G_WAH2_flow_HISTBS_*.csv (1900-2006; 1900 and 1901 spin-up)
    - Baseline: G2G_WAH2_flow_BS_*.csv (1975-2004)
    - Near-Future: G2G_WAH2_flow_NF_*.csv (2020-2049; 2020-2021 spin-up)
    - Far-Future: G2G_WAH2_flow_FF_*.csv (2070-2099; 2070-2071 spin-up)
  - Catchment reference: Each file corresponds to a NRFA catchment (the NRFA ID is appended to the filename).
  - Supporting metadata: MaRIUS_NRFAStationInfo.csv provides station details (station ID, river, location, G2G coordinates, catchment area, data issues).

- How to use in GIS and analyses
  - Baseline vs future comparisons: Compare G2G flows from NF/FF to BS (not to observed time series); for full context, compare results statistically across ensembles rather than matching exact dates.
  - Impacts modelling: Use future G2G river flows to drive downstream impact models (economic, ecological, agricultural) and compare against Baseline distributions.
  - Ensemble interpretation: Treat 100 ensemble members as plausible realizations of climate; focus on differences in distributions between historical and future periods rather than single-member changes.
  - Spatial alignment caveats: The 1 km G2G cell is chosen to match NRFA location and catchment; some minor differences in catchment areas may occur (up to 8%), which can affect small catchments more noticeably.
  - Temporal caveats: First two years of HISTBS and NF/FF should be treated as spin-up and not used for analyses of steady-state conditions.

- Limitations and considerations for GIS users
  - Natural-flow focus: G2G does not incorporate abstractions and discharges; results reflect natural flows under the driving climate data.
  - Data quality and resolution gaps: Data are spread across multiple sources and resolutions; data cleaning and compatibility checks may be required when integrating with other datasets.
  - PE construction and bias corrections: PE uses adjusted stomatal resistance values for future periods; precipitation bias correction is applied only to precipitation, not PE.
  - Calendar and timing: 360-day year assumption; monthly structure reflects this calendar.

- Acknowledgements and references
  - Source: MaRIUS project (Managing the Risks, Impacts and Uncertainties of droughts and water Scarcity), NERC-funded.
  - Key references cited for model components and methodology (e.g., Bell et al., Guillod et al., Rudd et al., Kay et al., Monteith, MORECS).