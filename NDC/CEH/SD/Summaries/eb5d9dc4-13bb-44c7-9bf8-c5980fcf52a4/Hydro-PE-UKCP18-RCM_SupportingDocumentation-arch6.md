# Potential evapotranspiration derived from the UK Climate Projections 2018 Regional Climate Model ensemble 1980-2080 (Hydro-PE UKCP18 RCM) Supporting information

## Overview
- Gridded daily potential evapotranspiration (PET) and PET with interception correction (PETI) derived from UKCP18 Regional Climate Model output at 12 km resolution over the UK for 1980–2080 under RCP8.5.
- PET calculated with Penman-Monteith for a well-watered grass surface; PETI adds interception correction on days with non-zero precipitation.
- PETI is designed to be consistent with MORECS v2.0 observational PET, using parameterisations from MORECS v2.0.
- Dataset intended for hydrological modelling in the UK.

## Data products and variables
- Two variables provided: daily total PET (kg m⁻² d⁻¹) and daily total PETI (kg m⁻² d⁻¹).
- Units kg m⁻² d⁻¹ are equivalent to mm d⁻¹.
- Data distributed as netCDF files adhering to CF v1.8 and ACDD v1-3; decadal files produced for each ensemble member and variable.
- File naming scheme encodes ensemble member, variable, grid, daily cadence, and year range (e.g., hydro-pe_ukcp18_rcm_rcp85_<ENS>_<VARN>_uk_12km_daily_<Y1>1201<Y2>1130.nc).

## Input data and ensemble
- Input climate data: UKCP18 regional projections on a 12 km grid for 1980–2080 (v20190731), a perturbed parameter ensemble of the HadGEM-GC3.05 regional model, nested within global model runs, run under RCP8.5.
- Calculations performed for each ensemble member to reflect CO₂ trajectory uncertainty.
- UKCP18 RCM output re-projected to the British National Grid (BNG) prior to publication.
- Primary inputs for PET and PETI: daily mean specific humidity at 1.5 m, daily mean sea level pressure, daily net surface shortwave flux, daily net surface longwave flux, daily mean wind speed at 10 m, daily mean air temperature at 1.5 m; PETI additionally uses daily precipitation.
- Ancillary data used: surface altitude, atmospheric CO₂ concentrations, land-sea mask.

## Calculations and parameterisations
- PET computed using the Penman-Monteith equation with parameters for a well-watered short grass surface.
- Derived quantities from model outputs: saturation humidity and its derivative, air density, total net radiation; aerodynamic resistance as a function of wind speed.
- Stomatal resistance adjusted for elevated CO₂ following Kruijt (2008) to reflect plant response.
- Numerous parameters aligned with MORECS v2.0 (e.g., ground heat flux as monthly mean, canopy height 0.15 m, stomatal/soil surface resistances).

## Interception correction (PETI)
- On days with precipitation, canopy interception water (CI) is subtracted from PET based on leaf area index and precipitation amount; correction enhanced in spring/summer/autumn to account for multiple daily precipitation events.
- Evaporation from canopy water (EI) computed with the canopy resistance set to zero, then PETI combines EP and CI when precipitation occurs; if no precipitation, PETI equals PET.

## Land-sea mask and data filling
- Calculations applied to grid boxes modelled as land; for some sea boxes containing land fractions, PET and PETI are filled by copying from the nearest suitable land grid box to support hydrological modeling that requires higher-resolution inputs.

## File format and structure
- NetCDF files following CF Metadata Conventions v1.8 and ACDD v1-3.
- Data stored in decadal files, one file per ensemble member and variable.
- Spatial grids are 12 km, aligned to the British National Grid (EPSG:27700). WGS84 coordinates (EPSG:4326) are also provided.
- Known issue: reading CF-compliant files with projected coordinate systems in ArcGIS may offset layers by ~10–100 m due to datum handling; adjust layers accordingly.

## Spatial information
- 12 km resolution on the British National Grid (EPSG:27700).
- Coordinates in eastings/northings (metres) with supplementary WGS84 latitude/longitude (EPSG:4326) provided.
- ArcGIS users should be aware of potential datum-related position offsets for some layers.

## Time information
- Daily mean values from 1980-12-01 to 2080-11-30.
- Time axis uses a 360-day calendar (12 months × 30 days) matching the underlying climate model; caution when comparing to Gregorian or 365-day calendars.

## Acknowledgements
- Supported by the Natural Environment Research Council (NE/S017380/1) as part of the Hydro-JULES programme.

## References (selected)
- UKCP18 regional projections and related methodological sources (MORECS v2.0, Kruijt 2008, Richards 1971, Stewart 1989).