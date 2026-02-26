# LCM2000 specification

- LCM2000 is a parcel-based thematic land cover map for the United Kingdom, updating the Land Cover Map of Great Britain (LCMGB) 1990 and extending coverage to Northern Ireland for a UK-wide dataset.
- It is derived from a computer classification of satellite imagery (primarily Landsat), with additional information from ancillary datasets; uses a hierarchical nomenclature aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats.
- The dataset is produced in both vector and raster formats, available in multiple versions with different levels of detail and spatial resolutions.

## Product versions overview

- Vector data (land parcels as polygons) with attached attribute lists.
  - Level 2: 26 LCM2000 Subclasses (standard, widely used).
  - Level 3: 72 Variant level details (special arrangements with CEH required for access and support).
  - Standard vector format: ESRI shapefile (ArcGIS may require Spatial Analyst for analysis).
- Raster data derived from the Vector database.
  - 25 m resolution: 26 Subclasses.
  - 1 km resolution: data derived from 25 m with two detail levels:
    - Subclass level: 26 Subclasses.
    - Aggregate level: 10 simplified Aggregate classes.
  - Raster formats: GeoTIFF (ArcGIS Spatial Analyst may be required).
- Note: The 1 km raster is not directly comparable with the LCM1990 dataset due to different construction methods.

## Dataset coverage

- Compiled on a 100 km tile basis; land parcels classified per tile and then assembled into tiles (some tiles merged for construction efficiency).
- Edge and overlap handling results in artefacts in a minority of cases (<0.1%), typically managed by users as described in the appendices.

## Hierarchical nomenclature

- Vector data provides Subclass and Variant detail (Level 2 and Level 3, respectively).
- Codes map to Broad Habitat classifications (e.g., broad-leaved/mixed woodland, coniferous woodland, arable, various grasslands, heath, bog, water, urban, coastal habitats, etc.).
- Some Variant details depend on dominant land cover at imaging time; distinctions may be limited where crops are harvested or data are dated.

## Vector polygon attributes

- Each parcel carries a set of attributes, including:
  - SegID: unique parcel identifier.
  - BHSub: dominant land cover type (Subclass code).
  - BHSubVar: dominant land cover type at Variant level (Level 3).
  - PerPixList: per-pixel list of top spectral subclasses (Level 3 only).
  - OpHistory: processing history (see below).
  - TotPixels: total number of pixels in the parcel.
  - CorePixels: pixels used for the maximum likelihood classification.
- OpHistory (processing history descriptor) provides detailed input data and classification steps (scene, sensor, acquisition dates, cloud hole patches, KBC rules applied, probability aggregation, and quality/other flags). Includes a six-field core with an optional seventh field describing additional conditions (e.g., edge erosion, data origin, training, etc.).

## OpHistory Attribute (processing history)

- The OpHistory field records scene number, sensor data, acquisition dates, cloud/hole patch indicators, spectral probability metrics, aggregation flags, numbers of Phase 1 and Phase 2 KBC rules applied, and quality flags.
- A seven-field descriptor provides a comprehensive trace of input imagery, processing steps, and data provenance for each parcel.

## Colour mapping and Broad Habitat descriptions

- Colour recipes (Table 5) specify display colours for the 26 Subclasses to aid visualization in GIS.
- Broad Habitats descriptions (Table 6) provide definitions for each habitat category (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Water, Montane, Inland rock, Built-up areas, Coastal habitats, etc.).
- These descriptions underpin the hierarchical mapping between the 26 Subclasses and broader habitat classifications used in policy and monitoring contexts.

## Further Information

- Land Cover Map homepage: www.ceh.ac.uk/data/lcm
- Contacts: spatialdata@ceh.ac.uk; phone 01491 692315
- Key methodological references:
  - Fuller, R.M. et al. (2002). The UK Land Cover Map 2000: construction of a parcel-based map from satellite images.
  - Smith, G.M. et al. (2001). Land Cover Map 2000: a parcel-based map from satellite images.
  - Jackson, D.L. (2000). Guidance on the interpretation of the Biodiversity Broad Habitat Classification (JNCC Report No. 307).

## Appendix 1: Dealing with edge overlap problems

- 100 km tiles created from overlapping imagery and cloud-hole patches may produce edge artefacts.
- Artefacts are rare (<0.1%) but can occur due to differing imagery at tile edges or during erosion/merging.
- Recommended approaches:
  - Visually tidy edge areas by dissolving boundaries between identical classes (preserve parcel-level attributes).
  - Clip to the 100 km tile edge or merge tiles with caution; each method has implications for parcel-level attributes (e.g., image history, TotPixels, CorePixels).
  - Use dissolve with Level 2 or Level 3 classifications; be aware that dissolving Level 3 data can lose Level 3 information.
  - If merging, prioritize the first input tile but assess edge cases where classifications differ.
  - For edge slivers, options include dissolving adjacent similar-class parcels, intelligent dissolution based on boundary length, or visual removal with care not to degrade source metadata.
- Guidance emphasizes maintaining data provenance and attribute integrity; edge artefacts should be handled by users based on their needs.

## Appendix 2: Good practice

- The document includes additional guidance on best practices for data use and management (specific content not provided in excerpt).

## Production philosophy and data governance

- Emphasises retaining as much information as possible; users are encouraged to customize and expand the dataset while preserving lineage.
- Unique SegID labeling should be retained to maintain clear communications with data management teams and between users.
- Documentation of changes is crucial for data management, security, and feedback to the LCM2000 team.

## Accuracy and applicability

- Acknowledges inevitable inaccuracies due to data model, scale, resolution, interpretation, and classification definitions.
- Cautions against assuming direct comparability with earlier data (e.g., LCM1990) or inferring precise change over time without considering methodological differences.
- Encourages users to consider context and metadata when evaluating data for monitoring and policy assessment.