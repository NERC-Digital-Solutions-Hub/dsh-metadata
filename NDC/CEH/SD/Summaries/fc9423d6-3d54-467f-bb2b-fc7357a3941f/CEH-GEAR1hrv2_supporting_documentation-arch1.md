# Data access and citation

- This document describes the CEH-GEAR1hr.v2 dataset: gridded hourly rainfall for Great Britain (GB) at 1-km resolution, derived from daily CEH-GEAR data and a dense network of raingauges.
- Data are available from the Environmental Information Data Centre. DOI: https://doi.org/10.5285/fc9423d6-3d54467f-bb2b-fc7357a3941f
- Required citations when using the data:
  - Lewis, E. et al. (2020). Gridded estimates of hourly areal rainfall for Great Britain - version 2 (1990-2016) [CEH-GEAR1hr.v2].
  - A detailed methodology paper: Lewis, E. et al. (2018). A rule based quality control method for hourly rainfall data and a 1 km resolution gridded hourly rainfall dataset for Great Britain: CEH-GEAR1hr.
- Please cite these articles as described in the data centre record.

## What the dataset is and what it covers

- CEH-GEAR1hr.v2 provides 1-km gridded hourly rainfall estimates for Great Britain from 1990 onwards; current coverage is 1990–2016, with ongoing extension as new raingauge data become available.
- The v2 release expands the gauge network (2,606 gauges vs 1,903 previously) and extends temporal coverage to 2016; methodology is unchanged from the original version.
- Hourly rainfall estimates are derived by temporally disaggregating the CEH-GEAR daily dataset using hourly gauge data to preserve daily totals and maintain realistic storm shapes.

## Data sources and quality control

- Gauge networks (2,606 gauges) contributing to hourly data:
  - Met Office MIDAS (382 gauges) via MIDAS Open
  - England Environment Agency (EA) WISKI archive (1622 gauges)
  - Natural Resources Wales (NRW) WISKI archive (257 gauges)
  - Scottish Environmental Protection Agency (SEPA) WISKI archive (345 gauges)
- CEH-GEAR daily dataset sources and QC:
  - CEH-GEAR daily data (Keller et al. 2015; Tanguy et al. 2019)
  - A systematic QC protocol (Lewis et al. 2018) is applied to discard erroneous hourly values
- Data quality: daily and hourly data pass multiple QC steps; gauges may be excluded if flagged as unreliable. For the hourly dataset, a subset of gauges with robust correlation and reliability metrics is used to build the final product.

## How hourly grids are derived

- The hourly grid for each day is created by selecting a subset of hourly gauges with complete records for that day; the number of gauges used varies (roughly 430–1,771) depending on data completeness.
- Nearest-neighbour interpolation (no height correction) assigns to each 1-km grid cell the hourly value from the nearest gauge, scaled by the gauge’s daily total to preserve daily totals.
- If the nearest gauge is more than 50 km away, or if the daily total indicates rain but the nearest hourly gauge shows none, a statistical disaggregation is applied using an average storm shape.
- The dataset includes metadata describing when statistical disaggregation was used for each grid cell/day.

## Statistical disaggregation and storm shapes

- An average storm shape (Table 1 in the source) is used to distribute daily rainfall into hours when the spatial interpolation is insufficient (e.g., far from gauges).
- The average storm shape is season- and daily-total-dependent, and begins at 9:00 for days when statistical disaggregation is applied.
- Statistical disaggregation is used for:
  - About 0–26% of grid squares for zero rainfall in the hourly record
  - About 0–11% of grid squares where the grid point is >50 km from a gauge
- The approach is designed to preserve daily totals and realistic storm shapes but can affect diurnal analyses and spatial smoothing.

## Minimum distance to gauges and distance-related flags

- The dataset records the minimum distance to the closest gauge used for each grid cell/day (Min_dist in meters).
- Mean distance is about 2.6 km; maximum distance reaches up to 100 km (west coast of Scotland).
- A 50 km distance threshold is used to decide when to apply statistical disaggregation (if exceeded, the daily total is distributed using the average storm shape).

## Format, structure, and usage notes

- Format: NetCDF4, CEH-GEAR1hr.v2, organized in monthly files (e.g., CEH-GEAR-1hr.v2_199001 for January 1990).
- Variables per file:
  - Rainfall_amount: hourly rainfall in kg/m2 (equivalent to mm)
  - Stat_disag: 1 if statistical disaggregation was used for that day, 0 otherwise
  - Min_dist: minimum distance to the closest hourly gauge used for deriving rainfall (in m)
- Global attributes:
  - time_coverage_resolution (ISO 8601: P1H for hourly)
  - time_coverage_duration (e.g., P27Y)
- Use considerations for analysts:
  - Statistical disaggregation affects diurnal cycles; hourly totals may be modulated by daily totals and not reflect true hourly rainfall trends.
  - Nearest-neighbour interpolation can yield "blocky" spatial patterns; datasets should be inspected with the included Min_dist metadata and disaggregation flags.
  - Always consult the accompanying metadata to understand when and where statistical disaggregation was applied for robust analyses.

## How to acknowledge and cite the dataset

- Cite the CEH-GEAR1hr.v2 dataset via the Data Centre DOI provided above.
- Also reference the methodological papers:
  - Lewis et al. (2018) for the QC methodology
  - Lewis et al. (2020) for the hourly GB rainfall dataset version 2

## Data availability and acknowledgments

- Data access: Environmental Information Data Centre
- Acknowledgements: SINATRA, CONVEX, INTENSE, and Hydro-JULES programs; thanks to national hydrometric teams (EA, SEPA, NRW, Met Office) for data collection, quality control, and provision.