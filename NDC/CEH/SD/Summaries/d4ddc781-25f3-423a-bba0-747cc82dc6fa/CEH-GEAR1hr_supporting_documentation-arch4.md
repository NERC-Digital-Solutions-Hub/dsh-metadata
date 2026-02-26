# CEH - Gridded Estimates of hourly Areal Rainfall (CEH-GEAR1hr)

## Overview
- 1-km gridded hourly rainfall estimates for Great Britain from 1990 onwards, derived by disaggregating CEH-GEAR daily data with hourly gauge observations.
- Daily totals from CEH-GEAR are preserved; hourly values reflect the nearest-station storm shape when hourly gauges are missing or distant.
- Dataset intended for hydrological modelling and related analyses; continues to be extended annually as new gauge data become available.

## Data Content and Format
- File structure: monthly NetCDF4 files (e.g., CEH-GEAR-1hr_199001 for January 1990).
- Variables:
  - Rainfall_amount: hourly rainfall in kg/m^2 (mm of rainfall)
  - Stat_disag: indicator of whether statistical disaggregation was used (1) or not (0)
  - Min_dist: minimum distance to the closest hourly gauge used for deriving rainfall (in meters)
- Grid and resolution: 1-km grid; hourly values represent rainfall accumulated in the previous hour.
- Metadata per day includes:
  - Distance to the gauge used (minimum distance grid)
  - Whether statistical disaggregation was applied for that day
- Availability of a detailed description and usage notes in the referenced papers.

## Data Provenance and Sources
- Primary gauge data: ~1,903 UK rain gauges from:
  - UK Met Office MIDAS
  - England Environment Agency (EA)
  - Natural Resources Wales (NRW)
  - Scottish Environment Protection Agency (SEPA)
- Base daily dataset: CEH-GEAR daily rainfall estimates (Keller et al., 2015)
- Quality control: QC procedures and flagging system developed in Lewis et al., 2018
- Temporal coverage: 1990 onward; daily totals underpin hourly disaggregation

## Methodology and Processing
- Disaggregation approach:
  - Simple nearest-neighbour interpolation to produce 1-km hourly grids; no height correction to preserve storm shapes.
  - For each day, select gauges with complete hourly records; number of gauges per day varies (roughly 297–1,372).
  - For each hour, assign the hourly value from the nearest station as a fraction of the station’s daily total.
  - If the nearest gauge is >50 km away or the daily total has rainfall without corresponding hourly rainfall, apply an average “storm shape” from Table 1 to distribute the daily total across hours.
  - Hourly rainfall values are then scaled by the daily CEH-GEAR total to preserve daily totals.
- Statistical disaggregation:
  - Used for grid squares where the nearest gauge is >50 km away or when daily rain exists but hourly data does not (and other conditions apply).
  - Average storm shapes (Table 1) indicate mean diurnal distributions, varying by daily total and season.
  - Start time for these disaggregations is 9:00 in the grid hourly data.
- Minimum distance considerations:
  - Minimum distance grid files provided per day; mean distance ~11.3 km; maximum distance ~97.7 km on Scotland’s west coast.
  - Threshold of 50 km is applied to exclude grids where gauge representativeness would be too low.

## Quality Control and Validation
- Three-step QC process:
  1) Compare gauge data to CEH-GEAR daily data to identify suspect gauges.
  2) Apply automated QC flags (Table 2) to suspect hourly values.
  3) Use rule-based decisions (Table 3) to treat flagged hours as erroneous and set to missing (-999).
- Post-QC data selection:
  - Gauges with Spearman rs > 0.8 and P00+P11 > 0.8 are used to form the dataset.
- Notable limitations:
  - Statistical disaggregation can affect diurnal patterns (peaks around 9–11 am).
  - Nearest-neighbour interpolation can produce “blocky” spatial patterns and does not smooth across space.
- Documentation emphasizes caution in interpreting hourly trends and diurnal cycles and requires reviewing metadata for analysis.

## Usage Guidance and Limitations
- Suitable for hydrological modelling and related analyses; users should consider:
  - The diurnal distribution is influenced by the average storm shapes used in disaggregation.
  - Diurnal trend analyses may be affected by the disaggregation approach.
  - Spatial analyses may exhibit blocky patterns due to the interpolation method.
- Important for analysts to consult metadata (Min_dist, Stat_disag flags) when designing studies.
- Data extension: continues to be updated annually as new gauge data become available.

## Access, Citation, and References
- Data access: Environmental Information Data Centre (link provided in the dataset documentation).
- Required citations:
  - Primary data description and dataset: Lewis et al. 2019; CEH-GEAR1hr dataset use
  - QC methodology and dataset details: Lewis et al. 2018
  - CEH-GEAR daily dataset provenance: Keller et al. 2015
  - Gauge data source and archive: Met Office MIDAS (NCAS BADC)
- NetCDF4 format; dataset naming follows CEH-GEAR conventions.
- Users should cite:
  - Lewis, E. et al. 2019 for CEH-GEAR1hr usage
  - Lewis, E. et al. 2018 for QC processes
  - Keller, V.D.J. et al. 2015 for CEH-GEAR daily data
  - MIDAS and national gauge data sources as applicable