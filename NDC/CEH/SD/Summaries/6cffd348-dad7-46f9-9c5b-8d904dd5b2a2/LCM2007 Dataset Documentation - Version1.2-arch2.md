# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK land cover map for 2007 (LCM2007) provided as a range of data products to support diverse monitoring needs.
- Parcel-based classification using 23 Broad Habitat–based classes, derived from 20–30 m satellite imagery.
- Maps land cover (not land use) with a minimum mappable unit of 0.5 ha.
- Aimed at enabling consistent, comparable environmental monitoring and policy assessment over time.
- Noted that LCM2007 is complex; users are advised to consult the Final Report (Morton et al., 2011) for detailed methodology and limitations.

## Data Content and Classes
- 23 LCM2007 classes based on UK Biodiversity Action Plan Broad Habitats.
- Some Broad Habitats are subdivided (e.g., Built-up Areas and Gardens into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland).
- LCM2007 maps land cover (spectral signatures) rather than exact land use; certain land cover signatures may not directly indicate use.
- Unique object labeling: each parcel has a Parcel_ID for traceability.
- Rich metadata per polygon, including processing history and a top-5 spectral-class probability list (ProbList).
- Validation against ground reference data with average reported accuracy of 83% across 9127 polygons; local discrepancies may occur.

## Data Products and Resolutions
- Vector data set: polygons with attached attributes; 8.6 million polygons in Great Britain and 0.9 million in Northern Ireland.
- Raster data sets: 25 m and 1 km products derived from vector data; GB and NI provided in separate projections.
- Aggregated products: 1 km raster products include Dominant cover, Percentage cover for 23 classes, and Percentage/ Dominant for Aggregate classes.
- Different formats support varied applications, e.g., 25 m raster for detailed analysis; 1 km raster for national-scale modeling.

## Vector Data Set Details
- 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, TotPixels, Construct).
- BHSub provides sub-class descriptions; FieldCode offers codes used during production (not all accuracy assessed).
- INTCODE: integer class code (1–23) recommended for display and QA.
- KBE: Knowledge-Based Enhancements applied during processing; documented changes (e.g., soil correction, altitude correction).
- ProbList: top five spectral-class matches with associated probabilities.
- CorePixels and TotPixels describe pixel counts used in classification.

## Raster Data Set Details
- 25 m raster: 23 LCM2007 classes; Great Britain and Northern Ireland provided separately with their own extents and metadata.
- 1 km raster: derived by summarizing 25 m data to compute dominant class and percentage cover for both 23 classes and Aggregate classes.
- Data types, extents, and projections differ by region (GB vs NI).

## Data Access and Licensing
- 1 km raster data sets available via the CEH Information Gateway.
- Full vector product and 25 m raster available under licence on request from CEH; fees may apply.
- Application process documented on the CEH website; contact spatialdata@ceh.ac.uk for details.

## Validation and Accuracy
- Ground reference data collected to validate LCM2007 against spatially and thematically matched data.
- Overall average accuracy reported as 83%, acknowledging that local accuracy can vary and some classes are more difficult to distinguish.

## Change Detection
- Change mapping across LCM1990, LCM2000, and LCM2007 is complex due to:
  - Different class definitions across versions.
  - Different spatial structures and resolutions.
  - Typical classification error rates (~20%), which may obscure real change in Broad Habitats.
- LCM2007 is therefore not ideal for straightforward change detection without careful re-interpretation.

## Projection and Coordinate System
- GB vector and raster data use British National Grid (OSGB 1936); NI data use Irish National Grid (Ireland 1965) for certain products.
- NI is progressing toward the Ireland Transverse Mercator (ITM) projection; users may reproject as needed.

## File Size and Data Volume
- Vector (GB): ~4.13 GB; Vector (NI): ~433 MB.
- Raster 25 m: GB ~1.36 GB; NI ~46 MB.
- 1 km products: 21 MB to 49 KB (depending on product type and region).

## Metadata and Documentation
- Rich metadata for polygons, including construction history, source imagery, KBE history, and ProbList.
- Appendix 3 provides standard LCM2007 colour mapping for visualization.
- Final Report and supporting literature (Morton et al., 2011; Jackson, 2000) provide in-depth methodological context.

## Appendix Highlights
- Appendix 1: LCM2007 class descriptions (broad habitats and representative sub-classes).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3: Standard colour mapping for LCM2007 classes (used in visuals and ArcGIS layers).
- Appendix 4: Updates to products (Version 1.2, May 2014) including additions like OS Tile updates and inclusion of water class in some 1 km products.

## Acknowledgements
- Acknowledges data sources and collaborators (Landsat, SPOT, AWIFS, Ordnance Survey, etc.) and the Countryside Survey Partnership.
- Copyright and licensing notices for data sources and outputs.