# CEH - Gridded Estimates of Areal Rainfall (CEH - GEAR)

- A 1-km gridded dataset of daily and monthly rainfall estimates for Great Britain (GB) and Northern Ireland (NI), plus ~3,000 km2 of catchment in the Republic of Ireland, covering from 1890 onwards and extended annually as new raingauge data become available.
- Rainfall estimates are derived from the Met Office national precipitation database, produced under licence, with QA and synchronization between CEH and Met Office.

## Data sources

- Met Office MIDAS: definitive UK national daily and monthly rainfall totals; CEH maintains an in-house copy in an Oracle database and keeps it in sync with Met Office data; a systematic QC discards unrealistic extremes.
- Met Office SAAR 61-90: 1-km grid of average annual rainfall for GB (Spackman, 1993).
- Met Eireann SAAR 61-90: 1-km grid for Northern Ireland (Walsh, 2012).

## Method for deriving daily and monthly grids

- Interpolation: natural neighbour interpolation with normalisation by SAAR (no varying scale factor to reduce complexity).
- Monthly grids:
  - Use monthly raingauges and daily gauges that have complete monthly data; daily values summed to monthly totals where appropriate.
  - If a daily gauge coincides with a monthly gauge, only the monthly value is used to avoid error from accumulating daily measurements.
- Daily grids (two-stage process):
  1) Apply natural neighbour interpolation to daily raingauges to produce provisional grids.
  2) Normalize with a monthly correction factor so the sum of daily grids matches the monthly grids, incorporating information from monthly data in remote locations.
- Units: rainfall depth in millimetres (mm).

## Minimum distance grids and gap information

- Minimum distance to the nearest gauge: 100 km threshold; grids are not produced beyond this distance to avoid unrepresentative estimates.
- Ancillary grids (monthly and daily sets, updated yearly):
  - Year of first missing data per grid point
  - Year of last missing data per grid point
  - Total number of missing days per grid point for the whole period

## Quality control (QC) and data validation

- 4-step QC against high rainfall values using a 200-year reference rainfall (from the 1-day rainfall-depth model linked to the Flood Estimation Handbook).
- Steps include:
  - Flagging days/gauges exceeding reference rainfall
  - Cross-checks with major UK rainfall events databases
  - Visual assessment with daily rainfall maps (post-1961 GB) to identify realistic patterns
  - Time-series comparison with up to the 10 nearest gauges (prioritizing 3, then up to 7 more if needed)
- Decisions on ORVs (observed rainfall values) consider:
  - Multi-day accumulations (often due to non-daily measurements) are rejected
  - Large discrepancies (<20% of neighboring gauges within 10 km) can lead to rejection
  - Extreme single values (e.g., 469 mm, 999.9 mm) are rejected
- All data determined non-suitable during inconsistent periods are excluded from the rainfall database used for grid construction.

## Data format and structure

- Storage: NetCDF4 format following CEH gridded dataset conventions.
- Organization: yearly files; GB and NI stored separately; daily and monthly grids stored in distinct files for each region.
- Core variables: rainfall amount and minimum distance to gauge.
- Ancillary data: yearly missing records files (NetCDF4) plus the three ancillary grids (monthly and daily) documenting data gaps.

## Practical governance and reuse considerations for Data Stewards

- Provenance and licensing: data rely on Met Office MIDAS; CEH maintains synchronized copies under licence; clear attribution and licensing implications.
- Standards and interoperability: NetCDF4 format and CEH conventions enable discoverability and interoperability with hydrological models and APIs.
- Update and maintenance: dataset extended annually with new raingauge data, ensuring longitudinal continuity.
- Metadata and discoverability: gap and distance grids help assess data completeness and model applicability; detailed QC process provides traceability for data quality.
- Limitations and caveats: 100 km representativeness constraint; pre-1961 data sparser, leading to geographical gaps; some periods or regions may have missing data affecting certain analyses.
- Usage implications: suitable for hydrological modeling and regional rainfall estimation, with explicit documentation of data gaps, QC procedures, and interpolation assumptions to support responsible data governance and reuse.