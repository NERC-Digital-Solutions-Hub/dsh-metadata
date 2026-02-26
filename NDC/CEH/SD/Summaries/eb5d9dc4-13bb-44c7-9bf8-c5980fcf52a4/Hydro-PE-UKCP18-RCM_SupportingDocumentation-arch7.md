# Potential evapotranspiration derived from the UK Climate Projections 2018 Regional Climate Model ensemble 1980-2080 (Hydro-PE UKCP18 RCM) Supporting information

## Overview
- Gridded daily potential evapotranspiration (PET) and PET with interception correction (PETI) derived from UKCP18 12 km regional climate model output for 1980-2080 under RCP8.5.
- Intended for hydrological modelling and to provide a consistent PET/PETI dataset aligned with MORECS v2.0 parameters.

## What is included
- Two variables:
  - PET: daily total potential evapotranspiration (kg m^-2 d^-1), equivalent to mm d^-1.
  - PETI: PET with interception correction (kg m^-2 d^-1), accounts for canopy interception on days with precipitation.
- Calculated using Penman-Monteith for a well-watered grass surface; PETI includes interception adjustments.

## Input data and variables
- UKCP18 Regional Projections on a 12 km grid over the UK (1980-2080), v20190731, ensemble of perturbed parameter runs under RCP8.5.
- Core input variables (daily mean):
  - Specific humidity at 1.5 m (huss, qa)
  - Sea level pressure (psl)
  - Net surface shortwave flux (rss)
  - Net surface longwave flux (rls)
  - Wind speed at 10 m (sfcWind)
  - Temperature at 1.5 m (tas)
- PETI adds daily precipitation rate (pr).
- Ancillary data (from climate model simulations):
  - Surface altitude (m)
  - Atmospheric CO2 concentrations (ppmv)
  - Land-sea mask
- Calculations performed for each ensemble member; CO2 trajectories reflect scenario uncertainties.

## Processing approach (Penman-Monteith)
- PET computed using daily mean values; inputs are processed to derive saturation humidity, air density, net radiation, and resistances (aerodynamic and canopy) following MORECS v2.0 conventions.
- Parameters aligned with MORECS v2.0 for consistency, including grass surface characteristics and adjustments for CO2 effects on stomatal resistance.

## Interception correction (PETI)
- On days with zero precipitation, PETI equals PET.
- On days with positive precipitation, interception by the canopy is subtracted to yield EPI, then PETI=PET plus an interception term, following MORECS v2.0 logic.
- Interception adjustments are enhanced in spring–autumn to account for multiple daily precipitation events.

## Land-sea mask and filling
- Calculations apply only to grid boxes modelled as land.
- Some sea-classified boxes contain land fractions; PET/PETI are filled by copying from the nearest land grid box to ensure usable inputs for higher-resolution hydrological models.

## File format and naming
- NetCDF, CF Climate and Forecast v1.8; ACDD v1-3 compliant.
- Decadal files, one file per variable per ensemble member.
- Naming structure: hydro-pe_ukcp18_rcm_rcp85_<ENS>_<VARN>_uk_12km_daily_<Y1>1201<Y2>1130.nc
  - ENS: ensemble member code (01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, or 15)
  - VARN: pet or pet_i
  - Y1-Y2: start and end year of the file (e.g., 1980-1990, 1990-2000, etc.)

## Spatial information
- Grid: 12 km resolution, aligned to the British National Grid (BNG), EPSG:27700.
- Additional coordinates in WGS84 (EPSG:4326) are provided alongside the main grid.
- Note: ArcGIS may offset projected CF-compliant files if the datum differs from WGS84; adjustments in ArcGIS may be required.

## Time information
- Daily mean values from 1980-12-01 to 2080-11-30.
- Calendar: 360-day year (12 months × 30 days) reflecting the underlying climate model calendar; caution when comparing with Gregorian/365-day calendars.

## Acknowledgements
- Supported by Natural Environment Research Council (NE/S017380/1) as part of the Hydro-JULES programme.

## References (context)
- UKCP18 regional projections, MORECS v2.0 methodology, and related climate model ensembles and parameters informing the PET and PETI calculations.