# Supporting information for Grid-to-Grid model estimates of river flow for Northern Ireland driven by observed data (1980 to 2011)

## Overview
- UK-SCAPE program focus on climate impacts on water quantity; this dataset provides Grid-to-Grid (G2G) hydrological model estimates of river flow for Northern Ireland driven by observed meteorological data (1980–2011).
- Outputs are on a 1 km × 1 km grid across Northern Ireland, with values for monthly mean flows, annual maxima of daily mean flows, and annual minima of 7-day mean flows.
- A complementary dataset covers G2G estimates for NI driven by UKCP18 Regional (12 km) climate projections.
- Additional spatial datasets aid interpretation: digitally-derived catchment areas, majority-lake cells, and estimated gauging-station locations.

## What the data include
- Monthly mean river flow (m3 s-1) for each 1 km × 1 km non-tidal grid cell with catchment area ≥ 50 km².
- Annual maxima of daily mean river flow (m3 s-1) for the same grid cells.
- Annual minima of 7-day mean river flow (m3 s-1) for the same grid cells.
- Gridded data cover Northern Ireland on a 187 km × 170 km domain aligned with the GB National Grid; grid cell centers are 1 km apart.
- Outputs are provided in NetCDF4 format, with separate files for each variable and a specific naming convention.
- Supporting spatial datasets:
  - Catchment area grid (km²) draining to each 1 km × 1 km cell.
  - Lake grid identifying majority lake cells (>70% water).
  - NRFA gauging-station location grid and a CSV with NRFA station IDs.

## Grid-to-Grid (G2G) model overview
- G2G is a national-scale hydrological model that runs on a 1 km × 1 km grid with a 15-minute time-step.
- Configured for Northern Ireland and relevant Irish catchments draining to NI rivers, using a GB national grid for consistency.
- Outputs natural river flows for gauged and ungauged rivers, with parameters typically not calibrated to individual catchments (nationally applicable values used).
- Model includes the impact of urban/suburban land-cover on runoff; lake/reservoir storage is not explicitly modeled.

## Model inputs and data processing
- Meteorological inputs:
  - Daily 1 km precipitation (CEH-GEAR).
  - Monthly 40 km potential evaporation (MORECS).
  - Daily min and max temperature (Met Office) for the optional snow module.
- Precipitation and PE data are on the Irish grid and re-projected to the 1 km GB national grid.
- Temporal downscaling:
  - Precipitation distributed evenly over each daily time-step.
  - PE distributed evenly over each monthly time-step.
  - Temperature downscaled within the day using a sine curve.
- Gaps in PE and temperature data are infilled where needed.
- Spatial data (topography, soils) follow the conventions described in Bell et al. (2009).

## Data formats and file naming
- NetCDF4 format files for each variable:
  - Monthly mean river flow: G2G_NI_mmflow_obs_1980_2011.nc (Dec 1980–Nov 2011).
  - Annual maxima of daily mean river flow: G2G_NI_amaxflow_obs_1980_2011.nc (Oct 1981–Sep 2011).
  - Annual minima of 7-day mean river flow: G2G_NI_aminflow_obs_1980_2011.nc (Dec 1980–Nov 2011).
- NI 1 km × 1 km grid domain on the GB National Grid, extending from:
  - Lower left: (-7000, 440000) to upper right: (180000, 610000) meters.
- Values are provided only for non-tidal river cells with catchment area ≥ 50 km²; other cells are missing (-9999).
- Time stamps:
  - Monthly flows: days since 1900-01-01, assigned to the first day of each month.
  - Annual max/min: assigned to the start year of the 12-month period (e.g., 1981 for 1981–1982 period).
- Additional helper datasets:
  - CatchmentAreaGrid.nc
  - LakeGrid.nc
  - NRFAStationIDGrid.nc and NRFAStationIDs.csv
- Three extra datasets are provided to facilitate interpretation and validation:
  - Digitally-derived catchment areas (km²) draining to each 1 km grid cell.
  - Majority lake cells grid (land vs. lake vs. sea).
  - Estimated NRFA gauging-station locations on the 1 km grid, with NRFA IDs.

## Spatial context and limitations
- The dataset is focused on a NI domain and uses a GB grid alignment to standardize spatial references.
- Lakes and reservoirs are not explicitly modeled; lake storage effects on downstream flows are neglected, and lake cells may appear as river cells.
- NRFA-based validation can be affected by mismatches between NRFA catchments and the 1 km grid discretisation, especially for small catchments.
- G2G parameters are national defaults; no catchment-specific calibration is applied.

## How to use the data
- Compare G2G-derived flows with observed river flows from the NRFA (National River Flow Archive) to assess model performance.
- Cross-check NI G2G NI data with the UKCP18-driven NI projections dataset for climate-change scenarios.
- Use accompanying catchment, lake, and NRFA-station grids to contextualize flows at the 1 km grid scale and to locate comparison points with gauging stations.
- Suitable for map-based visualization and spatial analysis within GIS workflows; NetCDF4 format supports GIS-compatible extraction and visualization.

## Practical notes and caveats
- Data reflect natural river flows; urban effects are embedded in the model, but direct anthropogenic abstractions and discharges may not be fully captured.
- Lake/reservoir influence is not represented; some river-flow paths pass through lake cells as if they were rivers.
- For small catchments, discretisation to 1 km × 1 km can introduce proportionally larger errors in the derived catchment area draining to a grid cell.
- Weights and parameter values are nationally consistent rather than catchment-tailored.

## Acknowledgements
- Supported by Natural Environment Research Council award NE/R016429/1 (UK-SCAPE National Capability). Contributors: Kay, Davies, Lane, Rudd, Bell, etc.

## References
- Related methodological and data sources referenced in the dataset documentation (e.g., Bell et al., 2009; Kay et al., 2021; CEH-GEAR; MORECS; HadUK-Grid).