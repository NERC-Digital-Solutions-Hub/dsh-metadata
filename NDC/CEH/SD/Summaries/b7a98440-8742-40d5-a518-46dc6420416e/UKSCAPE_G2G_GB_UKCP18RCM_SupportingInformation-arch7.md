# Grid-to-Grid model estimates of river flow for Great Britain driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

## Overview
- UK-SCAPE programme provides Grid-to-Grid (G2G) hydrological model outputs for Britain at 1 km x 1 km resolution, driven by UKCP18 Regional (12 km) climate projections.
- Time span: December 1980 to November 2080 (water years October–September; December–November for minima).
- Outputs include monthly mean river flow, annual maxima of daily mean river flow, and annual minima of 7-day mean river flow.
- Data are on non-tidal GB river cells with catchment area ≥ 50 km²; supplied in NetCDF4 format. Spatial domain roughly 700 km x 1000 km on the GB National Grid (metres coordinates).

## Datasets included
- Gridded river flow estimates (1 km resolution) driven by UKCP18 Regional (12 km) data:
  - Monthly mean river flow (m³ s⁻¹)
  - Annual maxima of daily mean river flow (m³ s⁻¹) with dates of occurrence
  - Annual minima of 7-day mean river flow (m³ s⁻¹) with dates of occurrence
- Complementary spatial datasets:
  - Digitally-derived catchment areas on a 1 km grid
  - Estimated locations of flow gauging stations on the 1 km grid plus station information
- Optional: comparison data driven by observation-based inputs (e.g., NRFA)
- Ensemble-driven data: 12 PPE members (01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15)

## Model and inputs
- Model: Grid-to-Grid (G2G), national-scale hydrological model running on a 1 km grid with a 15-minute time-step.
- Inputs: daily precipitation, daily min/max temperature, daily potential evapotranspiration (PE); bias-corrected precipitation used; PE calculated via Penman-Monteith with adjustments for future CO₂.
- Driving data: UKCP18 Regional (12 km) projections, 12 PPE members, RCP8.5, 1980–2080.
- Downscaling approach:
  - Precipitation bias-corrected with monthly factors; downscaled to 1 km via spatial weighting; temporally distributed across model time-steps.
  - PE downscaled to 1 km and distributed across time-steps.
  - Temperature downscaled to 1 km using elevation-based lapse rates and daily sine curve modulation.
- Spatial scope: non-tidal river cells with catchment area ≥ 50 km².

## Spatial and temporal resolution
- Spatial: 1 km x 1 km grid across GB; 700 km × 1000 km domain on GB National Grid (coordinates in metres).
- Temporal: monthly means and annual extrema across 1980–2080; 30-day calendar months (360-day year) as per climate model data.

## Data formats and file structure
- NetCDF4 files, one per ensemble member and per variable:
  - G2G_GB_mmflow_UKCP18RCM_ ensnum _1980_2080.nc (monthly mean flows; 1980–2080)
  - G2G_GB_amaxflow_UKCP18RCM_ ensnum _1980_2080.nc (annual maxima; with occurrence dates)
  - G2G_GB_aminflow_UKCP18RCM_ ensnum _1980_2080.nc (annual minima; with occurrence dates)
- File naming conventions reflect:
  - ensnum = ensemble member (01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15)
  - Time range: 1980–2080
- Data grid:
  - 700 km × 1000 km GB domain; 1 km grid cells; values for non-tidal, catchment area ≥ 50 km²; missing values set to -9999.
  - Time encoding: days since 1900-01-01; monthly means nominally assigned to first day of the month.
- Auxiliary datasets:
  - UKSCAPE_G2G_GB_CatchmentAreaGrid.nc (catchment area per 1 km cell)
  - UKSCAPE_G2G_GB_NRFAStationIDGrid.nc (NRFA station locations on 1 km grid); accompanying CSV with station IDs

## Ensemble information
- 12 PPE ensemble members: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15.
- When comparing baseline vs future periods, use the same ensemble member for both periods.

## How to use
- Comparisons:
  - Compare G2G outputs (driven by UKCP18 Regional data) to those driven by observation-based inputs or observed river flow statistically over multi-decadal periods; avoid point-by-point temporal comparisons.
  - Use statistical comparisons to assess potential climate-change impacts on river flows (baseline vs future).
- GIS mapping:
  - Data are in a 1 km grid aligned with GB National Grid; suitable for map-based visualization and spatial analysis in GIS.
  - Use NetCDF outputs for gridded mapping; supplement with catchment area and NRFA station grids for gauging station comparisons.
- Considerations:
  - Calibration is not catchment-specific; model parameters are nationally applicable.
  - Urban/suburban land-cover effects are incorporated, but model performance varies with natural vs anthropogenically influenced basins.
  - Some discrepancies may occur for small catchments when discretized to 1 km grids.

## Data quality, limitations, and guidance
- G2G tends to perform best in natural-flow regimes and where observational records are strong; limitations exist in areas with artificial abstractions or complex subsurface hydrology.
- The 360-day calendar and 30-day months reflect the climate model structure; time stamping follows this convention.
- Minor changes to the G2G setup since MaRIUS-era releases are accounted for; differences in catchment area representation may occur for small basins.

## Access, acknowledgements, and references
- Funding: Natural Environment Research Council (UK-SCAPE, NE/R016429/1).
- Acknowledgements: contributions from team members cited in the dataset documentation.
- Key references for methods and context are listed within the dataset description (e.g., Bell et al. 2009; Kay et al. 2021; Guillod et al. 2017/2018; Murphy et al. 2018).