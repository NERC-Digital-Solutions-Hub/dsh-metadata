# CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use

## Overview
- CEH-GEAR provides 1-km gridded daily and monthly rainfall estimates for Great Britain, Northern Ireland, and part of the Republic of Ireland from 1890 onwards.
- Daily estimates refer to a 24-hour period from 09:00 on day t to 09:00 GTM on day t+1; monthly estimates are derived from daily data and/or monthly gauges.
- The dataset is extended annually as new raingauge data become available and follows CEH conventions stored in NetCDF4 format.

## Data sources
- Met Office MIDAS: definitive UK national daily and monthly rainfall totals; quality-controlled and synchronized with CEH’s Oracle/Met Office data.
- Met Office SAAR 61-90 grid (Great Britain) and Met Eireann SAAR 61-90 grid (Northern Ireland) for normalisation.
- Ancillary data and references used for quality checks and context.

## Method for deriving daily and monthly grids
- Interpolation: natural neighbour interpolation with normalisation by SAAR (no scale-factor variation due to limited improvement).
  - Daily rainfall at grid i, t is a weighted sum of surrounding gauges, normalised by S_j and scaled by S_i.
- Daily grids (two-stage process):
  1) Produce provisional daily grids from the daily raingauge network using natural neighbour interpolation.
  2) Adjust provisional daily grids with a monthly correction factor so that daily sums match the monthly grids, incorporating information from monthly gauges (especially in remote areas).
- Monthly grids:
  - Generated from the monthly raingauge network; for months with complete daily data, daily totals are summed to form the monthly value. If a daily gauge shares coordinates with a monthly gauge, the monthly gauge value is used to reduce accumulated error.
- Minimum distance principle:
  - A 100 km minimum distance threshold is applied; grids are not produced if the closest gauge exceeds 100 km. This is to maintain representativeness, especially for earlier (pre-1961) data with sparser networks.
- Gap and coverage information:
  - Ancillary grids (monthly and daily) document year of first/last missing data and total days missing per grid point.

## Quality control
- Purpose: identify and reject unrealistically high daily rainfall values using a 200-year return-period reference rainfall from the Flood Estimation Handbook model.
- Four-step QC procedure:
  1) Flag days where reference rainfall is exceeded.
  2) Cross-check identified events against major UK rainfall events database; known events are considered genuine.
  3) Use daily rainfall maps (post-1961 GB) to visually assess flagged events; genuine if rainfall pattern is plausible.
  4) For remaining cases, compare with time-series from up to ten nearby gauges (prioritizing three, then up to seven more if needed) using Time-Series Plotter; identify issues such as multiday accumulations or inconsistent recording frequency.
- Rejection criteria:
  - Multiday accumulations or inconsistent gauge data leading to unreliability are rejected.
  - Some extreme values are rejected (e.g., 469 mm, 999.9 mm).
  - If neighboring gauges show substantially lower rainfall, the event is rejected.
- Outcome: data flagged for multiday accumulation or with inconsistencies are removed from the rainfall database used for grid creation.

## Data format and structure
- Storage: NetCDF4 format following CEH gridded data conventions.
- Structure:
  - Yearly files separate GB and NI data.
  - Within each region, daily and monthly grids stored separately.
  - Core variables: rainfall amount and minimum distance to the nearest gauge used for estimation.
- Ancillary data:
  - Yearly missing-records files (NetCDF4) describing spatial/temporal extent of missing data.
  - Three ancillary grids (daily and monthly): first missing year, last missing year, total missing days per grid point for the entire period.

## Additional notes
- The dataset is designed for hydrological and modelling use, providing a quantified measure of data coverage and gaps through the minimum distance grids and ancillary missing-data grids.
- References and supporting literature underpin the QC methodology and interpolation approaches, ensuring traceability and methodological justification.