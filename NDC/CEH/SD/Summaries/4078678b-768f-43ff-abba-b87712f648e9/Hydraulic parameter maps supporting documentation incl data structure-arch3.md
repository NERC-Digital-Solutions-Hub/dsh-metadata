# High-resolution hydraulic parameter maps for surface soils in tropical South America

- Six sets of files related to surface soils in tropical South America are provided.
- Purpose: deliver parameter maps for fine-scale soil hydraulic models that drive land surface models, enabling representation of water movement through the soil matrix.
- Pedotransfer functions (PTFs) are used to derive hydraulic parameters from more readily available soil properties (e.g., texture, dry bulk density), with tropical-specific PTFs referenced.

## Data content and structure

- Parameter maps are available for all soil quantities in raster GeoTIFF and NetCDF formats at 15 arc-second resolution (about 450 m at the Equator).
- NetCDF files conform to the Climate and Forecast (CF) conventions.
- Two main parameterization approaches are included:
  - Cosby-based parameters (CosbyB, Cosbyksat, Cosbylambda, Cosbypsiem, CosbypsiePa, Cosbythsat) corresponding to the Cosby et al. (1984) framework.
  - Hodnett & Tomasella (HT) and Tomasella & Hodnett (TH) variants (HTalphaperm, HTaphaperPa, HTn, HTthres, HTthsat; THB, THlambda, THpsiem, THpsiePa, THthres, THthsat).
- The archive also includes equivalent sets addressing specified tropical soil water retention characteristics (e.g., n, α, θ_sat, θ_res) derived from tropical PTFs (Hodnett & Tomasella 2002; Tomasella & Hodnett 1998).
- Data structure in the zip file includes:
  - geotiff.Cosby*, geotiff.HT*, geotiff.TH* (GeoTIFF files)
  - netcdf.Cosby*, netcdf.HT*, netcdf.TH* (NetCDF files)

## Variables and parameterizations

- Cosby parameter set (example variables):
  - λ (dimensionless), B (1/λ), ψ_e (air-entry pressure in Pa or m), θ_sat (saturated water content), k_sat (saturated hydraulic conductivity)
- Tropical PTF-based sets (HT/TH) include:
  - α (or related parameters), n, θ_sat, θ_res, and threshold/sat parameters as applicable
- The documentation references standard sources for interpretation of these parameters:
  - Marshall, Holmes, and Rose (Soil Physics, 1996)
  - Cosby et al. (1984)
  - Hodnett & Tomasella (2002)
  - Tomasella & Hodnett (1998)

## Data provenance, standards, and references

- Parameters are derived from well-known pedotransfer functions for tropical soils, enabling estimation of soil-water retention and hydraulic conductivity characteristics from limited soil data.
- Key references:
  - Cosby, Hornberger, Clapp, Ginn (1984)
  - Hodnett, Tomasella (2002)
  - Tomasella, Hodnett (1998)
  - Marshall, Holmes, Rose (Soil Physics, 1996)

## Access, usage, and governance

- Formats provided: GeoTIFF and NetCDF (CF-conformant for NetCDF) to support interoperability with common environmental monitoring and modeling tools.
- The CF-conformant NetCDF files facilitate cross-dataset comparability and integration into monitoring frameworks and model evaluation workflows.
- Metadata and provenance are embedded via the standard data products and referenced literature, aiding traceability and reproducibility.
- The data are suitable for informing monitoring decisions, model parameterization, and scenario analysis related to soil water movement in tropical surface soils.

## Relevance for monitoring frameworks

- Provides high-resolution, standardized soil hydraulic parameters essential for evaluating and improving hydrological and land-surface models in tropical regions.
- Facilitates transparency and reproducibility through open formats and clearly defined parameterization schemes.
- Enables cross-disciplinary use (soil science, hydrology, climate modeling) by offering multiple parameter sets (Cosby, HT, TH) and clearly documented references.

## Considerations, limitations, and caveats

- Parameters are derived from pedotransfer functions; accuracy depends on the quality and representativeness of the input soil properties and the tropical PTFs used.
- Different parameterization schemes (Cosby vs. HT/TH) may yield different outcomes; users should select the approach appropriate to their application and acknowledge structural differences.
- While metadata and standard formats support data governance and sharing, users should assess ongoing data updates, provenance, and compatibility with other datasets in their monitoring framework.