# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK-wide parcel-based land cover map (LCM2007) using 23 classes based on UK Biodiversity Action Plan Broad Habitats.
- Derived from summer-winter satellite composites with 20–30 m pixels.
- Distinguishes land cover (not always land use); minimum mappable area >0.5 ha; parcels <0.5 ha or lines <20 m dissolved into surrounding landscape.
- Data products available in vector and raster formats for Great Britain and Northern Ireland (GB NI), with multiple spatial and thematic resolutions.
- Not a replacement for LCM2000; builds on OSMM and other vector frameworks to improve GIS compatibility.

## Data Model and Classes
- 23 LCM2007 classes (based on Broad Habitats); some splits in certain habitats (e.g., Built-up Areas and Gardens into Suburban/Urban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Sand dune variants).
- Vector dataset contains polygons with 10 attributes, including:
  - Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE, KBE (processing history), ProbList, CorePixels, Construct, TotPixels.
  - ProbList lists top 5 spectral class candidates; KBE documents knowledge-based enhancements and corrections.
- Raster datasets:
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: aggregated products (dominant class, percentage cover) for both 23 classes and aggregate classes.
- Appendix 2 provides mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes; Appendix 3 provides standard colour mappings.

## Data Quality, Validation, and Limitations
- Validation against ground reference data: average accuracy ~83% across 9,127 polygons; individual results vary by area.
- Change detection is not well supported due to differences in classes and spatial structure across LCM generations; typical classification error around 20% makes change detection challenging.
- Broad Habitat sub-classes may have lower validation confidence; users should perform own validation when using sub-class level data.
- LCM2007 is recommended to be used at its 23-class thematic resolution; some applications may utilize aggregated 1 km products.

## Data Access and Licensing
- 1 km raster data (GB and NI) available via the CEH Information Gateway.
- Full vector product and 25 m raster product available on request under licence; online application process and potential licence fees.
- Contact: spatialdata@ceh.ac.uk or CEH data portal for details.

## Data Details and Technical Specifications
- Vector data: ~10 million polygons; GB (~8.6M) and NI (~0.9M); 10 attributes per polygon; includes Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels.
- Raster data: 25 m (GB and NI) and 1 km (GB and NI) products; designed to support various applications from national-scale modelling to local analyses.
- Projections:
  - GB: British National Grid (OSGB36) with Transverse Mercator projection.
  - NI: Irish National Grid; NI moving to Ireland Transverse Mercator (ITM) projection in process; reproject as needed.
- File sizes (approximate guidance):
  - Vector (GB 100 km x 100 km shapefile): ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - 1 km rasters: 21–49 KB to 21 MB range depending on product type.
- Data formats and access considerations: vector data includes rich metadata and polygon-specific processing history; 25 m raster includes the spectral detail without polygon boundaries.

## Product Content and Usage Guidance
- Vector vs Raster trade-offs:
  - Vector: rich metadata per polygon, suitable for detailed queries, as well as integration with other GIS datasets; higher file sizes and more complex processing.
  - 25 m raster: simpler format with less overhead, useful for broad analyses and when polygon-level metadata are not required.
  - 1 km rasters: suitable for national-scale modelling and when merging with other large-scale datasets (e.g., meteorology, species distribution).
- Outputs correspond to the 23 LCM2007 classes and aggregates (for 1 km products) to support varied application needs.
- Unique Parcel_ID enables unambiguous communication among users; recommended to retain for data use and sharing.

## Projections, Updates, and Access Notes
- Updates (Version 1.2, May 2014) include:
  - OS Tile HZ (Fair Isle) added to vector and GB 25 m and 1 km products.
  - OS Tile NW (Stranraer) added to GB products.
  - Water class added to 1 km dominant/aggregate products for GB; NI updates include water in 1 km dominant aggregate class.
- Appendix 4 lists updates by product version and date.
- Acknowledgements credit data sources and partners (Landsat, SPOT, AWIFS, OS, etc.) and note copyright restrictions.

## Appendix Highlights (for Data Consumers)
- Appendix 1: LCM2007 classes with brief habitat descriptions and mapping considerations (e.g., distinctions among Broad Habitats such as Broadleaved woodland, Coniferous woodland, Arable and Horticulture, various grasslands, fen/marsh/swamp, bog, montane habitats, inland rock, coastal/littoral classes, urban/suburban, and dune/sediment categories).
- Appendix 2: Detailed relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode mappings and example class relationships).
- Appendix 3: Standard LCM2007 colour mapping (recipe) used in the Final Report, including RGB values for each class.
- Appendix 4: Update history (Version 1.2) detailing tile additions and new class inclusions.