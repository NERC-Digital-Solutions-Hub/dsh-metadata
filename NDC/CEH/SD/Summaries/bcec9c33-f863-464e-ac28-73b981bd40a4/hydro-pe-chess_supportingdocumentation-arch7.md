# Potential evapotranspiration derived from Climate Hydrology and Ecology Research Support System Meteorological gridded climate observations (Hydro-PE CHESS), 1961-2019 Supporting information

## Overview
- Dataset of two potential evapotranspiration (PET) variables for Great Britain on a 1 km grid (1961–2019).
  - PET: daily total potential evapotranspiration (kg m^-2 d^-1, equivalent to mm d^-1).
  - PETI: PET with interception correction (kg m^-2 d^-1, equivalent to mm d^-1).
- Derived from the CHESS-met meteorology dataset using an adaptation of the Hydro-PE method.
- PET calculated with Penman-Monteith for a well-watered grass surface; PETI includes canopy interception corrections consistent with MORECS v2.0.
- Intended for hydrological modelling and GIS-based analysis.

## Data generation and methodology
- Inputs:
  - CHESS-met dataset (Great Britain, 1961–2019) interpolated from MORECS 40 km to a 1 km grid.
  - Daily mean values of: air temperature (tas), specific humidity (huss), air pressure (psurf), wind speed (sfcWind), downwelling shortwave (rsds) and longwave (rlds) radiation.
  - For PETI: daily total precipitation (prec) from 0900 UTC day D to 0900 UTC day D+1.
- Penman-Monteith calculation:
  - Uses daily mean CHESS-met variables.
  - Parameters set for a well-watered short grass surface.
  - Derived quantities include specific humidity at saturation, air density, total net radiation, and aerodynamic resistance.
  - Calculations align with MORECS v2.0 parameterisations where applicable.
- Interception correction (PETI):
  - On non-precipitation days: PETI = PET.
  - On precipitation days: interception water is canopy-intercepted water (CI) with enhanced interception in spring/summer/autumn; canopy evaporation rate (EI) derived assuming open-water-like evaporation until canopy dries, then PETI reverts to PET.
  - PETI formula accounts for CI and EI relative to PET.
- Output units and interpretation:
  - PET and PETI units: kg m^-2 d^-1, equivalent to mm d^-1.

## Data format and structure
- File format: NetCDF (CF Metadata Conventions v1.8, ACDD v1-3).
- Temporal format: daily mean values.
- Storage: monthly NetCDF files; one file per variable (PET or PETI).
- Variables included in NetCDF:
  - pet or peti (the data variable)
  - time, time_bnds
  - crsOGB (OSGB 1936 / British National Grid)
  - x, x_bnds (easting, grid cell bounds)
  - y, y_bnds (northing, grid cell bounds)
  - lat, lon (grid cell centers)
- Spatial information:
  - Grid: 1 km resolution, aligned to British National Grid (BNG) / OSGB 1936.
  - Projection: EPSG:27700.
  - Coordinates: eastings/northings in metres; also provided as lat/lon in WGS84 (EPSG:4326).
- Known data-read issue:
  - ArcGIS may offset layers due to datum handling when reading projected CF-compliant files; manual adjustment in ArcGIS is recommended.

## Spatial and temporal coverage
- Spatial: Great Britain, 1 km grid.
- Temporal: daily mean values from 1961-01-01 to 2019-12-31.

## Applications for GIS and data users
- Suitable for GIS-based hydrological modelling and spatial analysis of evapotranspiration.
- Can be integrated with other gridded datasets on the same 1 km UK grid (BNG projection) for model inputs, scenario analyses, or policy-oriented maps.
- Ensure proper projection handling (BNG) and, if needed, reproject to your GIS project’s coordinate system.
- Use PETI where canopy interception effects are relevant; otherwise PET provides the well-watered baseline evapotranspiration.

## Acknowledgements and references
- Supported by Natural Environment Research Council (NE/S017380/1) as part of the Hydro-JULES programme.
- Key references include Hough (1995) MORECS v2.0, Richards (1971) for saturation humidity, and Robinson et al. (2023) Hydro-PE/CHESS-met context.