# CEH - Gridded Estimates of hourly Areal Rainfall - version 2 (CEH-GEAR1hr.v2)

- Overview: Updated 1-km gridded hourly rainfall dataset for Great Britain, covering 1990-2016 (and extending as new data become available). Built by temporally disaggregating CEH-GEAR daily data with a dense raingauge network and local interpolation to produce hourly grids that preserve daily totals.

- Data coverage and format:
  - Spatial: 1-km gridded cells across Great Britain.
  - Temporal: Hourly time steps; dataset spans 1990-2016 (with ongoing extensions planned).
  - Format: NetCDF4 files, organized monthly (e.g., CEH-GEAR-1hr.v2_199001 for January 1990).
  - Variables per file:
    - Rainfall_amount: hourly rainfall in kg/m2 (equivalent to mm).
    - Stat_disag: whether statistical disaggregation was used (1) or not (0) for that day.
    - Min_dist: minimum distance to the nearest hourly gauge used for deriving rainfall estimates (in meters).
  - Global attributes include time_coverage_resolution (P1H) and time_coverage_duration (e.g., P27Y).

- Data sources and provenance:
  - About 2,606 UK rain gauges from:
    - UK Met Office MIDAS (MO daily/hourly data; MO gauge network)
    - England Environment Agency (EA WISKI archive)
    - Natural Resources Wales (NRW WISKI)
    - Scottish Environmental Protection Agency (SEPA WISKI)
  - CEH-GEAR daily dataset (Keller et al. 2015; Tanguy et al. 2019) as the baseline for daily totals.
  - Quality control applied to hourly gauge data (see QC section).

- Method for deriving hourly grids:
  - Daily totals from CEH-GEAR are disaggregated into hourly values using hourly gauge data with a nearest-neighbour interpolation to a 1-km grid.
  - For each day, only gauges with complete records are used; the number of gauges per day varies (approximately 430–1771).
  - Interpolation: assign each grid cell the hourly rainfall value from the nearest station, as a fraction of the station’s daily total.
  - If the nearest station is >50 km away or if there is rainfall in the daily dataset but not in the hourly gauge, the grid square uses an average “storm shape” (statistical disaggregation) to preserve daily totals while reflecting typical hourly distribution.
  - The dataset documents when statistical disaggregation was used (Stat_disag flag).

- Minimum distance and statistical disaggregation:
  - A “minimum distance to gauge” grid is recorded per grid cell per day (mean distance ~2.6 km; maximum ~100 km on the west coast of Scotland).
  - A 50 km threshold is applied; grid cells farther than 50 km from the nearest gauge are treated with statistical disaggregation.
  - Statistical disaggregation uses average storm shapes (Table 1) that vary by daily total and season; the shape begins at 9:00 when applied.
  - Statistical disaggregation is used for:
    - About 0-26% of grid cells on any given day for zero-rainfall cases.
    - About 0-11% of grid cells overall for far-distance cases.
  - Metadata notes when statistical disaggregation was used and how it may affect diurnal and extreme-value analyses.

- Quality control (QC):
  - A three-step QC process to identify and reject erroneous hourly values:
    1) Compare gauge data to the CEH-GEAR daily gridded dataset to flag suspect gauges.
    2) Apply a suite of automated QC tests (flags QC1–QC15) to identify suspect hourly values.
    3) Apply a rule-based combination of QC flags (R1–R20) to treat flagged values as erroneous and replace with missing data.
  - QC flags cover thresholds, intense rainfall, daily accumulations, dry spells, neighbourhood checks, and manual identifications.
  - Non-exhaustive example: large hourly values, suspicious accumulations, dry spells, and neighbourhood anomalies are flagged and potentially removed.
  - Result: a reduced set of hourly steps used for grid construction; QC performance metrics are reported for both v1 and v2.

- Appropriateness and cautions for GIS analysis:
  - Designed for hydrological modeling and GIS-based rainfall analyses.
  - Diurnal patterns may be biased due to statistical disaggregation; trends in hourly rainfall may reflect the disaggregation method rather than real hourly changes.
  - Nearest-neighbour spatial interpolation can produce blocky spatial patterns; there is no smoothing between gauges.
  - Always inspect metadata (Stat_disag, Min_dist, QC flags) for robust analyses.

- Use cases relevant to GIS specialists:
  - Creating high-resolution (1-km) hourly rainfall maps for hydrological modeling, flood risk assessment, or climate impact studies.
  - Integrating with other spatial datasets (e.g., topography, land cover) to analyze rainfall distribution patterns and their hydrological effects.
  - Temporal analyses at hourly resolution across GB for historical event studies (1990-2016 window).

- Access and citation:
  - Data access and citation: Environmental Information Data Centre entry and DOI are provided; users must cite the dataset and its methodology.
  - Suggested citation: Lewis et al. (2020) Gridded estimates of hourly areal rainfall for Great Britain - version 2 (CEH-GEAR1hr.v2). NERC EIDC.
  - Related methodological references: Lewis et al. (2018) on QC methodology; Keller et al. (2015); Tanguy et al. (2019); MIDAS and other data-provider references.

- Acknowledgements and references:
  - Funded by SINATRA, CONVEX, INTENSE, and Hydro-JULES programs; appreciation extended to hydrometric teams across MO, EA, NRW, and SEPA.