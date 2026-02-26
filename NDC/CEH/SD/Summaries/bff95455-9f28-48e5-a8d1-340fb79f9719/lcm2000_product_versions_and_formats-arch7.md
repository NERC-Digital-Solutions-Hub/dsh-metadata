# LCM2000 specification

- LCM2000 is a parcel-based thematic classification of satellite imagery for the entire United Kingdom, updating and upgrading the Land Cover Map of Great Britain (LCMGB) 1990. It is derived mainly from Landsat data, covers all UK regions including Northern Ireland, and combines information from ancillary datasets. It uses a hierarchical Broad Habitat classification aligned with JNCC Broad Habitats and is produced in both vector and raster formats with multiple detail levels and resolutions.

## Product versions and data formats

- Vector data format
  - Polygons (land parcels) with attached attributes
  - Level 2: Standard detail with 26 LCM2000 Subclasses (most widely used)
  - Level 3: Detail down to 72 Variant level; higher support required; available by special arrangement
  - Standard vector format: ESRI shapefile (ArcGIS suitability may require Spatial Analyst)
- Raster data format
  - 25 m resolution: 26 Subclasses
  - 1 km resolution: Derived from 25 m; includes Subclass level (26) and Aggregated levels
    - Dominant values per pixel (Subclass level)
    - Percentage values per pixel (Subclass level)
    - Aggregate class level (10 aggregated classes)
    - Dominant values (Aggregate level)
    - Percentage values (Aggregate level)
- Note: Raster data are not directly comparable with LCM1990 due to different construction methods; not suitable for 10-year change estimation.

## Dataset coverage and tile structure

- Data compiled on a 100 km tile basis; parcels classified per tile and added to the appropriate tile.
- Some parcels straddle tile edges and may require special handling when merging tiles.
- 100 km tiles may contain multiple overlapping source images; overlaps are removed to produce a single parcel layer.

## Hierarchical nomenclature (Subclasses and Variants)

- Vector data provides Subclass and Variant detail (Level 2 and Level 3 codes).
- Variant detail (Level 3) may be limited in certain areas due to imaging conditions; some distinctions rely on contextual information and may be out-of-date.

## Vector polygon attributes (key fields)

- SegID: Unique parcel identifier (with OS 100 km square and segment number)
- BHSub: Dominant land cover type (Level 2 Subclass)
- BHSubVar: Dominant land cover type with Level 3 Variants (if present)
- PerPixList: Top five spectral subclasses per pixel (Level 3 only)
- OpHistory: Processing history descriptor (image dates, KBC rules, etc.)
- TotPixels: Total pixels in the parcel
- CorePixels: Pixels in the core area used for classification

## OpHistory attribute (processing history)

- Five fields describe input data and classification steps; a sixth field captures other information
- Includes scene number, sensor types (e.g., TM, IRS), image acquisition dates, and KBC details
- Also includes indicators for data adaptation (e.g., void filling, cloud patches)

## Colour recipes for mapping (LCM2000)

- 26 Subclasses have predefined display colors (Hue, Saturation, Value or RGB equivalents)
- Colors assigned to each Subclass (examples include Broad-leaved/mixed woodland, Coniferous woodland, Arable cereals, etc.)
- Useful for map-based visualisation in GIS environments

## Broad Habitat descriptions

- 16 Broad Habitat groups with descriptive definitions, including:
  - Broad-leaved/mixed woodland
  - Coniferous woodland
  - Arable and horticulture
  - Improved grassland
  - Neutral and Calcareous grasslands
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
  - Coastal habitats ( supra-littoral and littoral, rock and sediment)

## Appendix 1: Dealing with edge overlap problems

- Edge overlaps arise from mosaic of overlapping images and cloud hole patching; multiple layers of parcels per 100 km tile
- Artifacts are infrequent (<~0.1% of parcels) and include:
  - Edge variants due to different imagery, erosion/merging differences
  - Small parcels or slivers
- Visual tidy-up options:
  - Dissolve boundaries between adjacent parcels of the same class (preferably at the Level 2 classification)
  - Do not dissolve across the entire dataset to preserve parcel-level metadata
- Practical approaches for edge management (ArcMap context):
  - Clip data to 100 km tile edges; using Merge themes can impact parcel-level attributes
  - Union of tiles retains copies of attributes but may invalidate some edge parcel attributes
  - Dissolve after edge handling; ensure Level 3 (bhsubvar) information is preserved when needed
  - Use select features to limit processing to edge areas for performance
- Edge handling priority rules:
  - First input tile often takes precedence at the edge; if classifications differ, outcome depends on the chosen rule

## Appendix 1: Dealing with 'slivers' and small parcels

- Slivers or parcels smaller than minimum mappable unit can be addressed by:
  - Visual removal via legend tools
  - Dissolving with adjacent parcels of the same class
  - Intelligent dissolution into the neighboring parcel with the longest shared boundary
- Important: preserve dataset context and attribute integrity; consider the impact on analysis

## Customisation and production philosophy

- LCM2000 is designed as an information-rich data framework, not just a map
- Users are encouraged to adapt and extend the dataset, maintaining parcel-level metadata to document lineage and processing history
- Maintain SegID and provide documentation of changes to support traceability

## Production notes and data integrity

- The aim is to retain as much information as possible; preserve original attributes and history when editing
- When updating, copy and store changed attributes in new fields to retain provenance
- Be mindful of terminology: describing differences due to data model, scale, resolution, or classification decisions is preferable to labeling them as inaccuracies

## Further information and references

- Land Cover Map home page: www.ceh.ac.uk/data/lcm
- Contact: spatialdata@ceh.ac.uk or +44 (0)1491 692315
- Key methodological references:
  - Fuller et al. 2002; The UK Land Cover Map 2000: construction of a parcel-based vector map from satellite images
  - Smith et al. 2001; Land Cover Map 2000: a parcel-based map from satellite images
  - Jackson 2000; JNCC Guidance on Broad Habitat Classification definitions and relationships

## Appendix 2

- Good practice (content not included in provided text)