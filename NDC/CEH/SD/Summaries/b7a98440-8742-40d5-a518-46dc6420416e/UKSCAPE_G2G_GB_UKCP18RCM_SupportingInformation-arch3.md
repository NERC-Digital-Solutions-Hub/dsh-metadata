# Supporting information for: Grid-to-Grid model estimates of river flow for Great Britain driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

## Purpose and scope
- Describes Grid-to-Grid (G2G) hydrological model outputs for Great Britain, driven by UKCP18 Regional projections, covering 1980–2080 under RCP8.5.
- Provides 1 km x 1 km gridded river flow estimates to support climate impact and water resources monitoring.
- Includes a complementary dataset driven by observation-based input data and notes on Northern Ireland datasets to come.
- Work is part of UK-SCAPE (WP2) funded by the Natural Environment Research Council.

## What the dataset contains
- Monthly mean river flow (m3 s-1) on a 1 km grid.
- Annual maxima of daily mean river flow (m3 s-1) with dates of occurrence.
- Annual minima of 7-day mean river flow (m3 s-1) with dates of occurrence.
- Data for non-tidal rivers with catchment area ≥ 50 km2, on a 1 km grid.
- 12 ensemble member outputs (PPE) for 1980–2080; also provides a complementary, observation-driven dataset.
- Additional datasets:
  - Digitally-derived catchment areas (1 km grid).
  - Estimated locations of flow gauging stations on the 1 km grid and station metadata.

## Model and inputs
- G2G is a national-scale, grid-based hydrological model (1 km resolution; 15-minute time-step) that estimates natural river flows across GB.
- It uses spatial data rather than catchment-by-catchment calibration; certain parameters are globally applied (e.g., kinematic wave speeds).
- Inputs: daily precipitation, daily min/max temperature, daily potential evapotranspiration (PE).
- Driving data: UKCP18 Regional (12 km) projections; 12 PPE ensemble members for December 1980–November 2080 under RCP8.5.
- Applies a bias-correction to precipitation; PE computed with Penman-Monteith methodology; stomatal resistance adjusted for future CO2.
- Spatial downscaling from 12 km to 1 km, and temporal downscaling to model time-steps; elevation-based lapse rate for temperature; sine-based diurnal correction.

## Data processing and downscaling
- Precipitation downscaled using a spatial weighting derived from 1 km rainfall patterns; temporally allocated across model steps.
- PE fields downscaled to 1 km and distributed over time-steps.
- Temperature downscaled to 1 km using elevation and diurnal sine interpolation.
- Metadata and topographic/soil data aligned with the G2G configuration.

## Usage guidance
- Historical comparisons: statistically compare GB G2G outputs (driven by UKCP18) with observation-based inputs or NRFA observations; do not perform point-by-point day-to-day comparisons.
- Baseline vs. future: conduct statistical analyses over multi-decadal windows to assess climate-change impacts on river flows.
- Ensemble usage: use the same ensemble member for baseline and future periods; ensemble member numbers correspond to driving PPE members (01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15).
- The dataset is analogous to MaRIUS-G2G-WAH2-monthly datasets (weather@home2 driving data).

## Format and structure
- Data stored in NetCDF4, one file per ensemble member and per variable.
  - Examples: G2G_GB_mmflow_UKCP18RCM_ensnum_1980_2080.nc for monthly mean flow.
  - Similar naming for amaxflow and aminflow with corresponding time spans.
- Domain: 700 km × 1,000 km GB national grid (0 to 700000, 0 to 1000000 in metres).
- Resolution: 1 km grid; non-tidal river cells with catchment area ≥ 50 km2; missing values marked as -9999.
- Time convention: 30-day months (360-day calendar); time stamps in days since 1900-01-01; monthly flows assigned to the first day of the month.
- Dates for annual maxima/minima and their occurrence times included in the files.

## Additional datasets and validation aids
- CatchmentAreaGrid.nc: catchment area (km2) draining to each 1 km grid cell.
- NRFAStationIDGrid.nc and NRFAStationIDs.csv: estimated NRFA gauging station locations and identifiers mapped to the 1 km grid; enables comparisons with observed river flows at gauging sites.
- Noted potential mismatches: smaller catchments may show discrepancies between grid-based catchment areas and observed NRFA catchments due to discretisation.

## caveats and interpretation
- Caution that comparison with observed weather/flows should be statistical rather than pointwise due to non-equivalence of weather features and RCM PPE dates.
- G2G performance is strongest for natural-flow regimes; performance may degrade in highly regulated or complex sub-surface hydrology contexts.
- The model uses globally applied parameters rather than catchment-specific calibration.

## Data governance, metadata and sharing
- Emphasizes data provenance, methodological transparency (bias correction, downscaling, model setup).
- Encourages reproducibility and consistent use of ensemble members across periods.
- Metadata completeness and clear documentation are essential to enable robust monitoring and policy evaluation; recognition of potential barriers related to data accessibility and transformation needs.

## Acknowledgements and references
- Funded by NERC award NE/R016429/1 as part of UK-SCAPE National Capability.
- Acknowledges contributions and cites relevant methodological and prior work (Bell et al., Kay et al., Rudd et al., Guillod et al., Monteith, MORECS, etc.).