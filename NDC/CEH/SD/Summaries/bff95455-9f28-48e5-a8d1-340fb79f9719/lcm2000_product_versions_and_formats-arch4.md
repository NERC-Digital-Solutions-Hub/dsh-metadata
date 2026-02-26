# LCM2000

- Purpose and scope
  - UK-wide parcel-based land cover map updated from LCMGB1990, derived from Landsat imagery and ancillary data.
  - All-UK coverage (including Northern Ireland); available in both vector (parcels with attributes) and raster formats; produced in multiple detail levels and resolutions.
  - Classified using a hierarchical Broad Habitat classification (JNCC Broad Habitats) with additional detail where possible.
  - Not directly comparable to LCM1990 and not suitable for estimating change over the 10-year period (especially for raster data).

- Product versions and data formats
  - Vector data (polygons): Level 2 (26 Subclasses) as standard; Level 3 adds up to 72 Variant details (more variable accuracy across areas; requires expert interpretation; available by special arrangement with CEH).
  - Raster data (GeoTiff): 25m resolution with 26 Subclasses; 1km resolution with Subclass level (and Aggregate class level) and values for dominant and percentage cover.
  - Minimum mappable unit: >0.5 ha; parcels smaller than 0.5 ha dissolved into surrounding landscape; some edge cases may remain.
  - ArcGIS considerations: Vector typically in ESRI shapefile; Spatial Analyst extension may be required for analysis; raster may require ArcGIS Spatial Analyst.
  - Important note: Raster data are not directly comparable with the 1990 dataset due to different construction methods.

- Dataset coverage and structure
  - Data compiled on a 100km tile basis; each tile contains classified parcels added to the tile; tiles may be merged for construction.
  - Vector data include a hierarchical naming scheme with Subclass and Variant detail; attribute codes and descriptive tables provided.

- Hierarchical nomenclature and attributes
  - Subclass and Variant codes define land cover types; a detailed code list is provided (e.g., broad-leaved/mixed woodland, coniferous woodland, arable crops, various grassland and habitat types, coastal and marine habitats, towns, water bodies, etc.).
  - Contextual notes: ability to distinguish Level 3 variants depends on dominant land cover at image time; some distinctions may be precluded by harvests or other timing factors.
  - Vector parcels carry a set of attributes, including:
    - SegID: unique parcel identifier
    - BHSub: dominant land cover (Level 2)
    - BHSubVar: dominant Level 3 variant (where present)
    - PerPixList: list of top spectral subclasses per pixel (Level 3)
    - OpHistory: processing history (input data, KBC steps, imagery dates)
    - TotPixels, CorePixels: pixel counts for parcel and classification core
  - OpHistory (processing history descriptor) details:
    - Scene number, sensor type, image acquisition dates (summer/winter), single-date patches, and KBC rule counts
    - Indicates phase 1 (scene-dependent) and phase 2 (UK-wide) KBC rules applied
    - Includes a flag to denote special conditions (edits, training data, data quality notes)

- Colour recipes and habitat descriptions
  - Tabled colour mappings for 26 Subclasses to assist display and interpretation.
  - Broad Habitat descriptions provide definitions for each class (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grasslands, Bracken, Heaths, Fens/Marsh/Swamp, Water bodies, Montane habitats, Inland bare ground, Built-up areas, Coastal/Marine habitats).

- Production philosophy and data governance
  - Design emphasizes retaining as much information as possible; parcel-level metadata should be kept to document lineage and changes.
  - Unique Segid labeling is recommended to be preserved for traceability and communication with data management.
  - The framework is intended to be customizable and expandable for downstream research and applications.
  - Documentation of changes and metadata is essential for data management and security.
  - Users should be mindful of inherent inaccuracies due to data model, scale, resolution, interpretation, and class definitions; avoid overstating inaccuracies as the sole cause of misfit to user needs.

- Edge overlaps, artefacts, and how to handle
  - Edge overlaps arise from mosaicked images and cloud hole patching; 100km tiles were merged and may create artefacts.
  - Artefacts are typically rare (<0.1% of parcels) but can occur at tile edges; guidance provided for visual tidying and for technically removing edge artefacts.
  - Visual tidying: dissolve boundaries between adjacent parcels of the same class using legend tools (preserves parcel data).
  - Edge handling approaches in GIS (e.g., ArcMap):
    - Clip to 100km edge (may remove parcel-level attributes when merging or clipping).
    - Union of tiles (retains overlapping copies but may introduce incorrect edge attributes).
    - Dissolve boundaries between like classes after union/clip (affects attribute data; Level 3 requires bhsubvar).
    - Use selection tools to minimize processing on edge areas and preserve performance.
  - When multiple tiles are merged, the first input tile often has precedence for edge parcels; some cases may show differences if edge classifications differ.

- Slivers and small parcels
  - Slivers and parcels smaller than the minimum unit can appear; post-classification KBC helps, but users can:
    - Visually remove small parcels
    - Dissolve with adjacent similar-class parcels
    - Use intelligent dissolution based on the longest shared boundary with surrounding parcels

- Customisation and use
  - LCM2000 is intended as a data storage and analysis framework, not just a map.
  - Users are encouraged to adapt and expand the dataset, maintaining provenance and lineage through metadata and Segid labels.

- Access, references, and further information
  - For details and access: Land Cover Map home page and CEH contact information.
  - References for methodology and broad habitat definitions are provided ( Fuller et al., 2002; Smith et al., 2001; Jackson, 2000).
  - Appendix 2 contains Good Practice guidance (not detailed in the provided text).

- Takeaways for Data Leaders
  - LCM2000 offers a comprehensive, multi-format UK land cover dataset with rich metadata, suitable for wide-ranging analyses and as a data governance backbone for environmental applications.
  - Key considerations include managing edge artefacts, preserving parcel-level metadata, and balancing detail (Level 2 vs Level 3) with available support and data accuracy.
  - The dataset supports co-ownership and collaboration through standardized classifications, unique identifiers, and detailed provenance, while acknowledging limitations in temporal comparability and potential data gaps.