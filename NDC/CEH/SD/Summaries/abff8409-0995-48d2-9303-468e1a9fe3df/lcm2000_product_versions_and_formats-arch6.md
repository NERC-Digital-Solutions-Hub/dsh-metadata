# LCM2000 specification

- Overview
  - LCM2000 is a parcel-based thematic land cover map for the entire United Kingdom, upgrading LCMGB1990 and expanding to include Northern Ireland; produced from satellite imagery (primarily Landsat) with additional ancillary data.
  - Classified using a hierarchical nomenclature aligned to the JNCC Broad Habitats; available in vector and raster formats with multiple detail levels and resolutions.
  - Not directly comparable to LCM1990 for change analysis; raster and vector formats serve different use cases.

- Product versions overview
  - Vector data:
    - Level 2: 26 LCM2000 Subclasses (standard detail).
    - Level 3: 72 Variant level (more detail; requires expert interpretation; special arrangement with CEH).
    - Standard format: ESRI shapefile; Spatial Analyst extension recommended for ArcGIS.
  - Raster data (derived from vector):
    - 25m resolution: 26 Subclasses.
    - 1km resolution: Subclass level (26), Dominant values, and Percentage values; also aggregates to 10 Aggregate classes with Dominant and Percentage values.
  - Note: Raster 1km and 25m are not directly comparable to LCM1990 due to differing construction methods.

- Dataset coverage
  - Classified on a per-parcel basis within 100km tiles; images are mosaic’d and edge overlaps resolved through erosion/merging.
  - Tiles may contain duplicated parcels at edges; some artefacts may occur but are generally very small (<0.1%).

- Hierarchical nomenclature
  - Vector data supports Subclass and Variant detail; includes alpha codes (e.g., D, Db, Ds, etc.) and numeric Variant codes.
  - Broad Habitats provide the overall classification framework; detailed mappings exist in Tables 2 and 6 and related descriptions in Table 5 (colour recipes).

- Vector polygon attributes
  - Each parcel (SegID) has a set of attributes:
    - BHSub: Dominant land cover as hierarchical code (Level 2).
    - BHSubVar: Dominant land cover as Variant code (Level 3; present in Level 3).
    - PerPixList: Top-five spectral subclasses per pixel (Level 3 only).
    - OpHistory: Processing history details (dates, sensors, KBC rules, etc.).
    - TotPixels / CorePixels: Pixel counts for the parcel and its core area.
  - SegID acts as a unique parcel identifier for traceability.

- OpHistory attribute
  - Encodes per-segment processing history across:
    - Scene number, sensor (e.g., TM, IRS), acquisition dates (summer/winter), cloud-hole patches.
    - Spectral probability and aggregation flags.
    - Phase 1 and Phase 2 KBC (knowledge-based corrections) rules applied.
    - A sixth field with a single-character flag indicating edge processing or data specifics (e.g., erosion/merging, voids, training data).

- Colour recipes for LCM2000 mapping
  - Table of 26 Subclasses with recommended display colours (Hue, Saturation, Value and RGB equivalents) to aid visualization in GIS/Geo software.

- Broad Habitat descriptions
  - 16 Broad Habitats (e.g., Broad-leaved/mixed woodland; Coniferous woodland; Arable and horticulture; Improved/Neutral/Calcareous/Acid grassland; Bracken; Dwarf shrub heath; Fen/marsh/swamp; Bog; Standing water; Montane habitats; Inland bare ground; Built-up areas; Coastal habitats; etc.).
  - Each description outlines ecological characteristics and how mapping distinctions are made or treated (e.g., management effects, mapping thresholds, and cross-walks to other classifications).

- Further information and references
  - Contact details for data access and enquiries; links to the Land Cover Map home page and CEH methodology papers for LCM2000.
  - References include foundational papers describing the parcel-based construction from satellite images and the guidance on Broad Habitat classification.

- Appendix 1: Dealing with edge overlap problems
  - Edge overlaps arise from mosaicking multiple images; parcels straddling 100km tile edges may be retained in both tiles.
  - Artefacts and differences can occur when eroding/merging edges; typical impact is very small.
  - Recommended approaches:
    - Visually tidy edge areas by dissolving boundaries between adjacent parcels of the same class (without dissolving across the entire dataset to preserve parcel-level attributes).
    - For robust merging, clip to tile edges or use union/ dissolve with caution, understanding that some source attributes may be invalid after edge processing.
    - For Level 3 data, preserve bhsubvar during dissolving to avoid losing important detail.
    - Use selective dissolving and feature selection to speed up processing and minimize attribute loss.
  - Priority and overlap effects: first-input tile often governs edge attributes; some inconsistencies may occur if classifications differ at overlaps.

- Customisation, labelling, and production philosophy
  - LCM2000 is designed as a flexible data storage/analysis framework; users are encouraged to customize while preserving parcel-level metadata and lineage.
  - Each parcel has a unique Segid label to maintain traceability back to LCM2000 data management.
  - Production philosophy emphasizes retaining as much information as possible and documenting changes; encourages keeping original attributes while recording alterations in new attributes.

- Documentation and accuracy
  - Comprehensive documentation is essential for data management and auditability.
  - Use careful terminology for differences arising from data model, scale, resolution, or class definitions; LCM2000 acknowledges inherent inaccuracies but aims to meet user needs.

- Practical considerations for data use
  - Choose the appropriate product version (vector Level 2/Level 3 or raster 25m/1km) based on the use case.
  - When analyzing change, prefer consistent data sources and be cautious about cross-version raster comparisons and LCM1990 compatibility.
  - Preserve Segid and detailed OpHistory for provenance and reproducibility in data analyses and product development.