# LCM2000 specification

- Purpose and scope
  - LCM2000 is a parcel-based thematic classification of satellite imagery covering the entire United Kingdom.
  - It updates and upgrades the Land Cover Map of Great Britain (LCMGB) 1990 and extends coverage to Northern Ireland for an all-UK dataset.
  - The classification is hierarchical and aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats, with additional detail where possible.
  - Available in both vector and raster formats, with multiple versions offering varying levels of detail and resolutions.

- Product versions overview
  - Vector data format (land parcels with attributes)
    - Level 2: 26 Subclasses (standard level of detail).
    - Level 3: 72 Variant level (more detailed; may vary by area; requires special arrangement with CEH staff).
    - Standard vector format: ESRI shapefile (ArcGIS users may need Spatial Analyst for certain analyses).
  - Raster data format (derived from vector)
    - 25 m resolution raster: 26 Subclasses.
    - 1 km resolution raster: derived from 25 m with two levels of detail:
      - Subclass level: Subclasses 26.
      - Aggregate and Dominant/Percentage values for 1 km cells at Subclass and Aggregate levels.
    - Note: Raster data are not directly comparable with LCM1990 due to different construction methods and are not suitable for estimating changes over the 10-year period.

- Dataset coverage and structure
  - Compiled on a 100 km tile basis; land parcels classified within each tile and then mosaicked.
  - Some tiles may be merged or simplified to facilitate construction.
  - 0.5 ha is the minimum mappable area; smaller parcels are dissolved into surrounding landscape during production.

- Hierarchical nomenclature
  - Vector data provides Subclass and Variant detail (level 2 and level 3).
  - Codes and alpha-numeric identifiers (e.g., various Subclass and Variant codes) map to land cover types.
  - Variant distinctions depend on dominant land cover at the time of imaging; some distinctions rely on contextual information and may not always be up-to-date.
  - A comprehensive mapping table (Subclass codes and Variant codes) is included; Level 3 detail may require expert interpretation.

- Vector polygon attributes and data fields
  - SegID: Unique identifier for each parcel (includes 100 km square and segment number).
  - BHSub: Dominant land cover type as a hierarchical code (Level 2).
  - BHSubVar: Dominant land cover type as a hierarchical code (Level 3).
  - PerPixList: Per-pixel list by percentage area of top five spectral subclasses (Level 3 only).
  - OpHistory: Processing history descriptor detailing input data and classification steps.
  - TotPixels: Total pixels within the parcel.
  - CorePixels: Pixels within the core area used for maximum likelihood classification.
  - OpHistory descriptor (PHD): Contains six fields about input data and classification stages (plus an extra field for other information). It encodes scene number, sensor, acquisition dates, cloud/hole patches, spectral probability, KBC rules, etc.
  - Scene/Sensor/Date details (Table 4): Maps scene numbers to sensors (TM, IRS) and acquisition dates; notes about single-date patches (S, W, or X for montane) and data patches.

- OpHistory and production provenance
  - OpHistory stores the full processing lineage, including image dates and number of knowledge-based correction (KBC) rules applied (phase 1 and phase 2).
  - Important for data provenance, reproducibility, and auditing.

- Colour mapping (colour recipes)
  - A defined color display scheme for the 26 Subclasses (and associated broad habitat types) to facilitate visual interpretation.
  - Colors are specified in HSV and RGB equivalents for display purposes (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable cereals, Improved grassland, etc.).
  - Provides consistent visualization across datasets and versions.

- Broad Habitat descriptions
  - The 16 Broad Habitat categories (e.g., Broad-leaved/mixed woodland; Coniferous woodland; Arable and horticulture; Improved/Neutral/Calcareous/Acid grassland; Bracken; Dwarf shrub heath; Fen/marsh/swamp; Bog; Standing water; Montane habitats; Inland bare ground; Built-up areas; Coastal habitats) with detailed ecosystem descriptions and interpretation notes.
  - Descriptions include how management, seasonality, and imaging context can affect classification outcomes.

- Appendix 1: Dealing with edge overlap problems
  - 100 km tiles create multiple overlapping layers of parcels; overlaps are removed by erosion and merging to produce a single layer, while some edge parcels are retained in adjacent tiles.
  - Artefacts from edge processing are rare (<0.1%) but can occur, such as boundary mismatches, slivers, or parcels classified from different imagery at tile edges.
  - Visual and GIS-based remedies:
    - Visual tidying by dissolving boundaries between adjacent parcels of the same class (using legend tools) without altering underlying attribute data.
    - Clipping to tile edges, union of tiles, or dissolving boundaries can affect parcel-level attributes and history; use with caution.
    - For Level 3 data, ensure bhsubvar is preserved during dissolves to avoid losing Level 3 information.
  - Edge management strategies include prioritizing the first input tile during merges and careful handling of near-edge parcels.

- Appendix 2: Good practice
  - The document references Appendix 2 on good practice, but detailed content is not included in the provided text.

- Production philosophy and data governance
  - Emphasis on retaining as much information as possible; dataset is information-rich.
  - Recommend maintaining parcel-level meta-data and lineage when altering data, with new attributes to record changes.
  - Unique Segid labeling is encouraged to support traceability and communication with the data management team.
  - Documenting changes is essential for data management, security, and feedback loops to the data producers.

- Accuracy and limitations
  - Acknowledges inevitable inaccuracies due to data model, scale, resolution, interpretation, and class definitions.
  - Distinguish between genuine data model differences and inaccuracies when communicating data quality or fit to user needs.
  - LCM2000 is not intended as a direct time-change dataset with LCM1990, and certain comparisons should be avoided.

- Further information and references
  - For data access and inquiries, contact CEH Spatial Data: spatialdata@ceh.ac.uk or 01491 692315.
  - Methodology references include Fuller et al. (2002) on construction of a parcel-based vector map from satellite images; Smith et al. (2001) on a parcel-based map; and Jackson (2000) guidance on Broad Habitat classification definitions and relationships.
  - Broad Habitat descriptions align with JNCC guidance (BNCC 2000).