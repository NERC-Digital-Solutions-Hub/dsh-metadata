# High-resolution hydraulic parameter maps for surface soils in tropical South America

## Overview
- Presents six sets of files related to surface soils in tropical South America.
- Provides parameter maps for soil hydraulic models that drive water movement through the soil matrix.
- Parameters derived from pedotransfer functions (PTFs) using related soil properties (e.g., texture, dry bulk density).

## Data and formats
- Available as raster GeoTIFF and NetCDF formats.
- Spatial resolution: 15 arc-second (approximately 450 m at the equator).
- NetCDF files conform to Climate and Forecast (CF) conventions.
- Data structure includes multiple parameter families packaged in a single archive.

## Variables and methods
- Core hydraulic parameters (per standard soil hydraulic modeling):
  - λ (dimensionless) and B (= 1/λ)
  - Air-entry (bubbling) pressure ψe (Pa or meters of pressure head)
  - Saturated soil water content θsat (cm³/cm³)
  - Saturated hydraulic conductivity ksat (mm/s)
- Additional parameters (from Hodnett & Tomasella tropical PTFs):
  - n (dimensionless), α (in 1/m or 1/Pa), θres (cm³/cm³)
- Data sets included:
  - Cosby (CosbyB, Cosbyksat, Cosbylambda, Cosbypsiem, CosbypsiePa, Cosbythsat)
  - HT (HTalphaperm, HTaphaperPa, HTn, HTthres, HTthsat)
  - TH (THB, THlambda, THpsiem, THpsiePa, THthres, THthsat)
- Each set exists in both GeoTIFF and NetCDF formats.
- Key literature for parameter relationships and PTFs cited (e.g., Cosby et al. 1984; Hodnett & Tomasella 2002; Tomasella & Hodnett 1998; Marshall et al. 1996; Marthews et al. 2014).

## Data structure and access
- Zip archive contains organized groups by parameter family (Cosby, HT, TH) across GeoTIFF and NetCDF formats.
- Documentation links to supporting references for interpretation of parameters and PTF methods.
- Designed to support integration with other data layers (e.g., texture, density) for comprehensive soil hydrology analyses.

## Usage and applications
- Facilitates high-resolution soil hydraulic modeling in tropical South America.
- Enables researchers and practitioners to build self-serve data products for land-surface and hydrological simulations.
- NetCDF CF-compliant data aid interoperability, while GeoTIFFs support straightforward GIS visualization.
- Useful for combining with ancillary data (soil texture, bulk density) to derive site-specific soil-water characteristic curves.

## References and context
- Marshall, Holmes, and Rose (Soil Physics; 1996)
- Hodnett & Tomasella (2002) tropical soil water-retention PTFs
- Tomasella & Hodnett (1998) Estimating soil water retention characteristics
- Cosby et al. (1984) Relationships of soil moisture characteristics to soil properties
- Marthews et al. (2014) associated publications and context