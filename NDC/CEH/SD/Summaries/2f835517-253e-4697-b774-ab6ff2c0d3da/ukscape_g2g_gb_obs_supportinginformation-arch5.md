# Supporting information for Grid-to-Grid model estimates of river flow for Great Britain driven by observed data (1980 to 2011)

- The dataset provides Grid-to-Grid (G2G) hydrological model estimates of natural river flows for Great Britain on a 1 km x 1 km grid, driven by observation-based meteorological data for 1980–2011.
- It is part of UK-SCAPE, focused on climate-change impacts on water quantity (river flow) across Britain, with a complementary dataset using UKCP18 Regional (12 km) climate projections for cross-comparison.

## What is included
- G2G model outputs at 1 km x 1 km resolution for non-tidal rivers with catchment area >= 50 km², including:
  - Monthly mean river flow (m³ s⁻¹)
  - Annual maxima of daily mean river flow (m³ s⁻¹)
  - Annual minima of 7-day mean river flow (m³ s⁻¹)
- Outputs are provided for:
  - Historical period 1980–2011 (water years Oct–Sep for maxima; Dec–Nov for minima)
  - For Great Britain (GB) on a 700 km x 1000 km domain
- Two additional spatial datasets to aid interpretation:
  - Digitally-derived catchment areas (km²) draining to each 1 km grid cell
  - Estimated locations of NRFA river flow gauging stations on the 1 km grid, with station IDs (NRFA)

## Grid-to-Grid (G2G) model overview
- National-scale hydrological model with 1 km grid, 15-minute time-step, across GB; outputs natural river flows for gauged and ungauged rivers.
- Calibrated using nationally-applicable parameters (no catchment-specific calibration); urban/suburban land-cover effects accounted for via runoff routing.
- Inputs required: precipitation, potential evaporation (PE), and daily min/max temperature (for optional snow module).
- Performance: best for catchments with natural flow regimes and accurate observation records; less accurate where abstractions/discharges or complex sub-surface hydrology are present.

## Model input data and processing
- Meteorological inputs:
  - Daily 1 km precipitation (CEH-GEAR)
  - Monthly 1 km PE for short grass (MORECS)
  - Daily 1 km min/max temperature (Met Office)
- Temporal and spatial downscaling:
  - Precipitation distributed evenly within each daily time-step
  - PE distributed within each monthly time-step
  - Temperature downscaled to daily using a sine curve
- Spatial data used to configure G2G (as in prior Bell et al. work)

## Data format and structure
- File format: NetCDF4, one file per variable
- File naming and periods:
  - Monthly mean river flow: G2G_GB_mmflow_obs_1980_2011.nc (Dec 1980–Nov 2011)
  - Annual maxima of daily mean river flow: G2G_GB_amaxflow_obs_1980_2011.nc (Oct 1981–Sep 2011)
  - Annual minima of 7-day mean river flow: G2G_GB_aminflow_obs_1980_2011.nc (Dec 1980–Nov 2011)
- Domain and data values:
  - Domain: 0 to 700,000 m (x) and 0 to 1,000,000 m (y) on the GB National Grid
  - 1 km grid cells with catchment area ≥ 50 km²
  - Missing values set to -9999
  - Time stamp format: days since 1900-01-01; monthly means assigned to first day of the month
  - Annual maxima/minima assigned to the start year of the corresponding 12-month period
- Additional grid datasets:
  - UKSCAPE_G2G_GB_CatchmentAreaGrid.nc (catchment area per grid cell)
  - UKSCAPE_G2G_GB_NRFAStationIDGrid.nc (station locations with NRFA IDs)
  - NRFAStationIDs.csv (supplemental station information)

## How to use the datasets
- Compare G2G outputs with observed river flows from NRFA as a validation/reference.
- Use alongside the UKCP18-driven G2G dataset for climate-projection analyses (different driving data and period).
- The gauging-station grid enables association of modeled flows with observed NRFA stations, with caveats for small catchments where discretisation may diverge from observed boundaries.
- This set updates MaRIUS-G2G-MORECS monthly data but differs in period (1980–2011 vs broader prior ranges) and minor model/land-sea mask updates.

## Spatial and temporal coverage
- Temporal: 1980–2011 (observed driving data)
- Spatial: Great Britain mainland; 1 km x 1 km grid; non-tidal river cells; catchment area ≥ 50 km²

## Data quality, limitations, and caveats
- Catchment discretisation to 1 km grids can introduce errors for smaller catchments; NRFA catchment areas at a given grid cell may not exactly match observed NRFA catchments.
- G2G parameters are nationally uniform; local catchment calibration is not performed.
- Outputs are designated for non-tidal rivers; applicability to tidal or near-coastal areas is not specified.
- Some differences with the MaRIUS G2G dataset due to updated land-sea mask and network discretisation.

## Related datasets and comparability
- Complementary dataset: G2G river flows across GB driven by UKCP18 Regional (12 km) climate projections.
- Similar structure and conventions to MaRIUS G2G datasets, with updates to period and configuration.

## Acknowledgements and references
- Funded by the Natural Environment Research Council under the UK-SCAPE programme (award NE/R016429/1).
- Acknowledges advice from named contributors.
- Key references include Bell et al. (2009, 2016, 2018), Rudd et al. (2017), Formetta et al. (2018), Davies & Bell (2009), Hough & Jones (1997), Met Office HadUK-Grid (2019).