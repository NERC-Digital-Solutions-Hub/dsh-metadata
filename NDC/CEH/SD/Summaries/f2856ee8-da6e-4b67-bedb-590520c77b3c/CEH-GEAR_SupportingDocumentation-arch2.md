# CEH - Gridded Estimates of Areal Rainfall (CEH - GEAR)

## I. Brief Description
- 1-km gridded estimates of daily and monthly rainfall for Great Britain (GB), Northern Ireland (NI), and ~3000 km² of catchment in the Republic of Ireland, from 1890 onwards; ongoing extension each year with new raingauge data.
- Derived from the Met Office national precipitation database; monthly estimates use UK raingauge totals; daily/monthly values produced via natural neighbour interpolation with SAAR-based normalisation; daily rainfall refers to a 24-hour period from 09:00 on day to 09:00 GMT the next day.
- Developed under guidance of BS7843-4:2012; detailed methodology described in Keller et al. (2014).

## II. Data Sources
### II.1 Data Sources
- Met Office MIDAS national dataset of daily and monthly precipitation; CEH holds a synced copy in its Oracle DB; QC applied to remove unrealistic extremes; dataset updated monthly under licence.
- Met Office SAAR 61–90 1-km grid for GB (Spackman, 1993).
- Met Éireann 1961–1990 1-km SAAR grid for NI (Walsh, 2012).

### II.2 Method for deriving the daily and monthly grids
- Interpolation: natural neighbour with SAAR normalisation; all available gauges used for each day.
- Monthly grids: built from monthly gauges plus daily gauges with a complete monthly dataset; if a daily gauge coincides with a monthly gauge, the monthly gauge is used in interpolation.
- Daily grids: two-stage process:
  1) provisional daily grids via natural neighbour interpolation of daily gauges.
  2) adjust provisional daily grids with a monthly-correction factor so the daily totals align with the monthly grids, incorporating information from monthly grids in data-sparse areas.
- Outputs expressed as rainfall depth in millimetres.

### II.3 Minimum distance grids
- Record distance to the closest gauge for each grid point; a 100 km threshold is applied—if exceeded, rainfall grids are not calculated to avoid unreliable estimates.
- Important for pre-1961 data when gauge network density was low, leading to missing values in some regions (Scotland, Wales, SW England).
- Ancillary grids (monthly and daily): 1) year of first missing data, 2) year of last missing data, 3) total number of missing days per grid point; updated yearly.

## III. Quality Control
- 4-step QC to identify and reject unrealistically high daily rainfall values (200-year reference rainfall).
  1) Flag days where reference rainfall is exceeded.
  2) Cross-check with major UK rainfall-event database; matches deemed genuine.
  3) Visual assessment using daily rainfall maps when available; genuine if rainfall pattern is sensible.
  4) Time-series comparison with up to 10 (then 7) nearest gauges; reject multiday accumulations, inconsistent data, and extreme local anomalies (e.g., data gaps, flagged incorrect measurements).
- If data are flagged as multiday accumulation, or inconsistent, the affected periods are removed from the rainfall database used to produce grids. Remaining values are accepted, including those with no gauge nearby but with consistent daily records.

## IV. Format of the CEH-GEAR Dataset
- Stored in NetCDF4 format following CEH gridded dataset conventions; organized by year with separate files for GB and NI, and separate daily and monthly grids.
- Core variables: rainfall amount (mm) and minimum distance to the gauge used.
- Missing-data metadata included as yearly NetCDF4 files; three ancillary grids (first missing year, last missing year, total missing days) for both monthly and daily data.

## References
- Keller et al. (2014). CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use.
- Spackman (1993); Walsh (2012). SAAR grids for GB and NI.
- Collier et al. (2002); Stewart et al. (2011); Svensson et al. (2009); additional methodological references as listed.