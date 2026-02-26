# High-resolution hydraulic parameter maps for surface soils in tropical South America

- Six sets of files related to surface soils in tropical South America, intended for use in soil hydraulic modelling and land-surface models.
- Parameters are derived from pedotransfer functions (PTFs) that estimate unavailable soil variables from more accessible properties (e.g., texture, bulk density).
- Parameter maps are provided as raster GeoTIFF and NetCDF at 15 arc-second resolution (~450 m at the Equator), with NetCDF files conforming to Climate and Forecast (CF) conventions.

## Data content and formats

- GeoTIFF and NetCDF raster maps for all listed soil quantities at 15 arc-sec resolution.
- NetCDF files adhere to CF conventions, facilitating interoperability with common modelling tools.
- Data structure packages are delivered as a ZIP containing both GeoTIFF and NetCDF variants.

## Variables and parameters

- General set:
  - λ (dimensionless)
  - B (= 1/λ)
  - Air-entry (bubbling) pressure ψ_e (Pa or m pressure head)
  - Saturated soil water content θ_sat (cm³/cm³)
  - Saturated soil hydraulic conductivity k_sat (mm/s)
- Additional set (where applicable):
  - θ_res (residual soil water content, cm³/cm³)
- PTF-based parameters (Hodnett & Tomasella, 2002):
  - n (dimensionless)
  - α (per meter or per Pa)
  - θ_sat
  - θ_res
- File-level naming examples (in the ZIP):
  - geotiff CosbyB, Cosbyksat, Cosbylambda, Cosbypsiem, CosbypsiePa, Cosbythsat
  - geotiff HT (HTalphaperm, HTaphaperPa, HTn, HTthres, HTthsat)
  - geotiff TH (THB, THlambda, THpsiem, THpsiePa, THthres, THthsat)
  - netcdf.Cosby, netcdf.HT, netcdf.TH (analogous variable sets)

## Methodology and references

- Based on pedotransfer functions to estimate soil hydraulic properties from more accessible soil properties.
- Key reference points:
  - Cosby et al. (1984): statistical relationships between soil moisture characteristics and physical properties.
  - Hodnett & Tomasella (2002): tropical-specific PTFs offering more sophisticated retention parameter estimates than texture-based PTFs.
  - Marshall, Holmes, & Rose (Soil Physics, 1996): foundational soil physics context.
  - Tomasella & Hodnett (1998): estimating water-retention characteristics from limited data in tropical contexts.

## Use cases and practical considerations

- Suited for feeding high-resolution hydraulic parameters into land surface models and climate/eco-physiology analyses.
- Enables analysis of water movement through the soil matrix under tropical conditions at a finer scale than coarser global datasets.
- Important considerations for analysts:
  - The parameters are PTF-derived and carries uncertainties inherent to the underlying soil data and tropical soil variability.
  - 450 m resolution may still be smoothing local heterogeneity; local validation recommended.
  - Data accessibility is enhanced by CF-compliant NetCDF and standard GIS formats (GeoTIFF).
  - Ensure awareness of administrative boundaries and regional specificity when aggregating or downscaling results.

## Metadata, provenance, and data management

- Datasets are designed to be discoverable and usable via standard metadata practices; NetCDF CF compliance supports reproducibility and interoperability.
- Clear file naming and structured data organization (Cosby, HT, TH groups) aid in provenance tracking and reuse.
- Encourages tracking of data sources and referencing in analyses and publications.