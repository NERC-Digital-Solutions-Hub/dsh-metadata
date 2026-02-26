Supporting Information

- I. Brief Description of the dataset
  - CEH-GEAR provides 1-km gridded daily and monthly rainfall estimates for Great Britain, Northern Ireland, and approximately 3000 km2 of catchment in the Republic of Ireland, from 1890 onwards; originally 1890–2012, with annual extensions as new raingauge data become available.
  - Estimates are derived from the Met Office historical precipitation data; monthly grids use monthly totals, daily grids use daily data (full months where available); natural neighbour interpolation with normalisation by SAAR 61–90; daily rainfall represents 24-hour rainfall from 09:00 on a day to 09:00 GTM the next day.
  - The dataset follows CEH conventions and BS7843-4:2012 guidance; detailed description available in Keller et al. (2014).

- II.1 Data Sources
  - Met Office MIDAS national dataset of daily and monthly precipitation, provided to CEH monthly under licence; CEH maintains a synchronized copy on Oracle and applies QC to discard unrealistic extremes (Section III).
  - Met Office SAAR 1-km grids (1961–1990) for GB; Met Eireann 1961–1990 SAAR grid for NI.

- II.2 Method for deriving the daily and monthly grids
  - Daily and monthly grids are produced via interpolation using all available raingauges for each day.
  - Monthly grids: derived from monthly networks; daily gauges with complete monthly data are summed to monthly totals; when a daily gauge shares coordinates with a monthly gauge, the monthly gauge is used to avoid larger errors.
  - Daily grids: two-stage process
    1) provisional daily grids from natural neighbour interpolation using daily gauges;
    2) correction to ensure the sum of daily grids matches the monthly grid, incorporating information from monthly grids (especially in remote areas with few daily gauges).
  - Daily and monthly rainfall values are in millimetres.

- II.2 Minimum distance grids
  - A 100 km minimum-distance threshold is applied; grids are not calculated if the closest gauge is farther than 100 km, to avoid low representativeness.
  - To aid users (especially modellers) in assessing gaps, ancillary grids are produced (one set for monthly, one for daily) indicating:
    - Year of first missing data per grid point,
    - Year of last missing data per grid point,
    - Total number of missing days per grid point for the period.
  - Minimum distance values are in metres.

- QC and data validation (embedded in II.2 and mentioned in the process)
  - A four-step quality control (QC) process for gauges exceeding 200-year rainfall, using a reference rainfall model (latest 200-year rainfall estimates) and cross-checks with major UK rainfall events.
  - Steps include visual checks against daily rainfall maps and time-series comparisons with nearby gauges (up to the 10 closest gauges; initially the three closest, then expanding if needed).
  - Special attention to multiday accumulations and data flags; data flagged as multiday accumulations or inconsistent are rejected; if remaining ORVs lack reliable nearby gauges, they may be retained if daily records are consistent and plausible.
  - The QC process targets removal of unrealistic values (e.g., extreme values) and ensures consistency between daily and monthly data.

- IV. Format of the CEH-GEAR dataset
  - Stored in NetCDF4 format following CEH gridded dataset conventions; organized as yearly files.
  - Separate files for Great Britain and Northern Ireland; within each, daily and monthly grids are stored separately.
  - Core variables: rainfall amount and minimum distance to the nearest gauge.
  - Additional yearly missing-record NetCDF4 files summarize missing data; three ancillary grids (monthly and daily) provide:
    - Year of first missing data for each grid point,
    - Year of last missing data for each grid point,
    - Total number of missing days for each grid point over the period.

- References
  - Key sources and related documentation cited for methodology, QA, and data sources (e.g., Collier et al., 2002; Keller et al., 2014; Spackman, 1993; Walsh, 2012; Stewart et al., 2011; Svensson et al., 2009; Collier et al., 2002).