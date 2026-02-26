# LCM2000 specification

- LCM2000 is a parcel-based thematic land cover map for the United Kingdom, derived from Landsat imagery with ancillary data, covering all of the UK including Northern Ireland.
- It is produced in both vector (parcels with attributes) and raster formats, in multiple versions with varying detail and spatial resolutions.
- The classification is aligned with the JNCC Broad Habitats hierarchy, with additional detail where possible, to meet user needs across habitat types.
- The raster dataset is not directly comparable with the LCM1990 dataset due to different construction methods.

## Product versions and data formats

- Vector data (polygons) with attributes:
  - Level 2: 26 Subclasses (standard, widely used)
  - Level 3: 72 Variants (more detailed; available by special arrangement with CEH)
  - Standard format: ESRI shapefile (ArcGIS often requires Spatial Analyst for analysis)
- Raster data (GeoTiff) at:
  - 25 m resolution: 26 Subclasses
  - 1 km resolution: derived from 25 m, includes Subclass level (26), Dominant values, and Percentage values; also 10 Aggregate classes with Dominant and Percentage
- Minimum mapping unit: >0.5 ha (parcels ≤0.5 ha are dissolved into surrounding areas)
- Note: Raster 25 m and 1 km rasters are not directly interchangeable with LCM1990

## Dataset coverage and tiling

- Data compiled on a 100 km tile basis; parcels are classified per tile and added to the appropriate tile.
- Some tiles were merged to simplify construction; parcels crossing tile edges are retained in both adjoining tiles.
- Edge overlaps and mosaic artefacts can occur due to multi-source imagery and cloud hole filling.

## Nomenclature and attributes

- Vector data provides hierarchical Subclass and Variant details; codes are documented in a detailed table (including Level 2 Subclass codes and Level 3 Variant codes).
- Subclass vs Variant distinction is important; some GIS displays may show Subclass codes as Level 2 values.
- Class definitions follow Broad Habitat concepts, with some areas where distinctions depend on dominant cover at imaging time.

## Vector polygon attributes and provenance

- Each land parcel has attributes such as:
  - SegID: unique parcel identifier (stable for communications and tracking)
  - BHSub: dominant land cover as a hierarchical code (Level 2)
  - BHSubVar: dominant land cover Variant (Level 3)
  - PerPixList: per-pixel top five spectral subclasses (Level 3 only)
  - OpHistory: processing history descriptor for each parcel (input data, processing stages, KBC rules, image dates)
  - TotPixels and CorePixels: pixel counts for the parcel
- OpHistory contains a six-field descriptor capturing:
  - Scene number, sensor type, image acquisition dates
  - Single-date cloud hole patch indicators
  - Spectral probability (top-choice spectral subclass probability, scaled)
  - Probability aggregation flag (whether aggregation rules were applied)
  - Phase 1 and Phase 2 KBC rule counts
  - A seventh field with a single-character flag for special situations (e.g., edge merging, voids, training data)

## Colour mapping and Broad Habitat descriptions

- Colour recipes (26 Subclasses) are provided for display, with specific H/S/V values and approximate RGB equivalents to aid interpretation.
- Broad Habitat descriptions define major habitat groups (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Water habitats, Montane, Inland bare ground, Built-up areas, Coastal and littoral habitats).

## Data quality, edge artefacts and handling (Appendix 1)

- Edge overlaps from multiple imagery layers can create artefacts when mosaicking 100 km tiles.
- Artefacts are typically rare (<0.1% of parcels) and can be addressed by user-side tidying:
  - Visual dissolution of boundaries between adjacent parcels of the same class
  - Clipping or merging tiles with care (understanding attribute changes may occur)
  - Using dissolve or union operations with attention to preserving Level 3 BHSubVar data
  - For “slivers” or sub-minimum parcels, methods include visual removal, dissolving with adjacent similar-class parcels, or intelligent dissolving based on longest shared boundary
- When merging tiles, the first input tile often takes precedence at edges; some edge parcels may have differing classifications across tiles

## Customisation, governance, and production philosophy

- LCM2000 is intended as an extensible data storage and analysis framework; users are encouraged to customise while preserving lineage.
- Unique labeling: SegID should be retained to maintain traceability back to data management teams.
- Production philosophy emphasizes retaining as much information as possible; new or altered attributes should be documented or stored in new fields.
- Fully documenting changes is essential for data management and security; results enable effective feedback to the data management team.

## Limitations, accuracy, and cautions

- LCM2000 inherently contains inaccuracies due to data model, scale, resolution, and interpretation limitations; these should not be assumed to indicate user-identified errors.
- Raster data should not be used for estimating change over the 10-year period with LCM1990 due to methodological differences.

## Access, references, and further information

- Further information and access: Land Cover Map homepage at www.ceh.ac.uk/data/lcm; contact spatialdata@ceh.ac.uk or 01491 692315
- Methodology references:
  - Fuller et al. (2002): The UK Land Cover Map 2000: construction of a parcel-based vector map from satellite images
  - Smith et al. (2001): Land Cover Map 2000: a parcel-based map from satellite images
  - Jackson (2000): JNCC Report No. 307: Guidance on interpretation of Biodiversity Broad Habitat Classification
- Appendix 2: Good practice (content not included in provided text)