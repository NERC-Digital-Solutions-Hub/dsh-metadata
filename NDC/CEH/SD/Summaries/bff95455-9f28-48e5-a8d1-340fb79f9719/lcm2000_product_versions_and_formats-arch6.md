# LCM2000 specification

- LCM2000 is a parcel-based thematic classification of satellite imagery that maps land cover across the entire United Kingdom, updating the Land Cover Map of Great Britain (LCMGB) 1990 and expanding coverage to Northern Ireland for an all-UK dataset.
- It uses a hierarchical nomenclature aligned with JNCC Broad Habitats, recording broad habitat types and additional detail where possible for wider use.
- Produced in both vector and raster formats, with multiple versions offering different levels of detail and spatial resolutions.

## Product formats and versions

- Vector data (parcels) with attributes:
  - Level 2: 26 LCM2000 Subclasses (standard, most widely used)
  - Level 3: up to 72 Variant level (special arrangement with CEH staff; higher support required)
  - Standard format: ESRI shapefile (ArcGIS may require Spatial Analyst for further analysis)
- Raster data (derived from vector):
  - 25 m grid: 26 Subclasses
  - 1 km grid: derived from 25 m with two detail levels
    - Subclass level: 26 Subclasses
    - Dominant values and Percentage values per 1 km pixel
  - Aggregate class level (10 simplified aggregates) with Dominant and Percentage values
  - Standard raster format: GeoTiff (ArcGIS Spatial Analyst recommended)
- Important note: Raster data are not directly comparable with LCM1990 and are not suitable for estimating change over the 10-year period.

## Dataset coverage and nomenclature

- Coverage is compiled on a 100 km tile basis; land parcels are classified per parcel and added to the appropriate 100 km tile.
- The dataset is mosaicked from multiple source images; some tiles have merged sources to simplify construction.
- Classifications include a hierarchical Subclass/Variant structure; Variant level detail varies by imagery and may require expert interpretation.

## Vector polygon attributes and OpHistory

- Each land parcel (SegID) carries a set of attributes, including:
  - BHSub: dominant land cover (Subclass)
  - BHSubVar: dominant land cover (Variant, Level 3)
  - PerPixList: top-five spectral subclasses by pixel percentage
  - OpHistory: processing history details (image dates, KBC rules, etc.)
  - TotPixels and CorePixels: pixel counts
- OpHistory (PHD) provides a five-field descriptor per parcel detailing input data, classification stages, knowledge-based corrections (KBC), and production history; a sixth field holds other information.
- A detailed table (Table 4) lists scenes, sensors, and acquisition dates used per area, clarifying the data provenance and processing steps.

## Colour mapping and Broad Habitat descriptions

- Colour recipes (Table 5) provide recommended display colors for the 26 Subclasses to aid visualization in GIS.
- Broad Habitat descriptions (Table 6) cover major habitat groups, including:
  - Broad-leaved/mixed woodland and coniferous woodland
  - Arable and horticulture; improved, neutral, calcareous, and acid grasslands
  - Bracken; dwarf shrub heath; fen/marsh/swamp; bog; standing water and canals
  - Montane habitats; inland rock; built-up areas and gardens
  - Coastal habitats: Supra-littoral and Littoral rock and sediment
  - Inland water bodies and urban/rural development categories
- Notes indicate that distinctions at Variant level depend on dominant land cover at image time and may be limited in some areas (e.g., post-harvest crops).

## Practical usage, data quality, and limitations

- The dataset is intended as an extensible data storage and analysis framework; users are encouraged to customize while preserving provenance.
- LCM2000 aims to retain as much information as possible; users should maintain parcel-level metadata to document lineage and changes.
- Users should be mindful of inaccuracies arising from data model, scale, resolution, interpretation, and target class definitions; LCM2000 is not intended to imply perfect accuracy.
- The raster dataset is not a direct change-detection product relative to LCM1990; differences may reflect methodological changes rather than real-world change.

## Appendix highlights

- Appendix 1: Dealing with edge overlap problems
  - Edge overlaps occur where tiles share parcels; overlaps are removed through erosion and merging to yield a single parcel layer per 100 km tile, though some artifacts may remain and are usually <0.1% of parcels.
  - Artefacts include differing classifications at tile edges and potential boundary boundaries between same-class parcels.
  - Practical remedies include visual tidying (dissolving boundaries between adjacent parcels of the same class via GIS tools), clipping to tile edges, or using union/ dissolve operations with awareness of attribute changes.
  - For Level 3 data, preserve bhsubvar during dissolving to avoid losing key information; ordering of input tiles can affect edge parcels in merges.
  - Slivers and very small parcels can be handled by visual removal, dissolving with adjacent same-class parcels, or “intelligent” dissolving based on longest shared boundary, while preserving data context.
- Appendix 2: Good practice
  - Acknowledges guidance on responsible data handling and documentation (details not provided in the excerpt).
- Production philosophy and customization
  - Emphasizes retaining extensive information and allowing user-driven customization and expansion.
  - Each parcel has a unique Segid; retaining this identifier supports clear communication with the data management team.
  - When modifying data, maintain lineage by recording changes in new attributes or preserving originals.

## Further information

- Land Cover Map home: www.ceh.ac.uk/data/lcm
- Contact: spatialdata@ceh.ac.uk or +44 (0)1491 692315
- Key references:
  - Fuller et al. 2002; Smith et al. 2001; Jackson 2000
  - For Broad Habitat classification guidance: JNCC Report No. 307