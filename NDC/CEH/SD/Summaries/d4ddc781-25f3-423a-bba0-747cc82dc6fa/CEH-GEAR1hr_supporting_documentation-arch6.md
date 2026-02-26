# CEH - Gridded Estimates of hourly Areal Rainfall (CEH-GEAR1hr)

## Data access and citation
- Data are available from the Environmental Information Data Centre (EIDC): https://doi.org/10.5285/d4ddc781-25f3423a-bba0-747cc82dc6fa
- Required citation when using the data: Lewis, E.; Quinn, N.; Blenkinsop, S.; et al. (2019). Gridded estimates of hourly areal rainfall for Great Britain (1990-2014) [CEHGEAR1hr]. NERC EIDC. https://doi.org/10.5285/d4ddc781-25f3423a-bba0-747cc82dc6fa
- Detailed dataset description and methods described in Lewis et al. (2018) and related references; please cite these articles where relevant.

## Brief dataset description
- CEH-GEAR1hr provides 1-km gridded hourly rainfall estimates for Great Britain from 1990 onwards.
- Hourly data are derived by temporally disaggregating the CEH-GEAR daily data using hourly gauge data, ensuring consistency with daily totals.
- Daily data sources: Met Office (national database), EA, NRW, and SEPA; hourly gauge data from 1,903 UK gauges.
- Nearest-neighbour interpolation is used to create hourly grids, with statistical disaggregation applied in specific cases to preserve daily totals and storm shapes.
- Metadata include the minimum distance to the gauge used for each grid cell and whether statistical disaggregation was used for a given day.

## Data sources
- 1,903 UK rain gauges from:
  - Met Office MIDAS
  - England Environment Agency (EA)
  - Natural Resources Wales (NRW)
  - Scottish Environmental Protection Agency (SEPA)
- CEH-GEAR daily dataset (Keller et al. 2015)
- Quality control procedures applied to hourly gauge data (see Lewis et al. 2018 for details)

## Method for deriving the hourly grids
- Use a simple nearest-neighbour interpolation on a 1-km grid to preserve storm shapes, based on complete daily records.
- For each day, only gauges with complete records are used; number of gauges per day ranges from ~297 to ~1,372.
- Hourly values for a grid square are assigned as the nearest station hourly rainfall value scaled by the station’s daily total.
- If the nearest gauge is >50 km away or if daily rainfall exists but the hourly gauge shows no rain, a statistical disaggregation (average storm shape) is used instead.
- The average storm shapes used for disaggregation depend on daily total and season, with a 9:00 start time when applied (see Table 1 in the dataset description).

## Minimum distance grids
- Each grid cell has a minimum distance to the closest gauge used on that day.
- Mean distance: 11.3 km; maximum distance: 97.7 km (west coast of Scotland).
- A 50 km minimum distance threshold is applied; grids farther than 50 km are not calculated to avoid poor representativeness.

## Statistical disaggregation grids
- Used when a grid cell is >50 km from a gauge or when there is daily rainfall but no corresponding hourly rainfall in gauges.
- Zero-rainfall disaggregation occurs for 0–26% of grid cells on any day; distance-based disaggregation occurs for 0–3%.
- The table of average storm shapes (Table 1) shows how hourly distribution is allocated for different daily totals and seasons.
- 97% of zero-rainfall disaggregation cases occur for daily totals < 1 mm.
- Statistical disaggregation can affect diurnal cycles and trend analyses; metadata should be consulted for specific days.

## Quality control (QC)
- QC process comprises three steps:
  - Step 1: Compare gauge data to the CEH-GEAR daily grid to identify suspect gauges.
  - Step 2: Apply a suite of automated QC flags to all data (Table 2).
  - Step 3: Apply an automated rule base (Table 3) to determine which flagged values are erroneous and should be removed (replaced with -999).
- The QC flags cover a range of anomalies, including extreme values, rapid changes, suspicious daily totals, and neighborhood checks.
- Only gauges with Spearman rank correlation rs > 0.8 and combined P11 + P00 > 0.8 after QC are used to create the dataset.

## Use and caveats
- Designed for hydrological modeling; users should ensure appropriateness for their analysis.
- Disaggregation assumptions (especially average storm shapes) affect diurnal cycles and trend analyses.
- Nearest-neighbour interpolation can produce non-smooth spatial patterns; visible “blocky” patterns may occur where rainfall is assigned identically across neighboring grid cells at the same times.
- Always inspect accompanying metadata (e.g., disaggregation flags, minimum distance grids) when conducting analyses.

## Format and contents
- Data format: NetCDF4, organized as monthly files (e.g., CEH-GEAR-1hr_199001 for January 1990).
- Variables per file:
  - Rainfall_amount: hourly rainfall in kg/m^2 (equivalent to mm depth)
  - Stat_disag: 1 if statistical disaggregation was used for that day, 0 otherwise
  - Min_dist: minimum distance to the nearest hourly gauge used for deriving rainfall estimates (in meters)

## References
- Keller, V.D.J., et al. (2015). CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological and other applications. Earth System Science Data, 7, 143-155.
- Lewis, E., et al. (2018). A rule-based quality control method for hourly rainfall data and a 1 km resolution gridded hourly rainfall dataset for Great Britain: CEH-GEAR1hr. Journal of Hydrology, 564, 930-943.
- Met Office (2012). MIDAS data.
- Additional supporting papers: Tanguy et al. (2015, 2016), Wilks (2006), Yoo & Ha (2007).