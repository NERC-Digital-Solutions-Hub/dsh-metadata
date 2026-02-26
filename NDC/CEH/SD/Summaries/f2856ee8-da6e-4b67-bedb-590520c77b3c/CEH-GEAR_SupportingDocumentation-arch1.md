# CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use

- Purpose: 1-km gridded estimates of daily and monthly rainfall for Great Britain, Northern Ireland, and approximately 3000 km2 of catchment in the Republic of Ireland, from 1890 onwards; extended annually as new raingauge data become available.
- Data provenance: Derived from the Met Office national precipitation database; QA/QC applied; dataset developed under British Standards BS7843-4:2012 guidance.
- Temporal scope: Initial coverage 1890–2012 with annual updates; daily grids use a 24-hour window (09:00 on day to 09:00 the next day).

## Data sources

- Met Office MIDAS: daily and monthly rainfall totals; UK national dataset supplied to CEH under licence; CEH maintains a synchronized copy.
- Quality control: systematic discarding of unrealistic extremes.
- Ancillary SAAR grids: Met Office 1961–1990 average annual rainfall (GB) and Met Éireann 1961–1990 SAAR (NI).

## Method for deriving daily and monthly grids

- Interpolation: natural neighbour interpolation with SAAR normalisation (no scale-factor variation due to limited improvement).
- Daily grids:
  - Stage 1: provisional grids via natural neighbour interpolation using all available daily raingauges.
  - Stage 2: adjust provisional daily grids with a monthly correction factor so that the sum across the day matches the monthly grid.
- Monthly grids:
  - Use monthly raingauge network and daily gauges with a complete monthly dataset; when a daily gauge shares coordinates with a monthly gauge, the monthly value is used.
- Output units: rainfall depth in millimetres (mm).

## Minimum distance grids and gap information

- Minimum distance: distance to the closest gauge used for each grid point; 100 km threshold applied (values beyond are not calculated) to preserve representativeness.
- Gaps: early periods (pre-1961) have sparser networks and more gaps, especially in Scotland, Wales, and SW England.
- Ancillary gap grids (updated yearly for both monthly and daily data):
  - Year of first missing data per grid point
  - Year of last missing data per grid point
  - Total number of days with missing data per grid point

## Quality control

- Objective: identify and reject erroneously high daily rainfall values using a 200-year rainfall reference (from the Flood Estimation Handbook).
- Four-step QC:
  1) Flag all days/gauges where the reference rainfall is exceeded.
  2) Cross-check flagged values against major UK rainfall events database; if matched, kept as genuine.
  3) Visual assessment using daily rainfall maps (post-1961 GB maps) to judge plausibility (reject unusual patterns like bull’s eyes).
  4) Time-series comparison with up to ten nearest gauges (practically three initially); resolve data issues (multiday accumulations, inconsistent sampling, or flag errors). If discrepancies persist, extend checks to up to seven nearby gauges.
- Rejection criteria within step 4:
  - Multiday accumulation records (e.g., measurements taken at fixed intervals) discarded
  - Neighbouring gauges report much lower rainfall (<20% of the ORV) within 10 km
  - Extreme values (e.g., 469 mm, 999.9 mm) rejected
- Outcome: only consistent daily records are retained; data during inconsistent periods removed from the rainfall database.

## Format and structure of the CEH-GEAR dataset

- File format: NetCDF4, CEH gridded dataset conventions.
- Organization: yearly files; separate files for Great Britain and Northern Ireland; daily and monthly grids stored separately.
- Core variables: rainfall amount and minimum distance (distance to closest gauge).
- Ancillary files: missing-record grids (NetCDF4) plus three ancillary grid sets (monthly and daily):
  - Year of first missing data
  - Year of last missing data
  - Total number of missing days
- Accessibility: designed to be discoverable and usable with metadata; supports modelers requiring full spatial-temporal coverage.

## References

- Includes sources for data consolidation, SAAR grids, QC methods, and rainfall-depth-frequency modeling used in the quality assessment.