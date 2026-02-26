# LCM2000 specification

- Overview
  - LCM2000 is a parcel-based thematic classification of satellite imagery for the entire United Kingdom, updating and upgrading the Land Cover Map of Great Britain (LCMGB) 1990.
  - Derived mainly from Landsat data, it covers the whole UK including Northern Ireland and incorporates ancillary datasets.
  - Uses a hierarchical nomenclature aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats, and provides additional detail where possible.
  - Available in vector and raster formats, with multiple versions offering varying levels of detail and spatial resolutions.

- Product versions overview
  - Vector data (parcels with attributes):
    - Level 2: Standard detail with 26 LCM2000 Subclasses.
    - Level 3: Detail down to 72 Variant level; higher detail quality varies by area and may require expert interpretation; Level 3 data available by special arrangement with CEH staff.
    - Standard vector format is ESRI shapefile (ArcGIS may require Spatial Analyst extension).
  - Raster data (derived from vector):
    - 25 m resolution with 26 Subclasses (and related 1 km products).
    - 1 km resolution products include Subclass level, Dominant values, and Percentage values; also 10 Aggregate classes with Dominant and Percentage values.
    - Raster formats are GeoTIFF (ArcGIS Spatial Analyst may be required).
  - Important note: Raster 2000 data are not directly comparable with LCM1990 due to different construction methods.

- Dataset coverage
  - Data compiled on a 100 km tile basis; classification occurs per parcel and parcels are added to their respective 100 km tiles.
  - Tiles were merged to simplify construction; some edge overlap artefacts can occur.

- Hierarchical nomenclature
  - Vector data provide Subclass and (where applicable) Variant detail.
  - Codes map to Level 2 Subclasses and Level 3 Variants (e.g., broad-leaved/mixed woodland, coniferous woodland, arable types, various grasslands, urban, water, etc.).
  - Subclass and Variant codes are presented in detail, with Alpha-codes and numeric Variant codes to support disaggregation and interpretation.

- Vector polygon attributes
  - SegID: Unique parcel identifier (includes OS 100 km square and segment number).
  - BHSub: Dominant land cover type (Level 2 subclass code).
  - BHSubVar: Dominant land cover type (Level 3 variant code) present in Level 3.
  - PerPixList: Top-five spectral subclasses per pixel list (Level 3 only).
  - OpHistory: Processing history for each segment, including image date(s) and knowledge-based correction (KBC) applied (present in both Level 2 and Level 3).
  - TotPixels: Total pixels in the parcel.
  - CorePixels: Pixels in the core area used for maximum likelihood classification.
  - The OpHistory field details the scene, sensor, acquisition dates, cloud hole patches, and KBC rules applied.

- Colour recipes for LCM2000 mapping
  - A defined color palette is provided for display of the 26 Subclasses, including Hue, Saturation, Value and approximate RGB equivalents (used for map visualization).

- LCM2000 Broad Habitat descriptions
  - Broad habitat categories are described to facilitate interpretation and cross-walking with other classifications, covering broad-leaved/mixed woodland, coniferous woodland, arable/horticulture, various grasslands (neutral, calcareous, acid), bracken, dwarf shrub heath, fen/marsh/swamp, bog, standing water, montane habitats, inland rocks, and built-up areas, among others.
  - Each category includes descriptive criteria and notes on distinguishing features and potential ambiguities.

- Further information
  - Contact CEH for data access and sales; references to methodology:
    - Fuller et al. (2002) on constructing a parcel-based vector map from satellite images.
    - Smith et al. (2001) on Land Cover Map 2000 methodology.
    - Jackson (2000) guidance on Broad Habitat classification definitions and relationships.

- Appendix 1: Dealing with edge overlap problems
  - Edge overlaps arise from mosaicking multiple images and patching cloud holes; a single-layer parcel map is produced by erosion and merging.
  - Artefacts at tile edges are infrequent (<0.1%) but can occur, including differing parcel classifications across overlaps and slivers.
  - Visual tidying is possible by dissolving boundaries between adjacent parcels of the same class (recommended over full-map dissolving to preserve parcel-level attributes).
  - Data handling options:
    - Clip data to 100 km tile edges (may discard parcel metadata).
    - Use Union to merge tiles (preserves attributes but may create invalid edge parcel data).
    - Dissolve boundaries between like classes (affects 2D classification but can invalidate some source attributes).
    - For Level 3 (Variant) data, ensure BHSubVar is preserved during dissolving.
  - Edge cleanup can be aided by selecting edge areas before dissolving to limit processing time.
  - Priority of tile input during merging may influence edge results when classifications differ.

- Appendix 2: Good practice
  - Contains guidance (not detailed in the provided text).

- Production philosophy and data governance
  - The production philosophy emphasizes retaining as much information as possible.
  - Parcel-level meta-data should document lineage and processing history; preserve original attributes or copy them when modifying.
  - Thorough documentation of changes is essential for data management and accountability.

- Accuracy and reporting
  - Acknowledges inherent data inaccuracies due to model, resolution, interpretation, and classification thresholds.
  - Users should distinguish between data model differences and actual inaccuracy; LCM2000’s differences from prior maps reflect methodological differences, not just errors.