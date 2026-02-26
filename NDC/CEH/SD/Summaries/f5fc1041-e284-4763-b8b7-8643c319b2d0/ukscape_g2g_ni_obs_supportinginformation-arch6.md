# Supporting information for Grid-to-Grid model estimates of river flow for Northern Ireland driven by observed data (1980 to 2011)

## Overview
- Describes Grid-to-Grid (G2G) hydrological model outputs for Northern Ireland (NI) driven by observed meteorological data (1980–2011).
- NI data produced on a 1 km x 1 km grid using the GB national grid, for non-tidal river cells with catchment area ≥ 50 km².
- Outputs include:
  - Monthly mean river flow (m3 s-1)
  - Annual maxima of daily mean river flow (m3 s-1)
  - Annual minima of 7-day mean river flow (m3 s-1)
- A complementary dataset provides G2G NI river flows driven by UKCP18 Regional (12 km) climate projections.
- Three additional spatial datasets aid interpretation: digitally-derived catchment areas, majority lake cells, and estimated NRFA gauging station locations.

## What is included
- Gridded river-flow estimates for NI on a 1 km x 1 km grid (non-tidal, catchment area ≥50 km²).
- Historical period flows for comparison with observed gauged flows (NRFA).
- Related datasets:
  - UKSCAPE_G2G_NI_CatchmentAreaGrid.nc (catchment areas in km²)
  - UKSCAPE_G2G_NI_LakeGrid.nc (majority lake cells)
  - UKSCAPE_G2G_NI_NRFAStationIDGrid.nc and UKSCAPE_NI_NRFAStationIDs.csv (NRFA gauging station locations)
- Time coverage: monthly and annual summaries spanning 1980–2011 (varies by metric).

## Grid-to-Grid model and inputs
- G2G is a national-scale grid-based hydrological model (1 km x 1 km, 15-minute time-step).
- Configuration now covers NI and adjacent catchments draining to NI rivers.
- Outputs natural river flows (gauged and ungauged) with globally applicable parameters (calibration not per catchment).
- Inputs required:
  - Daily precipitation (CEH-GEAR)
  - Monthly potential evapotranspiration (MORECS)
  - Daily min/max temperature (Met Office HadUK-Grid)
- Precipitation and PE data reprojected to the 1 km GB grid; temporal downscaling methods described; some infilling where data gaps occur.
- Lakes/reservoirs not explicitly accounted for; lakes treated as rivers in affected cells.

## Data formats and file naming
- Gridded data stored as NetCDF4 files, one file per variable.
- File naming:
  - Monthly mean river flow: G2G_NI_mmflow_obs_1980_2011.nc (Dec 1980–Nov 2011)
  - Annual maxima of daily mean river flow: G2G_NI_amaxflow_obs_1980_2011.nc (Oct 1981–Sep 2011)
  - Annual minima of 7-day mean river flow: G2G_NI_aminflow_obs_1980_2011.nc (Dec 1980–Nov 2011)
- Domain and grid details:
  - NI domain: 187 km x 170 km on GB National Grid
  - Spatial extent: lower-left corner (-7000, 440000) to upper-right (180000, 610000)
  - Grid cell center coordinates used for values; non-tidal river cells only
  - Missing values indicated by -9999
- Time stamps:
  - Time units: days since 1900-01-01
  - Monthly values assigned to the first day of each month
  - Annual maxima/minima assigned to the start year of the 12-month period

## How to use the datasets
- Compare G2G NI flows with observed NRFA river flows for validation and interpretation.
- Analyze alongside the UKCP18 Regional (12 km) climate-projected G2G NI flows for future-change assessment.
- Use ancillary datasets to contextualize results:
  - CatchmentAreaGrid: catchment area draining to each 1 km grid cell
  - LakeGrid: identifies majority lake cells (water >70% area)
  - NRFAStationIDGrid and NRFAStationIDs.csv: best NI NRFA gauging-station locations on the 1 km grid
- Practical considerations:
  - Lake and reservoir impacts on downstream flows are not modeled; river-flow grid cells within lakes may not reflect final downstream hydrology.
  - Some small catchments may exhibit discretisation-related discrepancies between the 1 km grid and observed NRFA catchment areas.

## Ancillary datasets and purpose
- Catchment area grid (UKSCAPE_G2G_NI_CatchmentAreaGrid.nc): km² draining to each 1 km cell.
- Lake grid (UKSCAPE_G2G_NI_LakeGrid.nc): 1 for land, 2 for lake, -9999 for sea; helps identify lake-affected cells.
- NRFA station location grid (UKSCAPE_G2G_NI_NRFAStationIDGrid.nc) and CSV (UKSCAPE_NI_NRFAStationIDs.csv): maps 1 km grid cells to NRFA stations for validation.

## Limitations and caveats
- Lakes and water bodies not modeled for storage/regulation; some lakes appear as river cells in the dataset.
- NRFA catchment areas for some smaller basins may differ from the 1 km grid discretisation, introducing potential errors in exact catchment attribution.
- Model calibration is not catchment-specific; performance is generally good for natural-flow regimes but may be weaker where human regulation or complex sub-surface hydrology dominate (noted in NI evaluation, e.g., flows downstream of Lough Neagh).

## Acknowledgements and references
- Funded by Natural Environment Research Council (NERC) award NE/R016429/1 as part of UK-SCAPE National Capability.
- Acknowledges contributions from research and advisory colleagues.
- Key references include Bell et al. (2009, 2016), Kay et al. (2021), Rudd et al. (2017), Rowland et al. (2017), and related CEH and Met Office datasets.