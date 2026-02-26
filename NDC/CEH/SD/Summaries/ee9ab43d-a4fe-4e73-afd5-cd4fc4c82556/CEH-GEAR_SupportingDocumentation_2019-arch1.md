# CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use

- Purpose: Provide high-resolution gridded rainfall estimates to support hydrological modelling, trend analysis, and decision-making.

## Data Access & Citation
- Access via dataset link: https://doi.org/10.5285/ee9ab43d-a4fe-4e73-afd5-cd4fc4c82556
- Citation required: Tanguy et al. (2016) CEH-GEAR dataset
- Licensing and reuse conditions: available at https://doi.org/10.5285/ee9ab43da4fe-4e73-afd5-cd4fc4c82556

## Dataset Description
- Coverage: 1-km gridded daily and monthly rainfall for Great Britain (GB) and Northern Ireland (NI), plus ~3000 km2 catchment in the Republic of Ireland.
- Temporal extent: from 1890 onward; initial coverage up to 2012, extended annually as new raingauge data become available.
- Output: rainfall depth in millimetres (mm) for daily grids and monthly grids.
- Key design: daily grids reflect 24-hour rainfall from 09:00 on a day to 09:00 GMT the next day.
- Normalisation: daily and monthly estimates are normalised with SAAR (seasonal annual average rainfall) grids; interpolation uses natural neighbour method.

## Data Sources
- Met Office: collated daily and monthly rainfall totals; MIDAS as the definitive UK national dataset (synced with CEH).
- Met Office SAAR grids for 1961–1990 (GB) and SAAR for 1961–1990 in Northern Ireland (via Met Eireann).
- Quality control applied to remove unrealistic extremes in the raw observations prior to interpolation.

## Derivation Method
- Interpolation: natural neighbour interpolation using all available raingauges for a given day.
- Daily grids:
  - Stage 1: provisional daily grids via natural neighbour interpolation.
  - Stage 2: adjust provisional grids with a monthly correction factor so daily sums align with monthly grids.
  - Note: if a daily gauge shares coordinates with a monthly gauge, the monthly value is used.
- Monthly grids:
  - Constructed from monthly gauges and complete daily data where available; daily values can be summed to create monthly totals when applicable.
- Representativeness: a minimum distance approach ensures grid points rely on nearby gauges.

## Minimum Distance Grids
- Threshold: 100 km minimum distance from the nearest gauge; grids beyond this are not produced.
- Ancillary grids (updated yearly):
  - Year of first missing data for each grid point (monthly and daily).
  - Year of last missing data for each grid point (monthly and daily).
  - Total number of missing days per grid point (whole period).

## Quality Control
- A 4-step QC against a 200-year return-period rainfall model (reference rainfall) to identify and reject unrealistic high values.
- Steps include cross-checks with major rainfall event databases, visual checks of daily maps, and comparison with nearby gauge time series.
- Handling of multiday accumulations and data flags:
  - Multiday accumulation issues lead to exclusion of affected data.
  - If nearby gauges show inconsistencies or significant deviations, or if anomalies are due to reporting practices, such data may be rejected.
- Outcome: only consistent daily rainfall records are retained; some extreme values and problematic periods are removed from the dataset.

## Format & Structure
- Format: NetCDF4, following CEH gridded dataset conventions.
- Structure: yearly files; GB and NI stored separately; daily and monthly grids stored in separate files.
- Core variables: rainfall amount (mm) and minimum distance to gauge.
- Ancillary files: yearly missing data records (NetCDF4) plus three ancillary grids for monthly and daily data:
  - Year of first missing data per grid point
  - Year of last missing data per grid point
  - Total days missing per grid point

## References
- Collier, C.G., Fox, N.I., Hand, W.H. 2002. Extreme Rainfall and Flood Event Recognition.
- Keller et al. 2014. CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use.
- Spackman 1993; Stewart et al. 2011; Svensson et al. 2009; Walsh 2012 (related methodological and data context).