# Potential evapotranspiration derived from HadUK-Grid 1km gridded climate observations 1969-2021 (Hydro-PE HadUK-Grid) Supporting information

## Overview
- Gridded daily potential evapotranspiration (PET) and PET with interception correction (PETI) at 1 km resolution across the United Kingdom for 1969–2021.
- PET is calculated with Penman–Monteith parameterised for a well-watered grass surface; PETI adds interception correction on days with precipitation.
- Data are derived from the HadUK-Grid meteorological dataset (v1.0.3.0 for 1969–2020 and v1.1.0.0 for 2021); PET and PETI calculations align with MORECS v2.0 parameterisations.

## Data Products
- Two variables:
  - PET: daily total potential evapotranspiration (kg m^-2 d^-1), equivalent to mm d^-1.
  - PETI: daily PET with interception correction (kg m^-2 d^-1).
- Intended for hydrological modelling in the UK and consistency with MORECS v2.0 history.

## Input Data and Derivation
- Input: HadUK-Grid v1.0.3.0 (1969–2020) and v1.1.0.0 (2021) on a 1 km UK grid; monthly data interpolated to daily.
- Required inputs for PET and PETI:
  - Monthly means: water vapour pressure (pv), sea level pressure (psl), sunshine hours (sun), 10 m wind speed (sfcWind), daily max/min temperatures (tasmax, tasmin).
  - Daily precipitation (P) for PETI.
  - Ancillary: surface altitude and Ångström coefficients (a, b, c).
- Calculations:
  - Penman–Monteith equation with adjustments to reflect surface conditions and MORECS-based parameterisations.
  - Daily mean temperature derived from tasmax/tasmin, with specific handling near the end of timeseries.
  - Net radiation as the sum of net shortwave and net longwave, derived from sunshine hours, temperature, and vapour pressure.
  - Aerodynamic and canopy resistances computed as prescribed by MORECS v2.0.
  - Parameters tuned for a well-watered short grass surface; several inputs are scaled or derived from the HadUK-Grid data.

## Interception Correction (PETI)
- On days with precipitation (P > 0): PETI is PET plus canopy interception adjustments.
- Intercepted water CI (kg m^-2 d^-1) calculated from precipitation and leaf area index; enhanced during spring/summer/autumn for multiple events.
- Evaporation from canopy water EI estimated by setting canopy resistance to zero, then PETI transitions back to PET once canopy is dry.

## Interpolation and Time Series Handling
- Monthly variables interpolated to daily using quadratic interpolation, with the 15th of each month treated as the timestamp.
- To avoid inconsistencies when new years are added, the last year of already-interpolated daily data is concatenated with new monthly data and interpolated as a single series, preserving the old end but introducing extrapolation there.

## Spatial and Temporal Coverage
- Spatial: 1 km grid aligned to the British National Grid (EPSG:27700); WGS84 lat/lon (EPSG:4326) provided as well.
- Temporal: daily mean values from 1969-01-01 to 2021-12-31; monthly data timestamped at mid-month.

## File Format and Access
- Files distributed as NetCDF (CF Metadata Conventions v1.8; ACDD v1-3).
- Structure: monthly NetCDF files for each variable (pet or peti) and year; naming follows a consistent scheme.
- Known caveat: reading CF-compliant files in ArcGIS may offset layers by 10–100 m due to datum assumptions; adjust using standard ArcGIS procedures.

## Data Quality, Limitations, and Consistency
- Designed to be consistent with MORECS v2.0 documentation and parameterisations.
- Handling of negative values: pv and sun may become negative due to interpolation but are reset to zero when this occurs.
- Some approximations and assumptions (e.g., net longwave using air temperature) reflect alignment with MORECS methodology.
- Interpolation introduces uncertainties, particularly at the ends of the timeseries; the method deliberately preserves continuity across year updates.

## Use, Reuse, and Acknowledgements
- Primary purpose: support UK hydrological modelling with a consistent PET/PETI dataset.
- Acknowledgements: Natural Environment Research Council (NE/S017380/1) as part of the Hydro-JULES programme.
- Key references include MORECS v2.0, HadUK-Grid documentation, EU-DEM, and foundational radiation and evapotranspiration literature.