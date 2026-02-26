# CEH - Gridded Estimates of Areal Rainfall (CEH - GEAR)

## Overview
- 1-km gridded daily and monthly rainfall estimates for Great Britain (GB) and Northern Ireland (NI), plus ~3000 km2 catchment in the Republic of Ireland (ROI), starting from 1890.
- Initially covering 1890–2012; extended yearly as new raingauge data become available.
- Rainfall estimates derived from the Met Office national precipitation data; daily/monthly totals used to build grids.
- Interpolation via natural neighbour method with normalization by average annual rainfall (SAAR); day defined as 09:00 on day to 09:00 GTM on next day.
- Developed in accordance with British Standards BS7843-4:2012.

## Data Coverage and Timeframe
- Geographic coverage: GB, NI, and ROI catchment (~3000 km2).
- Temporal coverage: 1890 onward; daily and monthly grids available, with annual NetCDF4 files.

## Data Sources
- Met Office MIDAS national dataset of daily and monthly precipitation totals (definitive UK data).
- CEH maintains a synchronized copy in its ORACLE database; QC applied to remove unrealistic extremes.
- SAAR 61-90 rainfall grids used for normalization: GB (Spackman, 1993) and NI (Walsh, 2012).

## Methodology for Daily and Monthly Grids
- Interpolation: natural neighbour method with SAAR normalisation (no distance-varying scale factor).
- Monthly grids: built from monthly gauges and daily gauges with complete monthly data; if a daily gauge shares coordinates with a monthly gauge, the monthly value is used.
- Daily grids: two-stage process
  1) provisional daily grids via natural neighbour interpolation using daily gauges.
  2) adjust provisional daily grids with a monthly correction factor so the sum matches the monthly grids, incorporating information from monthly data in remote areas.

## Minimum Distance Grids and Gap Information
- Minimum distance to closest gauge threshold set at 100 km; grids not calculated where this threshold is exceeded (notably pre-1961 when network density was low).
- Ancillary grids (monthly and daily) to inform users about gaps:
  - Year of first missing data for each grid point.
  - Year of last missing data for each grid point.
  - Total number of missing days for each grid point for the whole period.
- These ancillary grids are updated yearly with each new dataset version.

## Quality Control Procedures
- 4-step QC to identify and validate exceptionally high rainfall values (200-year return period rainfall estimates used as reference).
  1) Identify days/gauges where reference rainfall is exceeded.
  2) Cross-check with UK major rainfall event database; if matched, ORV deemed genuine.
  3) Visual assessment using daily rainfall maps (post-1961GB) to judge plausibility.
  4) Time-series comparison using up to 10 nearest gauges; exclude multiday accumulations and inconsistent records; reject cases with neighboring gauges showing far lower values or obviously erroneous extremes (e.g., 469 mm, 999.9 mm).
- Multiday accumulation cases and inconsistent periods are rejected; data flagged as not suitable for use are removed from the rainfall database.

## Data Format and Structure
- Stored in NetCDF4 format following CEH gridded dataset conventions.
- Yearly files; GB and NI data stored separately; daily and monthly grids stored in separate files.
- Core variables: rainfall amount and minimum distance to gauge.
- Accompanied by missing-data files (NetCDF4) and three ancillary grids for missing data (first year, last year, total days missing) for both monthly and daily data.

## Use and Accessibility
- Designed for environmental monitoring and hydrological analysis; provides standardized, QA-filtered rainfall data across a long temporal span.
- Ancillary gap information aids modelling and gap-filling efforts; recognises limitations in early data due to sparser gauge networks.
- Data quality measures and documentation support rigorous scrutiny of environmental health and policy-related analyses, with potential for integration with other datasets to enhance monitoring value.