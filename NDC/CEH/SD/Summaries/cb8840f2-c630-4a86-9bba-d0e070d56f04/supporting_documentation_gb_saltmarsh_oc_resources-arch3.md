# Supporting document for: GB_saltmarsh_OC_resources.zip

## Overview
- Describes spatial mapping of surficial (top 10 cm) soil organic carbon (OC) storage and OC stocks across 438 Great British saltmarshes, covering 451.65 km2.
- Part of the Carbon Storage in Intertidal Environments (C-SIDE) project; data resource integrates OC data, vegetation maps, and saltmarsh extents to quantify carbon storage.
- Geographic scope spans Great Britain (Scotland, England, Wales) using decoupled data sources from UK-wide mapping efforts.

## Dataset and variables
- Primary output: Saltmarsh surficial soil OC stock (tonnes OC) and OC density (kg OC m-2) for the top 10 cm.
- Locations and structure: Observations/observations grid described by sample location (latitude/longitude and X/Y), and marsh area (km2) for 438 marshes.
- Vegetation/classification: OC calculations performed for each class of saltmarsh vegetation and marsh zone (NVC-based classes).
- Data inputs: OC content (% wt.) and dry bulk density (kg m-3) for surficial soils from NERC C-Side and Marine Scotland data; saltmarsh extents and zonation from Environment Agency (England), Haynes (Scotland), Natural Resources Wales.
- Outputs: Bespoke GIS layers mapping OC storage across GB saltmarsh soils to a 10 cm depth, including OC storage (kg OC m-2) and total stock (tonnes OC).

## Methodology and analysis
- Calculation approach: Stock and storage values are derived by combining mean OC storage per NVC class/marsh zone with existing saltmarsh mappings.
- Data processing: Calculations performed within a Monte Carlo framework to propagate uncertainty.
- Monte Carlo details: 1,000,000 samples drawn from a distribution (out of 100,000,000 total) for variables such as area, OC content, and dry bulk density to populate stock calculations.
- QA and calibration: Calibration procedures and data checking entries are marked as NA in the resource.

## Data sources and provenance
- OC content and dry bulk density: NERC C-Side project (Ruranska et al., 2020, 2022) and related 2019–2022 English and Welsh data.
- Physical/geochemical context: Marine Scotland data (Miller et al., 2022).
- Saltmarsh extent and zonation: England (Environment Agency, 2021); Scotland (Haynes, 2016); Wales (Natural Resources Wales, 2016).
- Software/tools: ESRI ArcGIS used for GIS processing.

## Geographic scope and formats
- Geographic coverage: Great Britain (Scotland, England, Wales).
- Spatial reference: OSGB 1936.
- File formats: Shapefiles with associated metadata (.cpg, .dbf, .prj, .sbn, .sbx, .shp, .shx).

## Relevance for monitoring frameworks
- Provides a spatially explicit, policy-relevant indicator of surficial OC storage across saltmarshes to support monitoring of carbon storage in intertidal environments.
- Enables tracking of OC stocks by marsh zone and vegetation class, facilitating evaluation of conservation/restoration policies and climate-related decision making.
- Data are anchored in published, peer-reviewed data sources and national scale maps, aiding comparability and integration into broader environmental health metrics.

## Limitations and governance considerations
- Some data quality checks and calibration steps are marked NA, indicating potential metadata gaps.
- Public sharing and data governance aspects are not fully detailed within the resource; users may need to verify metadata completeness and provenance for reuse.
- Regional data integration relies on multiple public maps and datasets, which may have differing update cycles and resolutions.