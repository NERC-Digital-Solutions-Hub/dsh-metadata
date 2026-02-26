# LCM2000 specification

- LCM2000 is a parcel-based thematic classification of satellite image data covering the entire United Kingdom, upgrading the Land Cover Map of Great Britain (LCMGB) from 1990 and producing an all-UK dataset (including Northern Ireland).
- Classified from Landsat-based imagery and supplemented with ancillary datasets; aligned to the Joint Nature Conservation Committee (JNCC) Broad Habitats classification, with additional detail where possible.
- Available in vector and raster formats, with multiple product versions offering different levels of detail and spatial resolutions.

## Product versions overview

- Vector data
  - Level 2: Standard level with 26 LCM2000 Subclasses.
  - Level 3: Detailed down to 72 Variant levels; higher detail may vary in accuracy by area and requires special arrangement with CEH staff.
- Raster data
  - 25 m resolution: 26 Subclasses.
  - 1 km resolution: Derived from 25 m raster; includes Subclass level, Dominant values, and Percentage values; also supports Aggregate class level (10 simplified aggregates) with Dominant and Percentage values.
- Formats
  - Vector: Polygons (land parcels) with attributes; standard vector format is an ESRI shapefile (Spatial Analyst extension may be needed in ArcGIS).
  - Raster: GeoTIFF; two resolutions available (25 m and 1 km).
- Important note: The LCM2000 raster dataset is not directly comparable with the LCM1990 dataset due to differing construction methods and is not suitable for estimating change over the 10-year period.

## Dataset coverage

- Compiled on a 100 km tile basis; imagery classified per parcel and added to the corresponding 100 km tile (tiles may be merged to simplify construction).
- Edge parcels may straddle tile boundaries and be present in multiple tiles.

## Hierarchical nomenclature

- Vector data provides Subclass detail and, for Level 3, Variant detail.
- Codes include Subclass codes and Variant codes (e.g., broad habitat types such as Broad-leaved/mixed woodland; Coniferous woodland; Arable and horticulture; etc.).
- Each parcel carries a BHSub (dominant land cover subclass code) and may include BHSubVar (Variant code) where available; context and dominance at imaging time affect variant recognition.
- A colour and naming scheme is provided for display across the 26 Subclasses.

## Vector polygon attributes

- SegID: Unique identifier for each land parcel, indicating the 100 km square and segment number.
- BHSub: Dominant land cover subclass (WidespreadBH.LCMSubclass).
- BHSubVar: Variant level for Level 3 (if present).
- PerPixList: Per-pixel list of top spectral subclasses within the parcel (Level 3 only).
- OpHistory: Processing history descriptor detailing image date(s) and knowledge-based corrections and rules applied.
- TotPixels: Total pixels in the parcel.
- CorePixels: Pixels within the core area used for maximum likelihood classification.

## OpHistory Attribute

- Contains a six-field Processing History Descriptor (PHD) for each parcel, with fields for scene number, sensor, acquisition dates, and flags for processing steps (KBC rules, probability aggregation, etc.), plus an additional information field.
- Includes a key mapping of scene data (sensor type, acquisition dates) and interpretation of spectral probabilities and KBC rule counts.

## Colour recipes for LCM2000 mapping

- A colour mapping is provided for all 26 Subclasses to aid display performance, with specific Hue, Saturation, Value (or RGB equivalents) values for each subclass.
- The palette is designed to distinguish major habitat types (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable cereals, Improved grassland, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Water, Montane, Inland rock, Built-up areas, Coastal habitats, etc.).

## LCM2000 Broad Habitat descriptions

- Broad-leaved, mixed and yew woodland
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
- Rivers, streams
- Montane Habitats
- Inland rock
- Built-up areas and gardens
- Supra-littoral rock
- Supra-littoral sediment
- Littoral rock
- Littoral sediment
- Inshore sublittoral sediment
- Inshore sublittoral rock
- Offshore shelf sediment/rock
- Continental shelf slope
- Oceanic seas
- These broad habitat descriptions provide guidance on interpretation and the relationships between habitat types and their spectral/classification characteristics.

## Further Information

- Data and methodology information available at the Land Cover Map homepage: www.ceh.ac.uk/data/lcm
- Contact: spatialdata@ceh.ac.uk or phone 01491 692315; references to Fuller et al. (2002) and Smith et al. (2001) for methodology.

## Appendix 1: Dealing with edge overlap problems

- Edge overlaps arise from mosaicking multiple overlapping images; 100 km tiles contain multiple layers of overlapping parcels.
- Artefacts may occur at tile edges due to differing imagery and erosion/merging operations; these artefacts are typically very rare (<0.1% of parcels).
- Practical approaches to address edge artefacts visually and operationally:
  - Visual tidying: dissolve boundaries between adjacent parcels of the same class using legend tools (ArcMap) without degrading source attributes.
  - Edge clipping: clip data to the 100 km tile edge and merge tiles; note that clipping can invalidate parcel-level attributes (TotPixels, OpHistory, etc.) for edge parcels.
  - Union/merge approaches: merging tiles can preserve attributes but may introduce incorrect values for overlapping edge parcels.
  - For Level 3 data, ensure bhSubVar is preserved during dissolves to avoid losing level-3 information.
  - Edge-specific selection can speed up boundary dissolves; priority often given to the first input tile when merging.
- Handling slivers and very small parcels:
  - Visual removal or dissolving into surrounding parcels of the same class.
  - Intelligent dissolving based on the longest shared boundary with the most similar adjacent class.
  - When removing small parcels, preserve awareness of their potential impact on the dataset as a whole.

## Appendix 2: Good practice

- (Note: The provided text does not include the contents of Appendix 2; see the original document for details.)

## Customisation, production philosophy and data integrity

- LCM2000 is designed as a data storage and analysis framework; users are encouraged to modify and extend their version while retaining lineage and parcel-level metadata.
- Unique Segid labeling should be retained to maintain communication with the data management team and among users.
- Production philosophy emphasizes preserving as much information as possible; attribute lineage should be maintained when altering data.
- Documenting changes is essential for data management and traceability.
- Users should recognise that differences arising from data model, scale, resolution, interpretation, or target class definitions contribute to inaccuracy; LCM2000 acknowledges these limitations but can still meet many user needs.