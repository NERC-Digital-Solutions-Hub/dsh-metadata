# CEH - GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use

## Overview
- 1-km gridded rainfall estimates for Great Britain (GB) and Northern Ireland (NI), plus ~3000 km2 catchment in the Republic of Ireland, from 1890 onwards; extended annually as new raingauge data become available.
- Daily rainfall estimates cover a 24-hour period from 09:00 on a day to 09:00 GMT the next day; monthly estimates aggregate daily data where complete months exist.
- Developed from Met Office observed precipitation data, using natural neighbour interpolation with SAAR-based normalisation; aligned with British Standards BS7843-4:2012.
- Dataset is foundational for hydrological and climate analyses and is described in detail in Keller et al. (2014).

## Data scope and coverage
- Geographic coverage: GB, NI as separate yearly NetCDF files; plus ~3000 km2 of ROI catchment.
- Temporal coverage: from 1890 onwards; initially 1890–2012, with annual updates.
- Outputs: daily and monthly rainfall grids; associated minimum distance to the nearest gauge grid; and missing-data ancillary information.

## Data sources
- Met Office MIDAS: daily and monthly gauge totals for the UK; QC applied to remove unrealistic extremes.
- SAAR 61–90 grids: GB and NI (GB from Spackman 1993; NI from Walsh 2012).
- CEH maintains replicated datasets in its Oracle database; synchronization with Met Office’s MIDAS version is routine.

## Methodology

### Interpolation and normalisation
- Interpolation method: natural neighbour interpolation.
- Normalisation: by SAAR values; a varying SAAR normalisation scale factor was rejected due to marginal improvement vs. added complexity.
- Rainfall at grid point i, t: weighted sum of surrounding gauges j, scaled by S_j and S_i (see formula in text).

### Daily grid production (two-stage)
- Stage 1: provisional daily grids via daily raingauges.
- Stage 2: adjust provisional daily grids with a monthly correction factor so that the sum of daily grids matches the monthly grid, incorporating information from monthly gauges (particularly in remote areas).

### Monthly grid production
- Generated from the monthly raingauge network; when a daily gauge shares coordinates with a monthly gauge, the monthly value is used to reduce cumulative error.

## Minimum distance grids and data gaps
- Minimum distance to nearest gauge: threshold set at 100 km; if greater, rainfall at that grid point is not calculated.
- Rationale: gauge representativeness declines beyond 100 km, especially in sparsely gauged pre-1961 periods (Scotland, Wales, SW England).
- Ancillary grids (annual, for daily and monthly data): 
  - Year of first missing data per grid point
  - Year of last missing data per grid point
  - Total number of missing days per grid point
- These ancillary grids are updated yearly and help users assess spatial/temporal coverage and uncertainty.

## Quality control (QC)
- Purpose: identify and reject unrealistically high daily rainfall values; compare with a 200-year return period rainfall estimate (reference rainfall) using the Flood Estimation Handbook model.
- Four-step QC for each gauge:
  1) Identify days where reference rainfall is exceeded.
  2) Cross-check with major UK rainfall events databases; if matched, treat as genuine.
  3) Visual assessment using post-1961 CB maps to distinguish genuine widespread events from anomalies.
  4) Time-series comparisons with up to 10 closest gauges; if inconsistencies or multi-day accumulations are suspected (e.g., weekly data, flag errors), invalidate affected periods.
- Outcomes:
  - Multiday accumulations are rejected (not suitable for daily grids).
  - If neighboring gauges show much lower rainfall within 10 km, the event may be rejected.
  - Extreme single-values (e.g., 469 mm, 999.9 mm) are rejected.
  - Remaining observations with consistent daily records are accepted.
- Data flagged as unreliable are removed from the rainfall database used for grid generation.

## Dataset format and structure
- Storage: NetCDF4 format following CEH gridded dataset conventions.
- Organization: yearly files; GB and NI stored separately; daily and monthly grids stored in distinct files.
- Core variables: rainfall amount and minimum distance to the nearest gauge used for estimation.
- Ancillary data: yearly missing-record files (NetCDF4) and three ancillary grids (monthly and daily) describing missing data:
  - Year of first missing data per grid point
  - Year of last missing data per grid point
  - Total days with missing data per grid point

## How this GIS-focused data supports map-based analysis
- Provides high-resolution (1 km) areal rainfall fields suitable for hydrological modelling, flood risk assessment, and climate impact studies.
- Clear documentation of coverage gaps (minimum distance grids and missing-data ancillaries) aids in uncertainty assessment and gap-filling decisions.
- Separate GB and NI datasets with daily and monthly resolutions enable temporal analyses at different scales.
- QC procedures and transparency on data gaps help ensure responsible data integration into GIS workflows and spatial analyses.

## References
- Collier, C. G., Fox, N. I., Hand, W. H. (2002). Extreme Rainfall and Flood Event Recognition. Technical Report FD2201. Defra/Environment Agency.
- Keller, V. D. J., et al. (2014). CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK for hydrological use. Manuscript in Preparation.
- Spackman, A. (1993). Calculation and Mapping of Rainfall Averages for 1961-90. British Hydrology Society Meeting.
- Stewart, E. J., et al. (2011). Reservoir Safety - Long Return Period Rainfall. CEH project context.
- Svensson, C., et al. (2009). Data Consolidation. Defra WS194/2/39.
- Walsh, S. (2012). New Long-term rainfall averages for Ireland. National Hydrology Conference.