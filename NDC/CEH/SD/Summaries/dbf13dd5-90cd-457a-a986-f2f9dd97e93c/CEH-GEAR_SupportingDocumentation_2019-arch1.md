# CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use

- Purpose and scope
  - CEH-GEAR provides 1-km gridded daily and monthly rainfall estimates for Great Britain (GB), Northern Ireland (NI), and approximately 3,000 km2 of catchment in the Republic of Ireland (ROI) from 1890 onwards, with annual extensions as new raingauge data become available.
  - Estimates are derived from the Met Office observed precipitation database and are intended for hydrological use.

- Data coverage and updates
  - Coverage: GB, NI, and ROI; daily and monthly grids; originally 1890–2012, with ongoing annual updates.
  - Daily rainfall is defined for a 24-hour period from 09:00 on day t to 09:00 GMT on day t+1.

- Data sources
  - Met Office historical observations (daily and monthly totals) from the MIDAS national dataset, synchronized with CEH’s Oracle database; quality control discards unrealistic extremes.
  - SAAR (1961–1990) 1-km grids for GB and NI (Spackman 1993; Walsh 2012 for NI).
  - Metadata and methodological guidance follow CEH conventions and relevant literature.

- Method for deriving daily and monthly grids
  - Interpolation: natural neighbour interpolation with normalisation by SAAR; no varying SAAR scale factor due to limited improvement.
  - Daily grids
    - Stage 1: provisional daily grids via natural neighbour interpolation using all available gauges.
    - Stage 2: adjust provisional daily grids with a monthly correction factor so daily sums match the monthly grid totals.
  - Monthly grids
    - Generated from the monthly raingauge network; if a daily gauge has the same coordinates as a monthly gauge, the monthly value is used to avoid accumulation error.
  - Minimum distance grids (data quality and coverage)
    - Minimum distance to the nearest gauge is recorded; grid points farther than 100 km from any gauge are not estimated.
    - Ancillary grids created to document gaps: year of first missing data, year of last missing data, and total missing days per grid point (monthly, daily, and a paired set).

- Specific quality control and data screening
  - A 4-step QC compares daily observed rainfall to a 200-year return period reference rainfall (based on Flood Estimation Handbook model).
  - Steps include cross-checks with known major rainfall events, visual inspection against daily rainfall maps (post-1961 GB data), and time-series comparisons using nearby gauges.
  - Multiday accumulations, inconsistent gauges, and data flag issues in MIDAS can lead to rejections; flagged cases where data appear to be non-daily (e.g., weekly measurements) are removed.
  - Final dataset retains only observations passing QC; some days with insufficient data coverage remain unestimated.

- Data format and structure
  - Stored in NetCDF4 following CEH conventions; organized by year with separate files for GB and NI, and for daily and monthly data.
  - Core variables: rainfall amount and minimum distance to the nearest contributing gauge.
  - Ancillary files (NetCDF4) provide yearly missing data extents and the three gap-related grids (first missing year, last missing year, total missing days) for both daily and monthly data.

- Practical notes
  - The dataset is designed to be discoverable and usable, with attention to data provenance (sourcing from MIDAS, QA procedures) and documentation of spatial/temporal coverage gaps.
  - The methodology emphasizes incorporating monthly information into daily estimates to improve accuracy in locations with sparse daily data.