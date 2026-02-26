# Gridded estimates of hourly areal rainfall for Great Britain (1990-2014) [CEHGEAR1hr]

- The CEH-GEAR1hr dataset provides 1-km gridded hourly rainfall estimates for Great Britain from 1990 onward, initially covering 1990-2014 and planned for annual updates as new data arrive.
- Hourly values are produced by temporal disaggregation of CEH-GEAR daily data using hourly gauge observations, ensuring daily totals are consistent with the daily dataset.
- Data are intended for hydrological modeling and map-based GIS analyses, with detailed metadata describing disaggregation and data quality.

## Data access and citation

- Data availability: Environmental Information Data Centre (EIDC): https://doi.org/10.5285/d4ddc781-25f3-423a-bba0-747cc82dc6fa
- Usage citation:
  - Lewis, E.; Quinn, N.; Blenkinsop, S.; et al. (2019). Gridded estimates of hourly areal rainfall for Great Britain (1990-2014) [CEHGEAR1hr]. NERC EIDC. https://doi.org/10.5285/d4ddc781-25f3-423a-bba0-747cc82dc6fa
- Detailed methodology description:
  - Lewis, E.; Quinn, N.; Blenkinsop, S.; et al. (2018). A rule based quality control method for hourly rainfall data and a 1 km resolution gridded hourly rainfall dataset for Great Britain: CEH-GEAR1hr. Journal of Hydrology, 564, 930-943. https://doi.org/10.1016/j.jhydrol.2018.07.034

## Data description

- Content: 1-km gridded hourly rainfall estimates for GB from 1990 onward; hourly rainfall is the amount accumulated in the previous hour.
- Data sources:
  - 1,903 UK rain gauges from Met Office MIDAS, England Environment Agency (EA), Natural Resources Wales (NRW), and Scottish Environmental Protection Agency (SEPA)
  - CEH-GEAR daily dataset (Keller et al. 2015)
- Quality control: a comprehensive QC protocol is applied to hourly gauge data before disaggregation (see Lewis et al. 2018 for full details).

## Data processing and interpolation

- Interpolation method: simple nearest-neighbour interpolation to a 1-km grid to preserve real storm shapes; no height correction.
- Daily subset: only gauges with complete daily records are used for that day; number of gauges per day ranges from 297 to 1,372.
- Disaggregation workflow:
  - For each hour, assign the grid cell the nearest station hourly rainfall value as a fraction of the station’s daily total.
  - If the nearest station is >50 km away, or if daily rainfall exists but not hourly rainfall, use an average storm shape (statistical disaggregation) instead.
  - The hourly grid value = (nearest station hourly fraction) × (daily CEH-GEAR total).
- Statistical disaggregation:
  - Used when a grid cell is >50 km from a gauge or the daily total exists but no hourly data.
  - Average storm shapes are seasonally and total-dependent (Table 1 in Lewis et al. 2018); disaggregation typically starts at 9:00.
  - Statistics: about 0-26% of grid squares per day use disaggregation for zero rainfall; about 0-3% for distances >50 km.
- Metadata:
  - Min_dist grids: per grid cell daily minimum distance to the gauge used; mean 11.3 km, max 97.7 km on Scotland’s west coast.
  - A minimum distance threshold of 50 km is applied; grids beyond this are not calculated.

## Minimum distance and data coverage

- The dataset includes a per-day text file of the minimum distance to the nearest gauge (Min_dist).
- Threshold policy: if the minimum distance exceeds 50 km for a grid cell, the rainfall estimate for that cell for that day is not produced.
- Spatial representativeness is affected in data-sparse areas (e.g., early UK counties with sparse gauge networks).

## Quality control and data validity

- QC procedure (three steps):
  - Step 1: Compare gauge data with the CEH-GEAR daily grid to flag suspect gauges.
  - Step 2: Apply a suite of QC flags to all hourly values (Table 2 in Lewis et al. 2018).
  - Step 3: Apply a rule-base (Table 3) to determine the treatment of flagged data; erroneous values are removed and replaced with missing data (-999).
- Gauge selection for final dataset: only gauges with Spearman’s rank correlation rs > 0.8 and P00 + P11 > 0.8 after QC are used to create the dataset.

## Appropriate use and limitations for GIS work

- Designed for hydrological modeling; use with awareness of disaggregation effects:
  - Statistical disaggregation affects the diurnal cycle (peak around 10:00 in many cases).
  - The nearest-neighbour interpolation can produce blocky spatial patterns since it does not smooth between gauges.
  - Diurnal trends in hourly rainfall may be distorted due to the daily-total-driven disaggregation.
- Metadata should be consulted when conducting analyses to understand the disaggregation status and gauge proximity for each grid cell.

## Data format and file structure

- Format: NetCDF4 following CEH gridded dataset conventions.
- File structure: monthly files (e.g., CEH-GEAR-1hr_199001 for January 1990).
- Variables:
  - Rainfall_amount: hourly rainfall in kg/m2 (mm depth)
  - Stat_disag: 1 if statistical disaggregation was used for that day, 0 otherwise
  - Min_dist: minimum distance to nearest hourly gauge used for deriving rainfall (in meters)

## References

- Keller, V.D.J.; Tanguy, M.; Prosdocimi, I.; et al. (2015). CEHGEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological and other applications. Earth System Science Data, 7, 143-155. https://doi.org/10.5194/essd-7-143-2015
- Lewis, E.; Quinn, N.; Blenkinsop, S.; et al. (2018). A rule based quality control method for hourly rainfall data and a 1 km resolution gridded hourly rainfall dataset for Great Britain: CEH-GEAR1hr. Journal of Hydrology, 564, 930-943. https://doi.org/10.1016/j.jhydrol.2018.07.034
- Met Office Integrated Data Archive System (MIDAS) data (2012). http://catalogue.ceda.ac.uk/uuid/220a65615218d5c9cc9e4785a3234bd0
- Tanguy, M.; Dixon, H.; Prosdocimi, I.; et al. (2015). Gridded estimates of daily and monthly areal rainfall for the United Kingdom (1890-2014) [CEH-GEAR]. NERC EIDC. https://doi.org/10.5285/f2856ee8-da6e-4b67-bedb-590520c77b3c