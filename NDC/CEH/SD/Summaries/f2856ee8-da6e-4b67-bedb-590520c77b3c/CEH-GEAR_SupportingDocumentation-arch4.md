# CEH - Gridded Estimates of Areal Rainfall (CEH - GEAR)

- 1-km gridded estimates of daily and monthly rainfall for Great Britain (GB) and Northern Ireland (NI), plus ~3000 km2 catchment in the Republic of Ireland (ROI), from 1890 onwards.
- Initially covered 1890–2012; extended annually as new raingauge data become available.
- Rainfall estimates derived from the Met Office observed precipitation database; daily and monthly totals used to generate grids.
- Daily estimates refer to rainfall accumulated over 24 hours from 09:00 on a day to 09:00 GMT the next day.

## Data scope and coverage

- Geographic coverage: GB, NI, and ROI catchment area (~3000 km2); grids produced for daily and monthly scales.
- Temporal scope: from 1890 to present, with annual updates as new data arrive.
- Data format: NetCDF4, organized in yearly files; separate files for GB and NI; daily and monthly grids stored separately.

## Data sources

- Met Office MIDAS: definitive UK national dataset of daily and monthly precipitation (licenced to CEH; kept in sync with CEH).
- SAAR (Spatially Averaged Annual Rainfall) grids: 1961–1990 period for GB (61-90) and NI (Ireland SAAR) used for normalisation.
- Data compiled and quality-controlled to ensure realistic extremes.

## Methodology

- Interpolation: natural neighbour interpolation with normalisation by SAAR (no varying scale factor due to limited improvement).
- Daily grids:
  - Stage 1: provisional daily grids via natural neighbour interpolation using all available raingauges.
  - Stage 2: adjust provisional daily grids with a monthly correction factor so sums match the monthly grids.
- Monthly grids:
  - Use monthly raingauge data; for months with complete daily data, daily totals are summed to form a monthly reading; if a daily gauge shares coordinates with a monthly gauge, the monthly value is used to avoid compounding errors.
- Minimum distance / data coverage:
  - Distance to the closest gauge recorded; a 100 km threshold means grids beyond this distance are not calculated to avoid low representativeness.
  - Ancillary gap grids produced to show first/last missing year and total missing days per grid point (separate sets for daily and monthly data).

## Data quality control

- QC aims to identify and reject unrealistically high daily rainfall values using a 200-year return period reference rainfall (from the Flood Estimation Handbook).
- Four-step QC applied to each gauge:
  1) Flag days where reference rainfall is exceeded.
  2) Cross-check flagged days against major UK events database; genuine events retained.
  3) Visual assessment using day-specific rainfall maps to identify implausible patterns.
  4) Time-series comparison with up to 10 nearest gauges to detect inconsistencies; multiday accumulation issues or instrumental/logging problems lead to rejection.
- Outcomes:
  - Multiday accumulations rejected; inconsistent neighboring data lead to rejection of the affected periods.
  - Some extreme values removed; remaining data accepted if consistent and credible.

## Data structure and format

- Core data: rainfall amount and minimum distance (distance to nearest contributing gauge).
- Ancillary gap data: three grids for monthly data and three grids for daily data:
  - Year of first missing data per grid point.
  - Year of last missing data per grid point.
  - Total number of missing days per grid point for the entire period.
- File structure:
  - Yearly NetCDF4 files; GB and NI stored separately.
  - Separate NetCDF4 files for daily and monthly data.
  - Separate missing-records files and the three ancillary grids for both daily and monthly datasets.

## Updates, governance, and data management

- Data provenance:
  - Derived from official Met Office observations under licence; ongoing synchronization with Met Office MIDAS dataset.
  - Dataset adheres to CEH conventions for gridded data.
- Updates:
  - Expansion beyond 2012 is ongoing with annual incorporation of new raingauge data.
- User support and discoverability:
  - Ancillary gap information aids modelling and understanding of data coverage.
  - NetCDF4 format supports discoverability, interoperability, and reusability in hydrological and climate analyses.

## Applications and relevance for data leaders

- Provides a coherent, well-documented, annually updated rainfall product suitable for hydrological modelling, water resource planning, and policy analysis.
- Emphasizes data quality assurance, provenance, and clear metadata on data gaps and coverage, aligning with governance practices for reliable data products.
- Demonstrates end-to-end data system considerations: source licensing, standardisation, interpolation methods, data validation, and transparent gap reporting.