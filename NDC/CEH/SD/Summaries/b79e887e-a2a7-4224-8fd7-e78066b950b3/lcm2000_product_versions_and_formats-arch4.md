# LCM2000 specification

- LCM2000 is a parcel-based thematic classification of UK satellite imagery (primarily Landsat) that updates and substantially upgrades the Land Cover Map of GB (LCMGB 1990). It provides all-UK coverage, including Northern Ireland, and uses a hierarchical Broad Habitat classification (JNCC) with additional detail where possible. It is produced in both vector and raster formats and includes multiple product versions with varying detail and resolutions. It is not directly comparable to LCM1990 due to different methods.

## Product formats and versions

- Vector data (polygons with attributes)
  - Level 2: Standard detail with 26 Subclasses (most widely used)
  - Level 3: Detailed down to 72 Variant level (requires special arrangement and support)
- Raster data
  - 25 m resolution: 26 Subclasses
  - 1 km resolution: derived from 25 m with:
    - Subclass level (26 Subclasses)
    - Dominant values per pixel (1 km, Subclass)
    - Percentage values per pixel (1 km, Subclass)
    - Aggregate class level (10 Broad Aggregates)
    - Dominant values (1 km, Aggregate)
    - Percentage values (1 km, Aggregate)
- Standard raster format: GeoTIFF
- Note: Raster data are not directly comparable with LCM1990

## Dataset coverage and structure

- Compiled on a 100 km tile basis; parcels are classified per tile and added to the appropriate tile.
- Some parcels straddle tile edges; edges are managed through erosion/merge operations to produce a single parcel layer per tile.
- Tiles may be merged; the first input tile often takes precedence at edges, which can affect edge parcels.

## Hierarchical nomenclature and attributes

- Vector data provide Subclass (and Variant) detail; codes are defined in a hierarchical scheme (Table 2 in the document).
- Key attribute fields on parcels include:
  - SegID: Unique parcel identifier (includes OS grid reference)
  - BHSub: Dominant land cover type (Level 2)
  - BHSubVar: Dominant land cover type (Level 3; if present)
  - PerPixList: Top five spectral subclasses by pixel percentage (Level 3)
  - OpHistory: Processing history details (image dates, KBC rules)
  - TotPixels/CorePixels: Pixel counts related to each parcel
- An OpHistory descriptor (PHD) records input data and processing steps, including scene, sensor, dates, and KBC rules applied.

## Processing history, quality controls, and notes

- Processing history and knowledge-based corrections (KBC) are recorded per parcel.
- PHD fields capture:
  - Scene, sensor, acquisition dates
  - Single-date cloud hole patches
  - Spectral probability and aggregation details
  - Phase 1 and Phase 2 KBC rules applied
  - Additional quality flags (edge cases, eroded/introduced artifacts, training data usage)
- The document stresses that LCM2000 retains as much original information as possible and encourages preserving lineage in derivative work.

## Colour schemes and habitat descriptions

- Colour recipes provide recommended display colors for 26 Subclasses to aid visualization in GIS.
- Broad Habitat descriptions (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved grassland, Neutral/Calcareous/Acid grassland, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Water, Montane habitats, Inland bare ground, Built-up areas, Coastal/shoreline habitats) are defined with criteria and notes on edge cases and management practices.

## Edge overlaps and artefacts (Appendix 1)

- Edge overlaps arise from mosaicking multiple images; artefacts can include inconsistent parcel boundaries and small slivers.
- Strategies to deal with edge artefacts:
  - Visual tidying: dissolve boundaries between adjacent parcels of the same class (best done selectively to avoid losing attribute data)
  - GIS-based approaches: clip to 100 km tile edges or merge tiles, then dissolve like classes at Level 2 (with caution about losing original attributes)
  - For Level 3, preserve bhsubvar during dissolving to avoid losing Level 3 information
  - Use selective feature or region-based operations to streamline edge areas
- The document notes these artefacts are rare (often < 0.1% of parcels) and advises users to address them as needed.

## Good practice, customization, and governance (Appendix 2 and production philosophy)

- LCM2000 is designed as an extensible data storage and analysis framework; users are encouraged to customize while preserving parcel-level metadata to record lineage.
- Unique SegID labeling should be retained to enable traceability and communication with the data management team.
- Production philosophy emphasizes retaining maximum information and documenting changes, ensuring metadata and provenance accompany any modifications.
- Cautions about accuracy: differences stem from data model, scale, resolution, interpretation, or classification scheme; LCM2000 acknowledges inherent inaccuracies and advises against misattributing them as user-needs failures.

## Practical implications for Data Leaders

- Data stewardship: maintain metadata, lineage, and SegID to ensure traceability and reproducibility.
- Governance: manage both vector and raster products, including edge handling, versioning, and documentation of changes.
- Data quality and accessibility: understand processing history (OpHistory), KBC rules, and the impact of tile-edge artefacts on analyses.
- Usability for diverse users: provide clear classification hierarchy (Subclasses/Variants) and color schemes; ensure alignment with user needs (e.g., policy colleagues) via documentation and potential co-ownership of data products.
- Integration and strategy: leverage the all-UK coverage, multi-resolution formats, and rich attribute data to support wide networks and collaborations; be mindful of differences with historical datasets (LCM1990) when assessing change or comparability.
- Appendix awareness: refer to edge handling and good-practice guidance when deploying or distributing LCM2000 derivatives.