# Supporting information for Grid-to-Grid model estimates of soil moisture for Great Britain and Northern Ireland driven by observed data (1980 to 2011)

## Overview
- UK-SCAPE programme provides Grid-to-Grid (G2G) hydrological model outputs for monthly mean soil moisture on a 1 km x 1 km grid across Great Britain (GB) and Northern Ireland (NI), driven by observed meteorological data (1980–2011).
- Complementary datasets exist for soil moisture driven by UKCP18 Regional climate projections (1980–2080) and related river-flow datasets.
- Two extra spatial datasets identify majority lake cells to aid interpretation.

## Model and outputs
- Hydrological model: Grid-to-Grid (G2G), run on a 1 km x 1 km grid with a 15-minute internal time-step; configured to cover NI and Irish sub-catchments draining to NI rivers.
- Outputs: monthly averages of daily mean soil moisture in the unsaturated zone (θ, m water/m soil, 0 ≤ θ ≤ 1). These are depth-integrated soil-moisture values for the whole soil column.
- Domain and resolution:
  - GB: 700 km × 1000 km domain on the GB National Grid.
  - NI: 187 km × 170 km domain on the GB National Grid.
- Lake treatment: lakes and reservoirs are not simulated for storage/regulation; lake grid cells are included with soil moisture values as if rivers. Lakes are identified in dedicated lake grids.

## Model inputs and configuration
- Required input time-series:
  - Daily precipitation on 1 km grid (CEH-GEAR).
  - Monthly potential evaporation (PE) on a 40 km grid for short grass (MORECS).
  - Daily minimum and maximum temperatures on 1 km grid (Met Office).
- Snow module: optional, uses daily min/max temperatures for snow calculations.
- Data sources are downscaled/aggregated to the 1 km grid as part of the G2G configuration.
- Land-sea mask and topography/soil data used follow established UKCEH/Bell et al. conventions.

## Data files and formats
- Primary GB soil moisture file: G2G_GB_mmsoil_obs_1980_2011.nc (monthly mean soil moisture for GB, 1980 Dec to 2011 Nov).
- Primary NI soil moisture file: G2G_NI_mmsoil_obs_1980_2011.nc (monthly mean soil moisture for NI, 1980 Dec to 2011 Nov).
- Format: NetCDF4, following UKCEH gridded dataset conventions.
- Spatial extents and coordinates:
  - GB: 0,0 to 700000,1000000 (metres on GB National Grid).
  - NI: -7000,440000 to 180000,610000 (metres on GB National Grid).
- Time convention: timestamps are days since 1900-01-01; monthly values assigned to the first day of each month.
- Lake grids:
  - GB: UKSCAPE_G2G_GB_SoilMoisture_LakeGrid.nc
  - NI: UKSCAPE_G2G_NI_SoilMoisture_LakeGrid.nc
  - Grid values: 1 = land, 2 = lake, -9999 = sea.
- Acknowledgement data: includes lake cells to aid interpretation.

## How to use with GIS and related datasets
- Can be used as updates to MaRIUS-G2G-MORECS-monthly soil moisture data (1980–2011 period).
- Compare with UKCP18-driven G2G soil moisture (1980–2080) and corresponding river-flow datasets for integrated analyses.
- Suitable for map-based visualization, spatial profiling, and scenario planning of soil moisture.
- Data align with GB national grid, facilitating overlay with other GB NI spatial layers and hydrological datasets.

## Limitations and caveats
- Lake storage and regulation effects are not accounted for; lakes are treated as rivers in the model outputs.
- Model calibration is not performed for individual catchments; parameters are spatially uniform at the national scale.
- Performance tends to be best in natural-flow-dominated catchments; less accurate where artificial abstractions/discharges or complex sub-surface hydrology are present.
- Some rivers and hydrological responses may be affected by data gaps or resolution limits inherent in the input meteorological datasets.

## Acknowledgements and references
- Supported by Natural Environment Research Council award NE/R016429/1 as part of the UK-SCAPE programme.
- References include Bell et al. (2009, 2016, 2018), Rudd et al. (2017), Formetta et al. (2018), Hough and Jones (1997), Tanguy et al. (2016), and related deposition of HadUK-Grid data.