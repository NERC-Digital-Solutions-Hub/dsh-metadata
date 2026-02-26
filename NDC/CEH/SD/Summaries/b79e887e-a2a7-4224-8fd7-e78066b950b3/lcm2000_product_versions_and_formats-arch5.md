# LCM2000 specification

- Overview
  - LCM2000 is a UK-wide, parcel-based thematic land cover map derived mainly from Landsat satellite data, updating LCMGB1990 and expanding to cover Northern Ireland as well.
  - Classified using a hierarchical nomenclature aligned with JNCC Broad Habitats; available in vector and raster formats, with multiple detail levels and resolutions.
  - Not directly comparable with LCM1990 due to different production methods.

- Product versions and formats
  - Vector data (primarily polygons with per-parcel attributes)
    - Level 2: 26 Subclasses (most widely used)
    - Level 3: 72 Variant level (special arrangement with CEH staff; higher support required)
    - Standard vector format: ESRI Shapefile (ArcGIS may require Spatial Analyst for analysis)
  - Raster data (derived from vector, stored as GeoTiff)
    - 25m resolution: 26 Subclasses
    - 1km resolution: Subclass level (dominant values and percentage per pixel), and Aggregate class level (10 simplified aggregates with dominant and percentage)
  - Note on usage: Raster data are not directly comparable to LCM1990 due to methodological differences.

- Dataset coverage and tiling
  - Classified on a per-parcel basis within 100km square tiles; tiles are tiled and then merged as needed.
  - Some parcels straddle tile edges and may be duplicated across adjacent tiles.
  - Tiles may be merged with precedence given to the first input tile; edge overlap can affect classification and attributes.

- Hierarchical nomenclature and attribute codes
  - Vector data provide Subclass and Variant detail (Level 2 Subclass codes and Level 3 Variant codes).
  - Subclass codes and Variant codes are used in attribute fields such as BHSub (dominant land cover) and BHSubVar (dominant land cover Variant).
  - A lineage of codes is maintained to support detailed interpretation and cross-reference.

- Vector polygon attributes (key fields)
  - SegID: Unique identifier for each parcel (includes 100km tile and segment number).
  - BHSub: Dominant land cover type (Level 2 Subclass code).
  - BHSubVar: Variant detail for Level 3 (if present).
  - PerPixList: Top-five per-pixel spectral subclass composition (Level 3 only).
  - OpHistory: Processing history descriptor detailing image data and KBC steps.
  - TotPixels: Total pixels in the parcel.
  - CorePixels: Pixels in the core area used for maximum likelihood classification.

- OpHistory and provenance
  - OpHistory (PHD) comprises five fields documenting input data and classification steps, KBC (knowledge-based correction) stages, and an additional field for other information.
  - Scene, sensor, and acquisition dates are tracked (Table 4 describes sensor types and dates, e.g., TM, IRS; various summer/winter dates; cloud hole patches).
  - The six-field scheme includes additional flags for edge conditions and data treatment (e.g., haze, training data, edge-eroded merges).

- Colour mapping and broad habitat descriptions
  - Colour recipes (Table 5) provide display color values for the 26 Subclasses to support visualization.
  - Broad Habitat descriptions (Table 6) explain each major habitat class (e.g., Broad-leaved woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grassland, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Water bodies, Montane habitats, Inland bare ground, Built-up areas, Coastal habitats).

- Data quality, edge overlaps, and artefacts (Appendix 1)
  - Edge overlaps arise from mosaic of multiple images; a single 100km tile contains multiple parcel layers that are eroded/merged to form one layer.
  - Artefacts near tile edges can occur; remedies include visual tidying, dissolving boundaries between identical classes (with caveats about losing parcel-level metadata), clipping, or merging tiles (aware of attribute integrity).
  - For Level 3 data, dissolving must preserve bhsubvar to avoid losing Level 3 details.
  - Slivers and very small parcels can be addressed by dissolving with adjacent similar parcels or by intelligent dissolving based on shared boundaries, while maintaining overall data integrity.

- Customisation, provenance, and production philosophy
  - LCM2000 is designed as a data storage and analysis framework; users are encouraged to modify and expand their version while maintaining lineage.
  - Each parcel has a unique Segid to support unambiguous communication with data managers and other users.
  - A philosophy of retaining as much information as possible is embedded; changes should preserve metadata and, if attributes are altered, originals should be retained in new attributes.
  - Documenting changes is essential for data management and audit trails.

- Spatial coverage, data updates, and interoperability notes
  - Parcellation and classification are tied to 100km tiles; updates and edge handling can affect attribute data and should be considered when merging data from multiple sources.
  - The raster products are derived from the vector data and are provided at two resolutions; users should be cautious about cross-scale interpretation.
  - The document provides guidance on dealing with edge artefacts, slivers, and how to maintain data integrity during redistribution or re-assembly.

- Accuracy considerations
  - LCM2000 acknowledges inevitable inaccuracies due to data model, scale, resolution, interpretation, and class definitions.
  - Differences from LCM1990 reflect production differences rather than simple inaccuracies; users should interpret changes with an understanding of underlying methodologies.

- Further information and references
  - Contact: Land Cover Map data inquiries (spatialdata@ceh.ac.uk; phone numbers provided).
  - Additional resources include the Land Cover Map home page and key methodological papers detailing construction and classification approaches.

- Governance implications for Data Stewards
  - Ensure metadata completeness: Segid, BHSub, BHSubVar, OpHistory, TotPixels, CorePixels, scene/sensor/date details, and cloud-flag information.
  - Preserve provenance: maintain full processing history to support reproducibility and auditability.
  - Manage edge artefacts and slivers with documented procedures; record any adjustments or dissolves to data lineage.
  - Monitor versioning and format conversions (vector vs. raster) to sustain data interoperability and compatibility with downstream applications.
  - Maintain unique labeling (Segid) to enable traceability back to source imagery and processing steps.
  - Document changes and provide guidance for end users on handling edge cases, mosaic edges, and cross-tile merges.