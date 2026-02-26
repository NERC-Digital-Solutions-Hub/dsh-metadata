# Dataset documentation

## Overview
- Describes Land Cover Map 1990 (LCM1990), a UK parcel-based land cover map produced from Landsat-5 two-date composites at 30m resolution.
- Maps 21 land cover classes based on the UK Biodiversity Action Plan Broad Habitat definitions.
- Product family includes vector and raster formats (25m and 1km), designed for compatibility with later LCM versions to support long-term change analysis.
- Projections: Great Britain in British National Grid; Northern Ireland in TM75 Irish Grid.

## Data products and structure
- Vector data set
  - Approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Eight key attributes per polygon, including dominant class, class breakdown, mean confidence, and a unique geometry identifier (gid).
  - Includes per-polygon histogram of class composition (hist) and per-polygon classification confidence (conf).
- Raster data sets
  - 25m raster: three bands (dominant class per polygon, per-polygon mean confidence, percentage cover of the polygon by the modal class).
  - 1km raster (aggregates): dominant cover (21 target classes and 10 aggregate classes) plus percentage cover for both target and aggregate classes.
  - Coastal and land-water edge effects acknowledged; rounding may cause sums to deviate from 100 in 1km percentage products.
- Data formats and scale
  - Core product: LCM1990 vector; derived 25m raster; 1km percentage/dominant cover products.
  - Spatial detail and metadata trade-off: vector provides rich attributes; raster offers lighter-weight processing for certain applications.

## Class system and mapping
- 21 LCM1990 target classes aligned to Broad Habitats (JNCC Jackson, 2000).
- Some subdivisions within Broad Habitats:
  - Built-up Areas and Gardens: Urban and Suburban.
  - Dwarf Shrub Heath: Heather and Heather grassland.
  - Littoral/Habitat classes: various coastal divisions (e.g., Littoral Sediment, Saltmarsh).
- The vector attributes include a detailed hist field listing the class composition within each polygon, enabling exploration of mixed land-cover within polygons.

## Data quality, metadata, and uncertainty
- Rich metadata per polygon: dominant class, pixel counts per class, and per-polygon mean probability from the Random Forest classifier.
- Uncertainty information captured as mean per-polygon confidence (conf) and standard deviation (stdev).
- QA processes verify projections, spatial completeness, modal class presence, value ranges (0–100 for raster products), and pixel size accuracy.
- Validation against external datasets (e.g., Countryside Survey, National Forest Inventory) reported; outcomes to be published separately.
- Real-world caveats noted for certain habitat classes due to spectral limitations and MMU constraints.

## Data access and licensing
- Access to 25m and 1km raster products via the CEH Environmental Information Platform (eip.ceh.ac.uk).
- Full vector product available on request from CEH (licensing may apply).
- Licences and access terms may vary by user and application.

## Citations, DOIs, and provenance
- All LCM1990 products have individual DOIs, enabling precise citation and reproducibility.
- Example citation format provided; DOIs listed for GB vector, GB 25m raster, GB 1km products, NI vector, NI 25m raster, and NI 1km products.
- Guidance on data citation available via CEH Data citation resources.

## Projections, geographic coverage, and data structure details
- GB vector/raster use British National Grid (EPSG: 27700); Northern Ireland uses TM75 Irish Grid (EPSG: 29903).
- 25m and 1km rasters specify grid extents and pixel dimensions; detailed metadata (Table 4) provides coordinate origins and data type.

## Usage notes and interpretation
- LCM1990 maps land cover, not always directly inferable land use (e.g., arable land vs. grassland on recreation grounds).
- Minimum mappable unit is greater than 0.5 ha; polygons smaller than 0.5 ha are dissolved into surrounding areas.
- The mapping framework is designed for compatibility with later LCM versions (LCM2000/2007/2015) to enable long-term land-cover change studies.

## Further information and contact
- Data access and additional details: https://eip.ceh.ac.uk/lcm/lcmdata
- Contact: spatialdata@ceh.ac.uk
- Acknowledgement: NERC CEH support under award NE/R016429/1 (UK-SCAPE National Capability).
- Journal publication in preparation; full validation results to be published separately.

## Appendices and supplementary information
- Appendix 1–4 provide in-depth class definitions, color mappings, and details on composite images used in LCM1990.
- Appendix 2 summarises Biodiversity Action Plan Broad Habitats (JNCC) definitions used for class mapping.
- Appendix 3 outlines standard LCM color mapping; Appendix 4 lists composite image metadata.