# High-resolution hydraulic parameter maps for surface soils in tropical South America

## Overview
- Six sets of files providing high-resolution parameter maps for surface soils in tropical South America.
- Parameters support soil hydraulic models used in land surface modeling, derived from pedotransfer functions (PTFs) that estimate unavailable variables from more accessible soil properties (e.g., texture, bulk density).
- Data presented as maps in raster GeoTIFF and NetCDF formats at 15 arc-second resolution (~450 m at the Equator).

## Data formats and structure
- Available formats: GeoTIFF and NetCDF; NetCDF files conform to Climate and Forecast (CF) conventions.
- Data packages are organized by parameterization method:
  - Cosby parameterization (CosbyB, Cosbyksat, Cosbylambda, Cosbypsiem, CosbypsiePa, Cosbythsat)
  - HT parameterization (HTalphaperm, HTaphaperPa, HTn, HTthres, HTthsat)
  - TH parameterization (THB, THlambda, THpsiem, THpsiePa, THthres, THthsat)
- For each method, both GeoTIFF and NetCDF versions are provided:
  - geotiff.Cosby..., geotiff.HT..., geotiff.TH...
  - netcdf.Cosby..., netcdf.HT..., netcdf.TH...
- Each set contains maps for the core hydraulic parameters described below.

## Variables and parameters
- Core parameters (GeoTIFF/NetCDF formats):
  - λ (dimensionless)
  - B (equal to 1/λ)
  - Air-entry (bubbling) pressure ψe (Pa or meters of pressure head)
  - Saturated soil water content θsat (cm³/cm³)
  - Saturated hydraulic conductivity ks at (mm/s)
- Additional parameters (primarily from tropical PTFs):
  - n (dimensionless)
  - α (in 1/m or 1/Pa)
  - θres (residual soil water content, cm³/cm³)
- The dataset references Hodnett & Tomasella (2002) PTFs and other supporting literature for tropical soils.

## Data provenance and references
- General soil parameter context: Marshall et al. (1996); Marthews et al. (2014) for tropical soil work.
- Tropical PTFs and parameter relationships cited:
  - Hodnett, M. G. & Tomasella, J. (2002)
  - Tomasella, J. & Hodnett, M. G. (1998)
  - Cosby, B. J. et al. (1984)
- Data products are designed to be used in GIS workflows and climate/land-surface modeling.

## Geographic scope and resolution
- Geographic focus: surface soils in tropical South America.
- Spatial resolution: 15 arc-second (~450 meters at the equator).

## Practical use for GIS specialists
- Prepare map-based visualizations of soil hydraulic properties (e.g., moisture retention, infiltration, drainage).
- Integrate with other GIS layers to analyze hydrological processes and soil behavior in tropical regions.
- Utilize CF-compliant NetCDF files for interoperability with GIS and environmental modeling tools.
- Compare parameterizations (Cosby vs. HT vs. TH) to assess sensitivity of hydrological models to soil hydraulic parameters. 

## Considerations and caveats
- Parameters are derived from PTFs and literature; applicability may vary with local soil types and tropical conditions.
- Data quality and resolution constraints typical of pedotransfer-based products; users should validate against local observations when possible.
- Data packaging requires handling multiple parameterizations and formats; select appropriate GeoTIFF or NetCDF version for the intended GIS workflow.