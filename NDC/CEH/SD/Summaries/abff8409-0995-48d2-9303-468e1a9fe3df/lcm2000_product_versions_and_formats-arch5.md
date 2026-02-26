# LCM2000 specification

- LCM2000 is a parcel-based thematic classification of satellite imagery covering the entire United Kingdom, produced in both vector and raster formats. It builds on LCMGB (1990) and extends to include Northern Ireland for an all-UK dataset. The classification follows a hierarchical nomenclature aligned with the JNCC Broad Habitats and records additional detail where possible.
- The raster and vector products are designed for broad usability and can be produced at multiple resolutions and detail levels. A key caution is that the 2000 dataset is not directly comparable with the 1990 dataset due to different methodologies, and it should not be used to estimate change over the 10-year period.

## Product versions overview

- Vector data
  - Level 2: Standard detail, 26 LCM2000 Subclasses (most widely used).
  - Level 3: Detailed down to 72 Variant level; higher complexity and support required; available by special arrangement with CEH staff.
  - Standard vector format is ESRI shapefile; may require Spatial Analyst for advanced ArcGIS analysis.
- Raster data (derived from the vector base)
  - 25 m resolution: 26 Subclasses.
  - 1 km resolution: derived at two levels of detail
    - Subclass level: 26 Subclasses
    - Aggregate level: 10 Aggregate classes
  - For 1 km: Dominant values and Percentage values per pixel available at Subclass and Aggregate levels.
- Overall note: Raster formats are GeoTiff; ArcGIS Spatial Analyst may be required for analysis.

## Dataset coverage

- Classified on a 100 km tile basis; land parcels are assigned to their 100 km tile and then combined. Some tiles may be merged to simplify construction. The dataset is designed to be all-UK, including Northern Ireland.

## Hierarchical nomenclature

- Vector data provide Subclass and (for Level 3) Variant detail. Subclass and Variant codes correspond to a broad habitat framework, enabling detailed classification and cross-walking with other habitat schemes. The dataset includes a comprehensive code table linking Subclass and Variant codes (Level 2 and Level 3 codes).

## Vector polygon attributes

- Each land parcel (SegID) carries:
  - BHSub: Dominant land cover type as a hierarchical code (Level 2).
  - BHSubVar: Dominant land cover type as a Level 3 variant code (Level 3 only).
  - PerPixList: Top five spectral Subclasses by pixel percentage (Level 3 only).
  - OpHistory: Processing history detailing image data and classification steps.
  - TotPixels: Total pixels in the parcel.
  - CorePixels: Pixels in the core area used for maximum likelihood classification.
- SegID is a unique label for each parcel and is recommended to be retained to preserve traceability.

## OpHistory Attribute

- The process history descriptor (PHD) on each segment consists of six fields describing input data and classification steps, including scene number, sensor, acquisition dates, and KBC rules. A seventh field (free-form) records additional information.
- Example fields cover: scene number, sensor (Landsat TM, IRS, etc.), acquisition dates, cloud hole patches, spectral probability, aggregation flags, phase 1 and 2 KBC rules, and a final status flag.

## Colour recipes for LCM2000 mapping

- A color mapping (Table 5) provides display colors for the 26 Subclasses to aid visualization in GIS tools. Colours are specified in RGB values or their approximations for consistent display in map products.

## LCM2000 Broad Habitat descriptions

- The Broad Habitat classification comprises 16 main habitat groups, including:
  - Broad-leaved/mixed woodland and coniferous woodland
  - Arable and horticulture
  - Various grasslands (improved, neutral, calcareous, acid)
  - Bracken, dwarf shrub heath, fen/marsh/swamp, bog
  - Standing water and canals; rivers/streams
  - Montane habitats; inland rock
  - Built-up areas and gardens
  - Coastal habitats (supra-littoral and littoral rock/sediments)
  - Inshore sublittoral and offshore categories are not distinguished in LCM2000
- Descriptions provide guidance on what each Broad Habitat represents and how vegetation and land cover characteristics map to the classes.

## Further Information

- Source and contact: Land Cover Map home page (www.ceh.ac.uk/data/lcm) and spatialdata@ceh.ac.uk; CEH sales contact for questions.
- Methodology references: Fuller et al. (2002) on parcel-based map construction; Smith et al. (2001) on parcel-based maps from satellite images; Jackson (2000) on Broad Habitat guidance.

## Appendix 1: Dealing with edge overlap problems

- Edge overlaps arise from mosaic imagery and cloud hole patching, creating multiple overlapping parcel layers within a 100 km tile.
- Artefacts are rare (often <0.1% of parcels) and can be addressed by users if needed. Common approaches include:
  - Visual tidying by dissolving boundaries between adjacent parcels of the same class (not across the entire dataset to avoid losing parcel-level metadata).
  - Clipping to 100 km tile edges, using geoprocessing tools to merge, and then dissolving like classes at Level 2 (Level 3 requires bhsubvar).
  - Using union of tiles or selective dissolving with edge-area selection to protect attribute data.
  - Precedence rules: when merging tiles, the first input tile generally prevails at the edge; differences in classification at the edge may occur if tiles differ.
  - For “slivers” or sub-minimum-mappable parcels, options include visual removal, dissolving with adjacent same-class parcels, or "intelligent" dissolving based on the longest shared boundary with neighboring parcels.
- The guidance emphasizes preserving source attributes and avoiding unintended degradation of parcel-level information.

## Appendix 2: Good practice

- Additional guidance on best practices for data handling, modification, and documenting changes is provided (content not shown in excerpt).

## Production philosophy

- Aims to retain as much information as possible; the dataset is information-rich. When altering LCM2000 data, maintain parcel-level metadata to document lineage and processing history; keep original attributes or create new attributes to reflect changes.

## Customisation

- LCM2000 is presented as a data storage and analysis framework, allowing users to adapt and expand the database for their needs while maintaining data provenance and traceability.

## Unique labelling

- Each parcel receives a unique Segid label, which should be retained to enable unambiguous communication with the data management team and other users.

## Production governance: Accuracy and correspondence

- Users should distinguish between actual inaccuracies and differences due to data model, scale, resolution, interpretation, or target class definitions. While LCM2000 contains inevitable inaccuracies, these may not be the primary cause of any misfit to user needs.