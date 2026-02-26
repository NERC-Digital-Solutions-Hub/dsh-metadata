# Gridded estimates of hourly areal rainfall for Great Britain (1990-2014) [CEHGEAR1hr]

- Purpose and scope
  - Provides 1-km gridded hourly rainfall estimates for Great Britain from 1990 onwards, initially covering 1990-2014 with ongoing updates as new gauge data become available.
  - Designed to be used with hydrological models to assess environmental conditions and policy performance over time.

- What the dataset contains
  - Hourly rainfall values on a 1-km grid, representing rainfall accumulated in the previous hour.
  - Metadata on whether a grid cell used statistical disaggregation for that day and the minimum distance to the gauge used.
  - File structure: NetCDF4 format, monthly files (e.g., CEH-GEAR-1hr_199001 for January 1990) with variables:
    - Rainfall_amount: hourly precipitation in mm (kg/m^2)
    - Stat_disag: 1 if statistical disaggregation was used for that day, 0 otherwise
    - Min_dist: distance to the closest hourly gauge used (in meters)

- Data sources and coverage
  - Gauges: ~1,903 UK rain gauges from:
    - Met Office Integrated Data Archive System (MIDAS)
    - England Environment Agency (EA)
    - Natural Resources Wales (NRW)
    - Scottish Environmental Protection Agency (SEPA)
  - Supporting data: CEH-GEAR daily dataset (for daily totals) and gauge quality control data
  - Coverage: UK rainfall gauges used to derive hourly grids; many grids derive from nearest-neighbor interpolation to gauge data

- How hourly grids are derived
  - Start from CEH-GEAR daily rainfall totals
  - Use hourly gauge data to temporally disaggregate daily totals to hourly values
  - Nearest-neighbor interpolation to 1-km grid, preserving a storm’s shape
  - When the nearest gauge is >50 km away or hourly gauge data disagree with daily totals, apply a statistical disaggregation using average storm shapes
  - Hourly values are assigned as fractions of the station’s daily total, with a note on when statistical disaggregation was used
  - The “average storm shape” dataset provides typical hourly distributions for different daily totals and seasons (Table 1)

- Statistical disaggregation and thresholds
  - Statistical disaggregation used for grid cells >50 km from a gauge or when daily rain occurs but not hourly gauge data
  - Typical percentage of grid cells using disaggregation:
    - ~0–3% due to distance
    - 0–26% due to zero hourly readings on some days
  - Average storm shapes begin at 9:00 in the gridded dataset when applied
  - Disaggregation can influence diurnal-cycle analyses and should be accounted for in analyses

- Minimum distance to gauges and quality control
  - Minimum distance grids are provided per day; mean distance ~11.3 km; maximum distance ~97.7 km (west coast of Scotland)
  - A 50 km minimum distance threshold was used to ensure representativeness; calculations not performed beyond this threshold
  - Quality control (QC) is a three-step process:
    - Compare gauge data to CEH-GEAR daily data to flag suspect gauges
    - Apply a set of automated QC tests (flags QC1–QC14) to suspect hourly values
    - Use a rule-based system (R1–R20) to determine which flagged data are replaced with missing values
  - Gauges included in dataset require Spearman rs > 0.8 and P11+P00 > 0.8 after QC

- Format, usage, and caveats
  - NetCDF4 format following CEH conventions
  - Monthly files; users should inspect metadata (e.g., Stat_disag, Min_dist) for appropriate analyses
  - Important caveats:
    - Diurnal cycle in hourly data may be influenced by the disaggregation method (peak around 10:00 in certain cases)
    - Spatial patterns can appear blocky due to nearest-neighbor interpolation
    - Trends in hourly rainfall may be affected by how daily totals drive hourly allocations
  - Designed for hydrological modeling; ensure analysis accounts for disaggregation effects and metadata

- Appropriate use and considerations for analysts
  - Use with hydrological models and time-series analyses of rainfall-driven processes
  - When analyzing diurnal patterns or trends, account for the statistical disaggregation and the daily-to-hourly linkage
  - Incorporate metadata (e.g., Stat_disag, Min_dist) to understand potential biases in specific grid cells
  - Cross-check gauge quality flags and ensure gauge data meet the correlation thresholds before relying on specific grid estimates

- Access and citation
  - Data access: Environmental Information Data Centre external link and DOI
  - Primary citation for usage: Lewis, E.; Quinn, N.; Blenkinsop, S.; Fowler, H.J.; Freer, J.; Tanguy, M.; Hitt, O.; Coxon, G.; Bates, P.; Woods, R. (2019). Gridded estimates of hourly areal rainfall for Great Britain (1990-2014) [CEHGEAR1hr]
  - Relevant methodological references:
    - Lewis et al. (2018). A rule based quality control method for hourly rainfall data and a 1 km resolution gridded hourly rainfall dataset for Great Britain: CEH-GEAR1hr
    - Keller et al. (2015). CEHGEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK
    - Met Office MIDAS data and associated documentation
  - Usage note: Cite the dataset when using the data and acknowledge the QC and data provenance as described above