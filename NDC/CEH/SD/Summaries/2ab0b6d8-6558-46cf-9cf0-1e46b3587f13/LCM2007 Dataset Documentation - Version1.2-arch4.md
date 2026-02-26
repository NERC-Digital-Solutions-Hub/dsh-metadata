# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK land cover parcel classification (LCM2007) mapping 23 classes based on UK Biodiversity Action Plan Broad Habitats.
- Created from summer–winter satellite imagery with 20–30 m pixels; upgrades LCM2000 using OS cartography frameworks.
- Maps land cover (not necessarily land use); minimum mappable unit >0.5 ha; smaller parcels dissolved.
- Provides multiple data products to support diverse applications and user needs.

## Data Products and Characteristics
- Data products include:
  - Vector data set: polygons with rich metadata and 10 attributes per polygon.
  - 25 m raster data set.
  - 1 km raster data sets (dominant cover, percentage cover, and aggregates for both GB and NI).
- 23 LCM2007 classes are based on Broad Habitats; certain BHs subdivided (e.g., Urban vs Suburban).
- Each parcel in the vector has a unique Parcel_ID; Broad Habitat (BH) and Broad Habitat sub-class (BHSub) information provided; ProbList shows top spectral matches.
- Knowledge-based enhancements (KBE) recorded for each polygon; core pixel counts (CorePixels) used for classification confidence.
- Validation against ground reference polygons (9127 samples) yields an average accuracy of 83%; local deviations may occur.
- Not optimized for change detection due to differing class definitions and spatial structures across LCMs.

## Vector Data Set Details
- Contains about 8.6 million polygons for Great Britain and 0.9 million for Northern Ireland.
- Attributes include Parcel_ID, BH, BHSub, FieldCode, INTCODE (class for display/QA), KBE, ProbList, CorePixels, Construct, TotPixels, among others.
- Broad Habitat sub-classes (BHSub) provide additional detail but are not guaranteed to match LCM2007 accuracy; recommended user validation for sub-class usage.
- Unique labeling facilitates unambiguous cross-user communication.

## Raster Data Sets
- 25 m raster and 1 km raster products derived from the vector data.
- GB and NI provided separately due to different projections.
- Aggregate classes used for 1 km rasters; 23 LCM2007 classes also available in 25 m rasters.
- 1 km rasters include dominant class and percentage cover (both for 23 classes and aggregated classes).

## Map Projection and Data Sizes
- Projections:
  - Great Britain: British National Grid (OSGB36).
  - Northern Ireland: Irish National Grid (with NI transitioning toward ITM; reprojection supported).
- File sizes (typical guidance; may vary by format):
  - Vector (100 km x 100 km shapefile): GB ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - 1 km rasters: GB 21 MB–49 KB; NI smaller.
- Data access points:
  - 1 km rasters via CEH Information Gateway.
  - Full vector and 25 m raster available on request under licence from CEH (licence fees may apply).

## Data Access, Licensing, and Updates
- Access:
  - CEH gateway provides 1 km raster data.
  - Vector and 25 m raster available on licence by request from CEH.
- Version history:
  - Version 1.0 (July 2011) to Version 1.2 (May 2014) with dataset updates and change-detection notes.
  - Version 1.2 includes updates such as OS Tile HZ (Fair Isle), OS Tile NW (Stranraer), and inclusion of water class for several products.
- Appendix 3 provides standard colour mapping for visualisation; Appendix 4 lists updates.

## Quality, Limitations, and Considerations for Data Leaders
- LCM2007 is a complex dataset; thorough review of production methodology, metadata, and limitations is essential before use.
- Change mapping between LCMs is challenging due to class and spatial structure differences; not ideal for change detection.
- Grassland and some BH subclass distinctions (e.g., Neutral/Calcareous/Acid Grassland) can be misclassified; aggregation or user validation recommended for specific grassland classes.
- Maintain Parcel_ID for clear communication and provenance; leverage rich metadata and KBE history for audit trails.
- Data should be used with awareness of MMU, class definitions, and potential local discrepancies in accuracy. For detailed methodology and validation results, consult the Final Report for LCM2007 (Morton et al., 2011).

## Acknowledgements and Contact
- Acknowledges multiple data providers (Landsat, SPOT, AWIFS, Ordnance Survey, national mapping bodies, soil and hydrology data sources).
- Subject to copyright notices; CEH distributes Countryside Survey–related data with licensing and usage guidance.
- For access and licensing details, contact CEH spatialdata@ceh.ac.uk or visit CEH data portals.