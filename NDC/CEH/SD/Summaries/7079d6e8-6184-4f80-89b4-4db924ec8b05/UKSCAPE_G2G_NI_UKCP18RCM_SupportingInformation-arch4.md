# Supporting information for Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

- Data accessibility
  - Open Government Licence; dataset available at the UK Data Service DOI: 10.5285/7079d6e8-6184-4f80-89b4-4db924ec8b05
  - Must cite Kay et al. (2021) when using the dataset

- Brief dataset summary
  - UK-SCAPE program, Work Package 2 focus on climate change impacts on water quantity (river flow) in Britain
  - Provides Grid-to-Grid (G2G) hydrological model estimates on a 1km × 1km grid for Northern Ireland
  - Outputs include:
    - Monthly mean river flow (m3 s-1)
    - Annual maxima of daily mean river flow (m3 s-1)
    - Annual minima of 7-day mean river flow (m3 s-1)
  - Driven by UKCP18 Regional (12km) projections, using a 12-member perturbed parameter ensemble (PPE) of the Hadley Centre RCM
  - Time period: December 1980 to November 2080 under RCP 8.5
  - Complementary dataset driven by observation-based data also available
  - Three additional spatial datasets provided: catchment areas, majority lake cells, and estimated NRFA gauging station locations

- Hydrological model: Grid-to-Grid (G2G)
  - National-scale hydrological model on a 1km × 1km grid, 15-minute time-step
  - Configured to cover Northern Ireland and adjacent catchments draining to NI rivers
  - Outputs spatially-consistent gridded river flows for gauged and ungauged rivers
  - Uses globally-applicable parameters; typically not calibrated by catchment
  - Urban/suburban land-cover effects accounted for via model structure
  - Generally good performance in natural-flow catchments; caveats in heavily regulated or hydraulically complex areas (e.g., near Lough Neagh)
  - Requires inputs: precipitation, potential evapotranspiration (PE), daily min/max temperature (for optional snow module)

- Model input data
  - Meteorological inputs derived from UKCP18 Regional (12km) projections
  - 12 PPE ensemble members; Dec 1980 to Nov 2080; RCP8.5
  - Bias correction: precipitation corrected with monthly multiplicative factors
  - PE calculated with Penman-Monteith (MORECS-like approach) and stomatal resistance adjustments for CO2 effects
  - Downscaling strategy to 1km:
    - Precipitation: downscaled using spatial weighting from 1km rainfall patterns and temporally divided across model steps
    - PE: downscaled to 1km by copying 12km values
    - Temperature: downscaled with elevation-based lapse rate; diurnal scaling using a sine curve
  - Base topography/soil datasets used as in Bell et al. (2009)

- How to use the dataset
  - For historical periods, compare G2G NI outputs with observation-based inputs or NRFA data; compare statistically over multi-decadal periods rather than point-by-point
  - For baseline vs future periods, assess potential climate-change impacts on river flows
  - Ensemble usage:
    - Ensemble members: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15
    - Use the same ensemble member across periods for comparisons
  - Limitations to consider:
    - Water bodies (lakes/reservoirs) and lake storage effects are not modeled; lakes treated as rivers
    - Some flows in NI (e.g., near Lough Neagh) may be affected by flood regulation and are not perfectly captured
    - River flows include 1km cells within lakes; an additional file identifies majority lake cells
    - 360-day calendar (30-day months) leads to 30-day months in data
    - Non-tidal, catchment area ≥ 50 km2; non-sea cells only
    - G2G outputs include dates of maxima/minima; times are given as days since 1900-01-01
  - Supporting datasets to aid use:
    - UKSCAPE_G2G_NI_CatchmentAreaGrid.nc: catchment area per 1km cell
    - UKSCAPE_G2G_NI_LakeGrid.nc: majority lake cell identification
    - UKSCAPE_G2G_NI_NRFAStationIDGrid.nc and UKSCAPE_NI_NRFAStationIDs.csv: estimated NRFA gauging station locations on the 1km grid

- Format and data structure
  - Gridded data stored as NetCDF4 files, one file per ensemble member and per variable
  - File naming:
    - G2G_NI_mmflow_UKCP18RCM_ensnum_1980_2080.nc (monthly mean river flow)
    - G2G_NI_amaxflow_UKCP18RCM_ensnum_1980_2080.nc (annual maxima of daily mean river flow and dates)
    - G2G_NI_aminflow_UKCP18RCM_ensnum_1980_2080.nc (annual minima of 7-day mean river flow and dates)
  - Spatial domain: NI on GB National Grid (187 km × 170 km) coordinates provided; non-tidal, catchment area ≥ 50 km2
  - Time conventions:
    - 30-day months due to 360-day calendar
    - Monthly flows nominally assigned to first day of month
    - Annual maxima/minima assigned to start year of the corresponding 12-month period
    - Dates of occurrences provided as days since 1900-01-01
  - Quality flags: non-tidal cells with no data are set to -9999; lakes are included in river-flow grids where applicable

- Additional notes and acknowledgements
  - Acknowledges NERC award NE/R016429/1; UK-SCAPE National Capability
  - Acknowledges contributors and related methodological references

- References (selection)
  - Bell et al. (2007, 2009, 2016), Kay et al. (2021), Lane & Kay (2021), Rudd et al. (2016, 2017), Robinson et al. (2021), Murphy et al. (2018), Rowland et al. (2017), and related UKCP18 documentation