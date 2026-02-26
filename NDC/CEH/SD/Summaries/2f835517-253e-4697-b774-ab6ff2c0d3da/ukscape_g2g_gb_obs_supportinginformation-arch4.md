# Supporting information for Grid-to-Grid model estimates of river flow for Great Britain driven by observed data (1980 to 2011)

## Overview
- UK-SCAPE program (five-year, NERC-funded) includes work on climate change impacts on water quantity, producing Grid-to-Grid (G2G) hydrological model estimates of river flow across Britain driven by observed meteorological data (1980–2011).
- Outputs provide 1 km x 1 km gridded estimates of: monthly mean river flow, annual maxima of daily mean river flow, and annual minima of 7-day mean river flow.
- A companion dataset provides G2G estimates driven by UKCP18 Regional (12 km) projections.
- Two additional spatial datasets accompany the flows: digitally-derived catchment areas and estimated locations of flow gauging stations (NRFA) on a 1 km grid.

## Data content
- G2G model outputs for Great Britain:
  - Monthly mean river flow (m3 s-1)
  - Annual maxima of daily mean river flow (m3 s-1)
  - Annual minima of 7-day mean river flow (m3 s-1)
- Spatial coverage: non-sea, non-tidal 1 km grid cells with catchment area ≥ 50 km2.
- Temporal coverage: 1980–2011 (water years defined as Oct–Sep or Dec–Nov for respective metrics).
- Complementary datasets: UKCP18-driven G2G GB flows; catchment-area grid; NRFA station locations with station IDs.

## Model details (Grid-to-Grid, G2G)
- National-scale, grid-based hydrological model operating on a 1 km x 1 km grid with a 15-minute time-step.
- Produces natural-flow estimates for gauged and ungauged rivers; relies on spatial datasets rather than catchment-specific calibration.
- Uses broadly applicable parameter values (e.g., kinematic wave speeds) and accounts for urban/suburban runoff effects via land-cover inputs.
- Performance: strongest for natural-flow regimes; less accurate where artificial abstractions/discharges or complex subsurface hydrology dominate.

## Model inputs
- Precipitation: daily 1 km grids (CEH-GEAR)
- Potential evaporation (PE): monthly 40 km grids (MORECS)
- Temperature: daily min/max 1 km grids (Met Office)
- Snow module upgrades use daily min/max temperatures (optional)
- Spatial inputs include topography and soil data as per Bell et al. (2009)

## How to use the datasets
- Compare G2G outputs with observed river flows from NRFA to assess model performance.
- These monthly flows update MaRIUS-G2G-MORECS monthly data; differences arise from shorter 1980–2011 period, updated land-sea mask, and minor network discretisation changes.
- Data can be analyzed alongside the UKCP18-driven G2G dataset for scenario comparisons.
- The NRFA-station grid allows evaluation at gauged locations; note potential mismatches for some small catchments due to discretisation.

## Format of the data and access
- Files are NetCDF4 per variable, following CEH gridded dataset conventions.
- Example file names:
  - Monthly mean flow: G2G_GB_mmflow_obs_1980_2011.nc
  - Annual maximum flow: G2G_GB_amaxflow_obs_1980_2011.nc
  - Annual minimum flow: G2G_GB_aminflow_obs_1980_2011.nc
- Spatial domain: 700 km x 1000 km (GB National Grid) from (0,0) to (700000,1000000) meters.
- Grid cells represent the centre of the 1 km x 1 km cell; values outside the catchment area ≥50 km2 are set to missing (-9999).
- Time stamps: days since 1900-01-01; monthly data assigned to the first day of the month; annual extrema assigned to the start year of the 12-month period.
- Supplementary spatial datasets:
  - UKSCAPE_G2G_GB_CatchmentAreaGrid.nc: catchment area (km2) per 1 km cell
  - UKSCAPE_G2G_GB_NRFAStationIDGrid.nc: estimated NRFA station IDs per 1 km cell; station details in accompanying CSV
- Data access and file conventions align with MaRIUS G2G outputs and CEH gridded data standards.

## Supplementary datasets and matching notes
- Catchment-area grid helps interpret flows relative to drainage area.
- NRFA station grid enables comparison to observed gauging data; some small-catchment matches may diverge from official NRFA catchments due to discretisation at 1 km resolution.
- Two additional NRFA stations are included in the CSV file; station IDs reference NRFA numbers.

## Limitations and caveats
- Some discrepancies can arise when matching 1 km grid cells to observed NRFA catchments, especially for small basins.
- G2G uses fixed, nationally applicable parameters and may under- or over-estimate flows where sub-surface hydrology or human abstractions are complex.
- Interpretation should consider potential differences introduced by discretisation and the 1980–2011 observational driving period.

## Acknowledgements and references
- Funded by Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCAPE programme.
- Acknowledgements to contributors: Nuria Bachiller-Jareno, Ting Zhang, Oliver Robertson.
- Key references include Bell et al. (2009, 2016, 2018), Rudd et al. (2017), Formetta et al. (2018), Davies & Bell (2009), Tanguy et al. (2016), Met Office HadUK-Grid data (2019).