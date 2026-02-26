# CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use

## Overview
- CEH-GEAR provides 1-km gridded estimates of daily and monthly rainfall for Great Britain, Northern Ireland, and approximately 3000 km2 of catchment in the Republic of Ireland from 1890 onwards.
- The dataset is updated annually as new raingauge data become available and is developed to support hydrological use with governance and interoperability in mind.
- Conforms to the British Standards BS7843-4:2012 guidance.

## Access, licensing and citation
- Data access: https://doi.org/10.5285/ee9ab43d-a4fe-4e73-afd5-cd4fc4c82556
- Citation: Tanguy, M.; Dixon, H.; Prosdocimi, I.; Morris, D. G.; Keller, V. D. J. (2016). Gridded estimates of daily and monthly areal rainfall for the United Kingdom (1890-2015) [CEH-GEAR]. NERC Environmental Information Data Centre. https://doi.org/10.5285/ee9ab43d-a4fe-4e73-afd5-cd4fc4c82556
- Licensing and reuse: full data licensing and reuse conditions available at https://doi.org/10.5285/ee9ab43da4fe-4e73-afd5-cd4fc4c82556
- Data format: NetCDF4; separate yearly files for Great Britain and Northern Ireland; daily and monthly grids stored separately; core variables are rainfall amount and minimum distance to the gauge.

## Dataset description (scope and content)
- Coverage: GB, NI, and ~3000 km2 of ROI catchment; time period from 1890 onwards; initial coverage 1890–2012, with annual extensions.
- Temporal resolution: daily and monthly rainfall grids; daily rainfall refers to rainfall accumulated over 24 hours from 09:00 on a day to 09:00 the next day.
- Standards: dataset developed in line with CEH conventions and relevant quality considerations.

## Data sources
- Met Office MIDAS: definitive UK national daily and monthly rainfall data; QC applied to remove unrealistic extremes.
- SAAR grids: Met Office 1961–1990 1-km rainfall averages for GB (SAAR 61-90); Met Éireann 1961–1990 1-km SAAR grid for NI.

## Method for deriving daily and monthly grids
- Interpolation: natural neighbour interpolation with normalisation by SAAR; fixed normalization scale factor.
- Daily data: use all available raingauges for each day; two-stage process to produce daily grids.
- Monthly data: use complete daily or monthly gauges; when a daily gauge shares coordinates with a monthly gauge, the monthly value is used to avoid error amplification.
- Daily grid construction: 
  - Stage 1: apply natural neighbour interpolation to daily gauges to produce provisional daily grids.
  - Stage 2: adjust provisional daily grids with a monthly correction factor so that their sum matches the corresponding monthly grid.

## Minimum distance grids and data coverage
- Minimum distance to nearest gauge is recorded; a 100 km threshold is applied to prevent unreliable estimates.
- To aid users (especially modelers) in understanding coverage gaps, ancillary grids are produced for daily and monthly data:
  - Year of first missing data per grid point
  - Year of last missing data per grid point
  - Total number of missing days per grid point
- These ancillary grids are updated yearly with each version.

## Quality control
- A 4-step QC process against a 200-year return period rainfall estimate (from the Flood Estimation Handbook model) identifies and flags potential anomalies.
- Steps include: identifying days exceeding reference rainfall, cross-checking against major rainfall event databases, visual assessment with daily maps, and time-series comparisons with nearby gauges.
- Exclusions: multiday accumulations and inconsistent data (e.g., flags broken or gauge recording patterns) are removed; some extreme values are discarded; after QC, remaining data are used for grid generation.

## Data format and structure
- NetCDF4 format, CEH gridded dataset conventions.
- Structure:
  - Yearly files for GB and NI
  - Separate files for daily and monthly grids
  - Core variables: rainfall amount and minimum distance
  - Yearly missing-records NetCDF4 files
  - Ancillary grids (three per monthly and daily datasets): first missing year, last missing year, total missing days

## Update and maintenance
- The CEH-GEAR dataset is extended annually as new raingauge data become available.
- Quality control and interpolation steps are reapplied to generate updated daily and monthly grids.

## Data governance considerations and limitations
- Gaps and representativeness: 100 km minimum distance threshold leads to missing data in sparser periods/regions, notably pre-1961; users should consult ancillary grids to assess spatial/temporal coverage.
- Data sources and provenance: provenance relies on Met Office MIDAS data and regional SAAR grids; QC processes document the treatment of potentially erroneous observations.
- Usage guidance: citation is mandatory; licensing conditions govern reuse; NetCDF4 format supports interoperability and integration into hydrological workflows.

## References
- Collier, C. G., Fox, N. I. and Hand, W. H. (2002). Extreme Rainfall and Flood Event Recognition. Technical Report FD2201. Defra/Environment Agency, Flood and Coastal.
- Keller, V. D. J., Tanguy, M., Prosdocimi, I., et al. (2014). CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use. Manuscript in Preparation.
- Spackman, (1993). Calculation and Mapping of Rainfall Averages for 1961-90. British Hydrology Society Meeting.
- Stewart, E. J., Jones, D. A., Svensson, C., et al. (2011). Reservoir Safety - Long Return Period Rainfall. CEH project reference.
- Svensson, C., Folwell, S., Dempsey, P., et al. (2009). Data Consolidation. Defra project WS194/2/39.
- Walsh, S. (2012). New Long-term rainfall averages for Ireland. National Hydrology Conference.