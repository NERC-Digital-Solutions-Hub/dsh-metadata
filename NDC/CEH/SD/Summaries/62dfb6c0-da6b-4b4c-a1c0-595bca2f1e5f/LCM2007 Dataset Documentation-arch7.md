# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK parcel-based land cover classification (LCM2007) with 23 classes based on Broad Habitats.
- Uses 20–30 m pixel summer–winter composite satellite imagery; updates LCM2000; builds on generalised cartography (OSMM/Large-scale Vector) for GB and NI.
- Maps land cover (not strictly land use); provides rich metadata and documentation for QA and traceability.
- Highly recommended to consult the Final Report for full methodology and limitations (Morton et al., 2011).

## Data Products and Formats
- Vector Data Set
  - Polygons with 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
  - ~8.6 million GB polygons and ~0.9 million NI polygons.
  - Includes Broad Habitat sub-classes (BHSub) and FieldCode with provenance and knowledge-based enhancements (KBE).
- Raster Data Sets
  - 25 m and 1 km rasters derived from the vector dataset.
  - GB and NI provided in separate projections; 1 km products include dominant and percentage cover for both LCM2007 classes and Aggregate classes.
- Metadata and labeling
  - Unique Parcel_ID for each parcel; detailed polygon construction history and spectral probability lists.
  - Appendix 2 and Appendix 3 provide mappings between Broad Habitats, LCM2007 classes, and colour coding.

## Classification and Classes
- 23 LCM2007 classes aligned to UK Broad Habitats (Jackson 2000).
- Some Broad Habitats are further divided into subclasses (e.g., Built-up Areas into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Saltmarsh vs. other).
- LCM2007 is validated at the 23-class thematic resolution; Broad Habitat subclasses exist mainly for display of ProbList and refinement but may require user validation for analysis.
- Conceptual emphasis: LCM2007 maps land cover (spectral signature) rather than land use.

## Data Model and Attributes (Vector)
- Parcel_ID: Unique parcel identifier (includes source image).
- BH: Dominant Broad Habitat class.
- BHSub: Broad Habitat sub-class description.
- FieldCode: Short field code for the sub-class (used in construction; accuracy not QA-assessed).
- INTCODE: Integer code (1–23) for display and QA-validated class.
- KBE: Knowledge-Based Enhancement history (processing notes and changes).
- ProbList: Top 5 spectral variant class probabilities.
- CorePixels: Core pixels used for maximum likelihood classification.
- Construct: Polygon construction provenance (OSMM generalised data, segmentation, etc.).
- TotPixels: Total pixels in polygon.

## Spatial Resolution and Data Structure
- Vector: ~10 million polygons; rich attributes per polygon.
- Raster: 25 m and 1 km products; separate GB/NI datasets; GB uses British National Grid; NI uses Irish National Grid (with NI moving toward ITM in the future).
- MMU and generalisation
  - Minimum mappable area > 0.5 ha; parcels < 0.5 ha and lines < 20 m dissolved into surroundings.
- Data concept: 25 m raster provides detailed land cover without per-polygon metadata; 1 km raster provides national-scale aggregates (dominant and percentage cover).

## Validation and Accuracy
- Ground reference validation: average accuracy ~83% across 9,127 polygons.
- Local discrepancies can occur; users should validate for their area, especially at sub-class level.

## Data Access and Licensing
- 1 km raster datasets: CEH Information Gateway (gateway.ceh.ac.uk).
- Full vector and 25 m raster products: available on request under licence from CEH; licensing fees may apply.
- Documentation and final report provide usage guidance and rights.

## Data Size and Coverage
- Vector (100 km × 100 km shapefile):
  - GB ~ 4.13 GB; NI ~ 433 MB.
- Raster 25 m:
  - GB ~ 1.36 GB; NI ~ 46 MB.
- Raster 1 km (UK):
  - 21 MB to 49 KB depending on dataset.
- Large file sizes; plan storage and processing accordingly.

## Projections and Coordinate Systems
- Great Britain vector and 25 m raster: British National Grid (OSGB 1936).
- Northern Ireland: Irish National Grid; 1 km products planned to switch to Ireland Transverse Mercator (ITM) in NI; re-projection supported.

## Practical Usage for GIS Specialists
- Use vector data for rich attribute analysis (Parcel_ID tracking, KBE history, ProbList) and precise delineation of land cover blocks.
- Use 25 m raster for processing efficiency and to avoid heavy attribute burden, while preserving land cover detail.
- Use 1 km raster products for national-scale modelling and integration with other 1 km datasets (e.g., meteorology, species distribution).
- Maintain Parcel_ID for clear communication and traceability between users.
- Be aware of potential misclassifications between grassland types and other complex habitats; validate Broad Habitat subclasses if used for decision-making.
- Refer to Final Report (Morton et al., 2011) for methodological limitations and detailed class definitions.

## Appendices and Colour Mapping
- Appendix 1: LCM2007 classes with descriptive reviews.
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes ( FieldCode ).
- Appendix 3: Standard LCM2007 colour mapping (RGB values per class) for display.

## References
- Morton, D. et al. (2011). Final Report for LCM2007 – the new UK Land Cover Map. Countryside Survey Technical Report No. 11/07.
- Jackson, D.L. (2000). Guidance on the interpretation of the Biodiversity Broad Habitat Classification. JNCC Report 307.