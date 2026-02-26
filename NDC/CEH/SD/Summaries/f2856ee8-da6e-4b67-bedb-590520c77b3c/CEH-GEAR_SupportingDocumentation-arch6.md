# CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use

- Overview
  - 1-km gridded estimates of daily and monthly rainfall for Great Britain, Northern Ireland, and a ~3000 km2 catchment in the Republic of Ireland, covering from 1890 onwards with annual updates as new raingauge data become available.
  - Rainfall estimates derived from the Met Office observed precipitation data; daily and monthly values defined over a 24-hour window from 09:00 to 09:00 GMT.
  - Interpolation follows natural neighbour method with normalisation by SAAR; dataset developed according to BS7843-4:2012 guidance.

- Data sources
  - Met Office MIDAS national dataset (daily and monthly totals), licensed to CEH; CEH maintains a synchronized copy.
  - Met Office SAAR 1961-1990 1-km grid for Great Britain; Met Éireann SAAR 1961-1990 1-km grid for Northern Ireland.
  - Quality control procedures to discard unrealistic extremes.

- How daily and monthly grids are derived
  - Daily grids:
    - Use all available daily raingauges with natural neighbour interpolation to produce provisional grids.
    - Apply a monthly correction factor so that daily sums align with the corresponding monthly grids.
  - Monthly grids:
    - Use the monthly raingauge network and daily gauges with a complete monthly dataset; when a daily gauge shares coordinates with a monthly gauge, the monthly gauge is used to avoid larger errors.
  - Daily vs monthly data interplay ensures information from monthly data informs daily estimates, especially in areas with sparse daily coverage.

- Minimum distance grids
  - A 100 km minimum distance threshold is applied to ensure representativeness; grids beyond this distance are not calculated.
  - This is particularly important for pre-1961 data with sparser networks.
  - Ancillary grids (three per dataset type: daily and monthly) provide:
    - Year of first missing data per grid point
    - Year of last missing data per grid point
    - Total days with missing data per grid point

- Quality control (QC)
  - A 4-step QC compares observed daily rainfall to a 200-year return-period rainfall estimate (using the Flood Estimation Handbook model).
  - Steps include cross-checks against major rainfall-event databases, visual assessment via daily rainfall maps, and time-series comparisons with nearby gauges (up to 10–closest gauges initially; extend if needed).
  - Multiday accumulations and inconsistent gauge records are identified (e.g., weekly measurements, incorrect data flags) and often rejected.
  - Remaining plausible high values are retained; data flagged as unreliable are removed from the rainfall database used for grid generation.

- Format and structure of CEH-GEAR
  - Stored in NetCDF4 format following CEH gridded dataset conventions.
  - Yearly files; separate files for Great Britain and Northern Ireland; daily and monthly grids stored separately.
  - Core variables: rainfall amount and minimum distance to the closest gauge used.
  - Ancillary NetCDF4 files provide missing-data extent (three grids for monthly data and three for daily data per year).
  - Additional annual missing-record files accompany the core data.

- Data provenance and references
  - Provisions align with established sources and methodologies (e.g., Collier et al., 2002; Keller et al., 2014; Stewart et al., 2011; Walsh, 2012; Spackman, 1993).
  - Dataset developed and maintained with explicit QC, interpolation, and normalization procedures to support hydrological use.

- Usage and accessibility notes for data support
  - Data are designed to enable self-serve analyses for hydrological and policy-related applications, including potential data products like gridded rainfall fields and gap analyses.
  - Licensing: data derived from Met Office MIDAS under licence; CEH maintains synchronized copies and QA processes to ensure data quality and usability.
  - Regular updates: monthly and annual extensions incorporated as new raingauge data become available.