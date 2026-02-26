# CEH - Gridded Estimates of Areal Rainfall (CEH - GEAR)

## Overview
- 1-km gridded estimates of daily and monthly rainfall for Great Britain (GB) and Northern Ireland (NI), plus ~3000 km2 of catchment in the Republic of Ireland.
- Time span from 1890 onwards; initial coverage 1890–2012 with annual extensions as new raingauge data become available.
- Derived from the UK Met Office observed precipitation database; monthly estimates use monthly and complete-day daily data; daily estimates are for the 24-hour period 09:00 on day to 09:00 GMT next day.
- Developed in line with British Standards BS7843-4:2012; detailed methodology described in Keller et al. (2014).

## Data sources and provenance
- Primary data: Met Office MIDAS national dataset (daily and monthly totals) with licensing to CEH; CEH keeps a synchronized copy in its Oracle database.
- Quality control: systematic QC to discard unrealistic extremes.
- Ancillary source grids:
  - Met Office SAAR 61-90 1-km grid for GB (Spackman, 1993).
  - Met Eireann 1961-90 1-km SAAR grid for NI (Walsh, 2012).

## Data collection and processing (methods)
- Interpolation: natural neighbour interpolation with normalization by SAAR; no variable scale factor.
- Daily grids:
  - Stage 1: provisional daily grids via natural neighbour interpolation using all available daily gauges.
  - Stage 2: adjust provisional daily grids with a monthly correction factor so the daily totals match the monthly grids.
- Monthly grids:
  - Generated from monthly raingauge network; if a daily gauge and monthly gauge share coordinates, the monthly gauge is used to avoid double-counting error.
- Minimum distance grids:
  - Record distance to the closest gauge; threshold of 100 km; grids not produced beyond this threshold due to representativeness concerns.
  - Pre-1961 density issues cause more gaps; ancillary grids provide gap timing and extent per grid point:
    - Year of first missing data
    - Year of last missing data
    - Total number of missing days
- File structure:
  - Data stored in NetCDF4 format, yearly files; GB and NI in separate files; daily and monthly grids stored separately.
  - Core variables: rainfall amount and minimum distance to the closest gauge.
  - Includes yearly missing-records files and three ancillary grids (monthly and daily) as above.

## Data quality control and validation
- Primary QC aims to identify and reject unrealistically high values using a 200-year return period reference rainfall model (Flood Estimation Handbook).
- Four-step QC for all gauges:
  1. Identify days where observed rainfall exceeds reference rainfall.
  2. Cross-check against a database of major UK rainfall events; if matched, consider genuine.
  3. Visual inspection with daily rainfall maps (post-1961 GB) to assess plausibility.
  4. Time-series comparison with up to ten nearest gauges (practically three near Gauges due to time), and then up to seven more if needed; assess multi-day accumulation issues and data recording irregularities.
- Rejection criteria during QC:
  - Multiday accumulation issues (e.g., gauges recording at fixed intervals) can cause false high values; such cases rejected.
  - Substantial discrepancies (<20% of nearby gauge) within 10 km lead to rejection.
  - Extreme single values (e.g., 469 mm, 999.9 mm) rejected.
  - Data within inconsistent periods or with incorrect flags removed from the rainfall dataset.
- Outcome: remaining selected ORVs (observed rainfall values) are accepted if they pass QC; otherwise removed from the dataset.

## Data format and accessibility
- NetCDF4 format, CEH Gridded Dataset Conventions.
- Yearly files with GB and NI data separated; daily and monthly grids stored separately within each file.
- Ancillary and missing-data grids accompany core data to inform users about data coverage and gaps.
- Dataset maintained with regular updates as new raingauge data become available; licensing and data sharing facilitated through CEH and Met Office collaboration.

## Governance, usability, and challenges for data stewards
- Licensing and provenance: data held and synchronized with Met Office MIDAS under licence; CEH ensures traceability to primary sources and maintains QC procedures.
- Metadata and discoverability: comprehensive documentation of data sources, processing steps, QC, and gap information; ancillary grids provide transparency on data completeness.
- Standards and interoperability: alignment with BS7843-4:2012; NetCDF4 format ensures interoperability with common hydrological modelling tools.
- Updates and reprocessing: annual extension with new years; maintained record of missing data extents to aid modelers in understanding spatial/temporal coverage.
- Key challenges reflected in dataset design:
  - Incomplete user needs and priorities addressed via explicit QA steps and detailed metadata.
  - Timely data acquisition challenges, especially for early periods with sparse networks (pre-1961).
  - Variability in data sources and formats addressed by standardized processing and normalization.
  - Handling of large observational networks and long time series with careful QC to avoid propagation of erroneous values.
  - Managing legacy data gaps and ensuring users are informed about spatial-temporal coverage through ancillary grids.