# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Purpose and scope
  - Land Cover Map 2007 (LCM2007) provides UK-wide land cover classifications to support environmental monitoring, policy scrutiny, and future decision-making.
  - Parcel-based classification with 23 Broad Habitat-based classes, derived from summer-winter satellite imagery (20-30 m pixels).
  - Maps land cover (not land use); minimum mappable unit is >0.5 ha; small parcels and very short linear features are dissolved into surrounding areas.
  - Built to upgrade LCM2000 using a spatial framework aligned with Generalised OS data; polygons correspond to real-world objects for GIS compatibility.
  - Includes rich metadata, processing history, and probability information to aid user validation.

- Data products and structure
  - Vector data set (GB and NI): polygons with 10 attributes each, including Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels; ~8.6 million polygons in GB and ~0.9 million in NI; provides 23 LCM2007 classes.
  - Raster data sets:
    - 25 m raster: 23 LCM2007 classes; two separate GB and NI datasets; 25 m pixelation with class values corresponding to LCM2007.
    - 1 km raster: aggregates - dominant and percentage cover for both 23 LCM2007 classes and 23 Aggregate classes (merged from LCM2007 classes).
  - Additional notes on class structure:
    - Some Broad Habitats are subdivided (e.g., Built-up Areas and Gardens into Suburban/Urban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Saltmarsh and others).
    - The QA process validates at the 23-class thematic resolution.

- Data access and licensing
  - 1 km raster data is openly available via the CEH Information Gateway.
  - Full vector product and 25 m raster product are available on request under license (fees may apply).
  - Data and associated colour mapping (Appendix 3) and ArcGIS-friendly styles are provided.

- Map projection, coordinate systems, and file sizes
  - GB data: British National Grid (OSGB 1936).
  - NI data: Irish National Grid (Ireland 1965); NI moving toward ITM (Ireland Transverse Mercator) with reprojecting support.
  - File sizes (guidance):
    - Vector (100 km x 100 km shapefile): GB ~4.13 GB; NI ~433 MB.
    - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
    - 1 km rasters: 21 MB to 49 KB depending on product.

- Metadata and quality assurance
  - Rich metadata per polygon including processing history, KBE, and ProbList with top spectral class probabilities.
  - 10 attributes per polygon; Parcel_ID preserves linkage to source imagery and segmentation.
  - QA/validation: ground reference data used; average thematic accuracy around 83% (with local higher or lower discrepancies).

- Validation and change mapping
  - Validation against 9127 ground reference polygons; average accuracy 83% across polygons.
  - Change mapping across LCM1990, LCM2000, and LCM2007 is complex due to differing classes and spatial frameworks; not well suited for reliable change detection.
  - Users are cautioned about spectral/class differences and MMU when comparing years or datasets.

- Data updates and version history
  - Version 1.2 (May 2014) updates:
    - Vector GB updated for OS Tile HZ (Fair Isle).
    - 25 m GB raster and 1 km GB products updated for Fair Isle and Stranraer; NI 1 km products updated to include water class.
  - Prior versions: Version 1.0 (2011 original) and Version 1.2 (2012) with dataset updates and change-detection notes.

- Appendices (highlights)
  - Appendix 1: LCM2007 class descriptions and brief habitat interpretations.
  - Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode mappings).
  - Appendix 3: Colour mapping recipe for LCM2007 classes (used in final reports and GIS displays).
  - Appendix 4: List of product updates (v1.2 changes across vector, 25 m, and 1 km datasets).

- Considerations for monitoring framework use
  - Strengths: rich metadata, high thematic resolution (23 Broad Habitat classes), multiple data formats (vector and raster) to support diverse analyses; well-suited for landscape-scale monitoring and integration with other ecological datasets.
  - Limitations: not ideal for precise change detection between years due to differing class definitions and spatial structure; significant data volume, especially vector; some Broad Habitat sub-classes require independent validation before use.
  - Data governance notes: preserve Parcel_ID and underlying data lineage; perform independent validation on Broad Habitat sub-classes if used for fine-scale analyses; ensure metadata is consulted to understand KBE history and classification changes.