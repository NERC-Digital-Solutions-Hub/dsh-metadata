# CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use

- The CEH - Gridded Estimates of Areal Rainfall (CEH-GEAR) provides 1-km gridded estimates of daily and monthly rainfall for Great Britain (GB) and Northern Ireland (NI), plus ~3000 km2 of catchment in the Republic of Ireland, from 1890 onwards. Initial coverage was 1890-2012 and the dataset is extended annually as new raingauge data become available.
- Rainfall estimates are derived from the Met Office observed precipitation database. Daily and monthly grids are created from UK raingauge totals, using natural neighbour interpolation with normalisation by SAAR (Seasonal Annual Average Rainfall). Daily rainfall is defined as rainfall accumulated over a 24-hour period from 09:00 on a day to 09:00 the next day.

- Access, citation & licensing
  - Data access: https://doi.org/10.5285/ee9ab43d-a4fe-4e73-afd5-cd4fc4c82556
  - Mandatory citation: Tanguy, M.; Dixon, H.; Prosdocimi, I.; Morris, D. G.; Keller, V. D. J. (2016). Gridded estimates of daily and monthly areal rainfall for the United Kingdom (1890-2015) [CEH-GEAR]. NERC Environmental Information Data Centre. https://doi.org/10.5285/ee9ab43d-a4fe-4e73-afd5-cd4fc4c82556
  - Licensing and reuse conditions: https://doi.org/10.5285/ee9ab43da4fe-4e73-afd5-cd4fc4c82556

- Data sources
  - Met Office collated daily and monthly UK rainfall totals (MIDAS database; in-sync copies held by CEH and licensed for use)
  - Met Office SAAR 61-90 1-km grid for Great Britain
  - Met Eireann SAAR 61-90 1-km grid for Northern Ireland

- Methodology (daily and monthly grids)
  - Interpolation: natural neighbour interpolation with SAAR normalisation (no varying scale factor)
  - Daily grids: two-stage process
    - Stage 1: apply natural neighbour interpolation using daily raingauges to produce provisional grids
    - Stage 2: adjust provisional daily grids with a monthly correction factor so the sum of daily grids matches the monthly grid
  - Monthly grids: generated from monthly raingauge totals; daily data summed to monthly when a complete month is available
  - Handling overlapping gauges: if a daily gauge shares coordinates with a monthly gauge, the monthly value is used in interpolation
  - Output units: rainfall depth in millimetres (mm)

- Minimum distance grids and data coverage
  - Minimum distance: 100 km threshold; grid points with no gauge within 100 km are not calculated
  - Ancillary coverage data: for both daily and monthly data
    - Year of the first missing data for each grid point
    - Year of the last missing data for each grid point
    - Total number of days with missing data for each grid point
  - Purpose: to inform users (especially models requiring full spatial/temporal coverage) about gaps and to document spatial extent of missing data

- Quality control (QC)
  - Five-step QC against a reference 1-day rainfall estimate (200-year return period) using the Flood Estimation Handbook model
  - Steps
    1) Identify days/gauges exceeding reference rainfall
    2) Cross-check remaining high values against major UK rainfall events database
    3) Visual assessment using daily rainfall maps (post-1961 GB maps available)
    4) Time-series comparison with up to the ten nearest gauges (typically starting with the three closest)
    5) Final decision on remaining cases; multiday accumulations and data flags issues may lead to rejection
  - Outcomes: multiday accumulations, inconsistent data, or nearby gauges showing much lower values can result in rejection of the ORV (observed rainfall value) and removal from the dataset

- Format, structure & data products
  - Storage format: NetCDF4, following CEH gridded dataset conventions
  - Organization: yearly files; GB and NI data stored separately; daily and monthly grids stored in separate files
  - Core variables: rainfall amount (mm) and minimum distance (distance to the closest gauge)
  - Missing data information: annual missing records files (NetCDF4) plus three ancillary grids for daily and monthly data (as above)
  - Ancillary grids (daily and monthly): supplementary files detailing the extent of data gaps over time

- Availability, updates & scope
  - Initial scope: 1890-2012; ongoing annual updates as new raingauge data become available
  - Geographic coverage: GB, NI, and approximately 3000 km2 in the Republic of Ireland
  - Data use notes: suitable for hydrological and related analyses; users should be aware of gaps in early data and minimum-distance limitations

- References (foundational sources)
  - Collier, C. G., Fox, N. I. and Hand, W. H. (2002). Extreme Rainfall and Flood Event Recognition
  - Keller, V. D. J. et al. (2014). CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use
  - Spackman (1993). Calculation and Mapping of Rainfall Averages for 1961-90
  - Stewart, E. J. et al. (2011). Reservoir Safety - Long Return Period Rainfall
  - Svensson, C. et al. (2009). Data Consolidation for Reservoir Safety
  - Walsh, S. (2012). New Long-term rainfall averages for Ireland