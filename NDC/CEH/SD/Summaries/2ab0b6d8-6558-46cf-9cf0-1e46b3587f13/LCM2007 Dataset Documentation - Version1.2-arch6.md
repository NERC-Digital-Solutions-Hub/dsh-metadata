# LAND COVER MAP 2007 DATASET DOCUMENTATION

- The Land Cover Map 2007 (LCM2007) is a UK-wide parcel-based land cover classification using 23 classes based on Broad Habitats, derived from 20–30 m satellite imagery. It updates LCM2000 and provides data products to support diverse GIS and policy needs. The documentation emphasizes understanding production methodology, metadata, and limitations.

## What LCM2007 is and how it’s structured

- Purpose: Map land cover (not land use) across Great Britain and Northern Ireland, with a minimum mapping unit of 0.5 ha; parcels smaller than 0.5 ha or lines under 20 m are dissolved into surrounding areas.
- Class framework: 23 LCM2007 classes aligned with UK Broad Habitats, with some subclasses subdivided (e.g., Built-up Areas and Gardens into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
- Data forms: Distributed as vector (polygons with detailed attributes) and raster (25 m and 1 km resolutions). GB and NI data are provided separately for projection consistency.

## Vector data set (GB and NI)

- Content: 8.6 million polygons in Great Britain and 0.9 million in Northern Ireland; each polygon includes 10 attributes.
- Key attributes:
  - Parcel_ID: Unique parcel identifier (with image source code).
  - BH: Dominant Broad Habitat class.
  - BHSub: Broad Habitat sub-class (descriptive FieldCode); includes ProbList.
  - FieldCode: Short textual class code for potential use with validation advised.
  - INTCODE: Display-friendly integer code (1–23) for the LCM2007 class.
  - KBE: Knowledge-Based Enhancement history (processing history and changes).
  - ProbList: Top 5 spectral-class probabilities for the polygon.
  - CorePixels, TotPixels: Pixel counts used in classification and polygon size.
  - Construct: Construction history (e.g., OSMM-based segmentation variants).
- Quality and limitations:
  - QA-supported class is LCM2007 class (INTCODE); Broad Habitat sub-classes and FieldCode require user validation if used for analysis beyond QA-class.
  - Ground reference validation reported average accuracy ~83% (with local variability).
  - Rich metadata attached to polygons to support provenance and processing history.
- Size considerations: Large vector files; recommended to plan for storage and processing needs.

## Raster data sets

- 25 m raster: 23 LCM2007 classes; GB and NI provided separately with respective projections.
- 1 km raster: Aggregated products derived from 25 m data; includes dominant class and percentage cover for both LCM2007 classes and Aggregate classes.
- Metadata: Table 3 provides spatial extents, pixel counts, coordinate systems, projections, and data types for GB and NI rasters.
- Aggregation: 1 km rasters summarize 25 m data to provide broader-scale summaries suitable for national-scale modeling.
- File characteristics: Raster data sizes smaller than full vector; useful for many large-scale GIS applications.

## Data access and projections

- Access methods:
  - 1 km raster data via CEH Information Gateway.
  - Full vector and 25 m raster products available on request under licence from CEH (data access via online application or contact spatialdata@ceh.ac.uk).
- Projections:
  - GB: British National Grid (OSGB 1936) for both vector and 25 m raster; 1 km rasters share the same system.
  - NI: Irish National Grid for both vector and 25 m raster; moving toward ITM (Ireland Transverse Mercator) projection in NI data; re-projection supported by GIS packages.
- Data size guidance:
  - Vector (GB 100 km x 100 km shapefile): ~4.13 GB; NI shapefile ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - 1 km rasters: 21 MB–49 KB depending on product. 

## Data content details and how to use them

- Classes and interpretation:
  - 23 LCM2007 classes aligned to Broad Habitats; some subclasses offer additional detail but may have lower validation confidence.
  - Appendix 2 provides mapping between LCM2007 classes and Broad Habitats/Sub-classes (useful for crosswalking with BH classifications).
  - Appendix 3 provides standard colour mappings for LCM2007 classes (also available as an ArcGIS .lyr).
- Output formats and use cases:
  - Vector data suitable for localized analyses with rich metadata per polygon; higher detail and potential for precise boundary queries.
  - 25 m raster for detailed surface mapping; 1 km rasters for regional/national analyses and integration with other large-scale datasets (e.g., meteorology, species distributions).
- Data quality and caveats:
  - Change detection is not recommended across LCM2007 years due to class and spatial structure differences and typical spectral change errors (~20%): not well-suited for monitoring land cover change.
  - Sub-class and FieldCode usage requires validation; recommended to rely on the QA-approved LCM2007 class (INTCODE) for primary analyses.
  - Some grassland classifications (Neutral/Calcareous) were often mis-classified as Improved Grassland in validation; consider aggregating classes if necessary or reading Morton et al. 2011 for detailed guidance.

## Documentation, updates, and acknowledgments

- Product documentation emphasizes reading the Final Report for comprehensive methodology and limitations (Morton et al., 2011).
- Appendices:
  - Appendix 1: LCM2007 class descriptions (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, various grassland types, bog, fen, saltmarsh, urban categories, etc.).
  - Appendix 2: Relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (including FieldCodes and ProbList implications).
  - Appendix 3: Colour mapping for LCM2007 classes.
  - Appendix 4: Updates to products (Version 1.2, May 2014) including tile additions and water class inclusion.
- Acknowledgments: Data derived from multiple satellite datasets and cartographic sources; credits to CEH, Ordnance Survey, and partner organizations.

## Quick takeaways for data support use

- Choose vector for detailed, attribution-rich analyses; use QA class INTCODE for core analysis, with caution for BHSub and FieldCode.
- Use 25 m raster for high-detail surface mapping; use 1 km raster for broad, national-scale insights and integration with other datasets.
- Be mindful of data gaps and limitations in change detection; avoid direct year-to-year change analysis without careful cross-walking and validation.
- Ensure appropriate data licensing and projection handling; leverage CEH gateway for access or contact CEH for licensing details.
- Retain Parcel_ID for precise communication and future data linking; consult the Appendices for class relationships and colour coding to support visualization.