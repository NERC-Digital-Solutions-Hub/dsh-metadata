CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use

## I. Brief Description of the dataset
- 1-km gridded daily and monthly rainfall estimates for Great Britain, Northern Ireland, and approximately 3,000 km2 of catchment in the Republic of Ireland, from 1890 onwards; extended annually as new raingauge data become available.
- Derived from the Met Office observed precipitation database; daily and monthly totals used to generate grids.
- Natural neighbour interpolation with SAAR normalisation to produce daily and monthly rainfall grids; day defined as 09:00 on day to 09:00 GMT next day.
- Monthly grids built from the monthly raingauge network and daily gauges with complete data for the month; when a daily gauge shares coordinates with a monthly gauge, the monthly value is used.
- Daily grids produced in two stages: (1) provisional natural neighbour interpolation using daily gauges; (2) adjustment with a monthly correction factor so daily sums match the monthly grids.
- Data stored in NetCDF4 format; organized in yearly files; separate files for GB and NI, with daily and monthly grids stored separately.

## II. Data Sources
- Met Office: collated historical daily and monthly observations; MIDAS national dataset supplied to CEH under licence; CEH keeps a synchronized copy and applies quality control to remove unrealistic extremes.
- Met Office SAAR (1961–1990) 1-km grid for Great Britain (Spackman, 1993).
- Met Éireann SAAR 1961–1990 1-km grid for Northern Ireland (Walsh, 2012).

## II.2 Method for deriving the daily and monthly grids
- Interpolation method: natural neighbour interpolation with SAAR normalisation; no additional scale factor for SAAR due to limited improvement.
- Use all available raingauges for each day; monthly grids rely on monthly gauges plus daily gauges with complete monthly data.
- Daily grids: (1) initial natural neighbour interpolation; (2) apply a monthly correction factor so daily totals align with monthly grids.

## II.2 Minimum distance grids
- Record the minimum distance from each grid point to the nearest gauge; threshold set at 100 km to maintain representativeness.
- Acknowledges lower network density pre-1961, causing some early grids to have missing values, especially in Scotland, Wales, and SW England.
- Ancillary grids (updated yearly) provide users with gap context:
  - Year of first missing data for each grid point
  - Year of last missing data for each grid point
  - Total number of missing days per grid point (separately for monthly and daily data)

## III. Quality Control
- Four-step QC to identify and reject unrealistically high daily rainfall values using a 200-year return-period reference rainfall (from the Flood Estimation Handbook model).
- Steps:
  - Identify days/gauges exceeding reference rainfall.
  - Cross-check against a database of major UK rainfall events; if matched, the value is genuine.
  - Visual assessment with daily rainfall maps (post-1961 GB maps available) to judge plausibility.
  - Time-series comparison using the closest gauges and an internal tool (Time-Series Plotter); multiday accumulation issues and gauge inconsistencies lead to rejection.
- Rejection criteria include multiday accumulation artifacts, inconsistent neighbour records, or extreme values; data removed from the rainfall database used for grid generation.

## IV. Format of the CEH-GEAR dataset
- NetCDF4 format following CEH gridded dataset conventions; yearly files; separate GB and NI datasets; daily and monthly grids stored separately.
- Core variables: rainfall amount and minimum distance to nearest gauge.
- Missing data awareness: yearly missing records files in NetCDF4, plus three ancillary grids (as described in II.2) summarising the extent of missing data.

## References
- Collier et al. (2002); Keller et al. (2014); Spackman (1993); Walsh (2012); Stewart et al. (2011); Svensson et al. (2009)