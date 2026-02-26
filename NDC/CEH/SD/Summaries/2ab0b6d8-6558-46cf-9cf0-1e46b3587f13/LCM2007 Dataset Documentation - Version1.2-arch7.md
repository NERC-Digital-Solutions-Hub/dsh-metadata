# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- parcel-based classification of UK land cover using 23 classes based on UK Broad Habitats
- built from summer-winter composite satellite imagery at 20–30 m pixels
- uses OS Master Map/Vector frameworks for GB and NI-specific vector segmentation
- maps land cover (not strictly land use); min mapping unit is >0.5 ha
- polygons dissolved for parcels smaller than 0.5 ha or linears < 20 m

## Data Products and Resolution
- vector data set: 8.6 million polygons (GB) and 0.9 million polygons (NI); 10 attributes per polygon
- 25 m raster: 23 LCM2007 classes; derived from the vector
- 1 km raster: summaries for GB and NI
  - 1 km products include dominant cover, percentage cover for both LCM2007 classes and Aggregate classes
- Aggregate classes: defined for 1 km rasters to reduce thematic resolution
- spatial detail aligns with Broad Habitat classifications; some subclasses offer finer distinctions (e.g., Suburban vs Urban)

## Class System and Metadata
- 23 LCM2007 classes derived from Broad Habitats; some subclasses exist (BHSub) for additional detail
- 1–10 attributes per polygon include:
  - Parcel_ID, BH (Broad Habitat), BHSub, FieldCode, INTCODE (display class, 1–23), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels
- unique Parcel_ID retained for unambiguous cross-user communication
- rich polygon metadata captures construction, original spectral classification, and knowledge-based enhancements (KBE)

## Data Quality and Validation
- ground reference validation against 9,127 polygons with average accuracy around 83%
- local discrepancies may occur; accuracy is an average metric across dataset
- change mapping is not well suited for LCM comparisons due to class differences, spatial structure, and typical spectral classification errors (~20%)

## Projections and Coordinate Systems
- Great Britain: British National Grid (OSGB36), Transverse Mercator
- Northern Ireland: Irish National Grid; NI moving toward Ireland Transverse Mercator (ITM)
- Users can reproject NI data to ITM as needed

## Data Access and Licensing
- 1 km raster data sets available via CEH Information Gateway
- full vector product and 25 m raster product available on request under license from CEH
- online application available; license fees may apply for some users/applications

## File Size and Data Volumes
- Vector (GB): ~4.13 GB; NI vector ~433 MB (example shapefile package)
- Raster 25 m: GB ~1.36 GB; NI ~46 MB
- 1 km rasters: smaller sizes (23-class percentage ~21 MB to 49 KB for dominant class)
- Data size considerations are important due to nearly 10 million polygons in the vector set

## Appendices and Colouring
- Appendix 1: LCM2007 classes with Broad Habitat mappings and notes on separation (e.g., Heather vs Heather grassland)
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat subclasses (for cross-walking)
- Appendix 3: Colour mapping recipe for standard LCM2007 classes (also provided as an ArcGIS .lyr)
- Appendix 4: Updates to products (Version 1.2, May 2014) including additional tiles (Fair Isle, Stranraer) and inclusion of water class in some 1 km products

## Practical Guidance for GIS Specialists
- retain Parcel_ID for clear communication and traceability
- choose data product by need:
  - 25 m vector: highest thematic and boundary detail with rich metadata
  - 25 m raster: simpler, metadata-light for processing
  - 1 km rasters: efficient for national-scale analyses or when integrating with large external datasets
- consider the 0.5 ha minimum mapping unit when interpreting small features
- be aware that LCM2007 captures land cover, not direct land use; spectral similarity can misclassify certain land uses (e.g., arable crops vs. fallow or grassland)
- for grasslands and certain habitats, use Appendix 1–3 guidance and consider independent validation if subclass-level accuracy matters
- for change detection across decades, use caution due to differing class schemes and spatial structures across LCM versions
- track updates (e.g., Version 1.2) for tile coverage changes and added classes (including water features) to ensure datasets align with current usage needs