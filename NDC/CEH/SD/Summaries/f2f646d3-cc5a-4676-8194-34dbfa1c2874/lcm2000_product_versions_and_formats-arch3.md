# LCM2000 specification

- LCM2000 is a UK-wide, parcel-based thematic map derived from satellite imagery (primarily Landsat) that updates and upgrades the Land Cover Map of Great Britain (LCMGB 1990). It covers all UK land cover, including Northern Ireland, and aligns with the Joint Nature Conservation Committee (JNCC) Broad Habitats classification. It is produced in both vector and raster formats with multiple detail and resolution options.

- Purpose and scope for monitoring:
  - Provides a consistent, hierarchical habitat classification for scrutiny of environmental policy and decision-making.
  - Useful for informing future monitoring and comparing broad habitat types across the UK.

- Product formats and detail levels:
  - Vector data: polygons representing land parcels with multiple attributes.
    - Level 2: 26 Subclasses (most widely used).
    - Level 3: up to 72 Variants; higher detail available by special arrangement with CEH.
    - Standard vector format is ESRI shapefile; ArcGIS may require Spatial Analyst for advanced analysis.
  - Raster data (GeoTIFF):
    - 25m resolution with 26 Subclasses (plus related 1km products derived from 25m data).
    - 1km resolution products include Dominant and Percentage values at Subclass and Aggregate class levels.
  - Note: Raster data are not directly comparable with LCM1990 due to different construction methods.

- Dataset coverage and structure:
  - Compiled on a 100km tile basis; classified per parcel and aggregated into tiles.
  - Tiles can be merged; some parcels straddle tile edges and may be duplicated across adjoining tiles.

- Hierarchical nomenclature:
  - Vector data offers Subclass and Variant detail with codes and alpha-numeric representations.
  - A cross-walk table maps Subclasses and Level-3 Variants (e.g., broad-leaved/mixed woodland, coniferous woodland, arable crops, etc.).

- Vector polygon attributes:
  - SegID: unique parcel identifier (includes UK grid information).
  - BHSub: dominant land-cover subclass (Level 2 code).
  - BHSubVar: Level 3 Variant code (where present).
  - PerPixList: top-five per-pixel subclass composition (Level 3 only).
  - OpHistory: processing history descriptor detailing input data and classification steps.
  - TotPixels / CorePixels: pixel counts for parcel and core classification area.

- OpHistory Attribute (processing history):
  - Encodes scene number, sensor, imaging dates, and processing steps (including knowledge-based correction, KBC).
  - Six fields summarize the input data and classification stages; a seventh field contains other notes.
  - Includes a detailed table of scenes, sensors (e.g., TM, IRS), and acquisition dates, plus single-date cloud-hole patches when applicable.
  - Includes a spectral probability measure and aggregation flags to reflect confidence and rule applications during phase 1 and phase 2 KBC.

- Colour mapping (display):
  - Each of the 26 Subclasses has a recommended RGB color recipe for display purposes (hues, saturations, values, and approximate RGB).
  - Facilitates visual interpretation of habitat types in maps and dashboards.

- Broad Habitat descriptions:
  - Provides descriptive definitions for Broad Habitats (e.g., Broad-leaved/mixed woodland; Coniferous woodland; Arable and horticulture; Improved grassland; Neutral/Calcareous/Acid grasslands; Bracken; Dwarf shrub heath; Fen/marsh/swamp; Bog; Standing water; Montane habitats; Inland bare ground; Built-up areas; Supra-littoral and Littoral habitats).
  - Each Broad Habitat includes guidance on mapping logic and potential ambiguities (e.g., effects of vegetation changes, spectral similarity, or seasonal differences).

- Appendix 1: Dealing with edge overlap problems:
  - Edges between 100km tiles can produce artefacts due to overlaps and patching for cloud holes.
  - Artefacts are rare (<0.1%) and can be mitigated by dissolution of boundaries between like classes, clipping, or merging tiles with attention to preserving parcel-level metadata.
  - If merging tiles, be aware of attribute changes and the primacy of the first input tile for overlapping edge parcels.
  - For Level 3 data, use bhsubvar during dissolving to preserve Level 3 information.

- Appendix 2: Good practice (not detailed here).

- Customisation and production philosophy:
  - LCM2000 is an information-rich framework, intended as a data storage and analysis platform that users can modify and expand.
  - Unique Segid labeling should be retained to preserve traceability and communication with data managers.
  - Documentation of changes and data lineage is encouraged to maintain data integrity and reproducibility.

- Production, governance, and data quality:
  - The production approach preserves as much information as possible, supports metadata retention, and encourages provenance tracking.
  - Users should acknowledge inherent inaccuracies due to data model, scale, resolution, and interpretation; differences do not automatically imply poor quality.
  - Emphasis on metadata, data management, and sharing of underlying data while maintaining clarity about data provenance and processing history.

- Further information and references:
  - Land Cover Map home page: www.ceh.ac.uk/data/lcm; contact: spatialdata@ceh.ac.uk or phone 01491 692315.
  - Methodology references: Fuller et al. (2002) for construction of parcel-based vector maps; Smith et al. (2001) on parcel-based mapping from satellite imagery.
  - Broad Habitat guidance: Jackson (2000), JNCC Report No. 307, for definitions and relationships with other habitat classifications.