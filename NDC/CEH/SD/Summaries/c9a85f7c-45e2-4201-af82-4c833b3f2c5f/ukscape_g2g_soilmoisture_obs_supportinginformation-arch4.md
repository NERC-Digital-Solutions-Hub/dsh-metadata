# Supporting information for Grid-to-Grid model estimates of soil moisture for Great Britain and Northern Ireland driven by observed data (1980 to 2011)

## Overview
- UK-SCAPE programme provides Grid-to-Grid (G2G) hydrological model estimates of monthly mean soil moisture on a 1 km x 1 km grid for Great Britain (GB) and Northern Ireland (NI) using observed meteorological data (1980–2011).
- Complementary dataset available for soil moisture driven by UKCP18 Regional (12 km) projections (1980–2080).
- Related datasets include G2G river flows for GB and NI; these are designed to support interpretation alongside soil moisture outputs.

## The Grid-to-Grid (G2G) model
- National-scale hydrological model operating on 1 km x 1 km grid (GB) at a 15-minute time-step; extended to NI and to some Irish catchments draining to NI rivers.
- Outputs provide spatially consistent gridded estimates of natural river flows and soil moisture; favors using pre-existing spatial datasets over catchment-specific calibration.
- Urban/suburban land-cover effects on runoff are accounted for; lakes, reservoirs, abstractions, and discharges are not.
- Model performance: good for natural-flow-dominated catchments with accurate flow records; reduced accuracy where artificial regulation or complex sub-surface hydrology dominates.

## Model inputs and processing
- Required inputs: precipitation (daily, 1 km, CEH-GEAR), potential evaporation (monthly, 40 km, MORECS), and daily min/max temperature (1 km, Met Office).
- Temperature downscaling within a day uses a sine curve; precipitation and PET data are distributed over model time-steps accordingly.
- Spatial data (topography, soils) align with the Bell et al. (2009) configuration.

## Data products and formats
- Soil moisture outputs: monthly averages of daily mean soil moisture in the unsaturated zone, reported as m water per m of soil (0 ≤ θ ≤ 1); depth-integrated across the soil column with spatially varying soil depth.
- Grid coverage: every non-sea 1 km x 1 km cell for GB and NI; lakes treated as grid cells and not excluded.
- File formats and naming:
  - GB: G2G_GB_mmsoil_obs_1980_2011.nc (monthly mean soil moisture, GB, Dec 1980–Nov 2011)
  - NI: G2G_NI_mmsoil_obs_1980_2011.nc (monthly mean soil moisture, NI, Dec 1980–Nov 2011)
- Spatial extents:
  - GB domain: 700 km x 1000 km on the GB National Grid (0,0 to 700000,1000000 m)
  - NI domain: 187 km x 170 km on the GB National Grid (-7000,440000 to 180000,610000 m)
- Time stamps: days since 1900-01-01; monthly values assigned to the first day of each month.
- Lake information: two extra lake-grid files identify majority lake cells (≥85% water) to aid interpretation; lake cells are included in soil moisture outputs (e.g., Lough Neagh and Lough Erne).

## Lake and water-body treatment
- Water bodies are not modeled for storage or regulation effects on downstream flows; lakes are treated as rivers in the data, and lake cells are included in the soil moisture grid.
- Lake-grid indicator files differentiate land versus lake cells.

## How to use the datasets
- These historical soil moisture estimates can be viewed as updates to MaRIUS-G2G-MORECS monthly soil moisture data (differences include shorter period 1980–2011, land-sea mask updates, and missing soil-type data infilling).
- Can be analyzed alongside:
  - UKCP18-driven soil moisture dataset (1980–2080) for comparative analysis with precipitation and climate projections.
  - Related river flow datasets for GB and NI to examine hydrological context.
- Important caveats:
  - Lakes and reservoirs are not explicitly modeled for regulation effects; lake grids are included but downstream impacts may be understated.
  - Model parameters rely on spatially fixed values; no catchment-specific calibration.
  - Performance varies with catchment regime and data quality of input meteorology, especially where anthropogenic influences are strong.

## Data provenance and acknowledgements
- Acknowledgement: Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCAPE programme delivering National Capability.
- Supporting references include foundational work on the G2G model, soil data usage, and related hydrological assessments.

## Related references and resources
- Foundational methodological and data references (e.g., Bell et al. 2009; Bell et al. 2016; Tanguy et al. 2016) and linked datasets (UKCP18-driven soil moisture and river-flow datasets) for workflow integration and comparative analyses.