# Supporting information for: Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080) v2

## Data access and citation
- Data licensed under the Open Government Licence v3.
- Source and DOI: https://doi.org/10.5285/76057b0a-b18f-496f-891c-d5b22bd0b291
- Required citation: Kay et al. (2022). Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080) v2. NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/76057b0a-b18f-496f-891c-d5b22bd0b291

## Brief summary of the dataset
- UK-SCAPE program context: five-year programme studying climate-change impacts on water quantity; Work Package 2 focuses on river flow across Britain.
- G2G outputs for Northern Ireland (NI):
  - Monthly mean river flow (m3 s-1)
  - Annual maxima of daily mean river flow (m3 s-1)
  - Annual minima of 7-day mean river flow (m3 s-1)
- Grid resolution and domain: 1 km x 1 km grid across NI; non-tidal, catchment area ≥ 50 km2.
- Forcing data: UKCP18 Regional (12 km) projections, 12-member perturbed parameter ensemble (PPE), period 1980–2080, RCP8.5.
- Complementary dataset uses observation-based input data.
- Additional spatial datasets provided: catchment areas (1 km grid), majority lake cells (1 km grid), estimated NRFA gauging station locations (1 km grid and CSV).

## Hydrological model - Grid-to-Grid (G2G)
- Nature of model: national-scale, 1 km x 1 km grid, 15-minute time-step; configured to NI and some ROI catchments draining to NI rivers.
- Outputs: spatially consistent gridded natural river flows for gauged and ungauged rivers.
- Calibration approach: uses globally applicable parameter values; no catchment-specific calibration; urban/suburban land-cover effects included via model structure.
- Performance: generally good across NI; best for natural-flow regimes; caveats downstream of Lough Neagh due to flood regulation.
- Required inputs: precipitation and potential evaporation (PE); daily min/max temperature for optional snow module.
- Output types: monthly mean flows, annual maxima of daily mean flows, and annual minima of 7-day mean flows; includes timing of maxima/minima.

## G2G model input data
- Forcing data: UKCP18 Regional (12 km) daily precipitation, daily min/max temperature, daily PE (bias-corrected and downscaled).
- Ensemble: 12 PPE members; calendar is 360-day year in model data.
- Bias correction: monthly multiplicative factors for precipitation; PE derived via Penman-Monteith method with MORECS-based stomatal resistance adjusted for CO2 effects.
- Downscaling to 1 km: spatial weighting from 1 km rainfall patterns; temporal downscaling by equal division across model time-steps.
- Additional spatial data used: topography and soil data per Bell et al. (2009).

## How to use the dataset
- Historical comparisons: can be made statistically against observation-based input or NRFA river flows; not point-by-point comparisons due to non-equivalence of weather features.
- Baseline vs future: enable statistical assessment of climate-change impacts on river flows.
- Ensemble usage: keep the same ensemble member when comparing periods (e.g., member 01 across both baseline and future).
- Lake/storage considerations: water bodies’ storage and regulation not accounted for; lakes treated as rivers (affects flows in lake cells, notably near Lough Neagh/Lough Erne).
- Gauging stations: NRFA gauging station locations mapped to 1 km grid cells; some catchment-area discrepancies may occur, especially for small basins.

## Format of the gridded datasets
- File format: NetCDF4, one file per ensemble member and per variable.
- File naming: G2G_NI_mmflow_UKCP18RCM_ensnum_1980_2080.nc (monthly mean flow); G2G_NI_amaxflow_UKCP18RCM_ensnum_1980_2080.nc (annual maxima with dates); G2G_NI_aminflow_UKCP18RCM_ensnum_1980_2080.nc (annual minima with dates).
- Ensemble identifiers: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15.
- Spatial domain: NI on GB National Grid, 187 km × 170 km; grid cell at centre coordinates; non-tidal river cells only; missing data flagged as -9999.
- Temporal details: 30-day months (360-day calendar); time units are days since 1900-01-01; monthly means assigned to first day of the month; maxima/minima dates provided.
- Availability window: Dec 1980–Nov 2080 (varies by metric).

## Supporting datasets
- UKSCAPE_G2G_NI_CatchmentAreaGrid.nc: catchment area (km2) per 1 km grid cell.
- UKSCAPE_G2G_NI_LakeGrid.nc: majority lake cells (1 for land, 2 for lake, -9999 sea).
- UKSCAPE_G2G_NI_NRFAStationIDGrid.nc and CSV: estimated NRFA gauging station locations corresponding to 43 NRFA stations.

## Acknowledgements
- Funded by Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE National Capability.
- Acknowledgement of contributions from listed individuals.

## References
- Key methodological and data references related to G2G, bias correction, snow module, and UKCP18-related research (cited within the document).