# LCM2000 specification

## Overview
- LCM2000 is a parcel-based thematic classification of satellite imagery covering the entire United Kingdom, updating the LCMGB 1990 and producing an all-UK dataset that includes Northern Ireland.
- Produces both vector (parcels) and raster formats, in multiple detail levels and spatial resolutions.
- Uses a hierarchical nomenclature aligned with the JNCC Broad Habitats, extending to provide additional detail where possible.
- Designed to be usable across a range of user needs, with data suitable for various GIS analyses and decision-making.

## Data Model and Coverage
- Vector data: polygons representing land parcels, each with a set of attributes.
- Coverage model: data compiled on a 100 km tile basis; parcels added to their corresponding tile.
- Minimum mappable unit: >0.5 ha; parcels <0.5 ha are dissolved into surrounding features during processing.
- Classification hierarchy: Target classes and Subclasses oriented to Broad Habitats, with additional Detail via Variants (Level 3) where available.
- Raster equivalents: 25 m raster (26 Subclasses) and 1 km raster (Subclass level with Dominant and Percentage options; also 1 km Aggregate class level with Dominant/Percentage).
- Note: Raster data is not directly comparable to LCM1990 due to differing construction methods.

## Product Versions
- Vector data formats:
  - Level 2 (Standard): 26 Subclasses.
  - Level 3: 72 Variant level detail; higher detail may vary by area and may require expert interpretation; available by special arrangement with CEH.
- Raster data formats (from vector):
  - 25 m resolution: 26 Subclasses.
  - 1 km resolution: Subclass level (26 Subclasses) with Dominant and Percentage, and 1 km Aggregate with Dominant and Percentage.
- Standard vector format is ESRI shapefile; ArcGIS users may require Spatial Analyst for advanced analysis.

## Vector Polygon Attributes
- SegID: Unique parcel identifier (including OS 100 km square and segment number).
- BHSub: Dominant land cover type (Level 2 Subclass code).
- BHSubVar: Dominant Level 3 Variant code (when present).
- PerPixList: Top five spectral subclasses per pixel list (not always present in Level 2).
- OpHistory: Processing history for the parcel (detailed below).
- TotPixels: Total pixels within the parcel.
- CorePixels: Pixels within the core area used for maximum likelihood classification.
- These attributes support lineage tracking, quality checks, and reprocessing if needed.

## OpHistory and Processing Provenance
- OpHistory (Processing History Descriptor, PHD) on each parcel records input data and all classification stages, knowledge-based corrections (KBC), and final dataset compilation.
- Fields include:
  - Scene number, Sensor (e.g., TM, IRS), Acquisition dates, Cloud hole patch indicator (single-date usage), and more.
  - Spectral probability values and aggregation flags indicating whether probability-based aggregation was applied in phase 1 KBC.
  - Phase 1 and Phase 2 KBC rule counts.
  - A sixth field with special flags (e.g., eroded, grown, void-filled, training data indicators, prior data sources).
- Tables map scene numbers to sensors and acquisition dates; guidance for interpreting the PHD is provided in the documentation.
- OpHistory enables full traceability of data lineage and decisions made during production.

## Colour Recipes and Broad Habitat Descriptions
- Color mappings provided for the 26 Subclasses to aid visualization and interpretation.
- Broad Habitat descriptions (Table 6) define the 16 broad habitat groups (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved grassland, Neutral/Calcareous/Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Water bodies, Montane habitats, Inland rock, Built-up areas, Coastal habitats, etc.).
- Descriptions capture high-level definitions and distinctions used during classification and interpretation.

## Data Use, Quality, and Limitations
- Acknowledges inevitable inaccuracies due to data model, scale, resolution, interpretation, and target definitions; differences should not be mischaracterized as mere inaccuracies.
- Raster and vector products contain rich metadata to support governance, use, and reproducibility.
- LCM2000 is designed to be an information-rich dataset; users are encouraged to preserve parcel-level metadata and maintain a clear lineage when modifying data.
- LCM2000 raster data is not suitable for estimating change over the 10-year period against LCM1990 due to methodological differences.

## Edge Overlaps and Artefacts (Appendix 1)
- The mosaic of multiple overlapping images and cloud-hole patches creates edge overlaps within 100 km tiles; overlaps were removed via erosion and merging to form a single parcel layer, with some parcels straddling tile edges retained in both tiles.
- Artefacts may include boundary inconsistencies, slivers, and parcels with differing classifications at tile edges; these are typically <0.1% of parcels but may require user remediation.
- Practical remediation guidance:
  - Visual tidy-up: dissolve boundaries between adjacent parcels of the same class (without removing parcel attributes).
  - Data-level remedies: clip to tile edges, merge tiles (watch attribute integrity), or dissolve at Level 2 (and Level 3 where applicable) while preserving important attributes.
  - For Level 3, preserve bhsubvar during dissolves to avoid losing critical variant information.
  - Use selective dissolves or the union tool with caution to avoid losing source metadata or corrupting attributes.
  - When merging tiles, the first input tile often dictates edge parcel attributes; edge refinements should consider this priority.

## Customisation, Production Philosophy, and Governance
- LCM2000 is intended as a flexible storage and analysis framework, not just a map; users are encouraged to adapt, expand, and build upon the dataset.
- Unique SegID labeling should be retained to ensure traceability back to the data management team.
- Production philosophy emphasizes retaining as much information as possible; users should document lineage and changes, keeping original attributes alongside new attributes or in new fields.
- Documentation of changes is essential for data management, security, and feedback loops to the data management team.

## Further Information and References
- Land Cover Map homepage: www.ceh.ac.uk/data/lcm
- Enquiries: spatialdata@ceh.ac.uk or +44 (0)1491 692315
- Key references for methodology and classification definitions are provided, including studies on the construction of parcel-based maps from satellite images and JNCC broad habitat classifications.