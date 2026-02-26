# Supporting Information for Gridded estimates of daily and monthly areal rainfall for the United Kingdom (1890-2015) [CEH-GEAR]

## Overview
- CEH-GEAR provides 1-km gridded estimates of daily and monthly rainfall for Great Britain, Northern Ireland, and ~3000 km² of catchment in the Republic of Ireland from 1890 onwards; extensions occur annually as new raingauge data become available.
- Estimates are derived from the Met Office national precipitation database and produced using natural neighbour interpolation with SAAR-based normalisation.
- Daily rainfall refers to the 24-hour period from 09:00 on a given day to 09:00 GMT the next day.
- Developed in line with British Standards BS7843-4:2012 and described in Keller et al. (2014).

## Data coverage and updates
- Time span: 1890–present (annually updated with new years of raingauge data).
- Geographic scope: Great Britain, Northern Ireland, and ~3000 km² in the Republic of Ireland.
- Output formats: daily and monthly grids, stored in NetCDF4 format, year-by-year.

## Data sources
- Met Office MIDAS: definitive UK national daily and monthly rainfall totals; CEH copies and synchronises with MIDAS on a rolling monthly basis; QC applied to remove unrealistic extremes.
- SAAR 61-90: Met Office 1-km average annual rainfall grid for GB (Spackman 1993) used for normalisation.
- SAAR 61-90 Ireland: Met Eireann 1-km SAAR grid for Northern Ireland (Walsh 2012).

## Interpolation and data derivation
- Interpolation method: natural neighbour interpolation with normalisation by SAAR (no varying scale factor chosen for simplicity and computational efficiency).
- Daily grids:
  - Stage 1: provisional grids produced from all available daily raingauges.
  - Stage 2: adjustment using a monthly correction factor so daily grids sum to the monthly grid; if a daily gauge shares coordinates with a monthly gauge, the monthly gauge is used instead to avoid double counting.
- Monthly grids:
  - Generated from monthly raingauges; when a daily gauge has a complete month, its sum is used; otherwise, monthly gauges interpolate the monthly total.
- Output values: rainfall depth in millimetres (mm).

## Spatial coverage and data quality controls
- Minimum distance grids: a 100 km minimum distance threshold is applied; grid points beyond this distance are not calculated to avoid unrepresentative estimates.
- Ancillary grids for gaps: three ancillary grids (monthly and daily) track:
  - Year of the first missing data for each grid point
  - Year of the last missing data for each grid point
  - Total number of missing days per grid point
- Quality control (QC) of daily rainfall:
  - A four-step protocol compares observed daily rainfall against a 200-year rainfall reference from the Flood Estimation Handbook (return period analysis).
  - Steps include cross-checks with major UK rainfall events, visual assessment against daily rainfall maps (post-1961 GB), and time-series comparisons with nearby gauges.
  - Multiday accumulations and inconsistent or badly flagged data are identified and often rejected; data flagged as unreliable are removed from the dataset used to produce grids.

## Data format, storage, and metadata
- Storage: NetCDF4 format, organized by year; separate folders for Great Britain and Northern Ireland; separate subfolders for daily and monthly grids.
- Core variables: rainfall amount and minimum distance to the nearest used gauge.
- Missing data metadata: yearly missing data records, plus three ancillary grids (first missing year, last missing year, total missing days).
- Data licensing: derived from Met Office data; updates and data integrity procedures maintained to ensure synchronization with MIDAS.

## Practical use and implications for monitoring
- Designed to support hydrological and environmental monitoring with consistent, standardized outputs suitable for trend analysis over long time periods.
- Transparent QA processes and documentation enable scrutiny of data quality and methodological choices.
- Aims to enhance data value by providing long-term, gap-aware rainfall fields and by enabling access to underlying data through accompanying ancillary grids.

## References
- Collier, C. G., Fox, N. I., Hand, W. H. (2002). Extreme Rainfall and Flood Event Recognition. Technical Report FD2201.
- Keller, V. D. J. et al. (2015). CEHGEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use. Earth System Science Data, 7, 143-155.
- Spackman, (1993). Calculation and Mapping of Rainfall Averages for 1961-90.
- Stewart, E. J. et al. (2011). Reservoir Safety - Long Return Period Rainfall. Defra/Environment Agency.
- Svensson, C. et al. (2009). Report on Data Consolidation. Defra project WS194/2/39.
- Walsh, S. (2012). New Long-term rainfall averages for Ireland. National Hydrology Conference.