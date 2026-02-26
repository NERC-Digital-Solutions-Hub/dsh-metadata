# CEH - Gridded Estimates of Areal Rainfall (CEH - GEAR)

## Brief Description
- 1-km gridded estimates of daily and monthly rainfall for Great Britain (GB) and Northern Ireland (NI) plus ~3000 km2 in the Republic of Ireland, from 1890 onwards; extendable annually as new raingauge data become available.
- Derived from the Met Office national precipitation observations; daily/monthly totals produced from UK raingauge network; natural neighbour interpolation with normalization by average annual rainfall (SAAR).
- Rainfall day refers to 24-hour period 09:00 day to 09:00 next day.
- Developed under guidance of CEH standards (BS7843-4:2012); detailed methodology documented in Keller et al. (2014).

## Data Sources
- Met Office MIDAS: definitive UK national daily and monthly rainfall dataset, provided to CEH under licence; CEH maintains a synchronized copy in Oracle with ongoing QC.
- SAAR grids: 1961-1990 1-km rainfall averages for GB (Spackman, 1993) and NI (Walsh, 2012).
- QC procedures applied to discard unrealistic extremes.

## Method for Deriving Daily and Monthly Grids
- Interpolation: natural neighbour interpolation using all available raingauges; SAAR-normalised scale factor used for normalization (no SAAR varying scale factor due to marginal improvements).
- Daily grids: two-stage approach
  1) provisional daily grids from daily network interpolation.
  2) adjustment with a monthly correction factor so daily sums match the monthly grids (monthly data integrated to daily estimates).
- Monthly grids: derived from monthly raingauge network and complete-dataset daily gauges; if a daily gauge shares coordinates with a monthly gauge, the monthly gauge is used to minimize accumulation errors.
- Output units: rainfall depth in millimetres (mm).

## Minimum Distance Grids
- Recorded distance to the closest gauge per grid point; a 100 km threshold applied to avoid unreliable estimates.
- For early (pre-1961) grids with sparse networks, gaps are common (Scotland, Wales, SW England).
- Ancillary grids (updated yearly): for monthly and daily data
  - Year of first missing data per grid point
  - Year of last missing data per grid point
  - Total number of missing days per grid point

## Quality Control
- Purpose: identify and reject unrealistically high daily rainfall values.
- 4-step QC (per gauge):
  1) Flag days where reference 1-day rainfall (200-year return) is exceeded.
  2) Cross-check flagged events against major UK rainfall events database; if matched, considered genuine.
  3) Visual assessment using day-specific rainfall maps (post-1961 GB) to judge plausibility.
  4) Time-series comparison with up to 10 nearest gauges (within 10 km) using Time-Series Plotter; if data appear inconsistent (e.g., multi-day accumulations, irregular reporting), reject.
- Outcomes:
  - Reject multiday accumulation data and identify periods of inconsistency; remove affected data from rainfall database.
  - If neighboring gauges show much lower values (<20%), or obviously implausible values (e.g., 469 mm, 999.9 mm), reject.
  - Accepted data may include gauges with no nearby comparisons if records are consistent.
- Note: flagged multiday accumulations and inconsistent periods are excluded from grid generation.

## Format and Data Access
- Format: NetCDF4, following CEH gridded dataset conventions.
- Structure: yearly files; GB and NI data stored separately; daily and monthly data stored in distinct files for each locale.
- Core variables: rainfall amount and minimum distance to the gauge used.
- Ancillary datasets: yearly missing data records (NetCDF4) plus three ancillary grids (monthly and daily) detailing missing data timelines and totals.
- Documentation and provenance are embedded via references and adherence to standard CEH conventions.

## References
- Foundational methodologies and datasets from CEH and collaborating institutions, including Met Office data sources and SAAR models, with supporting literature on rainfall estimation, data consolidation, and quality control practices.