# (Hydro-PE HadUK-Grid) Supporting information

## Overview
- Gridded potential evapotranspiration calculated on a 1 km UK grid for 1969–2022, with two variables:
  - PET: daily total potential evapotranspiration (kg m-2 d-1)
  - PETI: daily total PET with interception correction (kg m-2 d-1)
- Derived from the HadUK-Grid dataset (v1.0.3.0 for 1969–2020; v1.1.0.0 for 2021; v1.2.0 for 2022)
- PET and PETI calculated using Penman-Monteith for a well-watered grass surface
- PETI includes interception by canopy on days with precipitation
- Dataset expanded to include 2022; corrections and minor bugs addressed from previous versions
- Intended for hydrological modelling and compatibility with MORECS v2.0 parameterisations

## Data and file format
- Format: NetCDF, CF Metadata Conventions v1.8; ACDD v1-3 compliant
- Structure: daily mean values (1969-01-01 to 2022-12-31), with monthly inputs interpolated to daily
- Spatial grid: 1 km resolution, aligned to British National Grid (EPSG:27700); WGS84 lat/lon provided (EPSG:4326)
- Time information: daily means; monthly data interpolated to daily using quadratic interpolation
- File organization: daily data stored in monthly NetCDF files per variable; file naming follows a defined structure (document notes a specific naming pattern)

## Variables and inputs
- PET and PETI computed from:
  - Monthly mean water vapour pressure (pv), mean sea level pressure (psl), sunshine hours (sun)
  - Daily wind speed at 10 m (sfcWind)
  - Daily max/min air temperatures (tasmax, tasmin)
  - Daily precipitation (rainfall) for PETI
  - Ancillary data: surface altitude (EU-DEM v1.1), Ångström coefficients (a, b, c)
- Interpolation inputs (monthly to daily): quadratic interpolation
- Derived quantities and additional inputs:
  - Surface air pressure adjusted to grid altitude and converted to Pa
  - Net radiation (shortwave and longwave) derived from sunshine hours, temperature, vapour pressure
  - Aerodynamic resistance and canopy resistance computed per MORECS v2.0 conventions
  - Parameters for grass surface (well-watered) used in Penman-Monteith

## Calculation methodologies
- Penman-Monteith equation used to compute EP (PET) with day-mean temperature and daily interpolated values for other inputs
- Key adjustments to align with MORECS v2.0:
  - Temperature averages: mean daily temperature from tasmax and tasmin
  - Specific humidity and its gradients derived from temperature and pressure
  - Air density from temperature and pressure
  - Net radiation from shortwave and longwave components
  - Aerodynamic resistance based on wind speed and canopy height (0.15 m)
  - Canopy resistance derived from stomatal and soil surface resistances
- PETI (interception-corrected PET) procedure:
  - On non-precipitation days, PETI = PET
  - On precipitation days, canopy interception water CI is evaporated at E_I; PETI adjusts with CI and potential interception rate
  - Special handling to avoid negative/intermediate NaN values in certain edge cases
- Interception correction details follow MORECS v2.0, with daily adjustments for multiple precipitation events

## Interpolation and data integrity considerations
- Quadratic interpolation treats each gridbox’s entire un-interpolated monthly time series for daily interpolation
- To avoid inconsistencies when updating with new years of HadUK-Grid data:
  - The last year of existing daily data is kept, and interpolation is redone only on the new monthly data appended to it
  - This preserves continuity at the end of the old timeseries, though the tail remains extrapolated

## Known issues and data quality updates
- Missing data and zero-wind issues in prior versions:
  - 0 wind speed during monthly-to-daily interpolation caused division-by-zero in PET; fixed by flooring 0 wind to the minimum non-zero daily wind
  - Missing data over St Kilda fixed by linear time interpolation of monthly data
- PETI-specific minor bugs:
  - Edge cases where PEI equals zero or is negative (condensation) could yield NaNs or incorrect PETI values; fixes implemented (e.g., t_to_dry adjustments)
- Overall impact of these issues deemed minor

## Spatial and temporal information
- Spatial: 1 km grid aligned to EPSG:27700; latitude/longitude provided in EPSG:4326
- Time: daily mean values from 1969-01-01 to 2022-12-31
- Data availability reflects the HadUK-Grid updates; input data cover 1862–2022, but PET/PETI inputs are available from 1969 onward

## Access, references, and acknowledgments
- Supported by Natural Environment Research Council awards NE/S017380/1 and NE/X019063/1 (Hydro-JULES programme)
- References include MORECS v2.0 documentation and related HadUK-Grid data sources

## Relevance for GIS specialists
- Provides ready-to-map 1 km PET and PETI surfaces for hydrological and climate-related analyses
- Data are in a GIS-friendly, CF-compliant NetCDF format with clear spatial reference and time coverage
- Clear notes on coordinate systems, potential ArcGIS reading offset due to datum, and data update practices for maintaining spatial-temporal consistency
- Suitable for creating map-based data products and facilitating audience-friendly visualisations of evapotranspiration trends across the UK over multiple decades