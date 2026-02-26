# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview and purpose
- Provides a range of data products to support diverse user needs for UK land cover mapping (LCM2007), highlighting that it maps land cover (not land use) using 23 classes aligned to Broad Habitats.
- Delivered as vector (polygons with metadata) and raster (25m and 1km) products across Great Britain and Northern Ireland.
- Built as an upgrade to LCM2000 with a framework based on generalised cartography and image segmentation to produce polygons that reflect real-world objects.

## Data content and structure

- LCM2007 scope
  - Parcel-based classification of the UK with 23 classes based on Broad Habitats.
  - Uses summer-winter satellite composites at 20–30 m resolution.
  - Includes improvements in spatial framework (OSMM for GB, L&S for NI) and image segmentation for clearer object boundaries.
  - Maps land cover (not always directly inferring land use).

- Vector data set (GB and NI)
  - GB: ~8.6 million polygons; NI: ~0.9 million polygons.
  - Each polygon has 10 attributes, including:
    - Parcel_ID: unique identifier (with source image tag).
    - BH: Broad Habitat (dominant class at Broad Habitat level).
    - BHSub: Broad Habitat sub-class (descriptive text of FieldCode).
    - FieldCode: short text for classification coding (use with caution without validation).
    - INTCODE: integer display class (1–23) for user-friendly display; QA validated class.
    - KBE: Knowledge-Based Enhancement history (processing history and changes).
    - ProbList: top 5 spectral class probabilities for the polygon.
    - CorePixels and TotPixels: pixel counts used in classification.
    - Construct: lineage of polygon construction (OSMM-based inputs and segmentation).
  - Sub-classes (BHSub) provide additional detail but are not as rigorously QA'd as primary LCM2007 classes; validation advised if used at the sub-class level.
  - Rich metadata accompanying polygons (processing history, source imagery, calibration steps).

- 23 LCM2007 classes and structure
  - Class mapping to Broad Habitats with occasional subdivisions (e.g., Built-up Areas divided into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland).
  - Appendix 2 describes relationship between Broad Habitats, LCM2007 classes, and sub-classes; Appendix 1 provides class descriptions.
  - Class definitions emphasize spectral-based classification with knowledge-based refinements; some classes (e.g., Neutral/Calcareous/Acid Grassland) may require field validation for precise separation.

- Raster data sets
  - 25 m raster: 23 LCM2007 classes (GB and NI separate projections).
  - 1 km raster: aggregated data for broader analyses; includes Dominant cover and Percentage cover for both LCM2007 classes and Aggregate classes (combining 23 classes into fewer categories).
  - Metadata in Table 3 covers extents, pixel grids, coordinate systems, projections, datums, data types, and coordinate origins.
  - 25 m and 1 km rasters are derived from the vector data (consistency with vector at finer scale).

- Data access and licensing
  - 1 km raster data: accessible via CEH Information Gateway.
  - Full vector product and 25 m raster: available under licence on request from CEH (application via CEH data portal); licence fees may apply.
  - Northern Ireland data may be subject to separate licensing.

- Map projection and coordinate systems
  - GB data: British National Grid (OSGB 1936).
  - NI data: Irish National Grid (and moving toward ITM; GIS tools should reproject NI data if needed).

- File sizes and formats
  - Vector: large files (nearly 10 million polygons across GB and NI) with 10 attributes each.
  - Raster: 25 m and 1 km products provided in GeoTIFF-like formats; sizes vary by region (GB vs NI).

## Data quality and validation

- Ground reference validation
  - LCM2007 validated against 9,127 ground reference polygons; average thematic accuracy around 83%.
  - Validation results are an average across all polygons; local variations in accuracy may occur.
- Change mapping considerations
  - Change mapping across CEH products (1990, 2000, 2007) is complex due to inconsistent class mappings and spatial structures; typical image classification error (~20%) can obscure BH-level changes.
  - LCM2007 is not well suited for straightforward change detection without careful cross-walking between datasets.
- Sub-class reliability
  - Broad Habitat sub-classes (BHSub) provide additional detail but are not guaranteed to meet the QA level of primary LCM2007 classes; users should validate when using sub-class level data.

## Version history and updates

- Version 1.0 (Original): July 2011.
- Version 1.2: May 2012 (update to include dataset updates and change detection paragraph; renamed to align with updated datasets).
- Version 1.2 (May 2014) updates
  - GB vector v1.2 includes OS Tile HZ (Fair Isle).
  - GB 25 m raster v1.2 includes OS Tile HZ (Fair Isle) and OS Tile NW (Stranraer).
  - GB 1 km targets (percentage and dominant classes) updated to include water class (previously not included).
  - NI 1 km products updated to include water class.
- Product-specific version histories mirror these updates for vector, 25 m raster, and 1 km products in GB and NI.

## Appendices and related documentation

- Appendix 1: LCM2007 classes (descriptions and habitat interpretations; detailed criteria for each class).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (mapping guidance for cross-walking classes).
- Appendix 3: Colour mapping recipe for standard LCM2007 colours and class names (also available as an ArcGIS .lyr).
- Appendix 4: List of updates to products (version 1.2 changes, including new tiles and water class inclusion).

## Acknowledgements and licensing notes

- Datasets derived from multiple sources (Landsat, SPOT, AWIFS, Ordnance Survey, soil and elevation data, etc.) with Crown Copyright and third-party attributions.
- Reproduction and use governed by licenses (Ordnance Survey licenses, CEH data licensing, and other data rights).
- Documentation states alignment with Countryside Survey and Morton et al. (2011) Final Report for detailed methodology and classification framework.

## Practical governance considerations for Data Stewards

- Data governance and stewardship
  - LCM2007 provides richly attributed vector data with explicit provenance (Parcel_ID, image source, KBE history) and QA documentation; retain Parcel_ID and KBE traces to support data lineage.
  - Ensure appropriate licensing and attribution when distributing or integrating LCM2007 products; licensing varies by product type (vector/25 m raster vs 1 km raster).
  - Given the large size of the vector product, plan for storage, processing, and access in line with internal data governance and computing resources.
- Metadata and usability
  - Leverage the rich metadata and Appendix 1–3 details to ensure consistent interpretation across teams; validate Broad Habitat sub-classes if used for policy or reporting.
  - Use 1 km raster products for broad-scale analyses or when working with national-scale modelling, while preserving detailed vector fidelity where feasible.
- Interoperability and integration
  - Be mindful of coordinate system differences (GB vs NI) and forthcoming transition of NI data to ITM; implement re-projection steps as needed for integrated analyses.
  Use Appendix 2 mappings to align LCM2007 classes with Broad Habitats when connecting to other habitat datasets or policy frameworks.
- Change detection and historical comparisons
  - Exercise caution when comparing LCM2007 with earlier or later land cover products; document class mappings and potential misclassifications when performing trend analyses.
- Data quality assessment
  - Consider conducting independent validation if sub-classes or knowledge-based enhancements (KBE history) are used for decision-making; remember the official QA pertains to primary LCM2007 classes.