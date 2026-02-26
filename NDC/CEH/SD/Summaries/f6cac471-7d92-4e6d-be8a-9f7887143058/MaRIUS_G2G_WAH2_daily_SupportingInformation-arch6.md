# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain: weather@home2 (climate model) driving data [MaRIUS-G2G-WAH2-daily]

## Dataset overview
- Provides Grid-to-Grid (G2G) model estimates of daily mean river flow (m3 s-1) for 260 NRFA gauging stations across Great Britain.
- Time periods and ensembles:
  - Historical Baseline (HISTBS): 1900-2006
  - Baseline (BS): 1975-2004
  - Near-Future (NF): 2020-2049
  - Far-Future (FF): 2070-2099
  - Each period has 100 ensemble members (flow realizations)
- Meteorological driving data:
  - MaRIUS weather@home2 (WAH2) regional climate model (RCM) dataset
  - Multiple ensembles for historical and future climates, using RCP8.5
- Model and inputs:
  - Hydrological model: Grid-to-Grid (G2G) at 1 km x 1 km, 15-minute time-step
  - Inputs: precipitation and potential evaporation (PE) from WAH2
  - Precipitation bias-corrected; PE derived via Penman-Monteith; stomatal resistance adjustments used for future PE
- Outputs and format:
  - Daily mean natural flows (m3 s-1) for each NRFA-supported 1 km grid cell
  - CSV format, one file per catchment; 30-day months due to 360-day calendar
  - File naming: G2G_WAH2_flow_HISTBS_*.csv, G2G_WAH2_flow_BS_*.csv, G2G_WAH2_flow_NF_*.csv, G2G_WAH2_flow_FF_*.csv
  - Each file has a header; first column date, followed by 100 ensemble columns (1-100)
- Related data:
  - MaRIUS_NRFAStationInfo.csv providing NRFA station details and grid mappings

## Model details and inputs
- G2G model characteristics:
  - National-scale, 1 km resolution, 15-minute time-step
  - Uses land-cover and soil data; accounts for urban runoff effects
  - Calibrated with spatial datasets rather than catchment-specific parameter fitting
  - Snow module not used; precipitation treated as rain
  - Suitable for low-flow and drought analyses; does not include abstractions or discharges
- Data inputs and processing:
  - WAH2 precipitation and PE re-projected from ~25 km to 1 km grid
  - Precipitation bias correction applied; PE not bias-corrected
  - Spatial weighting within each climate box to distribute precipitation
  - 360-day calendar used (12×30-day months)
- Ensemble and period specifics:
  - Each period has 100 G2G simulations
  - BS is a 30-year subset of HISTBS; first two years of HISTBS, NF, FF are spin-up and should be ignored for analyses
  - Same ensemble numbers across periods are not directly comparable (e.g., BS1 ≠ NF1)

## Data usage guidance
- Comparisons and analyses:
  - For baseline (BS) and historical (HISTBS): compare G2G outputs to observation-based G2G runs or NRFA data statistically over multi-decadal scales, not as exact time-series matches
  - For future (NF/FF): compare NF/FF distributions to BS distributions, not to observed time series
  - Use ensemble spreads to assess uncertainty; avoid direct one-to-one member-to-member comparisons across periods
- Station-to-grid mapping:
  - Each NRFA gauging station is matched to the G2G cell closest in location and catchment area
  - Some small catchments may have discretisation errors; all G2G catchment areas are within 8% of NRFA catchment areas

## Format and access details
- File structure:
  - Historical Baseline: G2G_WAH2_flow_HISTBS_*.csv
  - Baseline: G2G_WAH2_flow_BS_*.csv
  - Near-Future: G2G_WAH2_flow_NF_*.csv
  - Far-Future: G2G_WAH2_flow_FF_*.csv
- CSV specifics:
  - One line header
  - Columns: Date, Ensemble 1, Ensemble 2, ..., Ensemble 100
  - NRFA catchment identifiers appear in the file naming as per http://nrfa.ceh.ac.uk/
- Related documentation:
  - MaRIUS_NRFAStationInfo.csv for NRFA station details and G2G mapping
- Acknowledgement and references:
  - Funded by UK NERC (NE/L010208/1) under the MaRIUS project
  - Key methodological references listed (Bell et al.; Guillod et al.; Hough & Jones; Monteith; Kay et al.; Rudd et al.)

## Limitations and caveats
- Catchment discretisation:
  - 1 km G2G cell catchments may differ from NRFA catchments; discretisation can introduce errors, particularly for small basins
  - All catchment area differences are within about 8%
- Calendar and timing:
  - 360-day year convention (12×30-day months) affects date alignment and interpretation
- Interpretive cautions:
  - Model outputs reflect natural flows (no abstractions/discharges) and are best used for statistical trend analyses and scenario comparisons rather than exact observed-time predictions

## Sources and references
- MaRIUS project context and data drive: Bell VA, Kay AL, Jones RG, Davies HN; RCM-based meteorology and G2G integration papers
- Methodological foundations and validation studies (e.g., bias correction, PE calculations, grid-based hydrological modeling) cited throughout the dataset description