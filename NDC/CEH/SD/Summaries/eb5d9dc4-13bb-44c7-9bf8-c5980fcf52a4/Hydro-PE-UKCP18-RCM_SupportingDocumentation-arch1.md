# Potential evapotranspiration derived from the UK Climate Projections 2018 Regional Climate Model ensemble 1980-2080 (Hydro-PE UKCP18 RCM) Supporting information

## Introduction
- Gridded daily potential evapotranspiration (PET) and PET with interception correction (PETI) derived from UKCP18 Regional Climate Model output at 12 km over the UK for 1980-2080 under RCP8.5.
- PET is calculated with the Penman-Monteith equation for a well-watered grass surface; PETI adds interception correction on days with precipitation.
- Units: kg m-2 d-1, equivalent to mm d-1.
- PET and PETI are developed for hydrological modelling; PETI is made to be consistent with MORECS v2.0 historical PET.

## Data and inputs
- Source data: UKCP18 RCM ensemble on a 12 km grid over the UK for 1980-2080, v20190731; perturbed parameter ensemble within HadGEM-GC3.05 runs, RCP8.5.
- Shared input variables for PET and PETI (daily means): specific humidity at 1.5 m, sea level pressure, net surface shortwave flux, net surface longwave flux, wind speed at 10 m, air temperature at 1.5 m.
- PETI additionally uses daily precipitation rate.
- Ancillary data: surface altitude, atmospheric CO2 concentrations, land-sea mask.
- Sea level pressure is adjusted to surface altitude and converted to Pa.
- Calculations performed for each ensemble member; ensemble CO2 trajectories reflect RCP8.5 uncertainty; UKCP18 RCM output re-projected to the British National Grid (BNG).

## Penman-Monteith calculation
- PET (E_P) computed with daily mean values via the Penman-Monteith formulation as a function of specific humidity and related variables.
- Key constants/inputs: latent heat (λ), specific heat capacity of air, psychrometric constant, canopy and aerodynamic resistances, and net radiation (Rn) and ground heat flux (G).
- Numerous inputs derived from model output: saturation humidity (qs) and its derivative, air density, total net radiation, aerodynamic resistance (from wind), stomatal resistance (related to leaf area index) with CO2 adjustments.
- Parameterisations use values consistent with MORECS v2.0 for a well-watered short grass surface (e.g., monthly mean ground heat flux, canopy height 0.15 m, stomatal resistance dependent on leaf area index, CO2-dependent stomatal adjustment per Kruijt 2008).

## Interception correction
- On days with no precipitation, PETI equals PET.
- On days with precipitation, interception by the canopy is estimated (CI) as a function of precipitation and leaf area index; spring-summer-autumn enhancement up to a factor of 2 to account for multiple daily precipitation events.
- Canopy evaporation rate (E_I) is computed with r_s = 0 (open water evaporation) until the canopy dries; PETI then reverts to PET.
- Final PETI = PET with interception corrections applied for wet days.

## Land-sea mask and filling
- Calculations use grid boxes modelled as land; some sea grid boxes contain land portions and are filled by copying PET/PETI from the nearest land grid box to ensure usable inputs for higher-resolution hydrological models.

## File format and naming
- NetCDF format (CF v1.8; ACDD v1.3); decadal files; one file per variable per ensemble member.
- File naming: hydro-pe_ukcp18_rcm_rcp85_[ENS]_[VARN]_uk_12km_daily_[Y1]1201[Y2]1130.nc
- Ensemble members (ENS): 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15.
- Variables (VARN): pet or peti.
- Time range: daily data from 1980-12-01 to 2080-11-30.

## Spatial information
- Spatial grid: 12 km, aligned to the British National Grid (BNG), EPSG:27700.
- Latitude/longitude provided in WGS84 (EPSG:4326).
- Note: ArcGIS-reading issues may offset layers due to datum differences; adjust layers if using ArcGIS.

## Time information
- Time coverage: daily mean values from 1980-12-01 to 2080-11-30.
- Calendar: artificial 360-day year (12 months x 30 days); caution when comparing with Gregorian or 365-day calendars.

## Acknowledgements
- Supported by the Natural Environment Research Council (NE/S017380/1) as part of the Hydro-JULES programme.

## References (conceptual context)
- MORECS v2.0 documentation and related methodology for historical PET consistency.
- Foundational works on Penman-Monteith calculation, saturation vapour pressure, CO2 effects on evapotranspiration, and interception estimates.