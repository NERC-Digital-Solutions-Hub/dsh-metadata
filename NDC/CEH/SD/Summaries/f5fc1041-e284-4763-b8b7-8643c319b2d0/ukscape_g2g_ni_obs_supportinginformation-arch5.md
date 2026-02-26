# Supporting information for Grid-to-Grid model estimates of river flow for Northern Ireland driven by observed data (1980 to 2011)

## Overview
- UK-SCAPE WP2 project context: research on climate-change impacts on water quantity across Britain; NI-focused Grid-to-Grid (G2G) hydrological outputs derived from observed meteorological data (1980–2011).
- Provides gridded, model-based river-flow estimates on a 1 km x 1 km grid for Northern Ireland, plus related spatial datasets to aid interpretation.
- Outputs include:
  - Monthly mean river flow (m³ s⁻¹)
  - Annual maxima of daily mean river flow (m³ s⁻¹)
  - Annual minima of 7-day mean river flow (m³ s⁻¹)
- Domain: non-tidal, land-based 1 km grid covering Northern Ireland with catchment area ≥ 50 km²; time series aligned to water years as defined in the dataset.
- Related datasets: complementary NI results driven by UKCP18 Regional (12 km) climate projections; additional NI and GB datasets for broader context.

## What is included
- Primary NI G2G flow estimates driven by observed meteorology (1980–2011):
  - Monthly mean flows
  - Annual maxima of daily mean flows
  - Annual minima of 7-day mean flows
- Complementary dataset: NI flows driven by UKCP18 Regional projections (12 km grid) for scenario comparison.
- Ancillary spatial datasets:
  - Digitally-derived catchment areas on a 1 km x 1 km grid
  - 1 km x 1 km grid identifying majority lake cells
  - Estimated locations of NRFA gauging stations on a 1 km x 1 km grid and station metadata (CSV)
- Acknowledgement of NERC support (NE/R016429/1) and project contributors.

## Hydrological model and approach
- Model: Grid-to-Grid (G2G), a national-scale hydrological model with a 1 km x 1 km grid and ~15-minute time-step.
- NI configuration aligned with GB national grid; covers NI catchments and connected Irish sub-catchments draining to NI rivers.
- Outputs natural river flows for gauged and ungauged rivers; parameters are nationally applicable with no catchment-specific calibration.
- Urban/suburban impacts included via land-cover effects; model performance generally good for natural-flow-dominated catchments; caveats for heavily regulated or complex subsurface hydrology (notable limitation near Lough Neagh).

## Model inputs
- Meteorological drivers:
  - Daily precipitation on 1 km grid (CEH-GEAR)
  - Monthly potential evaporation (PE) on 40 km grid (MORECS)
  - Daily min and max temperature on 1 km grid (Met Office)
- Preprocessing steps:
  - Re-project Irish grid data to the GB 1 km national grid
  - Distribute daily precipitation over sub-daily steps
  - Downscale PE monthly within model time-steps
  - Downscale temperature within the day using a sine curve
  - Infilling applied where data gaps exist
- Spatial data used for model configuration (topography, soils) as per Bell et al. 2009.

## Data format, structure, and file naming
- Gridded outputs stored as NetCDF4 (one file per variable) following CEH conventions.
- File naming (examples):
  - Monthly mean river flow: G2G_NI_mmflow_obs_1980_2011.nc
  - Annual maxima of daily mean river flow: G2G_NI_amaxflow_obs_1980_2011.nc
  - Annual minima of 7-day mean river flow: G2G_NI_aminflow_obs_1980_2011.nc
- Spatial domain: NI on GB National Grid, 187 km x 170 km, with coordinates and grid cell centroids defined; non-tidal, non-sea cells with catchment area ≥ 50 km² include data; others set to missing (-9999).
- Time representation:
  - Monthly means nominally assigned to the first day of each month
  - Annual maxima/minima assigned to the start year of the corresponding 12-month period (water-year-based)
- Supplementary datasets (for interpretation and validation):
  1) Catchment area grid (km²) draining to each 1 km cell
  2) Majority lake cell grid (binary/land-lake classification)
  3) NRFA gauging station locations grid and NRFA station IDs CSV
- NRFA station matching: 43 gauging stations mapped to appropriate 1 km grid cells; checks to ensure correct tributary alignment, though some small catchments may show mismatch between 1 km grid discretisation and observed NRFA catchments.

## How to use the datasets
- Compare G2G NI outputs with observed river flows from NRFA (National River Flow Archive) for validation and interpretation.
- Integrate with the complementary UKCP18-driven NI dataset for scenario-based analysis of potential flow changes.
- Consider lake/reservoir effects: the model does not account for lake storage; lake cells are treated as rivers, so downstream flows may reflect lake influence indirectly, particularly in lakes such as Lough Neagh and Lough Erne.
- Use the catchment and lake grids to refine spatial interpretation and to filter or aggregate results by catchment or lake presence.
- Note potential caveats for small catchments due to grid-scale discretisation and possible mismatches of NRFA catchment boundaries.

## Data quality, limitations, and caveats
- Lake/reservoir effects not explicitly modeled; can influence downstream flows in lake-rich areas.
- Calibration is not performed for individual catchments; parameterization is national, which may reduce accuracy for complex or regulated basins.
- Initial NI assessment indicates good performance across NI except downstream of Lough Neagh where flood regulation suppresses observed flows.
- Small catchments may exhibit errors due to discretisation and catchment-area mapping differences between observed NRFA catchments and the 1 km grid representation.
- Some data gaps are infilled during processing; users should review metadata for data quality notes.

## Provenance, citation, and references
- Data published as part of the UK-SCAPE programme and NERC EDS Environmental Information Data Centre; dataset cited with DOI: 10.5285/f5fc1041-e284-4763-b8b7-8643c319b2d0
- Acknowledgements to contributors (e.g., Nuria Bachiller-Jareno, Ting Zhang, Oliver Robertson)
- Key related references include Bell et al. (2009, 2016), Kay et al. (2021), Rudd et al. (2017), Formetta et al. (2018), Hough and Jones (1997), Tanguy et al. (2016), Rowland et al. (2017), Met Office HadUK-Grid updates, and CEH-GEAR data sources.

## Access and related resources
- Primary NI dataset released under the UK-SCAPE programme and referenced in the accompanying documentation
- Related GB datasets and NI datasets driven by UKCP18 projections are available and documented in parallel resources and DOIs linked in the accompanying summary.