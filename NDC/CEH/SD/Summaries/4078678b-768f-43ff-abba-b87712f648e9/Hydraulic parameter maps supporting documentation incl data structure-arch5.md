# High-resolution hydraulic parameter maps for surface soils in tropical South America

- Six sets of files related to surface soils in tropical South America are provided.
- Purpose: support soil hydraulic modeling in land surface models by supplying parameter maps derived from soil profile data using pedotransfer functions (PTFs), which estimate unavailable soil variables from related properties (e.g., texture, dry bulk density).
- Formats and resolution: parameter maps available in GeoTIFF and NetCDF formats at 15 arc-seconds (~450 m at the equator); NetCDF files conform to Climate and Forecast (CF) conventions.

## Data content and scope

- Parameters and maps cover all soil quantities used in fine-scale hydraulic models.
- Based on established PTF frameworks, including tropical-specific methods (e.g., Hodnett & Tomasella 2002; other classical references cited).
- General references for context: Marshall et al. (1996) and Marthews et al. (2014); additional methodological notes from Tomasella & Hodnett (1998).

## Variables and models

- Core soil hydraulic parameters (GeoTIFF/NetCDF):
  - λ (dimensionless)
  - B (equal to 1/λ)
  - Air-entry (bubbling) pressure ψe (Pa or m pressure head)
  - θsat (saturated volumetric water content)
  - ksat (saturated hydraulic conductivity)

- Additional parameters (as applicable, varied by dataset):
  - n (van Genuchten shape parameter)
  - α (m⁻¹ or Pa⁻¹ form)
  - θres (residual soil water content)

- Data are framed around tropical soil contexts using the Hodnett & Tomasella (2002) and related tropical PTFs, with detailed parameter sets and relationships described in the accompanying references.

## Data structure and file organization

- Data are packaged as six sets of files, with consistent naming patterns indicating source methods:
  - Cosby series (CosbyB, Cosbyksat, Cosbylambda, Cosbypsiem, CosbypsiePa, Cosbythsat)
  - HT series (HTalphaperm, HTaphaperPa, HTn, HTthres, HTthsat)
  - TH series (THB, THlambda, THpsiem, THpsiePa, THthres, THthsat)
- File formats within the archive:
  - geotiff.Cosby, netcdf.Cosby for the Cosby method
  - geotiff.HT, netcdf.HT for the HT method
  - geotiff.TH, netcdf.TH for the TH method
- Each set contains maps corresponding to the listed parameters, suitable for ingestion into spatial analysis or land surface models.

## Documentation and provenance

- Documentation references provide context for parameter definitions and usage:
  - Marshall, Holmes, and Rose (Soil Physics, 1996)
  - Hodnett & Tomasella (2002) on tropical soil water-retention parameters
  - Tomasella & Hodnett (1998) on estimating water retention characteristics from limited data
  - Marthews et al. (2014) related to the broader context of soil hydraulic parameters
- The dataset enables reproducibility by aligning with CF conventions for NetCDF and by detailing the parameter structure and source PTFs.

## Governance, stewardship, and usage considerations

- Relevance to Data Stewards: supports data governance for large collections by providing standardized, interoperable parameter maps (GeoTIFF and CF-compliant NetCDF) suitable for discovery, sharing, and reuse.
- Metadata and standards:
  - NetCDF files adhere to CF conventions, aiding interoperability.
  - Clear documentation of parameter definitions, units, and relationships is essential to ensure discoverability and proper use.
- Data sharing and updates:
  - Maintain awareness of model-specific parameter definitions and tropical PTF bases when updating or distributing subsequent versions.
  - Ensure that any data creators’ workflows align with established standards (accurate metadata, consistent naming, and proper format selections).
- Accessibility and use in practice:
  - Useful for researchers and practitioners implementing land surface models requiring high-resolution soil hydraulic parameters in tropical regions.
  - The archive structure and covered variables support integration into data catalogs and model pipelines, subject to licensing and access terms of the archive.