# Supporting Information for Gridded estimates of daily and monthly areal rainfall for the United Kingdom (1890-2015) [CEH-GEAR]

- Overview of CEH-GEAR
  - 1-km gridded estimates of daily and monthly rainfall for Great Britain (GB) and Northern Ireland (NI), plus ~3000 km2 of catchment in the Republic of Ireland (ROI), covering from 1890 onward; initial coverage 1890-2012, extended annually as new raingauge data become available.
  - Rainfall estimates derived from the Met Office national precipitation observations; daily and monthly totals are used to generate grids.
  - Daily rainfall is defined as the rainfall accumulated in 24 hours from 09:00 on a given day to 09:00 GMT the next day.
  - Dataset developed to British Standards BS7843-4:2012; described in Keller et al. (2014).

- Data sources and quality assurance
  - Primary data: Met Office MIDAS daily/monthly rainfall observations; CEH maintains a synchronized copy in an ORACLE database.
  - Quality control (QC) applied to discard unrealistic extremes.
  - Supporting grids for modelers include minimum distance to the closest gauge (distance to gauge used for estimates).

- Data sources in detail
  - Met Office daily/monthly totals from MIDAS (licensed to CEH; in-sync update procedures).
  - SAAR 1961-1990 1-km rainfall grids: GB (Spackman 1993) and NI (Met Eireann, Walsh 2012).

- Interpolation and normalisation method
  - Natural neighbour interpolation used to estimate rainfall at grid points, normalised by SAAR (seasonal-average annual rainfall).
  - A single SAAR normalisation factor was chosen (no varying scale factor) to balance model simplicity and performance.
  - Interpolation uses all available raingauges for a given day.

- Daily and monthly grid construction
  - Monthly grids: built from monthly gauges; daily gauges with a complete dataset for the month are summed to produce monthly totals; if a daily gauge shares coordinates with a monthly gauge, the monthly gauge value is used.
  - Daily grids: two-stage process
    - Stage 1: provisional daily grids from natural neighbour interpolation using daily raingauges.
    - Stage 2: adjust provisional daily grids with a monthly correction factor so that the sum matches the corresponding monthly grid.
  - Core outputs: rainfall depth in millimetres; also ancillary data (minimum distance grid).

- Minimum distance grids and data coverage
  - Minimum distance threshold of 100 km; grid points beyond this distance are not estimated to avoid unrepresentative results.
  - For pre-1961 data, sparser networks lead to gaps, especially in Scotland, Wales, and SW England.
  - Ancillary grids (updated annually) provide:
    - Year of the first missing data for each grid point
    - Year of the last missing data for each grid point
    - Total number of missing days for each grid point
  - Separate sets for monthly and daily data to aid users in understanding spatial-temporal gaps.

- Quality control procedure details
  - Four-step QC for all gauges:
    1) Identify days where the 200-year reference rainfall is exceeded.
    2) Cross-check with major UK rainfall event records; genuine events kept.
    3) Use available daily rainfall maps to assess plausibility; if unclear, proceed to step 4.
    4) Compare the time series with up to the ten closest gauges (prioritising as many nearby gauges as possible); multiday accumulations and data flags issues may lead to rejection.
  - Specific QC considerations
    - Multiday accumulation issues (e.g., weekly measurements, inconsistent data) identified and rejected for daily use.
    - If neighboring gauges show substantially lower rainfall (<20% within 10 km), the identified high event is rejected.
    - Extreme single-value rejections (e.g., 469 mm, 999.9 mm) occur.
  - Result: selected high values may be kept if supported by verifications; otherwise, data flagged as inconsistent are removed from the rainfall database used to produce grids.

- Data format and accessibility
  - Format: NetCDF4, following CEH gridded dataset conventions.
  - Organization: yearly files; GB and NI stored in distinct folders; daily and monthly grids stored separately.
  - Core variables: rainfall amount and minimum distance to the gauge.
  - Ancillary nets: yearly missing data files plus three ancillary grids for daily and monthly data (first missing year, last missing year, total days missing).

- References and documentation
  - Collier, C.G., Fox, N.I. & Hand, W.H. (2002). Extreme Rainfall and Flood Event Recognition.
  - Keller, V.D.J. et al. (2015). CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use.
  - Spackman (1993); Stewart et al. (2011); Svensson et al. (2009); Walsh (2012). Additional methodological and data source references.