# LCM2000 specification

- LCM2000 is a UK-wide parcel-based thematic land cover map, derived mainly from Landsat satellite imagery, updating and expanding on the Land Cover Map of Great Britain (LCMGB) 1990 and incorporating data for Northern Ireland to provide an all-UK dataset. It uses a hierarchical nomenclature aligned with the JNCC Broad Habitats and is produced in both vector and raster formats with multiple detail levels and resolutions.

- Purpose and governance relevance for Data Stewards:
  - Provides a rich, provenance-enabled dataset suitable for governance, discovery, and reuse across organizations.
  - Emphasizes documentation of data lineage, processing history, and class definitions to support data governance and user needs.

- Production scope and philosophy:
  - Retains as much information as possible; encourages users to preserve parcel-level metadata and lineage when modifying data.
  - Unique Segid labels enable unambiguous communication with data managers and other users.

- Product scope and outputs:
  - Vector: land parcels (polygons) with attributes; raster: derived grids at 25m and 1km resolutions with several detail levels.
  - All products include multiple detail levels:
    - Vector: Level 2 (26 Subclasses) is standard; Level 3 (72 Variant level) available by special arrangement with CEH.
    - Raster: 25m (26 Subclasses), 1km (Subclass level with Dominant and Percentage options; Aggregate class level with Dominant and Percentage).
  - The raster dataset is not directly comparable with LCM1990 due to different construction methods and should not be used for 10-year change estimation.

- Dataset coverage and structure:
  - Compiled on a 100km tile basis; imagery classified per parcel and then added to the corresponding 100km tile.
  - Minimum mappable unit is 0.5 ha; parcels smaller than 0.5 ha are dissolved into surrounding pixels unless processing difficulties prevent this.
  - Edge overlaps across tiles were resolved by erosion/merging to a single parcel layer per tile; parcels crossing tile edges may be represented in multiple tiles.

- Hierarchical nomenclature and attributes:
  - Vector data carry Subclass (and Variant for Level 3) codes, with associated alpha and numeric codes.
  - Subclass and Variant details are defined to map land cover types to Broad Habitat classifications; provide a detailed scheme for class interpretation and mapping consistency.

- Vector polygon attributes (key fields):
  - SegID: unique parcel identifier, includes OS 100km square and segment number; recommended to retain for data lineage.
  - BHSub: dominant land cover subclass code.
  - BHSubVar: (Level 3) dominant subclass variant code.
  - PerPixList: per-pixel top five spectral subclass percentages (Level 3 only).
  - OpHistory: processing history descriptor for each segment (image data, KBC rules, and dataset compilation steps); detailed explanation in the document.
  - TotPixels: total pixels in the segment.
  - CorePixels: pixels in the core area used for maximum likelihood classification.

- OpHistory (processing history descriptor):
  - Six-field structure describing input scenes, sensor types, acquisition dates, single-date cloud-hole patches, along with three numeric fields documenting spectral probabilities, aggregation flags, and KBC rules (phase 1 and 2).
  - Includes a scene-by-scene table (Table 4) detailing which sensors and dates contributed to each area.

- Colour recipes for mapping:
  - Provides specific RGB (or near-equivalent) values to display each of the 26 Subclasses for effective visualization.

- Broad Habitat descriptions (examples):
  - Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grassland, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Inland water, Montane habitats, Inland bare ground, Built-up areas, Supra-littoral and Littoral habitats, etc.
  - Each description includes the interpretation and distinguishing notes to aid consistent classification.

- Edge overlap and artifact handling (Appendix 1):
  - Edge overlaps occur due to mosaic of multiple images and cloud-hole patching; a single-layer mosaic is produced, with some edge artefacts possible.
  - Artefacts are rare (<0.1% of parcels per 100km tile); guidance provided for visually tidying edges, and technical steps for dealing with overlaps using clipping, merging, union, and dissolving operations.
  - Important considerations when dissolving boundaries: may invalidate parcel-level metadata; Level 3 (Variant) data requires careful handling to preserve key information.

- Slivers and small parcels:
  - Slivers or parcels smaller than minimum mapping unit can be managed visually (dissolve between same classes) or dissolved into neighboring parcels by boundary length or similarity criteria; preserve awareness of their potential impact on overall data interpretation.

- Customisation and usage:
  - LCM2000 is designed as a storage and analysis framework, not just a map; users are encouraged to customize and expand datasets while preserving provenance.
  - Retaining Segid and other original attributes supports communication with data management teams and interoperability across users.

- Production approach and change tracking:
  - Emphasis on maintaining documentation of changes and lineage for efficient data management and security.
  - Users should distinguish real data model/resolution/class-definition differences from inaccuracies when assessing mismatches between datasets.

- Accuracy and limitations:
  - Known inherent inaccuracies due to the data model, resolution, and interpretation; differences from 1990 data are not solely accuracy-related but also reflect methodological changes.

- Further information and contacts:
  - Land Cover Map project page and contact options available; references to methodological papers for deeper technical detail and Broad Habitat classifications (JNCC guidance).

- Appendix 2 Good practice:
  - Indicative guidance exists beyond Appendix 1, with further recommended practices for use and modification of LCM2000 data.