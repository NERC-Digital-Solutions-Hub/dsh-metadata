# CEH - Gridded Estimates of hourly Areal Rainfall - version 2 (CEH-GEAR1hr.v2)

- Overview
  - 1-km gridded hourly rainfall estimates for Great Britain (GB) from 1990 onwards; currently covering 1990–2016 with planned periodic updates.
  - Updated version (v2) expands the gauge network to 2,606 gauges (vs. 1,903 in the original) and extends temporal coverage; methodology remains the same.
  - Data derived by temporal disaggregation of CEH-GEAR daily data using hourly gauge data; hourly estimates preserve daily CEH-GEAR totals.
  - Data provided by major UK agencies (Met Office MIDAS, Environment Agency, NRW, SEPA).

- Data access and citation
  - Available from the Environmental Information Data Centre (EIDC).
  - Please cite: Lewis et al. (2020) CEH-GEAR1hr.v2 and the associated DOI.
  - Detailed methodology reference: Lewis et al. (2018) for the rule-based QC method.

- Data sources and quality assurance
  - Primary hourly gauge data from:
    - Met Office MIDAS Open (UK hourly rainfall data)
    - England Environment Agency (EA WISKI)
    - Natural Resources Wales (NRW WISKI)
    - Scottish Environmental Protection Agency (SEPA WISKI)
  - CEH-GEAR daily dataset as the base for daily totals; QC applied to hourly gauge data to discard erroneous values.
  - A comprehensive quality-control (QC) protocol with multiple flags (QC1–QC15) and a rule-based system to determine which flagged data are treated as erroneous (replaced with missing values).
  - Post-QC gauge-time-step rejection: original v1 rejected about 0.85% of time steps; v2 rejects about 0.97%.

- Method for deriving hourly grids
  - Use nearest-neighbour interpolation (no height correction) to preserve real storm shapes.
  - For each day, select gauges with complete records; number of gauges used per hour ranges roughly 430–1,771.
  - If the nearest gauge is >50 km away or if hourly data show rainfall not reflected in the nearest daily gauge, the hourly value is not used and a statistical disaggregation is applied.
  - Hourly grid values are derived by distributing daily CEH-GEAR totals proportionally to the nearest gauge’s hourly share, preserving daily sums and storm patterns.
  - Statistical disaggregation begins at 9:00 when used (Tables describe average hourly shapes by daily total and season).

- Statistical disaggregation and minimum-distance grids
  - Statistical disaggregation uses average “storm shapes” (Table 1) to allocate daily rainfall to hours, particularly where the nearest gauge is far away or where hourly data are missing.
  - Minimum distance to the closest gauge (Min_dist) is recorded for each grid point per day; mean distance ~2.6 km; maximum distance ~100 km (Scotland).
  - A 50 km threshold is used to decide whether to apply statistical disaggregation for a given grid cell on a given day.
  - Statistical disaggregation is used for 0–26% of grid squares on a given day (zero-rain hourly records) and 0–11% for far-from-gauge grid squares across 1990–2016; after 2000, far-from-gauge use declined as networks densified.
  - Metadata indicate whether statistical disaggregation was used on a given day.

- Format, metadata and data structure
  - NetCDF4 format, following CEH conventions; stored as monthly files (e.g., CEH-GEAR-1hr.v2_199001 for Jan 1990).
  - Variables in each file:
    - Rainfall_amount: hourly rainfall in kg/m2 (mm)
    - Stat_disag: 1 if statistical disaggregation was used for that day, 0 otherwise
    - Min_dist: minimum distance to the closest hourly gauge used (meters)
  - Global attributes include time_coverage_resolution (ISO 8601, e.g., P1H) and time_coverage_duration (e.g., P27Y).

- Data use considerations and caveats
  - Designed for hydrological modelling; diurnal cycle may be affected by statistical disaggregation (peak rainfall set to the disaggregation pattern starting at 9:00).
  - Hourly totals are conditioned by daily totals, which may affect interpretation of real hourly rainfall trends.
  - Nearest-neighbour interpolation can create non-smoothing, “blocky” spatial patterns where rainfall appears to start simultaneously across adjacent grid cells.
  - Always inspect metadata (Stat_disag, Min_dist, QC flags) for appropriate analysis and interpretation.

- Example interpretation and usage notes
  - Example storms illustrate changing gauge density over time: early period shows more grid points >50 km away (requiring disaggregation); by 2016, this distant-point usage is minimal.
  - Users should account for the disaggregation approach when conducting diurnal or high-resolution spatial analyses, and consider the potential impacts on trends or extreme-value analyses.

- Documentation, acknowledgments and references
  - Comprehensive description of methodology, QC, and data provenance in Lewis et al. (2018, Journal of Hydrology) and Lewis et al. (2020) for v2.
  - Data collection and publication supported by SINATRA, CONVEX, Hydro-JULES, and related NERC and ERC funding programs; thanks to hydrometric teams across Met Office, EA, NRW, and SEPA.