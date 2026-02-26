# LCM2000 specification

- Overview: LCM2000 is a parcel-based thematic land cover classification for the entire United Kingdom, updated from LCMGB 1990 and extending to Northern Ireland for the first all-UK dataset. It is produced from satellite imagery (primarily Landsat) with additional ancillary data and classified against a hierarchical Broad Habitat framework (JNCC Broad Habitats). Available in vector and raster formats, with multiple product versions at different detail levels and resolutions.

- Core aims for GIS use:
  - Provide map-based data to support spatial analysis and communication for policy, clients, and the public.
  - Deliver consistent, audience-appropriate land cover detail through a hierarchical structure (Target/Subclasses and optional Variants).
  - Enable combination and transformation of datasets at different resolutions while preserving metadata.

- Data formats and resolutions:
  - Vector: land parcels as polygons with rich attributes. 
    - Level 2: 26 LCM2000 Subclasses (most widely used).
    - Level 3: up to 72 Variant level detail (less consistent across areas; available by special arrangement).
  - Raster: derived from vector data, at two resolutions.
    - 25 m raster: 26 Subclasses.
    - 1 km raster: summarised at Subclass and Aggregate class levels, with Dominant and Percentage values.
  - Raster data is not directly comparable to LCM1990 due to different construction methods.

- Minimum mapping unit:
  - Minimum mappable area > 0.5 ha; parcels smaller than 0.5 ha are dissolved into surrounding areas using spectral or thematic proximity rules. In some areas, very small parcels may remain due to processing constraints.

- Dataset coverage and structure:
  - Compiled on a 100 km tile basis; parcels are classified per tile and added to the corresponding tile.
  - Tiles can be merged; overlaps are resolved to produce a single parcel layer per tile but artefacts may occur at tile edges.

- Hierarchical nomenclature:
  - Vector data provides both Subclass and Variant detail.
  - Subclass codes map to a defined set of land cover types, with Variant codes (Level 3) giving finer distinctions where available.
  - Examples of naming conventions include broad categories like Broad-leaved/mixed woodland (D), Coniferous woodland (Cf), Arable cereals (Ab/Ao/Aw), and various habitat types across grasslands, water, urban, and coastal classes.
  - Contextual information and dominant land cover at imaging time influence the level of Variant detail achievable.

- Vector polygon attributes:
  - SegID: unique identifier for each parcel; preserves 100 km tile context.
  - BHSub: dominant land cover type (Level 2/Subclass code).
  - BHSubVar: dominant land cover type (Level 3/Variant code) (Level 2 may not have this field).
  - PerPixList: top-five spectral subclasses per pixel (Level 3 only).
  - OpHistory: processing history for each parcel, including image dates and knowledge-based corrections (KBC) applied (both Level 2 and Level 3).
  - TotPixels and CorePixels: total and core-pixel counts for each parcel.
  - Detailed OpHistory field explains scene, sensor, image dates, and KBC/processing steps; a structured description (including a 6-field descriptor and a 7th field for flags) documents input data and classification history.

- OpHistory and data provenance:
  - The OpHistory (PHD) records input data, phase 1 KBC (scene-dependent) and phase 2 KBC rules, and other processing details, enabling traceability of classifications and changes.

- Colour mapping (Colour recipes for LCM2000 mapping):
  - A predefined color set assigns distinct hues for each of the 26 Subclasses to support clear map visualization.
  - Examples include: Broad-leaved/mixed woodland (yellow-red spectrum variants), Coniferous woodland (green-blue family), Arable cereals and horticulture (bright yellows/reds), Grassland classes (greens through different tints), Water and coastal habitats (blues), Urban and built-up areas (dark grays to blacks), and coastal/sea/wetland classes with distinct blues/teals.
  - The colour values are provided as Hue/Saturation/Value and approximate RGB equivalents to assist GIS work.

- Broad Habitat descriptions (high-level habitat groupings):
  - Includes categories such as Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Standing water, Montane habitats, Inland rock, and Built-up areas.
  - Each category has a description that clarifies the vegetation structure, management influences, and typical mapping considerations.
  - Coastal and littoral habitats ( Supra-littoral rock/sediment, Littoral rock/sediment, Saltmarsh, Sea/estuary) are described with attention to coastline delineation and spectral processing.

- Practical guidance for data handling and artefacts (Appendix 1):
  - Edge overlap problems arise from mosaicked overlapping imagery and cloud-hole patching, producing multiple layers of overlapping parcels within 100 km tiles.
  - Artefacts are rare (<0.1% of parcels) but can occur at tile edges. Users are advised to visually tidy edge areas by dissolving boundaries between identical classes (without altering pixel-level attributes) and using ArcMap legend tools.
  - Edge artefact remediation options include clipping to tile edges, union of tiles (retains multiple attribute sets and can invalidate some parcel-level data), and subsequent dissolves to remove boundaries between like classes. For Level 3 data, bhsubvar must be preserved during dissolves to avoid loss of critical information.
  - A common practice is to select edge parcels and dissolve only edge-area boundaries to minimize performance impacts while preserving source attributes elsewhere.

- Slivers and small parcels:
  - Very small parcels (<4 or others below minimum mapping unit) may occur due to patching with LCM1990 data. They can be visually removed or dissolved into neighboring parcels of the same class, or dissolved based on the longest shared boundary with a similar class.

- Customisation and data philosophy:
  - LCM2000 is designed as a data storage and analysis framework, not just a map. Users are encouraged to extend and adapt the database, retaining parcel-level metadata to preserve lineage and provenance.
  - Unique SegID labels should be retained to enable unambiguous communication with data managers and other users.
  - The production philosophy emphasizes retaining as much information as possible and documenting changes to support traceability and future use.

- Accuracy and interpretation:
  - Users should distinguish between inherent data inaccuracies due to modeling, scale, resolution, and interpretation versus actual errors.
  - LCM2000 acknowledges inevitable inaccuracies; differences from user needs may reflect data design choices rather than misclassification.

- Further information and references:
  - Contact CEH for data access and sales; references include Fuller et al. 2002 and Smith et al. 2001 for methodology and construction details, and Jackson 2000 for Broad Habitat definitions and relationships.

- Notes on availability:
  - Full product details, data formats, and versions are outlined in the document’s tables, including vector Level 2 (26 Subclasses) and Level 3 (72 Variants), raster 25 m (26 Subclasses) and 1 km (Subclass and Aggregate levels with Dominant and Percentage values).
  - The 100 km tile approach and edge overlap considerations are central to data handling and integration in GIS workflows.