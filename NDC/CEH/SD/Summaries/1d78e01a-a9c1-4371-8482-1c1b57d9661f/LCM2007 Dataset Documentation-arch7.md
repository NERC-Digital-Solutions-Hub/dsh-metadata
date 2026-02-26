# Land Cover Map 2007 Dataset Documentation

## Overview
- UK parcel-based land cover classification using 23 classes aligned with Broad Habitats.
- Based on summer-winter satellite composites with 20-30 m pixels.
- Maps land cover (not land use); minimum mappable area >0.5 ha; small parcels dissolved.
- Builds polygons that correspond to real-world objects; enhanced GIS compatibility.
- Provides rich metadata and provenance for polygons; validated against ground reference data (average accuracy ~83%).

## Data Products and Formats
- Vector Data Set
  - ~8.6 million polygons in Great Britain and ~0.9 million in Northern Ireland.
  - 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
  - Unique Parcel_ID for unambiguous communication; BHSub provides Broad Habitat sub-class descriptions; FieldCode includes classification notes; INTCODE is the class for display and QA.
  - Includes KBE (knowledge-based enhancements) history and ProbList (top 5 spectral matches).
- Raster Data Sets
  - 25 m and 1 km resolutions; GB and NI provided in separate data sets due to different projections.
  - 25 m: 23 LCM2007 classes; 1 km: aggregates of 23 classes (for simplified mapping).
  - 1 km rasters include Dominant cover and Percentage cover for both LCM2007 classes and Aggregate classes.
- Data Relationships
  - Appendix 1 lists 23 LCM2007 classes with Broad Habitat interpretations.
  - Appendix 2 maps Broad Habitats to LCM2007 classes and Broad Habitat subclasses.
  - Appendix 3 provides standard color mappings for display.

## Data Access and Licensing
- 1 km raster data: available via CEH Information Gateway.
- Full vector product and 25 m raster product: available on request under licence from CEH; online application or contact spatialdata@ceh.ac.uk; licence fees may apply.

## Projections, Coverage, and File Sizes
- Projections
  - Great Britain: British National Grid (OSGB 1936).
  - Northern Ireland: Irish National Grid (transitioning to Ireland Transverse Mercator ITM).
- Data Sizes (typical guidance)
  - Vector (100 km x 100 km shapefile): GB ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: 21 MB to 49 KB (depending on product).
- coordinate details reflect the south-west corner convention for pixel values.

## Data Quality, Validation, and Limitations
- Validation against ground reference polygons: average accuracy ~83%; indicates variation across features.
- Broad Habitat sub-classes (BHSub) and FieldCode are included but not all are QA validated; users should apply their own validation for sub-classes.
- Some grassland classes (e.g., Neutral/Calcareous Grassland) can be mis-classified as Improved Grassland; consult Morton et al. 2011 for detailed limitations.
- Broad Habitat classification reflects spectral signatures with some habitat distinctions difficult to resolve remotely; montane maps rely on altitude with cautions about validity.
- LCM2007 maps land cover from spectral data and knowledge-based enhancements (KBE); not all attributes have equivalent field accuracy.

## Use and Practical Guidance for GIS Specialists
- Recommended use at the highest thematic resolution (23 LCM2007 classes) for most GIS analyses; 1 km rasters suitable for national-scale modelling with other datasets.
- Consider maintaining Parcel_ID in vector products for clear communications and integration with other datasets.
- When using Broad Habitat sub-classes, perform independent validation or aggregation to ensure reliability for your application.
- For display, use Appendix 3 color mappings; for analysis, rely on INTCODE (1-23) aligned with QA validation.
- For comprehensive methodology, limitations, and cross-wataset assessments, consult the Final Report for LCM2007 (Morton et al., 2011) and related Jackson (2000) Broad Habitat guidance.

## Appendix Highlights
- Appendix 1: LCM2007 23 Broad Habitat classes with brief definitions (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, etc.).
- Appendix 2: Relationship table linking Broad Habitats, LCM2007 classes, and Broad Habitat subclasses (BHSub) with FieldCode mappings.
- Appendix 3: Colour mapping recipe for standard display of each LCM2007 class.