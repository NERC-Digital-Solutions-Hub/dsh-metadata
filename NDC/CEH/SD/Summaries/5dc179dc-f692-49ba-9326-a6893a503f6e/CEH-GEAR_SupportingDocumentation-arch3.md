# CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use

## I. Brief Description of the dataset
- CEH-GEAR provides 1-km gridded daily and monthly rainfall estimates for Great Britain, Northern Ireland, and approximately 3,000 km2 of catchment in the Republic of Ireland, starting from 1890 and extending annually with new data.
- Estimates are derived from the Met Office observed precipitation database. Monthly estimates use monthly and complete daily data from the UK raingauge network; daily estimates use all available gauges.
- Interpolation is performed with natural neighbour interpolation, normalised by average annual rainfall (SAAR). The daily rain amount refers to precipitation in a 24-hour window from 09:00 on day D to 09:00 GMT on day D+1.
- The dataset adheres to the British Standards BS7843-4:2012. A detailed description is available in Keller et al. (2014).

## II.1 Data Sources
- Met Office historical observations of weather elements for the UK (daily and monthly totals) via the MIDAS database, provided to CEH monthly under licence; CEH maintains a synchronized copy and applies quality control to discard unrealistic extremes.
- Met Office SAAR 61-90 1-km grid for Great Britain.
- Met Eireann 1961-1990 1-km SAAR grid for Northern Ireland.

## II.2 Method for deriving the daily and monthly grids
- Interpolation method: natural neighbour interpolation with SAAR normalisation; no additional changing scale factor for SAAR.
- Daily grids:
  - Stage 1: apply natural neighbour interpolation using all available daily raingauges to produce provisional daily grids.
  - Stage 2: adjust provisional daily grids with a monthly correction factor so daily sums align with the (more complete) monthly grids.
- Monthly grids:
  - Use monthly raingauges network; for months with complete daily data, sum daily readings to form monthly totals; if a daily gauge shares coordinates with a monthly gauge, the monthly gauge is used to avoid double-counting.
- Minimum distance grids (distance to nearest gauge):
  - A 100 km threshold is used; grid points beyond this distance are not calculated to avoid unrepresentative values.
  - To aid users, ancillary grids are produced (monthly and daily): year of first missing data, year of last missing data, and total days with missing data per grid point, updated yearly.

## II. Minimum distance grids and data coverage
- For early periods, lower gauge density caused geographical gaps (Scotland, Wales, parts of SW England); the minimum distance grids quantify these gaps.
- Ancillary grids provide spatial and temporal extent of missing data to assist modelling and gap assessment.

## III. Quality control (QC) procedure
- A 4-step QC targets unusually high daily rainfall values (200-year return period) using the latest rainfall-depth-frequency model and reference rainfall.
  - Step 1: Identify days/gauges where reference rainfall is exceeded.
  - Step 2: Cross-check high events against a rainfall-event database to decide if genuine.
  - Step 3: Visually inspect daily rainfall maps (post-1961 GB) for plausibility.
  - Step 4: Compare time series with up to ten nearby gauges (often three used due to time constraints) to identify inconsistencies; multiday accumulations and data flags issues are investigated.
- Rejection criteria within step 4 include: multiday accumulation issues, large discrepancies with neighbours (<20% within 10 km), and obviously erroneous extreme values.
- Any data deemed inconsistent or arising from problematic recordings are removed from the rainfall database used to produce grids.

## IV. Format of the CEH-GEAR dataset
- Stored in NetCDF4 format following CEH gridded dataset conventions.
- Yearly files; separate files for Great Britain and Northern Ireland, with daily and monthly grids stored separately.
- Core variables: rainfall amount and minimum distance (to the closest gauge used for estimation).
- Ancillary data: yearly missing-records NetCDF4 files and three ancillary grids (monthly and daily) describing missing data:
  - Year of first missing data per grid point.
  - Year of last missing data per grid point.
  - Total number of days with missing data per grid point for the entire period.

## References
- Collier, C. G., Fox, N. I. & Hand, W. H. (2002). Extreme Rainfall and Flood Event Recognition. Technical Report FD2201. Defra/Environment Agency.
- Keller, V. D. J., et al. (2014). CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use. Manuscript in Preparation.
- Spackman, (1993). Calculation and Mapping of Rainfall Averages for 1961-90. British Hydrology Society Meeting.
- Stewart, E. J., et al. (2011). Reservoir Safety - Long Return Period Rainfall. CEH project report.
- Svensson, C., et al. (2009). Data Consolidation. Defra project WS194/2/39.
- Walsh, S. (2012). New Long-term rainfall averages for Ireland. National Hydrology Conference.