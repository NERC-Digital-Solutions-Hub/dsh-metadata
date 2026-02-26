# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK parcel-based land cover classification using 23 Broad Habitat–based classes, mapped from 20–30 m satellite imagery.
- Replaces LCM2000; built on a spatial framework using OS MasterMap and related vector data to produce polygons representing real-world objects.
- Maps land cover (not strictly land use); minimum mappable unit is 0.5 ha; smaller parcels are dissolved into surrounding landscape.

## Data Structure and Products
- Vector Data Set:
  - 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
  - Unique Parcel_ID stored for unambiguous communication; Broad Habitat sub-classes (BHSub) included but not always QA-validated.
- Raster Data Sets:
  - 25 m and 1 km products derived from the vector data.
  - Great Britain and Northern Ireland provided separately due to different projections.
  - 1 km rasters: Dominant cover and Percentage cover for both 23 classes and Aggregate classes.
- Appendices (definitions and mappings) accompany the data products.

## Data Quality, Metadata, and Validation
- Rich per-polygon metadata capturing processing history, KBE (Knowledge-Based Enhancements), and ProbList (top 5 spectral class matches).
- Validation against ground reference data: average accuracy about 83% across 9127 polygons; local discrepancies may occur.
- The 23-class thematic resolution is validated; Broad Habitat sub-classes are included primarily for display and probability context and should be independently validated for critical use.

## Standards, Licensing, and Access
- Data Access:
  - 1 km raster data available via CEH Information Gateway.
  - Full vector product and 25 m raster product available on request under licence from CEH; online application process or direct contact provided.
  Licence fees may apply for some users/applications.
- Copyright and data provenance:
  - Datasets derived from Landsat, SPOT, AWIFS, and OS/cartographic sources; CEH/NERC and collaborators hold copyright as specified.

## Technical Details and Projections
- Projections:
  - Great Britain: British National Grid (BNG); Northern Ireland: Irish National Grid.
  NI is transitioning to Ireland Transverse Mercator (ITM); reprojecting supported in GIS.
- Data size (guidance):
  - Vector (Shapefile, 100 km × 100 km): GB ~ 4.13 GB; NI ~ 433 MB.
  - Raster 25 m: GB ~ 1.36 GB; NI ~ 46 MB.
  - Raster 1 km: 21 MB to 49 KB depending on product (dominant/percentage).

## Data Content and Use
- 23 LCM2007 classes are based on UK Broad Habitats with some subdivisions:
  - Examples: Built-up Areas and Gardens subdivided into Urban and Suburban; Dwarf Shrub Heath subdivided into Heather and Heather grassland; Littoral Sediment subdivided into Saltmarsh and others.
- The 25 m raster and the vector data are built to be broadly interoperable with other GIS datasets, though users should be mindful of the MMU and classification nuances.

## Appendices Highlights
- Appendix 1: LCM2007 Class Descriptions (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Neutral/Calcareous/Acid Grasslands, Fen/Marsh/Swamp, Bog, Montane, Inland Rock, Various Water/Littoral classes, Urban/Suburban).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat subclasses (FieldCode mappings and class numbers).
- Appendix 3: Standard LCM2007 colour mapping (RGB values) for display of each class.

## Further Information and References
- Primary reference: Morton et al., Final Report for LCM2007 (2011) – detailed methodology and assessment.
- Broad Habitat classification guidance: Jackson (2000) – definitions and relationships with other classifications.

## Governance and Stewardship Considerations
- Data Stewards should note the emphasis on data provenance, metadata richness, and QA limitations when curating LCM2007 assets.
- Maintain Parcel_ID to preserve tractable communication between users; apply independent validation when using Broad Habitat sub-classes.
- Plan for data updates and licensing considerations; ensure users understand the difference between 23-class detail and aggregated 1 km products for scalable analyses.
- Assess compatibility with existing data ecosystems (e.g., land cover vs. land use interpretation) and ensure clear documentation of methodology when sharing datasets.