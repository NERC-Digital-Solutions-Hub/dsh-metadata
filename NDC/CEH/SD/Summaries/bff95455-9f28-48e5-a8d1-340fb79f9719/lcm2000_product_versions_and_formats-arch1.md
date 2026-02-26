# LCM2000 specification

## Overview
- LCM2000 is a parcel-based thematic classification of UK satellite imagery, producing an all-UK land cover dataset (including Northern Ireland) derived mainly from Landsat imagery, with integration of ancillary datasets.
- Classified to align with the Joint Nature Conservation Committee (JNCC) Broad Habitats classification; aims to cover the full range of UK habitats and provide additional detail where possible.
- Available in both vector (parcel-based polygons) and raster formats; multiple product versions with different levels of detail and resolutions.
- Not directly comparable to LCM1990; raster data are derived from different methods.

## Product scope and formats
- Formats:
  - Vector: polygons (land parcels) with attached attributes; ESRI shapefile standard; Level 2 (26 Subclasses) is the standard widely used; Level 3 (72 Variants) available by special arrangement.
  - Raster: 25 m and 1 km resolutions; 25 m raster derived from vector; 1 km raster includes Subclass level data (and dominant or percentage values) and aggregate class level data.
- Minimum mappable area: >0.5 ha; parcels/linears ≤0.5 ha dissolved into surrounding landscape; some parcels smaller than 0.5 ha may remain due to processing constraints.
- Raster caveat: LCM2000 rasters are not directly comparable with LCM1990 rasters due to different construction methods; not suitable for estimating change over the 10-year period.
- Vector detail:
  - Level 2: 26 Subclasses (standard).
  - Level 3: 72 Variants (high detail; accuracy varies spatially; may require expert interpretation).

## Dataset coverage
- Classified on a 100 km tile basis; parcels added to their corresponding 100 km tile; some tiles merged to simplify construction.
- Source data include summer/winter composites or single images, with per-parcel classification and mosaic assembly across tiles.

## Hierarchical nomenclature
- Vector data provide Subclass (Level 2) and Variant (Level 3) details; each land cover type is coded (e.g., D, Dm, Cf, etc.) with corresponding Codes and Alpha-numeric variants.
- Subclass and Variant codes enable detailed classification, while context and dominant land cover influence the final mapping accuracy.

## Vector polygon attributes
- Each parcel carries a set of attributes:
  - SegID: unique parcel identifier (also used for provenance and communication with data managers).
  - BHSub: dominant land cover as Level 2 subclass code.
  - BHSubVar: dominant land cover as Level 3 variant code (where present).
  - PerPixList: list of top five spectral subclasses by pixel percentage (Level 3 present only).
  - OpHistory: processing history details (input data, dates, rules applied).
  - TotPixels: total pixels in the parcel.
  - CorePixels: pixels in the core area used for maximum likelihood classification.
- The OpHistory attribute encodes per-segment data about input scenes, sensors, acquisition dates, cloud-hole patches, spectral probabilities, and KBC (knowledge-based correction) rules.

## OpHistory attribute (key ideas)
- Each segment contains a descriptor of input data and processing history, including:
  - Scene number and the original input image data (scene-dependent processing and edge cases).
  - Sensor type (e.g., TM, IRS) and image acquisition dates.
  - Single-date cloud-hole patch indicator (S, W, or X).
  - Spectral probability metrics and aggregation flags.
  - Phase 1 and Phase 2 KBC rules applied.
  - A multi-character flag indicating special conditions (edge erasure, training data, prior data, etc.).

## Colour recipes for LCM2000 mapping
- 26 Subclasses are mapped to specific display colours (in HSV/RGB equivalents) to aid visual interpretation.
- Each colour specification includes Hue, Saturation, Value or approximate RGB values for consistent display.

## LCM2000 Broad Habitat descriptions
- Descriptions correspond to Broad Habitats such as:
  - Broad-leaved/mixed woodland
  - Coniferous woodland
  - Arable and horticulture
  - Improved grassland
  - Neutral and calcareous grasslands
  - Acid grassland
  - Bracken
  - Dwarf shrub heath
  - Fen, marsh, swamp
  - Bog
  - Standing/open water and inland waters
  - Montane habitats
  - Inland bare ground
  - Built-up areas and gardens
  - Coastal and littoral habitats (supra-littoral, littoral)
- Each habitat type has a description of its vegetation and structure to guide interpretation and cross-walking with other classifications.

## Further information and references
- Data access and contact: Land Cover Map home page (www.ceh.ac.uk/data/lcm), or spatialdata@ceh.ac.uk; telephone/office details provided.
- Key methodological references:
  - Fuller et al. 2002; Smith et al. 2001; Smith et al. 2000; documentation on methodology for parcel-based map construction.
  - Jackson 2000; guidance on interpretation of Biodiversity Broad Habitat Classification.
- Appendix references:
  - Appendix 1 discusses edge overlap problems (tile-edge mosaicking), artefacts, and how to visually or computationally tidy edge data (e.g., dissolving boundaries within the same class, clipping/merging tiles with caution about attribute validity).
  - Appendix 2 Good practice is referenced but not included in the provided text.

## Production, customization, and data management
- Customisation: LCM2000 is intended as an adaptable data storage and analysis framework; users are encouraged to modify and expand while preserving provenance.
- Unique labeling: SegID should be retained to enable unambiguous communications with data managers and other users.
- Production philosophy: retain as much information as possible; maintain parcel-level metadata to document lineage and processing history; keep original attributes when altering data.
- Documenting changes: thorough documentation of changes is essential for data management, security, and traceability.
- Accuracy vs. correspondence: differences may arise from data models, resolution, interpretation, or target class definitions; LCM2000 acknowledges inherent inaccuracies but emphasizes that these may not be the primary cause of unmet user needs.

Appendix note: The document also includes Appendix 1 (edge overlap handling) and Appendix 2 (Good practice), with Appendix 2 content not shown in the provided excerpt.