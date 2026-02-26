# High-resolution hydraulic parameter maps for surface soils in tropical South America

## Overview
- Six sets of files for surface soils in tropical South America.
- Provide hydraulic model parameters for fine-scale water movement in soils, derived from pedotransfer functions (PTFs) using soil properties such as texture and dry bulk density.
- Aimed at use within land surface models and environmental analyses to simulate hydrology and soil moisture dynamics.

## Data content and formats
- Parameter maps available as raster GeoTIFF and NetCDF at 15 arc-sec resolution (≈450 m at the Equator).
- NetCDF files conform to Climate and Forecast (CF) conventions.
- Key variables (typical PTF outputs):
  - λ (dimensionless) and B (= 1/λ)
  - Air-entry (bubbling) pressure ψe (Pa or m pressure head)
  - Saturated soil water content θsat (cm³/cm³)
  - Saturated soil hydraulic conductivity ks (mm/s)
- Tropical PTF variant (based on Hodnett & Tomasella, 2002) including:
  - n (dimensionless) and α (per meter or per Pa)
  - θsat and θres (residual water content)
- Data structure includes packages such as:
  - geotiff.Cosby, CosbyB, Cosbyksat, Cosbylambda, Cosbypsiem, CosbypsiePa, Cosbythsat
  - netcdf.Cosby, CosbyB, Cosbylambda, Cosbypsiem, CosbypsiePa, Cosbythsat
  - similarly for HT and TH groups
- References informing the parameter choices:
  - Marshall et al. (1996); Hodnett & Tomasella (2002); Tomasella & Hodnett (1998); Marthews et al. (2014).

## Provenance and usage notes
- Grounded in established soil physics literature for tropical soils; parameters align with standard soil water retention and hydraulic conductivity concepts used in land surface modeling.
- Suitable for integration into broader environmental analyses and policy-relevant monitoring when combined with complementary datasets.

## Accessibility and standards
- Six data sets prepared for standardized access, with clear naming conventions for Cosby, HT, and TH variants.
- GeoTIFF and NetCDF formats support easy integration into GIS and modeling workflows; NetCDF files adhere to CF conventions for interoperability.

## Relevance for environmental monitoring
- Enables consistent, high-resolution estimation of soil hydraulic properties across tropical South America.
- Supports simulations of infiltration, drainage, soil moisture, and related hydrological processes essential for ecosystem health assessments and policy performance tracking.

## Reuse and value enhancement
- Designed to increase data value beyond single-use by enabling combination with other environmental datasets, with standardized formats and accessible storage notes to facilitate broader reuse.