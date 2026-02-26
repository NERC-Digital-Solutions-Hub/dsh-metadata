# Supporting information for Grid-to-Grid model estimates of river flow for Great Britain driven by observed data (1980 to 2011)

## Overview
- UK-SCAPE project (UK Status, Change And Projections of the Environment) provides Grid-to-Grid (G2G) hydrological model estimates of river flow for Britain at 1 km x 1 km resolution, driven by observed meteorological data (1980–2011).
- Outputs include monthly mean river flow, annual maxima of daily mean river flow, and annual minima of 7-day mean river flow for non-tidal river cells with catchment area ≥ 50 km².
- A complementary dataset exists for G2G river flows driven by UKCP18 Regional (12 km) climate projections.

## The Grid-to-Grid (G2G) model
- National-scale hydrological model operating on a 1 km x 1 km grid with a 15-minute time-step.
- Produces spatially consistent natural river flows for gauged and ungauged rivers across Great Britain.
- Uses fixed, nationally applicable parameters (no catchment-specific calibration) and accounts for urban/suburban land-cover effects on runoff.
- Performs best in catchments with natural flow regimes and accurate flow records; less accurate where artificial abstractions/discharges or complex sub-surface hydrology dominate.
- Requires input time-series of precipitation, potential evapotranspiration (PE), and daily min/max temperature (for optional snow module).

## Input data and driving datasets
- Meteorological inputs:
  - Daily 1 km precipitation (CEH-GEAR).
  - Monthly 40 km PE for short grass (MORECS).
  - Daily 1 km min/max temperature (Met Office).
- Temporal and spatial processing:
  - Precipitation distributed evenly within each daily step; PE distributed within each monthly step; temperature downscaled with a sine curve.
  - Baseline topography and soil data align with Bell et al. (2009).

## Output datasets included
- 1 km x 1 km gridded outputs in NetCDF4:
  - Monthly mean river flow (m³ s⁻¹): G2G_GB_mmflow_obs_1980_2011.nc (Dec 1980–Nov 2011).
  - Annual maxima of daily mean river flow (m³ s⁻¹): G2G_GB_amaxflow_obs_1980_2011.nc (Oct 1981–Sep 2011).
  - Annual minima of 7-day mean river flow (m³ s⁻¹): G2G_GB_aminflow_obs_1980_2011.nc (Dec 1980–Nov 2011).
- Domain:
  - 700 km × 1000 km spatial extent on the GB National Grid (0–700000 m, 0–1000000 m).
  - Outputs provided only for non-tidal river cells with catchment area ≥ 50 km²; others set to -9999.

## Supporting spatial datasets
- Digitally-derived catchment areas (km²) draining to each 1 km x 1 km grid cell: UKSCAPE_G2G_GB_CatchmentAreaGrid.nc.
- Estimated locations of river flow gauging stations on the 1 km grid (NRFA-compatible): UKSCAPE_G2G_GB_NRFAStationIDGrid.nc, plus station information in NRFA station CSV (NRFAStationIDs.csv). Includes 1038 gauging stations; some additional stations are included in the CSV.

## Complementary datasets and comparisons
- Compared with flows driven by UKCP18 Regional (12 km) climate projections (see related dataset references).
- Annotations note that the 1 km G2G outputs may differ slightly from MaRIUS-G2G-MORECS monthly data due to shorter period, land-sea mask updates, and minor network discretisations.

## Data format and access details
- NetCDF4 files following CEH conventions; time stamps are days since 1900-01-01; monthly flows anchored to the first day of the month.
- Spatial cells represent the centre of each 1 km × 1 km grid box; values are missing (-9999) outside designated catchments.
- Specific notes on catchment-area representation: derived catchment areas on 1 km grid may not exactly match observed NRFA catchments, especially for small catchments.

## Using the datasets
- Use G2G outputs to compare with observed river flows (e.g., NRFA) for validation and to explore climate-change scenarios when combined with UKCP18 projections.
- The monthly dataset updates prior MaRIUS-G2G-MORECS monthly data; users should account for minor differences in period length, land-sea mask, and network discretisation.
- The NRFA station grid enables direct juxtaposition of modeled flows with observed station data at approximately corresponding river locations.

## Model limitations and caveats
- Calibration is not performed at the catchment level; parameters are nationally uniform.
- Model performance declines in heavily anthropogenically influenced systems or where subsurface hydrology is unusually complex.
- Spatial discretisation can introduce mismatches between the modeled catchment drainage area and the observed NRFA catchment, particularly for smaller basins.

## Acknowledgements and references
- Funded by the Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCAPE National Capability.
- Acknowledgements to colleagues for guidance.
- Key references addressing model methods and datasets:
  - Bell et al. (2009, 2016, 2018)
  - Davies & Bell (2009)
  - Formetta et al. (2018)
  - Hough & Jones (1997)
  - Met Office (HadUK-Grid) (2019)
  - Rudd et al. (2017)
  - Tanguy et al. (2016)