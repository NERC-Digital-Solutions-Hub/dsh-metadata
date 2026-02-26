# LCM2000

- LCM2000 is a parcel-based thematic map of land cover for the entire United Kingdom, built from satellite imagery (primarily Landsat) with supplemental ancillary data. It updates and upgrades the 1990 Land Cover Map of Great Britain (LCMGB) to provide a UK-wide dataset that supports environmental monitoring and policy assessment over time.
- The classification is hierarchical and aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats, enabling broad habitat assessments and broader user needs beyond a single class. It is produced in both vector (parcels) and raster formats, with multiple detail levels and resolutions.

## Data Structure and Content

- Classification hierarchy:
  - Target classes and Subclasses focus on Broad Habitats (as defined by JNCC) and are extended where possible for broader user needs.
  - Class Variants (Level 3) provide additional detail but may vary in accuracy across areas.
- Levels and formats:
  - Vector data (parcels) in ESRI shapefiles:
    - Level 2: 26 Subclasses (most widely used)
    - Level 3: up to 72 Variants (special arrangement required for access)
  - Raster data derived from the vector data:
    - 25 m grid: 26 Subclasses
    - 1 km grid: Subclass level (26), Dominant values, and Percentage values; 10 Aggregate classes derived from 26 Subclasses
- Important caveat: The 2000 raster data are not directly comparable with the 1990 LCMGB data and should not be used to estimate change over the 10-year period without careful consideration of methodological differences.

## Product Versions and Availability

- Vector and raster products are available in different detail levels and formats:
  - Vector:
    - Level 2: 26 Subclasses (standard)
    - Level 3: 72 Variants (special arrangement)
  - Raster:
    - 25 m resolution: 26 Subclasses
    - 1 km resolution: Subclass level, Dominant, and Percentage values; and 10 Aggregate classes with Dominant and Percentage values
- Standard raster format is GeoTIFF; ArcGIS users may need the Spatial Analyst extension.
- A warning: Raster data are not directly comparable to LCM1990; use consistent methodology when assessing temporal change.

## Dataset Coverage and Geography

- Coverage is UK-wide, organized on a 100 km tile basis. Images are classified per parcel and then added to the appropriate tile.
- Some tiles were merged to simplify construction; parcels crossing tile edges may be retained in both adjoining tiles.
- Edge overlaps, cloud holes, and patching using multiple dates created multi-layered parcels within tiles, resolved by erosion/merging to a single layer.

## Nomenclature and Coding

- Vector data provide Subclass and Variant detail. A comprehensive code table links subclass and variant codes to descriptive broad habitat types.
- The scheme emphasizes broad habitat categories while allowing more detailed subclass/variant information where feasible.
- Contextual information may help differentiate classes, but records may not always be up to date.

## Vector Polygon Attributes and Processing History

- Each land parcel (SegID) carries attributes including:
  - BHSub: Dominant land cover class (Level 2)
  - BHSubVar: Dominant class with Level 3 detail (Variant)
  - PerPixList: Top-five spectral subclass percentages within the parcel (Level 3)
  - OpHistory: Processing history, including image dates and knowledge-based corrections
  - TotPixels, CorePixels: Pixel counts for parcel extent and core area
- OpHistory (Processing History Descriptor, PHD) details input data, KBC (knowledge-based correction) steps, and final dataset compilation. It contains scene numbers, sensor types, acquisition dates, cloud-hole patch flags, spectral probability metrics, KBC rule counts, and flags indicating artefacts or data provenance.

## Colour Mapping and Habitat Descriptions

- Colour recipes (Table 5) define display colors for the 26 Subclasses to aid map interpretation in GIS and visualization tools.
- Broad Habitat descriptions (Table 6) provide interpretative definitions for major habitat groups, including:
  - Broad-leaved/mixed woodland and coniferous woodland
  - Arable and horticulture, improved grassland, neutral and calcareous grasslands, acid grassland
  - Bracken, dwarf shrub heath, fen/marsh/swamp, bog, standing water and canals, rivers/streams
  - Montane habitats, inland bare ground, built-up areas and gardens, coastal habitats (supra-littoral and littoral rock/sediment), and inland water
- The Broad Habitat framework underpins the classification and supports ecosystem- and policy-relevant analyses.

## Edge Overlaps, Slivers, and Good Practice

- Edge overlap problems arise from mosaicking multiple overlapping images and patching cloud holes:
  - Artefacts include edge-boundary inconsistencies, multiple layer parcels, and small slivers under 0.5 ha.
  - Guidance is provided to visually tidy edges and manage data integrity, including dissolving boundaries between adjacent parcels of the same class and careful handling of Level 3 data.
- Practical steps for handling edge artefacts in GIS (e.g., ArcMap):
  - Clip or merge tiles with attention to preserving parcel-level attributes
  - Use dissolve, union, and select features cautiously to avoid loss of lineage or important attributes
  - Be aware that merging can affect per-pixel and parcel-level metadata; prioritize maintaining the Segid and original attributes
- Slivers and very small parcels can be dealt with by visual removal, dissolving with adjacent similar-class parcels, or intelligent dissolution based on boundary length with surrounding parcels.
- The production philosophy emphasizes preserving information and lineage; any alterations should retain parcel metadata and document changes for traceability.

## Customisation, Production Philosophy, and Data Use

- LCM2000 is designed as a data storage and analysis framework, not just a map. Users are encouraged to customise and expand the dataset while preserving parcel-level metadata and lineage.
- Unique Segid labeling provides unambiguous communication with the data management team and between users.
- The aim is to retain as much information as possible; when altering data, copy and preserve original attributes in new fields to maintain a clear history.
- Users should document changes to support data security, reproducibility, and feedback to data custodians.

## Accuracy and Interpretation

- LCM2000 acknowledges inherent inaccuracies due to data model choices, scale, resolution, interpretation, and target-class definitions.
- Users should avoid mislabeling differences caused by these factors as measurement error; interpretations should consider the data’s methodological context.
- The dataset is not intended as a straightforward change-detection tool with LCM1990; differences reflect updated methods and data sources.

## Further Information and References

- For data access and inquiries: CEH Land Cover Map team (spatialdata@ceh.ac.uk; +44 1491 838800)
- Land Cover Map homepage: www.ceh.ac.uk/data/lcm
- Methodology references:
  - Fuller et al. 2002; The UK Land Cover Map 2000: construction of a parcel-based vector map from satellite images
  - Smith et al. 2001; Land Cover Map 2000: a parcel-based map from satellite images
  - Jackson 2000; Guidance on the interpretation of the Biodiversity Broad Habitat Classification (JNCC)
- Appendix 2: Good practice guidelines (not fully detailed in this document excerpt) and Appendix 1 provides detailed edge-management procedures.