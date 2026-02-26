# Supporting information for Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

## Data accessibility and citation
- Data are available under the Open Government Licence.
- DOI: 10.5285/7079d6e8-6184-4f80-89b4-4db924ec8b05
- Citation requirement: Kay et al. (2021). Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080). NERC EDS Environmental Information Data Centre.

## Brief dataset overview
- UK-SCAPE program on water quantity impacts; work package 2 provides Grid-to-Grid (G2G) hydrological model estimates of:
  - Monthly mean river flow (m3 s-1)
  - Annual maxima of daily mean river flow (m3 s-1)
  - Annual minima of 7-day mean river flow (m3 s-1)
- Spatial coverage: 1 km x 1 km grid across the UK; NI flows driven by UKCP18 Regional (12 km) projections.
- Period: December 1980 to November 2080 under RCP8.5; 12 ensemble perturbed-parameter members.
- Comparable datasets exist for Great Britain and observation-based inputs.
- Additional spatial datasets included to aid interpretation (catchment areas, majority lake cells, and NRFA gauging station locations).

## Hydrological model – Grid-to-Grid (G2G)
- National-scale hydrological model on a 1 km x 1 km grid with a 15-minute time-step.
- Configured to cover Northern Ireland and some cross-border sub-catchments; outputs natural river flows for gauged and ungauged rivers.
- Uses fixed, nationally-applicable parameters; calibrations not performed per catchment.
- Urban/suburban land cover effects are included in the runoff modelling.
- Performance: generally good in NI; caveat downstream of Lough Neagh where flood regulation affects observed flows.

## G2G model input data and processing
- Meteorological inputs from UKCP18 Regional (12 km) projections:
  - Daily precipitation, daily min/max temperature, daily potential evapotranspiration (PE).
  - 12 PPE ensemble members; period 1980-2080; 360-day calendar (12 x 30-day months).
- Pre-processing:
  - Bias-corrected precipitation using monthly multiplicative factors.
  - PE derived via Penman-Monteith (MORECS-compatible approach) with CO2-adjusted stomatal resistance.
  - 12 km data downscaled to 1 km using spatial weighting for precipitation; PE downscaled to 1 km; temperature downscaled with elevation-based lapse rate and sine-based diurnal variation.
- Domain and grid specifics:
  - NI domain: 187 km x 170 km on GB National Grid; 1 km x 1 km cells; non-tidal river cells with catchment area ≥ 50 km² receive data; others set to missing (-9999).
  - 30-day months; time stamps as “days since 1900-01-01”; monthly values assigned to first day of month.
  - Lakes and reservoirs not explicitly modelled; lake cells treated as rivers (lake storage effects neglected).
- Outputs delivered:
  - Monthly mean river flow, annual maxima of daily mean river flow (and dates of occurrence), annual minima of 7-day mean river flow (and dates of occurrence).

## How to use the dataset
- Historical comparisons:
  - Compare G2G NI flows driven by UKCP18 to those driven by observation-based data or observed river flow (NRFA) for statistical assessments over multi-decadal periods; avoid point-by-point time-aligned comparisons.
- Future/projection assessments:
  - Compare baseline vs. future periods statistically to evaluate potential climate-change impacts on river flows.
- Ensemble usage:
  - Use the same ensemble member for corresponding baseline and future periods (e.g., member 01 for both periods).
- caveats:
  - Water bodies (lakes) do not feed back into downstream flows via storage effects.
  - NRFA gauging station locations are approximated to 1 km grid cells; catchment areas derived may differ from observed NRFA catchments, especially for smaller basins.

## Format of the gridded datasets
- File format: NetCDF4; one file per ensemble member and per variable.
- Naming convention:
  - Monthly mean river flow: G2G_NI_mmflow_UKCP18RCM_ensnum_1980_2080.nc
  - Annual maxima of daily mean river flow (with dates): G2G_NI_amaxflow_UKCP18RCM_ensnum_1980_2080.nc
  - Annual minima of 7-day mean river flow (with dates): G2G_NI_aminflow_UKCP18RCM_ensnum_1980_2080.nc
- Ensemble members included: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15 (02, 03, 14 excluded).
- Spatial domain:
  - NI domain on GB National Grid: 187 km x 170 km; grid cells centered within coordinates spanning from lower left (-7000, 440000) to upper right (180000, 610000) meters.
  - 1 km x 1 km grid; non-tidal river cells with catchment area ≥ 50 km² only.
- Time and data specifics:
  - 30-day months due to 360-day calendar in climate model data.
  - Time variable: days since 1900-01-01; monthly flows nominally assigned to the first day of each month.
  - Annual maxima/minima dates provided as days since 1900-01-01.

## Additional spatial datasets (provided to aid use)
- UKSCAPE_G2G_NI_CatchmentAreaGrid.nc: catchment area (km²) draining to each 1 km grid box.
- UKSCAPE_G2G_NI_LakeGrid.nc: 1 km grid identifying majority lake cells (>70% water, with manual adjustments for Lough Erne).
- UKSCAPE_G2G_NI_NRFAStationIDGrid.nc and UKSCAPE_NI_NRFAStationIDs.csv: estimated locations of NRFA gauging stations on the 1 km grid; 0 indicates land, -9999 sea, NRFA ID at gauging locations.

## Acknowledgements and references
- Funded by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCAPE programme.
- References include foundational papers on the G2G model, bias correction, downscaling methods, and NRFA data integration (listed in the document).