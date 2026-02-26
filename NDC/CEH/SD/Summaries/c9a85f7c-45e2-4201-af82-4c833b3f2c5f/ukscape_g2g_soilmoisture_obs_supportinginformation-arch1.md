# Supporting information for Grid-to-Grid model estimates of soil moisture for Great Britain and Northern Ireland driven by observed data (1980 to 2011)

## Overview
- UK-SCAPE program produced Grid-to-Grid (G2G) soil moisture estimates on a 1km x 1km grid for Great Britain (GB) and Northern Ireland (NI), driven by observed meteorological data (1980–2011).
- Provides monthly mean soil moisture content (m water/m soil) as depth-integrated, across the unsaturated zone.
- Related datasets include G2G estimates driven by UKCP18 regional climate projections (1980–2080) and river-flow datasets for GB and NI.
- Two auxiliary spatial datasets identify majority lake cells to aid interpretation.

## Hydrological model and outputs
- Model: Grid-to-Grid (G2G), a national-scale hydrological model operating on a 1km x 1km grid with a 15-minute time-step (configured for GB and NI, plus drainage to NI rivers from the Republic of Ireland).
- Outputs: spatially consistent gridded estimates of natural river flows and soil moisture (monthly mean).
- Model approach:
  - Uses atmospheric forcing and spatial datasets rather than catchment-specific calibration.
  - Employs globally applicable parameter values when needed (e.g., kinematic wave speeds).
  - Accounts for urban/suburban land cover in runoff, but does not simulate lakes, reservoirs, abstractions, or discharges.
- Limitations:
  - Lakes and reservoir effects on downstream flows are not modeled; lake grid cells are treated as rivers for the dataset.
  - Performance is best in natural-flow-dominated catchments and where input data are reliable; less accurate under strong anthropogenic influence or complex subsurface hydrology.

## Input data and downscaling
- Meteorological inputs:
  - Daily 1km precipitation (CEH-GEAR).
  - Monthly 40km potential evaporation (PE) for short grass (MORECS).
  - Daily 1km min/max air temperatures (Met Office).
- Time handling:
  - Precipitation distributed evenly across daily steps.
  - PE distributed monthly across steps.
  - Temperature downscaled within day using a sine curve.
- Spatial inputs include topography and soil data as in Bell et al. (2009).

## Datasets and format
- Primary soil moisture datasets (monthly averages, daily mean soil moisture) for a 1km grid:
  - GB: G2G_GB_mmsoil_obs_1980_2011.nc
  - NI: G2G_NI_mmsoil_obs_1980_2011.nc
- Time period: December 1980 to November 2011.
- Spatial domain:
  - GB: 700 km × 1000 km on the GB National Grid.
  - NI: 187 km × 170 km on the GB National Grid.
- Time convention: time stamps are days since 1900-01-01; monthly values assigned to the first day of each month.
- Lake-related grids:
  - Majority lake cells identified in UKSCAPE_G2G_GB_SoilMoisture_LakeGrid.nc and UKSCAPE_G2G_NI_SoilMoisture_LakeGrid.nc (cells >85% water; 1 = land, 2 = lake, -9999 = sea).
- File characteristics:
  - NetCDF4 format for both GB and NI.
  - Metadata and dataset conventions follow UKCEH standards.
- Related complementary datasets:
  - Soil moisture driven by UKCP18 Regional (12km) data (1980–2080) for comparison.
  - Corresponding river-flow datasets for GB and NI.

## Using the datasets
- These historical soil moisture estimates update MaRIUS-G2G-MORECS-monthly soil moisture data with a shorter period (1980–2011) and revised land-sea masking and missing data infilling.
- Can be analyzed alongside UKCP18-driven soil moisture estimates and river-flow datasets to assess climate-driven changes and hydrological responses.
- Lake effects are not included; interpret lake-grid cells as land or rivers accordingly, noting potential downstream impacts are not represented.

## caveats and interpretation
- Do not expect precise calibration-derived catchment-specific parameter tuning; results reflect global parameters and input data quality.
- Water bodies are not represented with storage dynamics; downstream impacts via lakes/reservoirs are neglected.
- Users should consider data period, resolution, and lake treatment when applying to local or policy-relevant analyses.

## Acknowledgements
- Supported by Natural Environment Research Council award NE/R016429/1 as part of the UK-SCAPE programme delivering National Capability.

## References (selected)
- Bell, V.A., Kay, A.L., Davies, H.N., Jones, R.G. (2016, 2009, 2018) on G2G and related hydrological modeling approaches.
- Hough, M., Jones, RJA (1997); Tanguy, M. et al. (2016) for input datasets (MORECS, CEH-GEAR).
- Met Office HadUK-Grid and related climate observations.
- Rudd, A.C., Bell, V.A., Kay, A.L. (2017); Formetta, G. et al. (2018) for hydrological droughts and continuous modeling context.