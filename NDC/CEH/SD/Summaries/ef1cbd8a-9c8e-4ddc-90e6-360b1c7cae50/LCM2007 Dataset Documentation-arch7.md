# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK-wide parcel-based land cover classification (LCM2007) with 23 classes aligned to Broad Habitats.
- Based on summer-winter satellite composites at 20–30 m resolution; builds on LCM2000 with OS-based generalised cartography segmentation for GB and NI.
- Distinguishes land cover (not strictly land use); minimum mappable unit is >0.5 ha; parcels smaller than 0.5 ha or lines <20 m are dissolved.

## Data Products and Structure
- Vector Data Set
  - 8.6 million polygons (GB) and 0.9 million (NI).
  - 10 attributes per polygon, including Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (class code for display), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
  - Parcel_ID enables unambiguous communication; recommended to retain.
  - Sub-classes (BHSub) provide supplementary detail but are not QA-verified at the same level as LCM2007 classes.
  - Includes segmentation basis: OSMM, OSMM:SEG, OSMM:AGC:SEG.
- Raster Data Sets
  - 25 m and 1 km raster products derived from the vector.
  - 23 LCM2007 classes in 25 m; 1 km products provide dominance and percentage cover for both LCM2007 classes and Aggregated classes.
  - GB and NI provided separately due to different projections.
  - Data detail: 25 m GB 28000 x 52000 grid; 1 km GB 700 x 1300 grid; similar for NI with respective projections.

## Validation and Accuracy
- Ground reference validation against 9127 polygons.
- Average accuracy around 83% (subject to local variation; not uniform across all classes).

## Classifications and Relationships
- LCM2007 uses 23 classes linked to Broad Habitats (Appendix 1).
- Some Broad Habitats subdivided (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
- Appendix 2 details relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes with FieldCode mappings.
- Appendix 3 provides standard LCM2007 colour mapping (RGB values) for visualization.

## Data Access and Licensing
- 1 km raster data accessible via CEH Information Gateway (gateway.ceh.ac.uk).
- Full vector product and 25 m raster product available under licence on request from CEH (data@ceh.ac.uk or via www.ceh.ac.uk/data).
- Licence fees may apply for some users/applications.

## Projections and Spatial Referencing
- Great Britain: British National Grid (OSGB 1936); Transverse Mercator projection.
- Northern Ireland: Irish National Grid; NI moving toward Ireland Transverse Mercator (ITM) projection.
- Coordinates refer to the south-west corner of the lower-left pixel for raster products.

## File Size and Practical Considerations
- Vector dataset is large: ~10 million polygons with 10 attributes each.
- Example file sizes (rough guidance; vary by format):
  - Vector (100 km x 100 km shapefile): GB ~ 4.13 GB; NI ~ 433 MB.
  - Raster 25 m: GB ~ 1.36 GB; NI ~ 46 MB.
  - Raster 1 km: 21 MB to 49 KB (varies by product).
- Large data sizes influence handling, processing, and storage decisions.

## Usage Guidance for GIS Specialists
- Vector vs raster trade-offs:
  - Vector: rich metadata per polygon; higher detail but larger file sizes; good for precise attribute queries and integration with other GIS layers.
  - 25 m raster: simpler structure without polygon boundaries and extensive metadata; suitable for applications where metadata overhead is prohibitive.
  - 1 km rasters: efficient for national-scale analyses and integration with ancillary datasets (e.g., meteorology, species distributions).
- Data quality and limitations:
  - MMU excludes sub-0.5 ha features; some small patches may be dissolved or generalized.
  - LCM2007 maps land cover, not land use; spectrally similar classes can complicate interpretation of certain habitats.
  - Broad Habitat sub-classes provide probabilistic guidance (ProbList) and should be validated by users if used at that level.
- Recommended practices:
  - Retain Parcel_ID in vector products for traceability.
  - Validate Broad Habitat sub-classes if used for critical analyses.
  - Consult Final Report for methodology and limitations (Morton et al., 2011) and Broad Habitat guidance (Jackson, 2000).

## Additional Information and References
- Final Report for LCM2007: Morton et al. 2011 ( Countryside Survey Technical Report No. 11/07 ).
- Broad Habitat Classification guidance: Jackson 2000 (JNCC Report 307).
- Appendix materials provide detailed mappings, color schemes, and class definitions.

## Appendix Highlights (for quick reference)
- Appendix 1: LCM2007 classes with Brief Reviews and notes on mapping challenges (grasslands, heath, bog, montane, inland rock, coastal, urban, etc.).
- Appendix 2: Detailed mapping relationships between Broad Habitats, LCM2007 classes, and sub-classes (FieldCode mappings).
- Appendix 3: Colour mapping recipe for LCM2007 classes (RGB values per class).