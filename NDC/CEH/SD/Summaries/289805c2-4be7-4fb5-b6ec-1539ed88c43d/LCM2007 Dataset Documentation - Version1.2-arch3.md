# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK land cover is mapped as a parcel-based classification using 23 classes aligned with Broad Habitats; it maps land cover (not land use) and is derived from summer-winter satellite composites at 20–30 m resolution.
- It updates and improves upon LCM2000 by using a spatial framework based on OSMM and other large-scale vector data, enhancing GIS compatibility.
- Multiple data products are provided to support diverse monitoring needs and applications; detailed methodology and limitations are described in the final report (Morton et al., 2011).

## Data Products and Structure
- Vector Data Set
  - ~8.6 million polygons for Great Britain and ~0.9 million for Northern Ireland; each polygon has 10 attributes.
  - Key attributes: Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE, KBE (Knowledge-Based Enhancements), ProbList (top 5 spectral classes), CorePixels, TotPixels, Construct.
  - Parcel_ID should be retained for unambiguous communication.
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes; GB and NI provided separately; includes detailed class structure.
  - 1 km raster: derived products providing dominant and percentage cover for both 23 classes and aggregated classes; suitable for national-scale modelling.
- Access and formats
  - GB and NI data have separate projections (GB: British National Grid; NI: Irish National Grid; NI moving to ITM).
  - 1 km raster data accessible via the CEH Information Gateway; full vector and 25 m raster available on request (licence may apply).

## Classes, Metadata, and QA
- 23 LCM2007 classes, based on UK Broad Habitats; several Broad Habitats subdivided (e.g., Built-up Areas into Urban/Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).
- Rich polygon metadata including processing history (KBE), initial spectral classification, and probability lists (ProbList).
- Validation against ground reference data: 9127 reference polygons; average thematic accuracy about 83%; local discrepancies may occur.
- Sub-classes (BHSub) provide additional information but may require user validation for analyses at that granularity.

## Change Mapping and Limitations
- Change mapping across LCM1990, LCM2000, and LCM2007 is complex due to differing class schemes and spatial structures; LCM products are not well suited for straightforward change detection.
- Class distinctions can be challenging spectrally (e.g., Neutral vs Calcareous vs Improved Grassland) and are sometimes misclassified when compared with ground data (e.g., 2007 grassland classifications).
- Certain broad habitats (e.g., Fen/Marsh/Swamp, Montane Habitats, Bog) present spectral and mapping challenges, requiring caution and potential aggregation for some analyses.
- LCM2007 is validated at the 23-class thematic level; Broad Habitat subclass information exists but is not guaranteed to meet the same QA standards.

## Usage and Applications
- Designed to support a wide range of monitoring, governance, and policy-evaluation activities in environmental health and land-use planning.
- Vector data provide detailed attributes and a high-resolution foundation for local analyses; raster products (25 m and 1 km) enable broader-scale modelling and integration with other datasets (e.g., meteorology, species distributions).
- Documentation emphasizes consulting Morton et al. (2011) Final Report for comprehensive methodology and assessment.

## Data Access, Licensing, and Access Methods
- 1 km raster datasets: available via the CEH Information Gateway.
- Full vector product and 25 m raster: available on request from CEH; online application and licensing details at CEH data portal; licence fees may apply for some users/applications.
- Data use should adhere to metadata, provenance, and data governance guidelines described in the documentation.

## Data Projections, File Sizes, and Management
- Projections:
  - Great Britain: British National Grid; Ireland/Northern Ireland: Irish National Grid; NI moving toward ITM projection.
- File sizes (indicative):
  - Vector (GB 100 km x 100 km shapefile): ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: smaller (e.g., 23-class percentage ~21 MB; dominant class ~49 KB for GB).
- Data management considerations highlight large file sizes for vector data and the trade-off between detailed metadata and processing efficiency.

## Appendices and Updates
- Appendix 1: LCM2007 Classes – detailed descriptions and definitions for each Broad Habitat class and its subdivisions.
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (including FieldCodes).
- Appendix 3: LCM2007 colour mapping recipe for visualization (also available as ArcGIS .lyr file).
- Appendix 4: Updates to products (Version 1.2, May 2014) including additions (e.g., OS Tile updates for Fair Isle and Stranraer) and inclusion of water classes in 1 km products.
- Product Version History: GB and NI products have versioned releases (e.g., Vector GB v1.2; 25 m GB v1.2; NI versions similar).

## References and Acknowledgements
- Key sources: Morton et al. (2011) Final Report for LCM2007; Jackson (2000) guidance on Broad Habitat classification.
- Acknowledges multiple data providers and datasets (Landsat-TM5, SPOT, AWIFS, OS, RH boundaries, soils, etc.) and CEH/Countryside Survey partnership.
- Copyright and licensing notices for data sources are included in the documentation.