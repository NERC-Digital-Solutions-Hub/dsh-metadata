# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- Parcel-based UK land cover dataset using 23 classes based on UK Broad Habitats.
- Produced from summer-winter composite satellite imagery (20–30 m pixels).
- Updates LCM2000; uses OS MasterMap/large-scale vector frameworks; polygons represent real-world objects.
- Distinctly maps land cover (not strictly land use).

## Data Model and Metadata
- Vector data: polygons with 10 attributes each; ~8.6 million GB polygons and ~0.9 million NI polygons.
- Key attributes include: Parcel_ID (unique parcel identifier), BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (class number for display/QA), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, TotPixels, Construct (data source/origin), and more.
- Rich metadata for each polygon; preserves KBE history and links to spectral/classification details.
- Parcel_ID should be retained for traceability and communication between users.

## Classification and Thematic Structure
- 23 LCM2007 classes aligned with Broad Habitats; some subclasses provide additional detail (e.g., Suburban vs Urban, Heather vs Heather grassland).
- Appendix 2 describes relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- LCM2007 is validated at the 23-class thematic resolution; Broad Habitat sub-classes are provided mainly for informational/probability purposes and require user validation if used for analysis.

## Product Scope and Formats
- Vector data set: ~10 attributes per polygon; detailed polygon geometry plus metadata.
- Raster data sets derived from vector:
  - 25 m raster (23 LCM2007 classes; GB and NI provided separately with their projections).
  - 1 km raster products: dominant class, percentage cover for both LCM2007 classes and Aggregate classes.
- 1 km rasters provide a coarser summary suitable for national-scale analyses; 25 m rasters preserve detail with heavier attribute load.

## Accuracy and Validation
- Ground reference validation against 9,127 polygons; average accuracy ~83%.
- Accuracy varies locally; some misclassifications are expected, especially for certain subordinate classes.
- Users are advised to perform their own validation when using Broad Habitat sub-classes or when aggregating classes.

## Spatial Details and Projections
- Great Britain: British National Grid; Northern Ireland: Irish National Grid (with ongoing NI ITM transition).
- Northern Ireland data may be reprojected to ITM as available in GIS tools.

## File Sizes and Data Access
- Vector (GB): ~4.13 GB; Vector (NI): ~433 MB.
- Raster 25 m: GB ~1.36 GB; NI ~46 MB.
- Raster 1 km products: 21 MB to 49 KB depending on product.
- Access:
  - 1 km raster data via CEH Information Gateway.
  - Full vector and 25 m raster products available on license from CEH (application through CEH data portal; fees may apply).

## Practical Usage and Governance Considerations
- Data is land cover (not land use); interpretation requires caution where land use is ambiguous.
- Minimum mappable unit: > 0.5 ha; parcels < 0.5 ha and linear features dissolved into surrounding landscape.
- Large file sizes and complex metadata can affect processing; consider using 1 km rasters for large-area modelling or vector 25 m with metadata for detailed analyses.
- Broad Habitat sub-classes may have lower QA confidence; apply user validation for analyses at sub-class level.
- Keep Parcel_ID to maintain traceability and communication clarity among users.
- Colour mappings (Appendix 3) are provided for consistent visualization; refer to Final Report Morton et al. 2011 for production methodology and caveats.

## Data Access and Licensing
- Data available through CEH Information Gateway (1 km rasters).
- Full vector and 25 m raster products available on request under license; licensing details and fees apply.
- Contact: spatialdata@ceh.ac.uk or CEH data portal for application.

## Further Information and References
- Morton et al. (2011) Final Report for LCM2007 – detailed methodology and validation.
- Jackson (2000) guidance on Broad Habitat classification and relationships.
- Acknowledgements note shared datasets and data sources from multiple agencies and national bodies.
- Countryside Survey Partnership materials and related CEH documentation.

## Appendices (Overview)
- Appendix 1: LCM2007 Classes (descriptions and characteristics across Broad Habitats).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3: Colour mapping recipe for LCM2007 classes (color values for visualization).