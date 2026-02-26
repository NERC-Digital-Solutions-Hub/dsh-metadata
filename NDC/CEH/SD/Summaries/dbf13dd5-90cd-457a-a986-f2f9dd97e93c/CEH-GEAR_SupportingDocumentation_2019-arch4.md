# CEH - Gridded Estimates of Areal Rainfall (CEH - GEAR)

- Overview
  - 1-km gridded daily and monthly rainfall estimates for Great Britain, Northern Ireland, and approximately 3000 km2 of catchment in the Republic of Ireland, from 1890 onwards; extended annually with new raingauge data.
  - Rainfall estimates derived from the Met Office observed precipitation data; monthly estimates use monthly and complete daily data; daily estimates use daily data for 24-hour periods from 09:00 to 09:00 GMT; dataset developed to British Standards BS7843-4:2012.
  - Detailed methodology described in Keller et al. (2014).

- Data sources
  - Met Office MIDAS: daily and monthly UK rainfall totals; CEH keeps a synchronized copy on its Oracle database; quality control applied to discard unrealistic extremes.
  - Met Office SAAR grids (1961–1990) for GB (61-90) and Met Eireann SAAR for NI (61-90).

- Method for deriving daily and monthly grids
  - Interpolation: natural neighbour interpolation with normalisation by SAAR (no varying scale factor; keeps model simple and efficient).
  - Daily grids: all available raingauges used; two-stage process:
    - Stage 1: provisional daily grids from natural neighbour interpolation.
    - Stage 2: adjust provisional daily grids with a monthly correction factor to ensure daily sums align with monthly grids, allowing monthly information to influence daily estimates, especially in remote areas.
  - Monthly grids: generated from the monthly raingauge network; where daily gauge coordinates match a monthly gauge, the monthly value is used to avoid accumulated daily measurement error.
  - Grids express rainfall depth in millimetres.

- Minimum distance grids and data gaps
  - Minimum distance to the closest gauge set to 100 km; grids are not calculated where the closest gauge exceeds this distance to maintain representativeness.
  - This is particularly relevant for pre-1961 data, when network density was low, leading to gaps (notably in Scotland, Wales, and SW England).
  - Ancillary gap grids (updated yearly) provide:
    - Year of first missing data per grid point.
    - Year of last missing data per grid point.
    - Total number of missing days per grid point for the full period.
  - Separate sets for daily and monthly data.

- Quality control (QC)
  - A four-step QC against high values using a 200-year rainfall reference (from the Flood Estimation Handbook model).
  - Steps include:
    - Identify days/gauges where reference rainfall is exceeded.
    - Cross-check with major UK rainfall events database to confirm genuine events.
    - Visual inspection using daily rainfall maps when available; assess for realism (e.g., bull’s-eye patterns).
    - Time-series comparison with up to the three nearest gauges (four-stage process to identify multiday accumulations, inconsistent flags, and other data issues).
  - Exclusion criteria:
    - Multiday accumulations (observations not suitable for daily use) are rejected.
    - Significant inconsistencies with nearby gauges (e.g., much lower readings within 10 km) lead to rejection.
    - Some extreme values are discarded (e.g., 469 mm or 999.9 mm).
  - Data flagged as multiday accumulations are removed from the rainfall database used for grid generation.

- Format and structure
  - Stored in NetCDF4 format following CEH gridded dataset conventions.
  - Yearly files; separate files for Great Britain and Northern Ireland; daily and monthly grids stored separately.
  - Core variables: rainfall amount and minimum distance to the nearest gauge.
  - Missing data ancillary grids are provided in NetCDF4 format:
    - Year of first missing data per grid point.
    - Year of last missing data per grid point.
    - Total number of missing days per grid point for the whole period.
    - One set of three ancillary grids for monthly data and another set for daily data.

- Availability and updates
  - Initial dataset covers 1890-2012; extended annually as new raingauge data become available.
  - Data are prepared under licence with the Met Office MIDAS dataset; CEH maintains synchronized copies and updates.

- References
  - Collier, Fox, Hand (2002); Keller et al. (2014); Spackman (1993); Walsh (2012); Stewart et al. (2011); Svensson et al. (2009).