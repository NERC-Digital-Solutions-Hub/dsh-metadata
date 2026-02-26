# Potential evapotranspiration derived from the UK Climate Projections 2018 Regional Climate Model ensemble 1980-2080 (Hydro-PE UKCP18 RCM) Supporting information

## Overview
- Gridded potential evapotranspiration (PET) and PET with interception correction (PETI) derived from UKCP18 Regional Climate Model (RCM) output at 12 km resolution over the UK for 1980–2080 under RCP8.5.
- Two variables provided: daily total PET (kg m-2 d-1) and daily total PETI (kg m-2 d-1).
- PET is calculated with the Penman-Monteith equation for a well-watered grass surface; PETI includes interception corrections on days with precipitation.
- PET and PETI align with MORECS v2.0 for historical consistency; calculations parameterised accordingly.

## Data lineage and inputs
- Input data: UKCP18 RCM regional projections on a 12 km grid for 1980–2080, v20190731; perturbed parameter ensemble; re-projected to the British National Grid (BNG).
- RCP scenario: 8.5 (high warming).
- Core variables (daily mean): specific humidity at 1.5 m, sea level pressure, net surface shortwave flux, net surface longwave flux, 10 m wind speed, air temperature at 1.5 m.
- PETI additionally uses daily precipitation rate.
- Ancillary data: surface altitude, atmospheric CO2 concentrations, land–sea mask.
- Calculations require surface air pressure adjusted from sea level to grid altitude.

## Methodology: PET and PETI calculations
- PET: computed daily using Penman–Monteith with parameters for a well-watered grass surface; several inputs derived from UKCP18 outputs (e.g., saturation humidity, air density, total net radiation, aerodynamic resistance).
- Stomatal resistance adjusted for increasing CO2; canopy height set to 0.15 m; stomatal resistance increases with CO2 to reflect stomatal closure.
- PETI: on days with precipitation, CI (canopy interception) is estimated and used to reduce PET via an interception correction; when no precipitation, PETI equals PET. Interception corrections follow MORECS v2.0 methodology, with enhancement for multiple daily precipitation events.
- All calculations performed for each ensemble member to reflect CO2-driven uncertainty in trajectories.

## Interception correction details
- CI (water intercepted by canopy) computed as a function of precipitation and leaf area index; enhanced in spring–autumn for multiple precip events.
- Evaporation from canopy water (EI) derived assuming open-water evaporation; PETI transitions back to PET when canopy dries, otherwise adjusted by CI and EI.
- On days with P > 0 and CI < EI, EP I = EP + CI(1 − EP/EI); otherwise EP I = EP.

## Land–sea filling and data preparation
- Some grid boxes are modeled as sea but contain land fractions; PET and PETI are filled by copying values from the nearest comparable land grid box to ensure usable inputs for higher-resolution hydrological models.
- This approach avoids using unrepresentative meteorology over sea for hydrological disaggregation.

## File format, structure, and data organization
- Format: netCDF, CF Metadata Conventions v1.8 and ACDD v1-3.
- Data are provided as daily mean values, 1980-12-01 to 2080-11-30 (calendar aligned to the input climate data).
- Data organized in decadal files; naming structure includes ensemble member, variable (pet or peti), grid resolution (uk_12km), and time span.
- Spatial information: 12 km resolution, aligned to British National Grid (EPSG:27700); WGS84 (EPSG:4326) coordinates provided as well.
- Known ArcGIS reading caveat: projected-datum mismatches can cause small positional offsets; adjust using ArcGIS tools if needed.

## Time and calendar considerations
- Time coordinate uses a 360-day artificial calendar (12 months × 30 days) matching the underlying climate model; caution when comparing with Gregorian or 365-day calendars.

## Usage and interoperability
- Dataset intended for hydrological modelling and environmental assessment; PETI is designed to be consistent with MORECS v2.0 historical data for comparability.
- Ensemble-based approach captures uncertainty in CO2 trajectories and model parameterisations.
- Re-projection to BN grid supports integration with UK hydrological and land-surface models.

## Access, storage, and acknowledgement
- Data derived under the Hydro-JULES programme; supported by Natural Environment Research Council (NE/S017380/1).