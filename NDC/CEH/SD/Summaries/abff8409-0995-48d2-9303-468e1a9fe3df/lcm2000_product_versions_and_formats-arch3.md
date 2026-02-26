# LCM2000 specification

- LCM2000 is a parcel-based thematic classification of satellite imagery covering the entire United Kingdom, updating LCMGB1990 and extending to Northern Ireland for the first time to provide an all-UK dataset.
- It is derived from satellite imagery (primarily Landsat) and incorporates information from ancillary datasets.
- The classification uses a hierarchical nomenclature aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats, facilitating broader habitat-based interpretation and applications.
- Available in vector and raster formats, with multiple product versions offering varying levels of detail and resolutions.

## Product versions overview

- Vector data (parcels) with attributes; standard ESRI shapefile format; supports Level 2 (26 Subclasses) and Level 3 (72 Variant level) details; Level 3 data available by special arrangement with CEH.
- Raster data derived from the vector database:
  - 25 m resolution raster with 26 Subclasses.
  - 1 km resolution raster summarised at Subclass and Aggregate class levels, including dominant value and percentage values.
- Raster data is not directly comparable with LCM1990 due to different construction methods.
- Details on formats and resolutions:
  - Vector: Level 2 (aggregate) and Level 3 (variant) available.
  - Raster 25 m: Subclasses; Raster 1 km: Subclass and Aggregate with dominant and percentage values.

## Dataset coverage

- Data compiled on a 100 km tile basis; land parcels classified per parcel and added to their appropriate 100 km tile.
- Some tiles may be merged to simplify construction; a map illustrates 100 km tile coverage.

## Hierarchical nomenclature

- Vector data can provide both Subclass (Level 2) and Variant (Level 3) detail.
- Subclass and Variant codes map to 26 Subclasses and various Level 3 Variants (e.g., broad-leaved/mixed woodland, coniferous woodland, arable crops, etc.).
- Alpha and numeric codes accompany variants (e.g., D for Broad-leaved/mixed woodland; Dm for Broad-leaved/mixed variant; Cf for Coniferous woodland variant).
- The classification supports detailed Level 3 distinctions where possible, though accuracy may vary across areas.

## Vector polygon attributes

Each land parcel (SegID) carries a set of attributes, including:
- SegID: Unique parcel identifier (e.g., TQ005232); present for Level 2 and Level 3.
- BHSub: Dominant land cover type as hierarchical code (Level 2).
- BHSubVar: Variant code (Level 3) for the dominant land cover type.
- PerPixList: Top five spectral subclasses by percentage (present in Level 3).
- OpHistory: Processing history descriptor (input data, dates, KBC rules, etc.) with detailed history available.
- TotPixels: Total pixels within the parcel.
- CorePixels: Pixels within the core area used for maximum likelihood classification.

## OpHistory Attribute

- The OpHistory (PHD) contains five fields describing input data and stages of classification, knowledge-based correction (KBC), and dataset compilation; a sixth field covers other information.
- It encodes scene number, sensor (e.g., TM, IRS), acquisition dates, cloud/hole patches, spectral probability, aggregation flags, and phase 1/2 KBC rules.
- A sample descriptor illustrates how input imagery and processing steps are recorded per parcel.

## Colour recipes for LCM2000 mapping

- A predefined set of colour mappings is provided for display of the 26 Subclasses (and associated levels) to aid visualization.
- Colors are defined in terms of Hue, Saturation, Value and approximate RGB equivalents, with explicit values for representative Subclasses (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable cereals, Improved grassland, etc.).

## LCM2000 Broad Habitat descriptions

- Broad Habitat categories include:
  - Broad-leaved/mixed and yew woodland
  - Coniferous woodland
  - Boundaries and linear features
  - Arable and horticulture
  - Improved grassland
  - Neutral grassland
  - Calcareous grassland
  - Acid grassland
  - Bracken
  - Dwarf shrub heath
  - Fen, marsh and swamp
  - Bog
  - Standing open water and canals
  - Rivers and streams
  - Montane habitats
  - Inland rock
  - Built-up areas and gardens
  - Supra-littoral rock and sediment
  - Littoral rock and sediment
  - Inshore sublittoral sediment and rock
- Each category provides a description of vegetation, terrain, and typical management context to guide interpretation and mapping decisions.

## Appendix 1: Dealing with edge overlap problems

- Edge overlaps occur due to mosaic construction of multiple overlapping images and cloud hole patching; a single-layer parcel map is produced by erosion and merging.
- Artefacts at tile edges may include:
  - Different parcels classified using different imagery.
  - Edge parcels with inconsistent attributes due to tile-specific processing.
  - Slivers and very small parcels, often resulting from patching or clipping.
- Recommendations for users:
  - Visual tidying: dissolve boundaries between adjacent parcels of the same class using GIS legend tools, without altering underlying attribute data for the entire dataset.
  - Edge handling options:
    - Clip data to 100 km tile edges (note: may invalidate parcel-level metadata for clipped parcels).
    - Use union or dissolve with caveats about attribute validity after merging.
  - For Level 3 data, maintain bhsubvar delineations during dissolves to avoid losing important Level 3 information.
  - If tiles are merged, you can selectively dissolve edge areas to improve performance while preserving core data integrity.
- Handling of “slivers”:
  - Slivers can be removed visually or dissolved into adjacent same-class parcels using various GIS strategies, paying attention to context and data integrity.

## Appendix 2: Good practice

- (Not detailed in the provided text; referenced as a section for best practices.)

## Customisation, provenance and data management

- LCM2000 is designed as a data storage and analysis framework, not just a map; users are encouraged to modify and expand their version while retaining provenance.
- Unique labelling:
  - Each parcel has a SegID that should be retained to enable traceability and communication with data management teams.
- Production philosophy:
  - The production process aimed to retain as much information as possible; maintain parcel-level metadata and lineage when altering data.
- Documenting changes:
  - Thorough documentation of changes is essential for data management and reproducibility.
- Accuracy and interpretation:
  - Recognize that there are inherent inaccuracies due to data models, scale, resolution, and interpretation; differences from user needs may arise from these factors rather than a lack of accuracy.

# End note

- Important caveat: LCM2000 raster data is not directly comparable with LCM1990 due to methodological differences; the two datasets should not be used to estimate change over the 10-year period without careful consideration.