# Drought indicator time series for European NUTS regions based on remote sensing data (2000-2015)

- Overview
  - A dataset of remotely sensed drought indicators time series for European NUTS regions (levels 0–3) spanning 2000–2015.
  - Derived from CEH’s gridded drought indicators product, with additional land-use differentiation using a simplified LULC mask.
  - Storage format: CSV; data organized in folders.

- Data content and indicators
  - Indicators included:
    - Vegetation Condition Index (VCI) based on NDVI
    - Temperature Condition Index (TCI) based on Land Surface Temperature (LST)
    - Vegetation Health Index (VHI), a weighted combination of VCI and TCI (VHI = α·VCI + (1−α)·TCI, typically α = 0.5)
  - Spatial and temporal scope:
    - Extracted time series for European NUTS regions (levels 0, 1, 2, 3) using the 2013 NUTS nomenclature version.
  - Land cover differentiation:
    - For each NUTS region, five time series per indicator: one for each of four land cover classes (forest, crop, grass, shrub) and one for the whole region (no land cover differentiation).
  - Data inclusion criteria:
    - A time step is included only if at least 50% of pixels in the non-masked area have valid values.
    - Two No Data values: “--” (no valid pixels in the non-masked area) and “nan” (some valid pixels but <50% coverage).
  - Result: 15 time series per region (3 indicators × 5 land-cover classes/combination).

- Data sources and methodological provenance
  - Primary data sources:
    - CEH gridded drought indicators product (2000–2015) for Europe.
    - MODIS Land Cover Type (MCD12C1, 0.05°) for 2012 to derive the LULC mask.
  - Methodology:
    - VCI and TCI derived following established formulations (VCI from NDVI; TCI from LST; both using monthly min/max normalization).
    - VHI calculated as a combination of VCI and TCI with α typically set to 0.5.
    - NUTS regions used as spatial references; LULC masks applied per region to obtain class-specific series.
  - Project context:
    - Developed within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) to support monitoring and early warning systems.

- Format, structure, and data handling
  - Format: CSV files.
  - Structure: time series organized per region and per land-cover class, across the three indicators.
  - Processing notes:
    - Time steps with insufficient data (less than 50% valid pixels) are discarded to ensure representativeness.
    - Two No Data conventions explained to distinguish complete absence of data from partial data.
  - Documentation and metadata:
    - Associated supporting documentation, acknowledgments, and references provided to support dataset provenance and reproducibility.

- Data quality, governance, and reuse considerations
  - Data quality controls:
    - Explicit threshold (≥50% valid data) to determine inclusion of time steps.
    - Clear handling rules for missing data values and masked areas.
  - Provenance and transparency:
    - Clear lineage from CEH drought indicators and MODIS-based LULC, with defined NUTS region mapping and year-specific masking.
  - Reuse and application context:
    - Intended for use in monitoring and early warning systems (M&EW) at European scale, with alignment to regional (NUTS) administrative units to facilitate validation against impact data.