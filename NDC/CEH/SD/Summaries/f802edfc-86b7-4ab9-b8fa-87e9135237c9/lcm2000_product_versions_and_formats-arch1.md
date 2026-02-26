# LCM2000 specification

- LCM2000 is a parcel-based thematic land cover classification for the entire United Kingdom, updating and upgrading the LCMGB 1990 dataset and extending coverage to Northern Ireland for an all-UK dataset.
- Classifies satellite imagery (mainly Landsat) with additional ancillary data, using a hierarchical nomenclature aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats.
- Available in both vector and raster formats, with multiple detail levels and resolutions to support different uses.

## Product versions and data formats

- Vector data (polygons/land parcels) with attributes; standard Level 2 provides 26 Subclasses; Level 3 provides 72 Variants (more detailed, with varying accuracy by area; Level 3 may require special arrangement and additional support).
- Raster data (GeoTIFF) at two resolutions derived from the vector base:
  - 25 m grid: 26 Subclasses
  - 1 km grid: summarised at Subclass and Aggregate levels (dominant and percentage values)
- Raster products are not directly comparable to LCM1990 due to different production methods; suitable for many analyses but not for estimating 10-year change from 1990 to 2000.

## Dataset coverage and nomenclature

- Compiled on a 100 km tile basis; images classified per parcel and added to corresponding 100 km tile.
- Vector data supports Subclass and Variant detail (Level 2 and Level 3); subclass/variant codes are provided to describe land cover types.
- Hierarchical structure: Subclass codes and Variant codes map to a wide range of UK habitats; certain fields (e.g., BHSub, BHSubVar) indicate dominant land cover at the parcel level.

## Vector polygon attributes and OpHistory

- Each land parcel (SegID) carries a set of attributes:
  - BHSub: Dominant land cover type (Level 2/Subclass)
  - BHSubVar: Dominant land cover type (Level 3/Variant)
  - PerPixList: Top-five spectral subclasses by pixel percentage (Level 3 only)
  - OpHistory: Processing history details (image dates, KBC rules, etc.)
  - TotPixels: Total pixels in the parcel
  - CorePixels: Pixels in the parcel core used for maximum likelihood classification
- OpHistory is a six-field descriptor (plus a sixth field for other information) documenting:
  - Scene number, sensor, acquisition dates, and patching details
  - The six-field scheme includes indicators for image data and processing steps (e.g., KBC rules, probability aggregation)
- Detailed field descriptions and table references (including Table 4 with scene data) provide the provenance and lineage of each parcel.

## Colour mapping and Broad Habitat descriptions

- Colour recipes (Table 5) specify display colors for the 26 Subclasses to aid visualization, including Hue, Saturation, Value and approximate RGB equivalents.
- Broad Habitat descriptions (Table 6) outline meanings for major habitat groups, such as:
  - Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Standing water, Montane habitats, Inland rock, Built-up areas, coastal/littoral habitats, and more.
- The classification emphasizes broad habitat categories with detailed subclass distinctions where possible.

## Processing details and edge overlap (Appendix 1)

- LCM2000 mosaics from multiple overlapping images and cloud-hole patches create edge overlaps within 100 km tiles.
- Edge overlaps are resolved by erosion and merging to produce a single parcel layer; parcels straddling tile edges may be retained in adjacent tiles.
- Artefacts at tile edges can occur; users may visually tidy by dissolving boundaries between adjacent parcels of the same class (ArcMap legend tools recommended) but should avoid dissolving across all data to preserve parcel-level attributes.
- Edge handling options:
  - Clip to 100 km square edge (may discard parcel-level attributes)
  - Merge tiles with “Union” (retains overlapping parcels but may duplicate attributes)
  - Dissolve boundaries between like classes at Level 2 (and Level 3 using bhsubvar) with awareness of attribute data changes
  - Use selective dissolving (e.g., select edge parcels and dissolve) to balance speed and data integrity
- First-input tile precedence: when merging tiles, the attributes from the first input tile may be retained at overlaps; differences at the edge may occur depending on which tile is used.
- Slivers and very small parcels can be managed by visual removal, dissolving with adjacent similar parcels, or intelligent dissolving based on longest shared boundary; retain awareness of the potential loss of important attributes.

## Customisation, unique labeling, and production philosophy

- LCM2000 supports customization and the dataset is intended as a foundation for further research and applications.
- Unique SegID labels are assigned to each parcel; it is recommended to retain SegID for unambiguous communication with data managers and users.
- Production philosophy prioritizes retaining as much information as possible; users should record lineage and processing history when altering the data and keep original attributes in new fields if changes are made.
- Fully documenting changes aids data management and accountability.

## Accuracy and guidance

- LCM2000 acknowledges inherent inaccuracies due to data model, scale, resolution, interpretation, and class definitions; users should distinguish between inaccuracies and differences arising from methodological choices.
- The dataset provides rich attribute information to support interpretation, but users should consider scale and methodological differences when applying results to decision-making.

## Further information and references

- Land Cover Map home page: www.ceh.ac.uk/data/lcm
- Contact: spatialdata@ceh.ac.uk; phone 01491 692315
- Key methodological references:
  - Fuller et al. 2002. The UK Land Cover Map 2000: construction of a parcel-based vector map from satellite images
  - Smith et al. 2001. Land Cover Map 2000: a parcel-based map from satellite images
  - Jackson 2000. Guidance on interpretation of the Biodiversity Broad Habitat Classification (JNCC)
- Appendix 2 (Good practice) content is indicated but not included in the provided text.