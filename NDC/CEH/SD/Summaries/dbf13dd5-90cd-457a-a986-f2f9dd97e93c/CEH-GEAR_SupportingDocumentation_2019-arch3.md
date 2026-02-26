# CEH - Gridded Estimates of Areal Rainfall (CEH - GEAR)

## Overview
- Provides 1-km gridded estimates of daily and monthly rainfall for Great Britain (GB) and Northern Ireland (NI), plus ~3000 km2 of catchment in the Republic of Ireland, from 1890 onwards with annual updates.
- Rainfall estimates are derived from the Met Office observed precipitation database; daily and monthly grids are produced using rain gauge data and a natural neighbour interpolation with SAAR-based normalisation.
- Aims to support hydrological monitoring and policy evaluation by offering high-resolution rainfall inputs with transparent methods and quality controls.

## Data Coverage and Sources
- Coverage: GB, NI, and a defined ROI catchment, with data extending from 1890 and extended annually as new data become available.
- Primary data sources:
  - Met Office MIDAS daily and monthly rainfall totals (licensed to CEH; CEH keeps a synchronized copy).
  - SAAR 61-90 average annual rainfall grids for GB and NI.
  - Met Éireann SAAR grid for NI.
- Quality control (QC) is applied to discard unrealistic extremes prior to interpolation.

## Methodology
- Interpolation: natural neighbour interpolation with normalisation by SAAR; no extra scale factor for normalisation due to marginal improvements.
- Daily grids:
  - Step 1: provisional daily grids via natural neighbour interpolation using all available daily gauges.
  - Step 2: adjust provisional daily grids with a monthly correction factor to ensure daily sums align with monthly grids.
- Monthly grids:
  - Generated from monthly gauges and daily gauges with complete daily data for the month; when a daily gauge shares coordinates with a monthly gauge, the monthly value is used to avoid redundant accumulation errors.
- Minimum distance concept: distance to the closest gauge is recorded; a 100 km threshold is applied, below which grids are produced; above which grids are not trusted and gaps may occur, especially in early periods (pre-1961).

## Minimum Distance Grids and Ancillary Data
- Minimum distance grids: provide distance (in meters) from each grid point to the nearest gauge used.
- Ancillary grids (updated yearly) to characterize data gaps:
  - Year of first missing data for each grid point.
  - Year of last missing data for each grid point.
  - Total number of missing days per grid point for the entire period.
- Separate sets are maintained for monthly data and daily data to aid modelers needing full spatial/temporal coverage.

## Quality Control (QC)
- A 4-step QC protocol identifies and rejects excessively high rainfall readings:
  1) Identify days/gauges exceeding the 200-year return rainfall threshold.
  2) Cross-check remaining high values against major UK rainfall events database.
  3) Visual assessment using daily rainfall maps (post-1961 GB) to judge plausibility.
  4) Time-series comparisons using nearby gauges and manual checks (e.g., Time-Series Plotter); multiday accumulations and data flags issues may indicate unreliable data.
- Rejection criteria include multiday accumulation readings, inconsistent or missing neighbour corroboration, and extreme totals (e.g., 469 mm, 999.9 mm).
- Data associated with identified multiday accumulation periods are excluded from the rainfall grids.

## Data Format and Access
- Storage format: NetCDF4, following CEH gridded dataset conventions.
- Structure: yearly files; GB and NI data stored separately; daily and monthly grids stored in distinct files.
- Core variables: rainfall amount and minimum distance to the nearest gauge.
- Ancillary missing-data files accompany core data, detailing the extent and timing of gaps.

## Practical Implications for Monitoring Frameworks
- Delivers high-resolution rainfall inputs suitable for hydrological modelling, flood risk assessment, and environmental health monitoring.
- Transparent workflow from data sources through QA, interpolation, and gap reporting supports auditability and governance.
- The explicit handling of data gaps and quality flags helps identify where data limitations may influence policy evaluation or monitoring outcomes.
- Encourages data provenance and governance by documenting data sources, correction steps, and QC processes.