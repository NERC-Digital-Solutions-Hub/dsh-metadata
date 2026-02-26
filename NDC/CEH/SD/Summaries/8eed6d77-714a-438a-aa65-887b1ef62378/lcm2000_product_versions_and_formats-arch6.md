# LCM2000 specification

## Overview
- LCM2000 is a parcel-based thematic classification of UK land cover, derived mainly from Landsat satellite imagery, covering Great Britain and Northern Ireland for a single all-UK dataset.
- It is produced in both vector and raster formats, with a hierarchical nomenclature aligned to the Joint Nature Conservation Committee (JNCC) Broad Habitats.
- Multiple product versions exist, offering varying levels of detail and at different spatial resolutions.

## Product versions and formats
- Vector data (parcels with attributes):
  - Level 2: 26 Subclasses (standard widely used).
  - Level 3: 72 Variant level details (requires special arrangement and more user support).
  - Standard vector format is ESRI shapefile; ArcGIS users may need Spatial Analyst for advanced analysis.
- Raster data (GeoTiff):
  - 25 m resolution with 26 Subclasses.
  - 1 km resolution with:
    - Subclass level (26 Subclasses).
    - Dominant values per pixel at Subclass level.
    - Percentage values per pixel at Subclass level.
    - 10 Aggregate classes (combining Subclasses) with Dominant and Percentage values.
- Note: Raster data is not directly comparable to LCM1990 due to different construction methods.

## Dataset coverage
- Compiled on a 100 km tile basis; parcels are classified per tile and added to the appropriate 100 km tile.
- Some tiles are merged or adjusted to simplify construction.
- 0.5 ha is the minimum mappable area; parcels smaller than this are dissolved into surrounding areas where possible.
- The dataset is not directly change-detection-ready with older maps (e.g., LCM1990).

## Hierarchical nomenclature
- Vector data provides both Subclass and Variant detail (Level 2 and Level 3).
- Subclass codes and Variant codes are defined in detail (Level 2 and Level 3); Variant Level 3 clarifies finer distinctions where possible.
- Each land cover type has an alpha code (e.g., D for Broad-leaved woodland, C for Coniferous woodland) and a numeric Variant code.
- Ability to distinguish Variant level depends on dominant land cover in the image acquisition time and may be limited in some areas (e.g., harvested crops).

## Vector polygon attributes
- Each land parcel carries a set of attributes:
  - SegID: Unique identifier for each parcel (e.g., TQ005232); retained for communication with data managers.
  - BHSub: Dominant land cover type (Level 2 Subclass code).
  - BHSubVar: Dominant land cover Type (Level 3 Variant code) (Level 3 present).
  - PerPixList: Top five spectral subclasses by pixel percentage per segment (Level 3 present).
  - OpHistory: Processing history for the segment (image dates and KBC rules applied) (Level 2 and 3 present).
  - TotPixels: Total pixel count within the segment.
  - CorePixels: Pixels inside the core area used for maximum likelihood classification.
- OpHistory details the input data, scene, sensors, dates, and the progression through classification and correction steps.

## OpHistory Attribute
- The OpHistory Descriptor (PHD) on each segment contains five fields about input data and classification stages, plus a sixth field for other information.
- Includes scene number, sensor type, image acquisition dates, cloud-hole patch indicators, and flags for QA steps (KBC) and probability aggregation.
- A reference mapping table documents which image scenes and dates were used (including Landsat TM, IRS data, and dates).
- Also records the extent of Phase 1 and Phase 2 KBC rules applied and a quality/processing flag.

## Colour mapping (colour recipes)
- 26 Subclasses are assigned recommended display colours (Hue, Saturation, Value; and approximate RGB values) to assist visualization.
- Examples include:
  - Broad-leaved / mixed woodland: distinct hues and values.
  - Coniferous woodland; Arable cereals; Arable horticulture; Arable non-rotational; Improved grassland; Setaside grass; Neutral/Calcareous/Acid grasslands; Bracken; Dwarf shrub heath; Fen/marsh/swamp; Bog; Inland water; Montane habitats; Inland bare ground; Suburban/urban; Built-up areas; Coastal and marine-related habitats.
- The mapping supports consistent visual interpretation across subclasses and helps with quick UI differentiation.

## Broad Habitat descriptions
- A hierarchical broad habitat classification (JNCC Broad Habitats) is provided, including:
  - Broad-leaved/mixed woodland and yew woodland; Coniferous woodland.
  - Boundaries and linear features; Arable and horticulture; Improved grassland; Neutral grassland; Calcareous grassland; Acid grassland.
  - Bracken; Dwarf shrub heath; Fen/marsh/swamp; Bog; Standing water and canals; Rivers/streams.
  - Montane habitats; Inland rock; Built-up areas and gardens.
  - Coastal habitats: Supra-littoral and Littoral rock and sediment; Inshore sublittoral and related categories.
- Each habitat type is described in terms of its typical vegetation, structure, and mapping considerations (e.g., peat depth, vegetation density, and spectral separability).

## Further information
- Data access and inquiries: Land Cover Map home page, CEH; contact via spatialdata@ceh.ac.uk or phone.
- References for methodology:
  - Fuller et al. 2002; Smith et al. 2001; Smith et al. 2002 (remote sensing approach to parcel-based mapping).
  - Jackson 2000 (broad habitat classification definitions and relationships).
- For detailed Broad Habitat definitions, refer to the JNCC guidance (Table 6 descriptions).

## Appendix 1: Dealing with edge overlap problems
- Edge overlaps arise from mosaic imagery and cloud-hole patching; tiles contain multiple overlapping parcels.
- Overlaps are removed via erosion and merging to yield a single parcel layer per tile; parcels crossing tile edges may be retained in both neighboring tiles.
- Artefacts from edge handling are rare (<0.1% of parcels) but may occur, and users are advised to tidy visually if needed.
- Visual tidying can be done by dissolving boundaries between adjacent parcels of the same class using GIS tools, or by clipping/merging tiles with awareness of attribute data changes.
- Specific cautions:
  - Dissolving across the whole dataset can remove parcel-level attribute information.
  - Level 3 data requires preserving bhsubvar during dissolves to avoid losing Level 3 detail.
  - When merging tiles, the first input tile often precedes for edge parcels; some boundary effects may occur if different classifications exist at the edge.
- Techniques to speed up edge processing:
  - Use select feature tools to target edge areas before dissolving.
  - Be mindful of attribute integrity after merges (e.g., per-pixel counts and image history).

## Appendix 2: Good practice
- Guidance on best practices for working with LCM2000 data is provided; specific details are not included in this excerpt.

## Production philosophy
- Aims to retain as much information as possible; LCM2000 is an information-rich dataset.
- Encourage users to record lineage and processing history at the parcel level, and to preserve original attribute information when modifying data.

## Customisation
- LCM2000 is designed as a data storage and analysis framework, suitable for extension and adaptation.
- Users are encouraged to alter and expand the dataset while maintaining provenance.

## Unique labelling
- Each parcel has a unique SegID; retain this attribute for clear communication with data managers and other users.

## Production practices and data integrity
- Document changes thoroughly to enable traceability and data security.
- Be mindful that LCM2000 contains inevitable inaccuracies due to data model, scale, resolution, interpretation, and classification target definitions.
- Distinguish between incompatibilities due to modelling or resolution and true data inaccuracy when reporting differences.