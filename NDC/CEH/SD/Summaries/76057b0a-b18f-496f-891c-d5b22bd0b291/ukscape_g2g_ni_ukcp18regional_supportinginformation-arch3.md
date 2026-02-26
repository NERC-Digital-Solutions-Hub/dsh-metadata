# Supporting information for: Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080) v2

## Brief summary
- Provides Grid-to-Grid (G2G) hydrological model estimates of river flows for Northern Ireland, driven by UKCP18 Regional (12km) meteorological projections.
- Outputs include monthly mean river flow (m3 s-1), annual maxima of daily mean river flow (m3 s-1), and annual minima of 7-day mean river flow (m3 s-1) on a 1km x 1km grid; covers non-tidal, catchment areas ≥50 km2.
- Based on a 12-member perturbed parameter ensemble (PPE) of the Met Office Hadley Centre Regional Climate Model (RCM) for 1980-2080 under RCP8.5, with NI-specific configuration.
- Includes a complementary dataset driven by observation-based inputs for NI, plus three auxiliary spatial datasets: catchment areas (1km grid), majority lake cells (1km grid), and estimated NRFA gauging station locations (1km grid with station IDs).
- Notes model limitations: lakes and reservoir storage are not represented; some catchment-area discrepancies can occur for smaller basins; 360-day calendar in input data leads to 30-day months; ensemble member numbering excludes 02, 03, and 14.

## Data access and citation information
- Access: Open Government Licence v3.
- Source data DOI: 10.5285/76057b0a-b18f-496f-891c-d5b22bd0b291.
- Citation: Kay, A.L.; Rudd, A.C.; Davies, H.N.; Lane, R.A.; Bell, V.A. (2022). Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080) v2. NERC EDS Environmental Information Data Centre. Dataset. https://doi.org/10.5285/76057b0a-b18f-496f-891c-d5b22bd0b291.
- Funders/affiliations: UK-SCAPE programme, Natural Environment Research Council; award NE/R016429/1.

## Brief dataset overview (contents and purpose)
- UK-SCAPE WP2: impacts of climate change on water quantity across Britain; NI-specific G2G outputs driven by UKCP18 Regional projections.
- Outputs: grid-averaged river flow metrics for NI on 1km x 1km grid (non-tidal), plus times of occurrence for annual extremes.
- Complementary data allow interpretation against observations from NRFA or alternative datasets; users should perform statistical rather than point-by-point comparisons due to model-data differences.

## Hydrological model - Grid-to-Grid (G2G)
- A national-scale, grid-based hydrological model operating at 1km x 1km with ~15-minute time steps.
- Configured to NI and parts of Ireland draining to NI rivers; uses globally applicable parameter values (no catchment-specific calibration).
- Accounts for urbanization effects via land-cover influences on runoff; calibrated performance is generally strong in natural-flow regimes, with caveats in heavily regulated or complex subsurface conditions (notably near Lough Neagh).

## G2G model input data
- Forcing: UKCP18 Regional (12km) daily precipitation, daily min/max temperature, and daily potential evapotranspiration (PE) derived via bias-corrected methods.
- Ensembles: 12 PPE members of the Hadley Centre RCM, 1980-2080 under RCP8.5; data downscaled to 1km grid for NI.
- Bias correction and downscaling:
  - Precipitation bias corrected monthly, then downscaled spatially to 1km.
  - PE downscaled to 1km using extraction from MORECS-like methodology with adjustments for future CO2.
  - Temperature downscaled to 1km using elevation-based lapse rates and diurnal sine-based temporal downscaling.
- Supporting inputs: topography and soil data aligned with Bell et al. (2009) configurations; lake influence not accounted for in G2G.

## How to use the dataset
- Historical comparison: G2G NI outputs driven by UKCP18 can be statistically compared to those driven by observation-based input data or to observed river flow (NRFA) over multi-decadal periods; not suitable for point-for-point time-matching.
- Baseline vs. future: Use ensemble member consistency to compare period-to-period differences (e.g., same PPE member across baseline and future).
- Ensemble considerations: Members numbered 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15 (excluding 02, 03, 14).
- Limitations to interpret: lakes/reservoirs not simulated; some grid cells in lakes may show river-like flows; potential mismatches between derived and observed catchment areas for small basins.

## Format of the gridded datasets
- Output: NetCDF4 files, one per ensemble member and per variable.
- Files include:
  - G2G_NI_mmflow_UKCP18RCM_ensnum_1980_2080.nc (monthly mean river flow)
  - G2G_NI_amaxflow_UKCP18RCM_ensnum_1980_2080.nc (annual maxima of daily mean flow; with occurrence dates)
  - G2G_NI_aminflow_UKCP18RCM_ensnum_1980_2080.nc (annual minima of 7-day mean flow; with occurrence dates)
- Spatial domain: NI on GB National Grid, 187 km x 170 km (1km x 1km cells), non-tidal, with cells outside defined catchment area set to missing (-9999).
- Temporal: 30-day months due to 360-day calendar; time variable uses days since 1900-01-01; annual extrema assign dates corresponding to defined hydrological years.
- Auxiliary datasets provided:
  - UKSCAPE_G2G_NI_CatchmentAreaGrid.nc (catchment area per 1km cell)
  - UKSCAPE_G2G_NI_LakeGrid.nc (major lake cells)
  - UKSCAPE_G2G_NI_NRFAStationIDGrid.nc and UKSCAPE_NI_NRFAStationIDs.csv (estimated NRFA gauging station locations)

## Caveats and limitations
- Lake/reservoir storage effects are not represented; some lake cells appear as river cells.
- Potential mismatches between 1km grid catchment areas and observed NRFA catchments, especially for small basins.
- The 360-day calendar results in 30-day months; date alignment for extrema is defined by hydrological year conventions.
- Ensemble member consistency is essential across periods; avoid mixing members between baseline and future.

## Acknowledgements
- Funded by the Natural Environment Research Council (award NE/R016429/1) as part of UK-SCAPE National Capability.
- Acknowledges contributions from researchers including Nuria Bachiller-Jareno, Ting Zhang, and Oliver Robertson.

## References (selected)
- Bell VA, Kay AL, Davies HN, Jones RG (2016). An assessment of the possible impacts of climate change on snow and peak river flows across Britain.
- Bell VA, Kay AL, Jones RG et al. (2009). Development of a high resolution grid-based river flow model for use with regional climate model output.
- Kay AL (2021). Simulation of river flow in Britain under climate change: baseline performance and future seasonal changes.
- Lane RA, Kay AL (2021). Climate change impact on the magnitude and timing of hydrological extremes across Great Britain.
- Murphy JM, Harris GR et al. (2018). UKCP18 Land Projections: Science Report.
- Rudd AC, Bell VA, Kay AL (2017/2016). National-scale analysis of simulated hydrological droughts; Use of high-resolution climate model data for hydrological modelling.
- Rowland CS, Morton RD et al. (2017). Land Cover Map 2015.
- Robinson EL, Kay AL, et al. (2021). Potential evapotranspiration derived from UKCP18 Regional Model ensemble.