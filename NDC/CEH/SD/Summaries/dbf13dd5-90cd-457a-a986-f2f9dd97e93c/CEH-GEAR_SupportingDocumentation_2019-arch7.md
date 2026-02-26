# CEH - Gridded Estimates of Areal Rainfall (CEH - GEAR)

- 1-km gridded daily and monthly rainfall estimates for Great Britain (GB) and Northern Ireland (NI), plus ~3000 km2 of ROI catchment, spanning from 1890 onwards with annual updates as new raingauge data become available.
- Rainfall estimates derived from Met Office observed precipitation data using natural neighbour interpolation with SAAR (seasonal annual average rainfall) normalisation; daily estimates cover 09:00 day to 09:00 GMT next day.
- Dataset developed under guidance of British Standards BS7843-4:2012; detailed methodology described in Keller et al. (2014).

## I. Brief Description of the dataset

- Covers GB and NI with separate files; ROI data included within the same CEH-GEAR framework.
- Daily and monthly grids produced from raingauge networks; daily grids created via a two-stage process with a monthly correction factor to ensure consistency with monthly grids.
- Core outputs are rainfall depth in millimetres and a minimum distance grid (distance to the closest gauge used for estimation).

## II.1 Data Sources

- Met Office MIDAS: definitive UK national daily and monthly rainfall totals; quality-controlled and synchronized with CEH databases.
- CEH maintains a copy on its ORACLE database; QC applied to discard unrealistic extremes.
- SAAR grids used for normalisation: GB (1961-1990) from Spackman (1993) and NI (1961-1990) from Met Éireann (Walsh, 2012).

## II.2 Method for deriving the daily and monthly grids

- Interpolation: natural neighbour interpolation with SAAR-based normalisation.
- Daily grids:
  - Stage 1: provisional daily grids via natural neighbour interpolation using all available daily raingauges.
  - Stage 2: adjust provisional daily grids with a monthly correction factor to align with monthly grids.
- Monthly grids:
  - Generated from the monthly raingauge network; daily data with complete-month status summed to monthly totals when applicable; when a daily gauge shares coordinates with a monthly gauge, the monthly gauge prevails to avoid over-counting.
- All grids express rainfall depth (mm).

## II.2 Minimum distance grids

- A minimum distance threshold of 100 km is applied; grids are not produced where the closest gauge is farther than 100 km, due to representativeness concerns, especially pre-1961 when gauge density was sparser.
- Ancillary grids (three per data type: daily and monthly) record:
  - Year of the first missing data for each grid point
  - Year of the last missing data for each grid point
  - Total number of missing days for each grid point across the whole period

## III. Quality Control

- Purpose: identify and reject unrealistically high daily rainfall values using a 200-year return period reference rainfall model (based on Flood Estimation Handbook and related work).
- Four-step QC applied at all gauges:
  1. Identify days/gauges where reference rainfall is exceeded.
  2. Cross-check high values against major UK rainfall events database; if matched, considered genuine.
  3. Visual assessment using daily rainfall maps (post-1961 GB data) to judge plausibility.
  4. Time-series comparison with up to ten nearest gauges (prioritising three; extend to seven if needed) using Time-Series Plotter to detect inconsistencies; identify multiday accumulations and gauge data issues.
- Rejection criteria during step 4:
  - Multiday accumulation events (e.g., weekly measurements misinterpreted as daily).
  - Inconsistent neighboring data (much lower rainfall within 10 km).
  - Clear extreme values (e.g., 469 mm, 999.9 mm) or other anomalies.
- Outcome: only valid, consistent daily data are used in producing the rainfall grids.

## IV. Format of the CEH-GEAR dataset

- File format: NetCDF4, following CEH gridded dataset conventions.
- Structure: yearly files; GB and NI data stored separately; daily and monthly grids stored in distinct files.
- Core variables: rainfall amount (mm) and minimum distance (m) to the nearest gauge.
- Ancillary data:
  - Yearly missing records files (NetCDF4) detailing spatial/temporal extent of missing data.
  - Three ancillary grids (monthly and daily) per year set:
    - Year of first missing data per grid point
    - Year of last missing data per grid point
    - Total number of missing days per grid point for the period

## References

- Collier, C. G., Fox, N. I. and Hand, W. H. (2002). Extreme Rainfall and Flood Event Recognition. Technical Report FD2201. Defra/Environment Agency.
- Keller, V. D. J., et al. (2014). CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use. Manuscript in Preparation.
- Spackman, (1993). Calculation and Mapping of Rainfall Averages for 1961-90.
- Stewart, E. J., et al. (2011). Reservoir Safety - Long Return Period Rainfall. CEH project related.
- Svensson, C., et al. (2009). Data Consolidation for Reservoir Safety project.
- Walsh, S. (2012). New Long-term rainfall averages for Ireland.