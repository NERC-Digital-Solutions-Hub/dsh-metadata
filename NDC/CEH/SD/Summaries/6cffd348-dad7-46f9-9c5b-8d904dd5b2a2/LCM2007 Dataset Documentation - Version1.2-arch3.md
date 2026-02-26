# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Purpose and scope
  - Documents the Land Cover Map 2007 (LCM2007), a parcel-based UK land cover classification using 23 Broad Habitat–based classes.
  - Provides a range of data products to support monitoring, assessment of environmental health, and informing decisions; notes that final report Morton et al. (2011) contains more comprehensive evaluation.
  - Distinguishes land cover from land use and sets a minimum mappable unit (0.5 ha).

- Data products and structure
  - Vector data set
    - GB: ~8.6 million polygons; NI: ~0.9 million polygons.
    - Each polygon has 10 attributes (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
    - Key attributes
      - Parcel_ID: unique parcel identifier for communication and traceability.
      - BH and BHSub: Broad Habitat and sub-class descriptions.
      - FieldCode: short field-code string (recommended for use only with validation).
      - INTCODE: integer class code (1–23) for display and QA-validated class.
      - KBE: Knowledge-Based Enhancement history.
      - ProbList: top 5 spectral class probabilities.
      - Construct: history of polygon construction method (e.g., OSMM-derived).
    - Strong metadata and provenance retained; Parcel_ID and KBE history support traceability and reproducibility.
  - Raster data sets
    - 25 m and 1 km resolutions; separate data sets for Great Britain and Northern Ireland.
    - 25 m: 23 LCM2007 classes; 1 km: dominant class and percentage cover for both LCM2007 classes and Aggregate classes (merged versions for 1 km).
    - Metadata includes grid dimensions, extents, pixel size, data type (unsigned 8-bit), projection (GB: OSGB36; NI: Ireland 1965), and coordinate references.
  - Relationship and mapping
    - Appendix 2 provides the relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
    - Appendix 3 provides standard LCM2007 colour mapping for visualization.
    - Appendix 4 lists product updates (notably v1.2 in May 2014 with tile additions and water class inclusion).
  - Data access
    - 1 km raster data via CEH Information Gateway.
    - Full vector and 25 m raster products available by license on request from CEH (online application or via contact); potential license fees.

- Data quality, validation, and limitations
  - Validation
    - Ground reference data used to validate LCM2007 against polygons; average accuracy ~83% across 9,127 polygons (with local variation).
  - Change detection
    - Change mapping across CEH land cover products (1990, 2000, 2007) is complex due to differing classes, spatial structure, and typical ~20% classification error; LCM products are not well suited for change detection.
  - Sub-class caution
    - Broad Habitat sub-classes (BHSub) offer additional information but are not guaranteed the same accuracy/consistency as core LCM2007 classes; users should validate before analysis at the BHSub level.
  - Field-code usage
    - FieldCode values support historical/classifications but are not QA-validated; use with caution and validation.

- Geographic scope, projection, and file sizes
  - Projections
    - GB: British National Grid; NI: Irish National Grid (with NI transitioning toward ITM in progress).
  - File size expectations
    - Vector (GB 100 km × 100 km shapefile): ~4.13 GB; NI: ~433 MB.
    - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
    - Raster 1 km: smaller, with products ranging from ~21 MB to ~49 KB (GB).
  - Data structure implications
    - Vector data provide rich per-polygon metadata but result in large file sizes; 25 m raster offers lighter processing but without polygon-level metadata.

- Practical guidance for monitoring framework authors
  - Use and reuse
    - Leverage the rich metadata and construction history (KBE) for auditing data lineage and methods in monitoring frameworks.
    - Utilize Parcel_ID for traceability across data products and time series.
  - Data governance and openness
    - Be aware of data access restrictions; plan for licensing processes and potential fees.
    - Maintain data provenance and ensure metadata accompany data releases to facilitate reproducibility.
  - Data quality considerations
    - Rely on QA processes and consider performing independent validation, especially when using BHSub and FieldCode-derived insights.
    - Recognize limitations in change detection and exercise caution when interpreting year-to-year changes from these products.
  - Application context
    - Suitable for mapping land cover (not land use) and for UK-wide environmental health monitoring that benefits from a 23-class thematic resolution and multi-resolution data (vector, 25 m, 1 km).
    - For large-area modeling or coarse-grained analyses, the 1 km raster products are particularly useful; for detailed neighborhood-level analysis, the 25 m raster or vector products with rich attributes are appropriate.

- References, provenance, and acknowledgments
  - Core documentation: Morton et al., 2011, Final Report for LCM2007 – the new UK Land Cover Map.
  - Related classification framework: Jackson, 2000 (JNCC Broad Habitat definitions).
  - Data sources and acknowledgments include Landsat, SPOT, AVNIR/AWIFS, OS data, soils, elevation, and other national datasets.
  - Produced by CEH in collaboration with Countryside Survey partners; copyright and licensing information included.

- Versioning and updates
  - Version history: v1.0 (July 2011 original), v1.2 (May 2012; dataset updates and change-detection notes), v1.2 (May 2014; updates including new tiles and water class).
  - Appendix 4 documents specific product updates (e.g., inclusion of additional OS tiles, water class addition, and other minor refinements).