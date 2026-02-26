# Data access and citation

- The CEH-GEAR1hr dataset provides 1-km gridded hourly rainfall estimates for Great Britain from 1990 onwards, designed for hydrological and related analyses; data are hosted by the Environmental Information Data Centre (EIDC).
- Access and citation requirements:
  - Primary citation for dataset use: Lewis, E. et al. (2019). Gridded estimates of hourly areal rainfall for Great Britain (1990-2014) [CEHGEAR1hr]. NERC Environmental Information Data Centre. https://doi.org/10.5285/d4ddc781-25f3423a-bba0-747cc82dc6fa
  - Detailed methodology: Lewis, E. et al. (2018). A rule based quality control method for hourly rainfall data and a 1 km resolution gridded hourly rainfall dataset for Great Britain: CEH-GEAR1hr. Journal of Hydrology, 564, 930-943. https://doi.org/10.1016/j.jhydrol.2018.07.034
  - Dataset description background: Keller, V.D.J. et al. (2015). CEHGEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK. Earth System Science Data, 7, 143-155. https://doi.org/10.5194/essd-7-143-2015
- Data sources and scope:
  - Based on 1,903 UK rain gauges from Met Office MIDAS, EA, NRW, and SEPA; daily CEH-GEAR data provide the foundation for hourly disaggregation.
  - Daily data originate from the Met Office national database; hourly values are produced by disaggregating this daily data using observed hourly gauge data.
  - Metadata also includes minimum distance to the gauge used for each grid cell and whether statistical disaggregation was employed for that day.

## Brief dataset description

- CEH-GEAR1hr contains hourly rainfall estimates on a 1-km grid for Great Britain, starting in 1990 and extending annually as new gauge data become available.
- Hourly values are obtained by temporal disaggregation of CEH-GEAR daily totals using hourly gauge data; hourly rainfall refers to rainfall accumulated in the previous hour.
- Nearest-neighbour interpolation is used to generate 1-km grids, preserving storm shape; daily totals from CEH-GEAR are preserved.
- For some days, statistical disaggregation is used (see “Minimum distance grids” and “Statistical disaggregation grids”); this is indicated in metadata.
- For quality and reliability, only gauges with strong correlation to grid cells pass QC filters (see QC section).

## Data sources

- Gauge data: 1,903 UK gauges from:
  - Met Office Integrated Data Archive System (MIDAS)
  - England Environment Agency (EA)
  - Natural Resources Wales (NRW)
  - Scottish Environmental Protection Agency (SEPA)
- CEH-GEAR daily dataset (Keller et al. 2015) used for daily totals.
- Quality control (QC) procedure described and applied to hourly gauge data (Lewis et al. 2018).

## How hourly grids were derived

- A daily subset of hourly gauges is selected depending on data completeness; number of gauges used per day ranges roughly from 297 to 1,372.
- For each hour, hourly gauge values are assigned to the 1-km grid using nearest-neighbour interpolation, weighted as a fraction of the station’s daily total.
- If the nearest gauge is more than 50 km away, or if there is rain in the daily dataset but not in the hourly record, the value is not used and an average storm shape is applied instead.
- Statistical disaggregation uses average storm shapes (Table 1) when a grid cell is far from gauges or when hourly data are missing.
- The average storm shapes depend on daily total ranges and season; disaggregation typically starts at 9:00 for affected hours.

## Minimum distance grids

- For each grid cell and day, the distance to the nearest gauge used is recorded (minimum distance grid).
- Mean distance over the period is 11.3 km; maximum distance is 97.7 km (west coast of Scotland).
- A 50 km minimum-distance threshold is applied: if the nearest gauge is farther than 50 km, rainfall estimates for that grid cell on that day are not produced.
- Distances are provided in meters.

## Statistical disaggregation grids

- Metadata indicates whether a day used statistical disaggregation (due to distance >50 km or hourly record missing while daily record exists).
- Statistical disaggregation is used for 0-26% of grid cells on any day (0–3% for >50 km distance case, which declines after 2000 as networks densify).
- When used, Table 1 provides the average hourly rainfall shape by daily total range and season; disaggregation typically begins at 9:00 and assumes an averaged diurnal profile.
- In most cases, statistical disaggregation is for days with very small totals (<1 mm) in daily records.

## Quality control

- The QC process is three-step:
  1) Compare gauge data to the CEH-GEAR daily grid to identify suspect gauges.
  2) Apply a suite of QC tests (Table 2) to flag suspect hourly values.
  3) Apply an automated rule base (Table 3) to determine which flagged values are erroneous and should be removed (set to -999).
- QC flags (QC1–QC15) cover thresholds, intensity, month/day patterns, dryness, neighbourhood checks, and manual identifications.
- The rule base (R1–R20) defines how flagged data are treated (e.g., large hourly or daily values, seasonal patterns, consecutive dry spells, neighbourhood anomalies, and suspected accumulations). Substantial numbers of hours may be removed under various rules.
- Final dataset construction uses gauges with strong validation: Spearman rank correlation (r_s) > 0.8 and P00+P11 > 0.8 between gauge values and grid cells.

## Use and limitations

- The dataset is intended for hydrological models and related analyses.
- Important caveats:
  - Statistical disaggregation can affect diurnal cycles (peak rainfall may systematically occur around 10:00 in disaggregated hours).
  - Nearest-neighbour interpolation can produce spatial blockiness; it does not smooth across grid cells.
  - Daily totals drive hourly disaggregation, so trend analyses of hourly rainfall may not reflect real hourly-trend dynamics.
  - Metadata should be inspected to account for whether disaggregation was used for any given day.

## Data format and structure

- Format: NetCDF4, following CEH gridded dataset conventions.
- File organization: monthly files (e.g., CEH-GEAR-1hr_199001 for January 1990).
- Variables in each file:
  - Rainfall_amount: hourly rainfall in kg/m^2 (equivalent to mm).
  - Stat_disag: indicator (1 or 0) of whether statistical disaggregation was used for that day.
  - Min_dist: minimum distance to the nearest hourly gauge used (in meters).

## References

- Keller, V.D.J. et al. (2015). CEHGEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK. Earth System Science Data, 7, 143-155. https://doi.org/10.5194/essd-7-143-2015
- Lewis, E. et al. (2018). A rule based quality control method for hourly rainfall data and a 1 km resolution gridded hourly rainfall dataset for Great Britain: CEH-GEAR1hr. Journal of Hydrology, 564, 930-943. https://doi.org/10.1016/j.jhydrol.2018.07.034
- Lewis, E. et al. (2019). Gridded estimates of hourly areal rainfall for Great Britain (1990-2014) [CEHGEAR1hr]. NERC Environmental Information Data Centre. https://doi.org/10.5285/d4ddc781-25f3423a-bba0-747cc82dc6fa