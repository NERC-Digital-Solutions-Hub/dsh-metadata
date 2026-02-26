# LCM2000 specification

- Purpose and scope
  - LCM2000 is a UK-wide parcel-based thematic classification of satellite imagery, upgrading the Land Cover Map of Great Britain (LCMGB, 1990) and expanding to cover Northern Ireland for a comprehensive all-UK dataset.
  - Derived from Landsat imagery with additional ancillary data; classified to align with JNCC Broad Habitats and extended for broader user needs.
  - Available in vector and raster formats, with multiple versions and detail levels to support monitoring and policy evaluation over time.

- Data formats and detail levels
  - Vector data (parcels): polygons with attached attributes.
    - Level 2 (26 Subclasses) – standard, widely used.
    - Level 3 (72 Variant level) – finer detail; may vary in accuracy by area; available by special arrangement with CEH.
  - Raster data (GeoTIFF):
    - 25 m resolution: 26 Subclasses.
    - 1 km resolution: derived products at Subclass level (26), Aggregate level (10), with Dominant and Percentage values.
  - Note: Raster data are not directly comparable to LCM1990 due to different construction methods.

- Dataset coverage and structure
  - Compiled on a 100 km tile basis; parcels are classified and aggregated into 100 km tiles; some tiles merged for construction efficiency.
  - Vector data include hierarchical nomenclature and an attribute-rich schema to support detailed analysis and data integration.

- Nomenclature and classification
  - Hierarchical classification with Target and Subclasses (plus Level 3 Variants where provided).
  - Subclass and Variant codes are documented; display may show Level 2 codes in some GIS packages.
  - Ability to distinguish Variant level depends on dominant land cover at the time of imaging; some distinctions may be precluded by cropping or timing (e.g., harvested crops).

- Vector polygon attributes
  - SegID: unique parcel identifier (per 100 km tile context).
  - BHSub: Level 2 broad habitat subclass code (dominant).
  - BHSubVar: Level 3 variant code (when present).
  - PerPixList: top five spectral subclass percentages per pixel (Level 3 only).
  - OpHistory: processing history for the parcel (image dates, KBC rules, etc.).
  - TotPixels / CorePixels: counts of total and core pixels used for classification.

- OpHistory attribute (processing history)
  - Encodes scene number, sensor, acquisition dates, cloud hole patches, and knowledge-based corrections (KBC) applied in Phases 1 and 2.
  - Each field documents input data and classification steps to support traceability and reproducibility.

- Colour and habitat descriptions
  - Colour recipes (Table 5) provide display colors for each of the 26 Subclasses to aid visualization.
  - Broad Habitat descriptions (Table 6) define each broad habitat category (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grassland, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Water, Montane, Inland bare ground, Built-up areas, Coastal habitats).

- Usage for monitoring and data management
  - Designed as an information-rich dataset intended for monitoring environmental health and policy performance.
  - Production philosophy emphasizes preserving metadata and lineage; users are encouraged to retain SegID and associated attributes to maintain traceability.
  - Not an exact predictor of changes over time when comparing to older datasets; users should be cautious when comparing with LCM1990 or prior products.

- Edge overlaps and artefacts (Appendix 1)
  - 100 km tiles may contain overlapping parcels due to mosaic stitching and cloud-hole filling; overlaps are removed via erosion and merging to create a single layer per tile, with edge parcels retained in adjacent tiles.
  - Artefacts include boundary disagreements, slivers, and changes in parcel geometry at tile edges.
  - Visual tidying options:
    - Clip/merge tiles or dissolve boundaries between identical classes (preferably at Level 2 to avoid losing parcel metadata).
    - For Level 3, use bhsubvar during dissolves to preserve Level 3 information.
    - Use selective dissolves or feature-based selection to limit attribute data loss.
  - Slivers and small parcels can be addressed by visual removal, dissolving with adjacent similar parcels, or intelligent dissolving based on the longest shared boundary, with careful consideration of attribute integrity.

- Customisation, data management and provenance
  - LCM2000 can be customised and expanded by users; it serves as a data storage and analysis framework beyond a static map.
  - Unique SegID labeling should be retained to preserve traceability and facilitate communication with the data management team.
  - Emphasis on documenting changes to maintain data security, lineage, and reproducibility.

- Production philosophy and accuracy considerations
  - The approach prioritises retaining maximum information and metadata at parcel level.
  - Acknowledges inherent inaccuracies; users should distinguish differences due to data model, scale, resolution, interpretation, or class definitions from genuine inaccuracies.
  - LCM2000 data are designed to support consistent monitoring over time, with explicit guidance on handling artefacts and changes.

- Further information and references
  - Land Cover Map home page: www.ceh.ac.uk/data/lcm
  - Contact: spatialdata@ceh.ac.uk; phone 01491 692315
  - Key literature: Fuller et al. 2002; Smith et al. 2001; Jackson 2000 (JNCC Broad Habitat guidance).