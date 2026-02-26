# Data access and citation

- The CEH-GEAR1hr dataset provides 1-km gridded hourly rainfall estimates for Great Britain (GB) from 1990 onwards, derived by temporally disaggregating CEH-GEAR daily data using hourly gauge data.
- Data access and citation requirements:
  - Data is available at the Environmental Information Data Centre with the DOI provided.
  - When using the data, cite the dataset: Lewis et al. (2019) CEHGEAR1hr, and the accompanying description: Lewis et al. (2018) on the QA method, plus related foundational sources.
  - A detailed methodology reference: Lewis et al. (2018) for the rule-based QC and disaggregation approach.
- The dataset will continue to be extended annually as new raingauge data become available; metadata describes data provenance and processing steps.

## Dataset description and purpose

- Content: 1-km gridded hourly rainfall estimates for GB, with hourly values representing the rainfall accumulated in the previous hour.
- Origin: Hourly rainfall is produced by disaggregating CEH-GEAR daily data using hourly gauge data from Met Office MIDAS, EA, NRW, and SEPA, with the CEH-GEAR daily totals used to preserve overall sums.
- Scope: Covers from 1990 onwards; initial period 1990–2014, with ongoing annual updates.
- Intended use: Designed for hydrological models; suitable for many hydrological analyses but with caveats (see Appropriate use).

## Data sources and quality assurance

- Primary data sources:
  - Approximately 1,903 UK rain gauges from MIDAS, EA, NRW, and SEPA.
  - CEH-GEAR daily dataset as the basis for disaggregation.
- Quality control:
  - A three-step QC process: (1) compare gauge data to CEH-GEAR daily data to identify suspect gauges, (2) apply a comprehensive set of QC flags to all gauges, (3) apply an automated rule base to decide which flagged data are treated as erroneous and replaced with missing values.
  - The QC includes numerous flags (e.g., threshold exceedances, winter maxima, monthly accumulations, neighbourhood checks) and rules that remove hours or periods of suspect data.
- Validation criteria: Gauge and grid-cell correlation metrics are computed; only gauges with Spearman rs > 0.8 and combined P11+P00 > 0.8 after QC are used to create the dataset.

## Disaggregation method and spatial-temporal details

- Disaggregation approach:
  - Nearest-neighbour interpolation is used to allocate hourly values to a 1-km grid, preserving the storm shape and daily totals.
  - If the nearest gauge is more than 50 km away, or if there is rain in the daily total but not in the hourly gauge, a statistical disaggregation (average storm shape) is used for that grid cell.
  - The hourly grid values are obtained by multiplying the hourly fractions by the CEH-GEAR daily total.
- Minimum distance and coverage:
  - For each grid point, the minimum distance to the nearest gauge is recorded; a 50 km distance threshold is used to decide when to apply statistical disaggregation.
  - The mean distance to a gauge is about 11.3 km; maximum distance can be up to ~97.7 km on the west coast of Scotland (highlighting lower density in some areas).
- Statistical disaggregation grids:
  - Used when a grid cell is far from gauges or when hourly data are missing but daily totals exist; Table 1 provides average storm shapes used for disaggregation by daily total and season.
  - This disaggregation affects diurnal timing and magnitude in cells where it is applied; it is flagged in metadata per day.
- Data flags:
  - Metadata includes a flag indicating whether statistical disaggregation was used for a given day (Stat_disag).

## Data format, structure, and metadata

- Format: NetCDF4 following CEH gridded dataset conventions.
- File organization: Monthly files (e.g., CEH-GEAR-1hr_199001 for January 1990).
- Variables:
  - Rainfall_amount: hourly rainfall in kg/m2 (equivalent to mm).
  - Stat_disag: 1 if statistical disaggregation was used, 0 otherwise.
  - Min_dist: minimum distance to the closest hourly gauge used for deriving rainfall estimates (in meters).
- Additional metadata: Includes minimum distance grids per day, and notes on days where statistical disaggregation was used.

## Usage considerations and caveats

- For hydrological modeling, users should be aware:
  - Statistical disaggregation can alter the diurnal cycle (peak rainfall often around 10:00), and thus may affect analyses of hourly timing.
  - Trend analyses on hourly rainfall may be influenced by the daily-to-hourly disaggregation mechanism (the diurnal pattern is constrained by the daily totals).
  - Spatial patterns may appear “blocky” due to the nearest-neighbour interpolation, since rainfall is assigned to grid cells from the nearest gauge without smoothing between gauges.
- metadata review is essential to understand, for any analysis, whether a given day used disaggregation and how that affects results.
- Specific regional density issues:
  - Scotland has sparser gauge coverage, making the 50 km threshold more impactful; disaggregation usage was more common in data-sparse regions (though less frequent after network improvements post-2000).

## References and related documentation

- Keller et al. (2015) CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK.
- Lewis et al. (2018) A rule-based QC method for hourly rainfall data and a 1 km gridded hourly rainfall dataset for Great Britain: CEH-GEAR1hr.
- Met Office (MIDAS) data sources and related data centre references.
- Additional methodological and statistical references supporting QC and validation (e.g., Wilks 2006; Yoo & Ha 2007).