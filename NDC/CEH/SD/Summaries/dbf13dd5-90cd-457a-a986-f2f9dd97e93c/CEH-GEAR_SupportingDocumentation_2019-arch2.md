# CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use

## Overview
- 1-km gridded rainfall estimates for Great Britain (GB), Northern Ireland (NI), and approximately 3,000 km2 of catchment in the Republic of Ireland (ROI) from 1890 onwards.
- Daily and monthly rainfall, updated annually as new raingauge data become available.
- Rainfall estimates refer to 24-hour periods from 09:00 on day t to 09:00 GTM on day t+1.
- Developed using Met Office observed precipitation data and follows British Standards BS7843-4:2012 guidance.

## Data sources
- Met Office MIDAS database: daily and monthly totals; licensed to CEH; QC applied to remove unrealistic extremes.
- Met Office SAAR 61-90 grid for GB; Met Eireann SAAR 61-90 grid for NI.

## Methodology
- Interpolation: natural neighbour interpolation with normalization by SAAR (no scale-factor variation due to limited improvement).
- Daily grids: two-stage process
  1) provisional daily grids via natural neighbour interpolation using all available gauges.
  2) adjust provisional daily grids with a monthly correction factor so daily totals align with monthly grids.
- Monthly grids: generated from monthly raingauge network and daily gauges with a complete-month dataset; if a daily gauge coincides with a monthly gauge, the monthly value is used in interpolation to reduce accumulating error.
- Minimum distance grid: records the distance to the closest gauge used; 100 km threshold to ensure representativeness; pre-1961 networks sparser, leading to more missing values in early grids.

## Daily and monthly generation details
- Daily: interpolated grid, then corrected to ensure consistency with monthly totals.
- Monthly: sum of daily values where appropriate, or for months with complete daily data used as monthly gauges for interpolation.
- Outputs are rainfall depth in mm.

## Minimum distance grids and data gaps
- Minimum distance to nearest gauge is recorded; grids not calculated if the minimum distance exceeds 100 km.
- Ancillary grids (for both daily and monthly data) provide:
  - Year of the first missing data point for each grid cell.
  - Year of the last missing data point for each grid cell.
  - Total number of missing days per grid cell for the whole period.

## Quality control (QC)
- A four-step QC targets high rainfall values using a 200-year return period reference rainfall (from the Flood Estimation Handbook model).
- Steps:
  1) Identify days/gauges where reference rainfall is exceeded.
  2) Cross-check remaining cases against major UK rainfall events database; if matched, considered genuine.
  3) Use daily rainfall maps (post-1961 GB) for visual plausibility; genuine if patterns are sensible.
  4) For unresolved cases, compare time series across up to ten nearby gauges (prioritizing the closest); identify multiday accumulations, inconsistent reporting, or flagging issues; reject multiday accumulation cases or data with inconsistent near neighbors.
- Outcomes:
  - Rejection of multiday accumulations and data with inconsistent neighboring data.
  - Rejection of some extreme values (e.g., 469 mm, 999.9 mm).
  - Accepted remaining ORVs (including some with no nearby gauges but with consistent daily records).

## Format and structure of the CEH-GEAR dataset
- Stored in NetCDF4 following CEH gridded dataset conventions.
- Yearly files; GB and NI data stored separately, with separate daily and monthly grids within each file.
- Core variables: rainfall amount (mm) and minimum distance (m) to the closest gauge.
- Missing data metadata: yearly missing records files (NetCDF4) detailing spatial and temporal extent of missing data.
- Ancillary grids (monthly and daily sets):
  - Year of first missing data per grid point.
  - Year of last missing data per grid point.
  - Total number of missing days per grid point for the entire period.

## Practical notes for analysts
- Dataset extends from 1890 onwards; initial coverage 1890–2012 with annual extensions.
- Gridded rainfall estimates derived from national precipitation records with QA/QC to ensure reliability for hydrological analysis.
- Useful for assessing environmental health and policy performance over time, with explicit indicators of data coverage and quality gaps.