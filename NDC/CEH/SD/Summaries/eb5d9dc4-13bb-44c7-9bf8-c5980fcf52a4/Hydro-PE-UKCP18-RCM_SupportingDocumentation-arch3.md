Potential evapotranspiration derived from the UK Climate Projections 2018 Regional Climate Model ensemble 1980-2080 (Hydro-PE UKCP18 RCM) Supporting information

## Purpose and intended use
- Gridded daily potential evapotranspiration (PET) and PET with interception correction (PETI) derived from UKCP18 Regional Climate Model (RCM) outputs on a 12 km UK grid for 1980–2080 under RCP8.5.
- Designed for hydrological modelling and to support environmental change assessments, with PETI aligned to MORECS v2.0 observations where possible.
- PET and PETI enable scrutiny of water balance and evapotranspiration trends under high-warming scenarios.

## Data and calculation methods
- PET and PETI are computed from UKCP18 RCM outputs using Penman–Monteith for a well-watered grass surface.
- PETI adds interception correction on days with non-zero precipitation to account for canopy interception losses.
- Inputs include daily mean humidity, surface pressure, net radiation (shortwave and longwave), wind speed, temperature; PETI additionally uses daily precipitation.
- Calculations follow MORECS v2.0 parameterisations where applicable; stomatal resistance is adjusted for elevated CO2 (Kruijt 2008) to reflect stomatal response.
- Intercepted water (CI) and canopy evaporation (EI) are modelled; PETI switches to interception-corrected values when precipitation occurs and canopy is not yet dry.

## Data preparation and grid handling
- Processing applied to UKCP18 RCM ensemble outputs re-projected to the British National Grid (BNG; EPSG:27700) for consistency.
- Land-sea mask: calculations performed only for land grid boxes; sea boxes with some land fractions are filled by copying PET/PETI from the nearest comparable land grid box to support hydrological modelling.

## File format, structure, and accessibility
- Disseminated as netCDF files conforming to CF Metadata Conventions v1.8 and ACDD v1-3.
- Decadal files, one file per variable (pet or peti) per ensemble member.
- File naming structure: hydro-pe_ukcp18_rcm_rcp85_${ENS}_${VARN}_uk_12km_daily_${Y1}1201${Y2}1130.nc
  - ENS: ensemble member code (e.g., 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15)
  - VARN: pet or peti
  - Y1–Y2: first and last year of the file (e.g., 1980–1990)
- Spatial information: 12 km grids aligned to British National Grid; projection EPSG:27700 with optional WGS84 (EPSG:4326) coordinates provided.
- Temporal information: daily mean values from 1980-12-01 to 2080-11-30, using a 360-day calendar (12 months × 30 days) to match the underlying climate model calendar.

## Spatial and temporal coverage
- Spatial: United Kingdom region on a 12 km grid; land-only calculations with land-sea mask handling for modelling inputs.
- Temporal: Daily data spanning 1980–2080, starting in December and ending in November to maintain seasonal consistency; time axis uses a 360-day calendar.

## Known limitations and caveats
- ArcGIS reading issue: CF-compliant files with projected coordinates may offset display by 10–100 m unless adjusted; users should apply georeferencing corrections as needed.
- Calendar mismatch: data use a 360-day year; caution advised when comparing with Gregorian or 365-day calendars.
- Handling of sea grid cells containing land fractions relies on nearest land box imputation rather than re-running meteorology over sea.

## Data provenance and governance
- Produced under the Hydro-JULES programme with Natural Environment Research Council support (NE/S017380/1).
- Methodology cross-walked to MORECS v2.0 for historical consistency; ensemble approach captures CO2-driven stomatal and climate uncertainties under RCP8.5.
- Provides comprehensive metadata and documentation to support data discovery, reuse, and governance in policy-relevant monitoring.

## References and supporting material
- UKCP18 regional projections and associated data sources, MORECS v2.0, and related climate model ensembles underpin the dataset.
- Documentation includes input data descriptions, calculation steps, land-sea masking approach, and file format specifications.