# Supporting information for Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

## Data Accessibility and Citation
- Data are available under the Open Government Licence.
- Dataset citation required: Kay et al. (2021) Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 Regional (12km) data (1980 to 2080). NERC EDS Environmental Information Data Centre. DOI: 10.5285/7079d6e8-6184-4f80-89b4-4db924ec8b05.

## Dataset Summary
- UK-SCAPE program outputs: Grid-to-Grid (G2G) hydrological model estimates of river flow for Northern Ireland.
- Variables provided on a 1km x 1km grid:
  - Monthly mean river flow (m3 s-1)
  - Annual maxima of daily mean river flow (m3 s-1)
  - Annual minima of 7-day mean river flow (m3 s-1)
- Time period: December 1980 to November 2080 (water years Oct-Sep for maxima, Dec-Nov for minima).
- Driven by UKCP18 Regional (12km) projections for NI; includes a 12-member perturbed parameter ensemble (PPE) of the Met Office Hadley Centre Regional Climate Model (RCM).
- Emissions scenario: RCP8.5.
- Calendar: 360-day year in model data.
- A complementary dataset exists for NI flows driven by observation-based input data.

## Model and Data Pipeline
- Hydrological model: Grid-to-Grid (G2G), national-scale, 1km grid, 15-minute time-step; configured for NI and parts of ROI draining to NI rivers.
- Calibration: Uses nationally applicable parameter values; no catchment-specific calibration; urban/suburban land-cover effects included via model structure.
- Performance: Generally good across NI; strong in natural-flow regimes; reduced performance downstream of Lough Neagh due to flood regulation; broader GB performance well in natural regimes but less so with complex subsurface hydrology or artificial discharges.
- Input time-series: Daily precipitation, daily min/max temperature, daily potential evapotranspiration (PE) derived from meteorological dataset; PE calculated with Penman-Monteith scheme.
- Bias correction and downscaling:
  - Precipitation bias-corrected monthly multiplicative factors.
  - PE downscaled to 1km grid (same value across time-steps with spatial distribution preserved).
  - Precipitation downscaled from 12km to 1km using spatial weighting; daily values divided evenly across model time-steps.
  - Temperature downscaled to 1km using elevation-based lapse rates; temporal downscaling with a sine curve.
- Spatial scope: NI domain on GB National Grid; includes some ROI sub-catchments draining to NI rivers.

## Data Content and Structure
- Gridded outputs:
  - Monthly mean river flow (m3 s-1) for each non-sea, non-tidal 1km cell with catchment area ≥ 50 km2.
  - Annual maxima of daily mean river flow (m3 s-1) with dates of occurrence.
  - Annual minima of 7-day mean river flow (m3 s-1) with dates of occurrence.
- Ensemble members: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15 (excluding 02, 03, 14).
- File naming conventions (NetCDF4, CEH conventions):
  - Monthly mean flow: G2G_NI_mmflow_UKCP18RCM_ensnum_1980_2080.nc
  - Annual maxima: G2G_NI_amaxflow_UKCP18RCM_ensnum_1980_2080.nc
  - Annual minima: G2G_NI_aminflow_UKCP18RCM_ensnum_1980_2080.nc
- Spatial and temporal details:
  - Domain: NI on GB national grid, 187 km x 170 km; 1km grid cells with center coordinates specified.
  - 30-day model months; time stamps are days since 1900-01-01.
  - Annual maxima assigned to the start date of the 12-month period (e.g., 1981 max corresponds to Oct 1, 1981 – Sep 30, 1982); minima assigned to Dec 1, 1981 – Nov 30, 1982.
  - Missing values coded as -9999; non-tidal river cells only; values outside catchment area set to missing.
- Supporting datasets to aid use:
  - Catchment-area grid (km2) draining to each 1km cell.
  - Majority-lake cell grid (binary).
  - Estimated NRFA river-flow gauging station locations on the 1km grid and a CSV with NRFA IDs.
- Data access and usage aids:
  - Per-ensemble metadata and units included in NetCDF files.
  - Aids for comparing model outputs with observed flows or observation-based inputs.

## How to Use and Compare
- Historical comparisons:
  - Compare G2G NI outputs to observation-based inputs or observed river flow for statistical, not pointwise, comparisons due to non-identical weather features.
- Baseline vs. future comparisons:
  - Use same ensemble member across periods to assess potential climate-change impacts on river flows.
  - Ensemble spread captures climate-model uncertainty.
- Cautions:
  - Do not expect exact replication of observed flows at specific dates due to model structure and calendar/driver differences.
  - Lake and reservoir storage and regulation are not modeled; lakes are treated as rivers, so some flows near large lakes (e.g., Lough Neagh) may be biased.
  - Discrepancies may occur in small catchments due to 1km discretisation relative to actual catchment boundaries.
- Validation and interpretation:
  - Use the NRFA-station-aligned grid to compare modeled flows against observed station data where appropriate.
  - Consider whether results are driven by precipitation bias correction, PE calculation assumptions, or downscaling steps when interpreting results.

## Data Formats and File Organization
- File format: NetCDF4, one file per ensemble member and per variable (monthly, annual max, annual min).
- Ensemble indices: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15.
- Temporal coverage: 1980-2080; data for each grid cell represents the flow at the cell center.
- Spatial coverage: Northern Ireland on a 1km grid; non-tidal river cells with catchment ≥50 km2 included; lakes treated as river cells; some cells in lakes identified by separate lake grid file.
- Additional datasets:
  - UKSCAPE_G2G_NI_CatchmentAreaGrid.nc
  - UKSCAPE_G2G_NI_LakeGrid.nc
  - UKSCAPE_G2G_NI_NRFAStationIDGrid.nc
  - UKSCAPE_NI_NRFAStationIDs.csv

## Limitations and Uncertainties
- Lakes and reservoir regulation not accounted; lake cells included as rivers can affect downstream flow estimates (notably around large lakes).
- Model performance varies by catchment and regulatory context; less accurate where artificial discharges or complex subsurface hydrology dominate.
- Catchment-area discretisation to 1km can introduce errors for smaller basins; NRFA matching is carefully checked but some mismatches may persist.
- Temporal downscaling and bias correction choices (e.g., precipitation bias correction, PE assumptions) influence outputs; results should be interpreted statistically across multi-decadal periods.

## Acknowledgements and References
- Funded by Natural Environment Research Council (NERC) UK-SCAPE programme; award NE/R016429/1.
- Acknowledgements of individuals providing advice and related methodological references listed in the document.