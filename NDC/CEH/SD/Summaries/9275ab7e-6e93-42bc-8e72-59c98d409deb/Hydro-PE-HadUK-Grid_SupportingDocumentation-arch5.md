# Potential evapotranspiration derived from HadUK-Grid 1km gridded climate observations 1969-2021 (Hydro-PE HadUK-Grid) Supporting information

## Overview
- Gridded potential evapotranspiration (PET) with two variables: PET and PETI (interception-corrected PET).
- 1 km resolution over the UK, daily values for 1969–2021; PET calculated with Penman-Monteith for a well-watered grass surface.
- PETI adjusts PET on days with rainfall to account for canopy interception.
- Based on HadUK-Grid input data (v1.0.3.0 for 1969–2020 and v1.1.0.0 for 2021); aims for hydrological modelling consistency with MORECS v2.0.

## Data inputs and parameters
- Primary input: HadUK-Grid data (1969–2020 v1.0.3.0; 2021 v1.1.0.0) on a 1 km UK grid.
- Required variables (monthly, interpolated to daily): monthly mean water vapour pressure (pv), monthly mean sea level pressure (psl), monthly sunshine hours (sun), monthly mean wind speed at 10 m (u10), daily max/min temperatures (tasmax, tasmin).
- For PETI: daily precipitation (rainfall, P).
- Ancillary data: surface altitude (EU-DEM v1.1), Ångström coefficients (a, b, c).
- Daily time-step is produced by quadratic interpolation of monthly data; end-of-series handling preserves continuity when new years are added.
- Calculation inputs derived from HadUK-Grid data and additional parameterisations from MORECS v2.0 to ensure comparability.

## Calculations and dataset structure
- PET calculated via Penman-Monteith with parameters for a well-watered grass surface.
- PETI computed by applying interception correction on precipitation days, accounting for canopy interception and faster evaporation; if canopy interception exceeds PETI adjustments, PETI is set accordingly.
- Derived quantities include specific humidity, air density, net radiation (shortwave + longwave) from sunshine, temperature, and humidity, and aerodynamic/canopy resistances following MORECS v2.0.
- Daily PET and PETI values are based on daily mean temperature (averaging tasmax and tasmin with sampling rules for day boundaries).

## Interpolation and time-series handling
- Monthly values interpolated to daily using quadratic interpolation (assumes mid-month timestamps).
- To avoid retroactive changes when new years are added, the last year of existing daily data is merged with new monthly data and interpolated within that combined period; this preserves old data while adding new continuity, though the end of the old timespan remains an extrapolation.

## File format, spatial and time information
- Format: netCDF files complying with CF Metadata Conventions v1.8 and ACDD v1-3; daily mean values stored in monthly files for each variable (pet or peti, one file per year).
- Spatial information: 1 km grid aligned to British National Grid (BNG), projection EPSG:27700. WGS84 coordinates (EPSG:4326) are also provided.
- Time information: daily mean values from 1969-01-01 to 2021-12-31; monthly inputs interpolated to daily with mid-month timestamps.

## Data governance and stewardship considerations
- Provenance: explicit linkage to HadUK-Grid input data versions and MORECS v2.0 parameterisations.
- Versioning and updates: dataset updated with new HadUK-Grid years; older daily values preserved to maintain reproducibility, with continuity maintained by combining the last old year with new monthly data during interpolation.
- Metadata and discoverability: CF/ACDD-compliant metadata; clear documentation of input variables, calculation methods, and interpolation steps; spatial reference and known ArcGIS reading issue documented.
- Data quality and limitations: potential negative pv/sun values are corrected to zero post-interpolation; ArcGIS coordinate offset requires adjustment; interpolation may introduce small end-of-series extrapolations.
- Reuse and interoperability: PET and PETI aligned with MORECS v2.0 methodologies to support hydrological modelling and cross-dataset compatibility.

## Acknowledgements and references
- Supported by Natural Environment Research Council (NE/S017380/1) as part of the Hydro-JULES programme.
- References include MORECS v2.0, HadUK-Grid, EU-DEM, and Brutsaert/Linacre methodologies for long-wave and net radiation calculations.