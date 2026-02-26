# CEH-GEAR1hr.v2: Gridded Estimates of hourly Areal Rainfall for Great Britain - version 2 (1990-2016)

## Data access and citation
- Data available from the Environmental Information Data Centre (EIDC): https://doi.org/10.5285/fc9423d6-3d54467f-bb2b-fc7357a3941f
- Please cite:
  - Lewis, E. et al. (2020). Gridded estimates of hourly areal rainfall for Great Britain - version 2 (1990-2016) [CEH-GEAR1hr.v2]. NERC EIDC. https://doi.org/10.5285/fc9423d6-3d54-467f-bb2b-fc7357a3941f
  - Methodology reference: Lewis et al. (2018). A rule based quality control method for hourly rainfall data and a 1 km resolution gridded hourly rainfall dataset for Great Britain: CEH-GEAR1hr. J. Hydrol. 564, 930-943. https://doi.org/10.1016/j.jhydrol.2018.07.034
- Data description and QC methodology are detailed in Lewis et al. (2018); dataset is designed for hydrological modeling and environmental monitoring.

## Brief dataset description
- 1-km gridded estimates of hourly rainfall for Great Britain (GB) derived from 1990 onward; current coverage 1990–2016, with ongoing extensions as new raingauge data arrive.
- Version 2 expands the gauge network to 2,606 gauges (vs 1,903 in the original) and extends temporal coverage; daily totals are preserved in the hourly disaggregation.
- Hourly estimates come from temporal disaggregation of the CEH-GEAR daily dataset using hourly gauge data; nearest-neighbour interpolation is used to create 1-km grids and to distribute daily totals into hourly values.
- Nearest gauge data are from the Met Office (MO MIDAS), England Environment Agency (EA), Natural Resources Wales (NRW), and Scottish Environment Protection Agency (SEPA). Daily CEH-GEAR data come from the Met Office national precipitation database.
- Data are provided with metadata indicating where statistical disaggregation was used and the minimum distance to gauges for each grid cell.

## Data sources
- 2,606 UK rain gauges used (subset per day selected for completeness):
  - Met Office MIDAS: 382 gauges
  - EA WISKI: 1,622 gauges
  - NRW WISKI: 257 gauges
  - SEPA WISKI: 345 gauges
- CEH-GEAR daily dataset (Keller et al. 2015; Tanguy et al. 2019)
- Quality control (QC) procedure applied to hourly gauge data (Lewis et al. 2018)

## Method for deriving the hourly grids
- For each day, select a subset of hourly gauges with complete records.
- For each hour, interpolate onto a 1-km grid using nearest-neighbour interpolation, assigning each grid cell the nearest station hourly rainfall as a fraction of that station’s daily total.
- If the nearest station is >50 km away, or if daily rainfall exists but the nearest hourly gauge shows no rainfall, the station value is not used and an average storm shape is applied (statistical disaggregation is used to distribute the daily total).
- The hourly rainfall for a grid cell refers to the rainfall accumulated in the previous hour.

## Minimum distance grids and statistical disaggregation
- Minimum distance to the closest gauge for each grid point and day is recorded (Min_dist; grid per day).
- Threshold: 50 km; grids farther than this are not calculated, and statistical disaggregation is used for those grid points.
- Summary of distances: mean distance to gauge over the period is 2.6 km; maximum distance reaches 100 km along the west coast of Scotland.
- Statistical disaggregation:
  - Used when a grid cell is >50 km from a gauge or when there is rainfall in the daily total but not in the hourly gauge data.
  - Table 1 provides average hourly rainfall shapes by daily total and season for disaggregation.
  - The “Stat_disag” flag indicates whether statistical disaggregation was used for a given day.
  - Approximately 0–26% of grid squares on any given day use statistical disaggregation for zero rainfall in the hourly record; 0–11% use it due to distance >50 km (more common after 2000 as EA network density increased).

## Quality control (QC) and data quality
- QC procedure consists of three steps:
  - Step 1: Compare gauge data to CEH-GEAR daily dataset to identify suspect gauges for potential exclusion.
  - Step 2: Apply automated QC tests (QC1–QC15) to flag suspect hourly values.
  - Step 3: Apply automated rules (R1–R20) to determine which flagged values are erroneous and should be removed (replaced with -999).
- Gauge selection criteria for inclusion: Spearman correlation rs > 0.8 and P00 + P11 > 0.8 for daily vs hourly series.
- Outcome (rejection rate):
  - CEH-GEAR1hr.v1: about 0.85% of time steps rejected due to QC rules.
  - CEH-GEAR1hr.v2: about 0.97% of time steps rejected due to QC rules.
- The QC framework is described in detail in Lewis et al. (2018); automated rules cover a wide range of potential errors and storm behaviors.

## Dataset format and contents
- Storage format: NetCDF4, CEH gridded dataset conventions.
- File structure: monthly files (e.g., CEH-GEAR-1hr.v2_199001 for Jan 1990).
- Variables in each file:
  - Rainfall_amount: hourly rainfall in kg/m2 (equivalent to mm depth).
  - Stat_disag: 1 if statistical disaggregation was used, 0 otherwise.
  - Min_dist: minimum distance to the nearest hourly gauge used for estimation (in meters).
- Global attributes include time_coverage_resolution (P1H) and time_coverage_duration (P27Y); times are ISO 8601:2004 formatted.
- The dataset is designed for hydrological modeling and related environmental analyses.

## Appropriate use and caveats
- Suitable for hydrological models and trend monitoring, but with caveats:
  - Statistical disaggregation (average storm shapes) affects diurnal cycle analyses, since hourly shapes are imposed to some daily totals.
  - Nearest-neighbour interpolation can produce “blocky” spatial patterns, as grid cells receive the same hourly value if derived from the same nearby gauge.
  - Always consult metadata to understand where disaggregation or distance-based decisions were used for any grid cell.
- Users should consider the metadata when conducting analyses that rely on precise diurnal timing or fine spatial detail.

## Example storms and coverage notes
- The documentation includes example storms illustrating how gauge density changes over time (1990 vs 2016) and how distance to the nearest gauge influences disaggregation.
- Early storms show a higher fraction of grid points beyond 50 km from gauges; by 2016, this fraction is much smaller due to improved gauge density.

## Acknowledgements and references
- Methodology funded by SINATRA (NERC Flooding from Intense Rainfall) and CONVEX; data acquisition and publishing funded by Hydro-JULES and NERC programs.
- Acknowledges hydrometric teams across MO, EA, SEPA, NRW, and others for data provision and quality control.
- Key references:
  - Keller et al. 2015; Tanguy et al. 2019 (CEH-GEAR daily dataset)
  - Lewis et al. 2018 (QC method)
  - Lewis et al. 2020 (this CEH-GEAR1hr.v2 dataset)
  - Wilks (Statistical Methods in the Atmospheric Sciences) and Yoo & Ha (effects of zeros on rainfall statistics)