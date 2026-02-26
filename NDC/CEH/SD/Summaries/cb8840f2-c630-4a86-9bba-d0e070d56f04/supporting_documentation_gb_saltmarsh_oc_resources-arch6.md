# Supporting document for: GB_saltmarsh_OC_resources.zip

## Overview
- Describes a spatial dataset mapping surficial organic carbon (OC) storage and stocks in Great British saltmarshes (top 10 cm).
- Integrates OC density data and bulk density with existing saltmarsh vegetation maps to produce GIS layers of OC storage to 10 cm depth.
- Covers 451.65 km2 across 438 saltmarshes in Great Britain (Scotland, England, Wales).

## Data resource at a glance
- Data resource ID: Spatial mapping of surficial (top 10 cm) soil OC storage and stocks across Great British saltmarshes.
- Key outputs: OC storage density (kg OC m-2) and OC stocks (tonnes OC) for surficial soils.
- Locations: Observations mapped across Great Britain with decimal degrees and projected coordinates (X/Y).

## Spatial scope and structure
- Geographic coverage: Great Britain (Scotland, England, Wales) saltmarshes.
- Area mapped: 451.65 km2, including 438 individual marshes with OC stock estimates.
- Output format: GIS-compatible layers with OC storage by saltmarsh class/zone and vegetation type.

## Variables and measurements
- Primary variables:
  - Saltmarsh surficial soil OC stock (tonnes OC) per marsh
  - Organic Carbon Storage (kg OC m-2) for the top 10 cm
  - Marsh area (km2)
- Observational basis: OC content (%) and dry bulk density (kg m-3) for surficial soils, from NERC C-Side and Marine Scotland data.
- Vegetation/zone classes: Mean OC storage calculated per each NVC class or marsh zone, combined with national saltmarsh maps to produce layer-specific OC storage.

## Processing and analysis
- Calculation approach: Stock and storage determined for each vegetation/zone class using OC content and bulk density data.
- Dataset assembly: Combines species/zone maps with OC density estimates to generate GB-wide OC storage maps to 10 cm depth.
- Statistical handling: Monte Carlo Markov Chain (MCMC) framework used for stock calculations, sampling 1,000,000 draws from a larger 100,000,000-sample pool per variable (area, OC content, bulk density, etc.).

## Data quality and validation
- Calibration: Not applicable (NA).
- Data checking: Not described (NA).
- QA note: The MCMC approach provides probabilistic stock estimates, but explicit QA steps are not detailed in the record.

## Data formats and software
- Core file formats: Shapefile components (.shp, .shx, .dbf, .prj, .sbn, .sbx, .cpg) indicating GIS-ready spatial data.
- Projection: OSGB 1936 (British National Grid).
- Software: ESRI ArcGIS.

## Provenance and references
- Project: Carbon Storage in Intertidal Environments (C-SIDE).
- Funding: NERC (NE/R010846/1).
- Staff responsible: Craig Smeaton (University of St Andrews).
- Research team includes multiple institutions (University of St Andrews, UK Centre of Ecology and Hydrology, University of Glasgow, University of York, Bangor University).
- Key references/supporting datasets include:
  - Environment Agency (2021) Saltmarsh extent and zonation
  - Haynes (2016) Scottish saltmarsh survey
  - Natural Resources Wales (2016) Saltmarsh extent
  - Ruranska et al. (2020, 2022) surficial soil OC content and bulk density
  - Miller et al. (2022) Scottish saltmarsh soils

## Potential data products and use-cases for data support
- Create self-serve tools (dashboards, pivot analyses) for exploring OC storage by marsh, NVC class, or zone.
- Enable cross-dataset comparisons by integrating with other saltmarsh datasets or carbon datasets at the topsoil layer.
- Inform conservation and policy by quantifying spatially explicit OC stocks and densities across GB saltmarshes.
- Support scenario analyses using the MCMC-derived stock estimates to assess uncertainties in OC storage.

## Limitations and notes for reuse
- Explicit data quality checks are not documented (NA).
- Calibration details are not provided beyond the MCMC framework.
- Outputs reflect top 10 cm soil OC; deeper profiles not included.