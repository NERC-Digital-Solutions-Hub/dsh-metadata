# Supporting Information for Gridded estimates of daily and monthly areal rainfall for the United Kingdom (1890-2015) [CEH-GEAR]

- The CEH - Gridded Estimates of Areal Rainfall (CEH-GEAR) provides 1-km gridded daily and monthly rainfall for Great Britain (GB) and Northern Ireland (NI), plus ~3000 km2 in the Republic of Ireland (ROI), covering from 1890 onwards. Initially 1890–2012; extended annually as new raingauge data become available.
- Rainfall estimates are derived from the Met Office observed precipitation database; daily/monthly totals come from UK raingauge networks and are interpolated to grids using natural neighbour methods with SAAR-based normalisation.
- The dataset follows British Standards BS7843-4:2012 guidance.

## What the dataset contains

- Gridded daily and monthly rainfall depth in millimetres (mm) at 1-km resolution.
- A minimum distance grid for each point, indicating distance to the nearest gauge used for the estimate.
- Ancillary missing-data grids (monthly and daily) that describe where data are missing and the temporal extent of gaps.

## Data sources

- Met Office MIDAS database: definitive UK national daily/monthly rainfall data; QC applied to discard unrealistic extremes.
- Met Office SAAR 61–90 1-km grid for GB; Met Eireann 1961–1990 SAAR grid for NI.
- All data incorporated in CEH-GEAR under licence and kept in sync with Met Office data.

## Method for deriving daily and monthly grids

- Interpolation: natural neighbour interpolation with SAAR normalisation (no varying scale factor chosen).
- Daily grids:
  - Stage 1: apply natural neighbour interpolation using daily raingauges to produce provisional grids.
  - Stage 2: adjust provisional daily grids with a monthly correction factor so that the sum of daily grids matches the monthly grids.
  - If a daily gauge shares coordinates with a monthly gauge, the monthly gauge is used in interpolation to avoid double counting.
- Monthly grids:
  - Generated from monthly raingauges and daily gauges with complete data for the month; daily values are summed to form monthly totals where appropriate.
- Daily data represent rainfall depth that fell in a 24-hour period from 09:00 on day t to 09:00 on day t+1 GTM.

## Minimum distance (representativeness)

- A 100 km minimum-distance threshold is applied; grid points further than 100 km from any gauge are not estimated.
- Early grids (pre-1961) have more gaps due to sparser networks.
- To aid users, three ancillary grids are produced for both daily and monthly data:
  - Year of the first missing data for each grid point.
  - Year of the last missing data for each grid point.
  - Total number of days with missing data at each grid point for the entire period.

## Quality control (QC)

- A four-step QC identifies and rejects excessively high daily rainfall values:
  1) Flag days/gauges where reference 200-year rainfall is exceeded.
  2) Check if high values match major UK rainfall events; if so, considered genuine.
  3) Visual inspection using daily rainfall maps (post-1961 GB) to assess plausibility.
  4) Time-series comparison with up to ten nearest gauges using internal tools; if inconsistencies or multi-day accumulations are suspected (e.g., mismatched measurement periods or faulty flags), reject or further investigate.
- Multiday accumulations and inconsistent measurements are rejected; incomplete or flagged data that fail QC are omitted from rainfall grids.

## Dataset format and structure

- Format: NetCDF4, following CEH gridded dataset conventions.
- Organization: yearly files; GB and NI data stored in separate folders; monthly and daily grids stored in separate subfolders.
- Core variables:
  - Rainfall amount (mm)
  - Minimum distance (meters) to the nearest gauge used for estimation
- Ancillary files:
  - Yearly missing data records (NetCDF4)
  - Three ancillary grids (monthly and daily): first missing year, last missing year, total missing days per grid point
- Data are prepared for use in GIS workflows and hydrological modelling, with clear indication of spatial-temporal coverage and data quality.

## Spatial and temporal coverage

- Geographic: GB, NI, and ROI (approx. 3000 km2).
- Temporal: 1890–2015 (initial coverage 1890–2012; extended annually with new data).

## References

- Collier et al. (2002); Svensson et al. (2009); Walsh (2012); Keller et al. (2015); Stewart et al. (2011); Spackman (1993); Additional project and data source references as listed.