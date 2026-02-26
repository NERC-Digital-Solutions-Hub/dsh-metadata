# CEH - Gridded Estimates of hourly Areal Rainfall - version 2 (CEH-GEAR1hr.v2)

## Overview
- Updated 1-km gridded hourly rainfall dataset for Great Britain (GB) from 1990 onward; current coverage 1990-2016 with ongoing extension.
- Increased raingauge coverage in this version (2,606 gauges) compared with v1 (1,903 gauges).
- Hourly estimates derived by disaggregating CEH-GEAR daily totals using hourly gauge data; relies on daily CEH-GEAR totals to preserve those values.

## Data Content and Structure
- Format: NetCDF4, CEH-GEAR-1hr.v2 files organized monthly (e.g., CEH-GEAR-1hr.v2_199001 for January 1990).
- Variables per file:
  - Rainfall_amount: hourly rainfall in kg/m^2 (equivalent to mm).
  - Stat_disag: flag (1/0) indicating whether statistical disaggregation was used for that day.
  - Min_dist: minimum distance to the closest hourly gauge used for that grid point (meters).
- Global attributes:
  - time_coverage_resolution: P1H (hourly).
  - time_coverage_duration: P27Y (27 years).
- Output grid: 1 km resolution across GB with hourly timesteps starting at 9:00 when statistical disaggregation is applied.

## Data Sources and Coverage
- Gauge data (hourly) from 2,606 gauges across:
  - Met Office MIDAS (382 gauges)
  - England Environment Agency (EA) WISKI archive (≈1,622 gauges)
  - Natural Resources Wales (NRW) WISKI archive (257 gauges)
  - Scottish Environment Protection Agency (SEPA) WISKI archive (345 gauges)
- CEH-GEAR daily dataset used for daily totals and baseline grids.
- Quality control (QC) applied to hourly gauge data to discard erroneous values (see QC section).

## Methodology
- Nearest-neighbour interpolation without height correction to preserve storm shape, onto a 1 km grid.
- For each day, only gauges with complete records are used; the number of gauges varies daily (430–1,771).
- Hourly values assigned as the nearest station’s hourly value scaled by the station’s daily total.
- If the nearest gauge is >50 km away or if rain is in the daily record but not in the hourly record, statistical disaggregation is used to distribute the daily total into hours using average storm shapes (Table 1).
- The daily totals from CEH-GEAR daily dataset are preserved in the hourly disaggregation process; the average storm shapes were derived from all available gauges (Lewis et al., 2018).

## Statistical Disaggregation and Minimum Distance
- Statistical disaggregation applied when:
  - A grid square is >50 km from any gauge, or
  - There is daily rainfall but no corresponding hourly rainfall.
- Table 1 shows average hourly rainfall shapes for different daily total ranges and seasons; disaggregation typically begins at 9:00.
- Minimum distance grids record the distance from each grid point to the closest gauge for that day; mean distance ~2.6 km, max ~100 km (west Scotland).
- Threshold: 50 km minimum distance threshold for calculating grids; if exceeded, statistical disaggregation is used.

## Quality Control and Data Quality
- QC process is three steps:
  1. Identify suspect gauges by comparing gauge data to the CEH-GEAR daily dataset.
  2. Apply automated QC flags (Table 2) to all data.
  3. Apply rule-base (Table 3) to determine which flagged values are erroneous and replace with missing data (-999).
- Only gauges with Spearman rank correlation r_s > 0.8 and P00 + P11 > 0.8 after QC are used to create the dataset.
- QC impact (time steps rejected) shown in Tables: significant reduction from v1 to v2 (improved data quality).

## Usage Guidance and Limitations
- Designed for hydrological modelling; appropriate use requires awareness of:
  - Diurnal cycle impact: statistical disaggregation imposes fixed diurnal shapes, potentially biasing hourly patterns.
  - Trend analysis: hourly totals are modulated by daily totals, which can affect detected hourly trends.
  - Spatial analysis: nearest-neighbour interpolation can produce blocky spatial patterns; no smoothing between gauges.
- Metadata and disaggregation indicators must be used to interpret results correctly (Stat_disag flags; Min_dist values).

## Access, Citation, and Format
- Data access: Environmental Information Data Centre (EIDC); data DOI provided.
- Citation required:
  - Lewis, E.; Quinn, N.; Blenkinsop, S.; et al. (2020). Gridded estimates of hourly areal rainfall for Great Britain - version 2 (CEH-GEAR1hr.v2). NERC Environmental Information Data Centre. https://doi.org/10.5285/fc9423d6-3d54-467f-bb2b-fc7357a3941f
  - Methodology details in Lewis et al. (2018) Journal of Hydrology.
- Data content and methodology summary also references Keller et al. (2015) and Tanguy et al. (2019).

## Acknowledgements and References
- Funding and support from SINATRA, CONVEX, INTENSE, and Hydro-JULES programmes (NERC/NERC-related funding).
- Gratitude expressed to hydrometric teams across Met Office, EA, NRW, SEPA for data provision and quality control.