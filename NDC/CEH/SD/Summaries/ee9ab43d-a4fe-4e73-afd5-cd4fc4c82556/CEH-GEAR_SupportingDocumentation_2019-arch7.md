# CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use

## Overview
- A gridded rainfall dataset at 1-km resolution for Great Britain, Northern Ireland, and a ~3000 km2 catchment in the Republic of Ireland.
- Covers daily and monthly rainfall from 1890 onwards; extended annually as new data become available.
- Derived from Met Office raingauge observations; produced using natural neighbour interpolation with SAAR-based normalisation.
- Designed for hydrological and GIS applications, with quality control and transparency on data gaps.

## Data access and citation
- Data access: https://doi.org/10.5285/ee9ab43d-a4fe-4e73-afd5-cd4fc4c82556
- Required citation: Tanguy, M.; Dixon, H.; Prosdocimi, I.; Morris, D. G.; Keller, V. D. J. (2016). Gridded estimates of daily and monthly areal rainfall for the United Kingdom (1890-2015) [CEH-GEAR]. NERC Environmental Information Data Centre. https://doi.org/10.5285/ee9ab43d-a4fe-4e73-afd5-cd4fc4c82556
- Licensing: Full data licensing and reuse conditions at the provided DOI link.

## Data contents and format
- Core variables: rainfall amount (mm) and minimum distance to the gauge used for estimation.
- Data organization: yearly NetCDF4 files; separate files for Great Britain and Northern Ireland; separate daily and monthly grids.
- Ancillary data: yearly missing-record NetCDF4 files plus three ancillary grids (monthly and daily sets):
  - Year of first missing data per grid point
  - Year of last missing data per grid point
  - Total number of days with missing data per grid point
- All data are provided in NetCDF4 following CEH conventions.

## Spatial and temporal coverage
- Spatial: GB, NI, and ~3000 km2 catchment in ROI.
- Temporal: 1890–present (extension planned annually as new data arrive).
- Minimum distance flag: a threshold of 100 km used to decide whether a grid point estimate is considered reliable; grids with data beyond this threshold are not produced.

## Data sources and preprocessing
- Primary data: Met Office collated daily and monthly precipitation totals (MIDAS national dataset).
- Supporting SAAR grids: GB 1961–1990 SAAR; NI SAAR 1961–1990.
- Quality control: QC applied to daily rainfall inputs, including checks against a 200-year return-period rainfall model and cross-checks with major rainfall event databases and visual/time-series assessments.

## Methodology for grid construction
- Daily grids:
  - Stage 1: natural neighbour interpolation using all available daily gauges.
  - Stage 2: apply a monthly correction factor to align daily sums with monthly grids, ensuring consistency with monthly data and incorporating information from remote monthly gauges.
- Monthly grids:
  - Interpolated from monthly raingauge readings.
  - When a daily gauge shares coordinates with a monthly gauge, the monthly gauge is used for interpolation to minimize accumulation errors.
- Output: daily and monthly rainfall grids in millimeters.

## Minimum distance and data gaps
- Minimum distance grid indicates how far the nearest gauge is from each grid point (threshold: 100 km).
- Ancillary grids provide users with spatiotemporal extent of missing data, including first/last missing years and total missing days per point.
- Early periods (pre-1961) may have more gaps due to sparser networks, particularly in Scotland, Wales, and parts of southwest England.

## Quality control details
- Four-step QC to identify and reject unrealistically high daily rainfall values.
  - Step 1: flag potential high values using a 200-year reference rainfall.
  - Step 2: check matches against known major rainfall events.
  - Step 3: visual inspection using daily rainfall maps where available.
  - Step 4: time-series comparisons with up to ten nearby gauges; discard multiday accumulation data and inconsistent records.
- Multiday accumulation issues and data flags in source datasets can lead to rejection of certain records to preserve data quality.

## Practical notes for GIS users
- Data are at 1-km resolution with daily and monthly products; suitable for hydrological modeling, risk assessment, and map-based analyses.
- Daily grids are corrected to be consistent with monthly totals; the daily values reflect 24-hour rainfall from 09:00 day to 09:00 next day.
- Be mindful of data gaps, especially in pre-1961 periods; use the ancillary missing-data grids to assess reliability and coverage for each grid cell.
- Minimum distance information helps gauge the spatial representativeness of each grid estimate; consider excluding points beyond 100 km from gauges for certain analyses.
- Data licensing, citation requirements, and metadata are provided alongside the data.

## References (context)
- Key methodological and dataset references include CEH-GEAR development and supporting rainfall datasets, QA procedures, and interpolation strategies.