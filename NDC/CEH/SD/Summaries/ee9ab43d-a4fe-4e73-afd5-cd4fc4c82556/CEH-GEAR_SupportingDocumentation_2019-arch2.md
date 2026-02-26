# CEH - Gridded Estimates of Areal Rainfall (CEH-GEAR)

- The CEH-GEAR dataset provides 1-km gridded estimates of daily and monthly rainfall for Great Britain (GB) and Northern Ireland (NI), with approximately 3,000 km2 of catchment in the Republic of Ireland, covering data from 1890 onward and extending annually as new raingauge data become available.
- Outputs are derived from the Met Office observed precipitation dataset and produced following British Standards guidance.

## Data access and licensing

- Data can be accessed at the provided DOI link.
- Users must cite the dataset as: Tanguy et al. (2016) CEH-GEAR; NERC Environmental Information Data Centre.
- Full licensing and reuse conditions are available via the dataset's license URL.

## What the dataset contains

- Daily and monthly rainfall grids (in millimetres) at 1-km resolution for GB, NI, and ROI catchment, extending from 1890 to present.
- Two main formats/outputs:
  - Daily grids: provisional daily rainfall estimates, then adjusted to align with monthly totals.
  - Monthly grids: derived from UK raingauge totals, used to normalize and adjust daily grids.
- Distance-to-gauge information:
  - A minimum distance grid records the closest gauge distance to each grid point, with a 100 km cutoff for grid calculation.
- Ancillary grids:
  - For both monthly and daily data: year of the first missing data, year of the last missing data, and total number of missing days per grid point.

## Data sources

- Met Office MIDAS: definitive UK daily and monthly totals, quality-controlled and mirrored in CEH’s Oracle database.
- Met Office SAAR 1961-1990 grid for GB; Met Eireann SAAR 1961-1990 grid for NI.

## Processing methodology

- Interpolation method: natural neighbour interpolation with normalisation by SAAR (no variable scale-factor normalization).
- Daily grids:
  - Use all available daily raingauges to produce provisional grids.
  - Apply a monthly correction factor so that the sum of daily grids matches the monthly grid.
  - If a daily gauge shares coordinates with a monthly gauge, the monthly gauge value is used.
- Monthly grids:
  - Generated from the monthly raingauge network; when daily data for a month are complete, daily values for the month are summed and treated as a monthly reading.
- Representativeness threshold:
  - Grids are not produced if the minimum distance to the nearest gauge exceeds 100 km.

## Data quality control

- A four-step QC protocol identifies and rejects erroneously high values using a 200-year return-period rainfall reference (based on the Flood Estimation Handbook model).
  - Step 1: Flag potential high rainfall days/gauges.
  - Step 2: Cross-check against major UK rainfall events database.
  - Step 3: Visual check with daily rainfall maps (post-1961 GB) to assess plausibility.
  - Step 4: Compare with time series from up to ten nearby gauges; if inconsistencies are found (e.g., multiday accumulations, missing data, or flagged anomalies), reject the data.
- Multiday accumulation issues and incorrect flags in source data can lead to rejection of several observations to maintain data integrity.

## Data format and storage

- Stored in NetCDF4 format, following CEH gridded dataset conventions.
- Structure:
  - Yearly files; separate files for GB and NI; daily and monthly grids stored separately.
  - Core variables: rainfall amount (mm) and minimum distance to the closest used gauge.
  - Yearly missing data files (NetCDF4) summarize spatial/temporal gaps and are complemented by three ancillary grid sets (monthly and daily):
    - Year of first missing data for each grid point.
    - Year of last missing data for each grid point.
    - Total number of missing days per grid point for the entire period.

## Usage considerations for environmental analytics

- Provides standardized, long-term rainfall records suitable for environmental health and policy performance assessments over time.
- The explicit gap information and distance metrics support modelers in understanding data coverage and uncertainties.
- QC procedures enhance reliability for hydrological and climate trend analyses and policy evaluations.