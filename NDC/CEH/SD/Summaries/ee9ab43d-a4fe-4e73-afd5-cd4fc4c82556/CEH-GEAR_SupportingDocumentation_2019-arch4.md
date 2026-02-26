# Gridded estimates of daily and monthly areal rainfall for the United Kingdom (1890-2015) [CEH-GEAR]

- What it is
  - CEH-GEAR provides 1-km gridded estimates of daily and monthly rainfall for Great Britain (GB) and Northern Ireland (NI), plus ~3000 km2 of catchment in the Republic of Ireland, from 1890 onwards.
  - Covers daily and monthly rainfall; initial coverage 1890–2012 with annual extension as new raingauge data become available.
  - Estimates derived from the Met Office observed precipitation data; produced under CEH guidance and BS7843-4:2012 compliance.

- Data provenance and licensing
  - Primary data source: Met Office collated historical observations (MIDAS) with daily and monthly totals; QC applied to remove unrealistic extremes.
  - Supporting SAAR grids: 1961–1990 standard periods for GB (Spackman) and NI (Walsh).
  - Full data licensing and reuse conditions available; citation required when using the data.

- Data content and structure
  - Core variables: rainfall amount (mm) and minimum distance to the closest gauge used for estimation.
  - Format: NetCDF4; organized by year with separate files for GB and NI; daily and monthly grids stored separately.
  - Ancillary data: yearly missing-record files plus three ancillary grids for monthly and daily data:
    - Year of first missing data per grid point
    - Year of last missing data per grid point
    - Total number of missing days per grid point (for whole period)

- Methods used
  - Daily grids: natural neighbour interpolation using all available daily raingauges, followed by a monthly correction factor to align with monthly grids.
  - Monthly grids: constructed from monthly raingauges; if a daily gauge shares coordinates with a monthly gauge, the monthly value is used for interpolation to avoid accumulation errors.
  - Normalisation: SAAR-based normalisation; a varying scale factor for normalisation was rejected for simplicity and efficiency.
  - Distance threshold: minimum distance to nearest gauge set at 100 km; grids not produced when this threshold is exceeded to avoid overly extrapolated estimates.

- Data quality control
  - Multi-step QC to identify and reject unrealistically high daily rainfall values (200-year return period reference rainfall method).
  - Steps include cross-checks with major UK rainfall events, visual inspection against daily rainfall maps, and time-series comparisons with up to ten nearest gauges.
  - Common issues addressed: multiday accumulations, inconsistent recording intervals, data flags inaccuracies in the MIDAS dataset.
  - Result: remaining high values that are genuine are retained; unsuitable data removed from the rainfall database.

- Coverage, gaps, and limitations
  - Lower network density before 1961 leading to more missing data, especially in Scotland, Wales, and SW England.
  - 100 km minimum-distance threshold means some areas are not estimated; supplemented by ancillary gap grids to inform users of data extent.
  - Ancillary grids provide users with explicit gap years and total missing days for transparent gap assessment.

- Practical usage and considerations for Data Leaders
  - Suitable for hydrological modelling, climate analyses, and policy-support tasks requiring high-resolution rainfall fields.
  - Important to cite correctly (CEH-GEAR data citation) and reference the associated metadata and quality control procedures.
  - Be mindful of spatial and temporal gaps documented in ancillary grids; consider incorporating uncertainty due to data availability in analyses.
  - Updated annually with new raingauge data, enabling ongoing continuity and trend assessment.

- Updates and governance
  - Dataset extended annually as new years of raingauge data become available; versioning consistent via year-based NetCDF4 files.
  - Data management aligned with CEH conventions; documentation includes detailed QC methodology and gap metadata to support reproducibility.