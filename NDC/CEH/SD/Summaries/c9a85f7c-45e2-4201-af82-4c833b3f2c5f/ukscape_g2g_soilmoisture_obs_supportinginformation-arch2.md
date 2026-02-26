# Supporting information for Grid-to-Grid model estimates of soil moisture for Great Britain and Northern Ireland driven by observed data (1980 to 2011)

## Overview
- Presents Grid-to-Grid (G2G) model estimates of monthly mean soil moisture on a 1km x 1km grid for Great Britain (GB) and Northern Ireland (NI), driven by observed meteorological data for 1980–2011.
- Part of UK-SCAPE under the Natural Environment Research Council; aims to support climate-change impact analyses on water quantity and hydrology.
- Provides both GB and NI soil moisture outputs, with complementary datasets and lake grids to aid interpretation.

## Dataset scope and contents
- Spatial resolution and domain:
  - GB: 1km x 1km cells on the GB National Grid, 700 km x 1000 km domain.
  - NI: 1km x 1km cells on the GB National Grid, approximately 187 km x 170 km domain.
  - Includes cells within lakes (lake cells are included in outputs); two additional files identify majority lake cells.
- Temporal scope:
  - Monthly mean soil moisture (unsaturated zone) for December 1980 to November 2011.
  - Soil moisture defined as m water/m soil (0–1), interpreted as depth-integrated θ for the whole soil column.
- Outputs:
  - Primary: G2G_GB_mmsoil_obs_1980_2011.nc (GB) and G2G_NI_mmsoil_obs_1980_2011.nc (NI).
  - Lake grids: UKSCAPE_G2G_GB_SoilMoisture_LakeGrid.nc and UKSCAPE_G2G_NI_SoilMoisture_LakeGrid.nc (1 = land, 2 = lake, -9999 = sea).

## Grid-to-Grid model and inputs
- Model: National-scale hydrological Grid-to-Grid (G2G) with 1km x 1km resolution and 15-minute time steps; outputs natural river flows and soil moisture.
- Calibration: Uses spatial datasets; parameters such as lateral routing speeds are nationally applicable values; no catchment-specific calibration.
- Key inputs:
  - Precipitation: daily 1km CEH-GEAR data.
  - Potential evaporation (PE): monthly 40km MORECS data.
  - Temperature: daily min/max 1km Met Office data; daily values downscaled within the day using a sine curve.
- Land-surface parameters: spatially variable soil depth and properties; lakes, reservoirs, and anthropogenic abstractions are not explicitly modeled; lake storage effects on downstream flows are neglected.

## Data usage and interpretation
- Context:
  - These historical soil moisture estimates update MaRIUS-G2G-MORECS monthly soil moisture data (1980–2011 vs earlier data).
  - Can be analyzed alongside UKCP18-driven G2G soil moisture (1980–2080) and related river-flow datasets.
- Considerations:
  - Water bodies are not explicitly modeled in the hydrology, leading to lake cells being present in outputs; lake areas are identified separately.
  - Users should consider differences in land-sea masks and missing soil-type data infilling when comparing to other datasets.

## Data format and access
- File format: NetCDF4, following UKCEH gridded dataset conventions.
- Files:
  - GB soil moisture: G2G_GB_mmsoil_obs_1980_2011.nc
  - NI soil moisture: G2G_NI_mmsoil_obs_1980_2011.nc
- Time encoding: time stamps in days since 1900-01-01; monthly values assigned to the first day of each month.
- Spatial metadata:
  - GB: 0,0 to 700000,1000000 meters.
  - NI: -7000,440000 to 180000,610000 meters.
- Complementary datasets and extensions are provided for broader analyses (lake grids, UKCP18-driven soil moisture, river-flow datasets).

## Relationship to other datasets
- Complementary UKCP18-driven dataset: Grid-to-Grid soil moisture for GB and NI using 12km UKCP18 projections (1980–2080).
- Related river-flow datasets available for GB and NI to support hydrological impact assessments.
- Acknowledges alignment with MaRIUS-G2G-MORECS-monthly datasets, with specific updates and period differences.

## Limitations and caveats
- Lakes and reservoirs not explicitly modeled; lake grid cells are treated as rivers in outputs.
- Lake storage/regulation effects on downstream flows are neglected.
- Model parameters are not calibrated per catchment; sensitivity to natural vs anthropogenically influenced regimes may vary by basin.

## Acknowledgements
- Funded by Natural Environment Research Council under award NE/R016429/1 as part of the UK-SCAPE programme.

## References (examples)
- Bell VA, Kay AL, Davies HN, Jones RG (2016). Climate Change Impacts on Snow and Peak River Flows in Britain.
- Bell VA, Kay AL, Jones RG et al. (2009). Use of soil data in grid-based hydrological modeling.
- Met Office HadUK-Grid and related data sources.