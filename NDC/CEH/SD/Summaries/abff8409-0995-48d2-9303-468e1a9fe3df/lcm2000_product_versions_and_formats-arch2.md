# LCM2000 specification

- LCM2000 is a parcel-based thematic classification of UK satellite imagery covering the entire United Kingdom, extending the Land Cover Map of Great Britain (LCMGB) from 1990 to a UK-wide dataset (including Northern Ireland) derived mainly from Landsat with ancillary data.
- Classified using a hierarchical nomenclature aligned to JNCC Broad Habitats; aims to support broad habitat mapping while recording additional detail where possible.
- Produces both vector and raster formats with multiple versions and resolutions to suit different use cases.

## Product versions overview

- Minimum mappable area: >0.5 ha; parcels/lines smaller than 0.5 ha are dissolved into surrounding landscape during production.
- Vector data formats:
  - Level 2: 26 LCM2000 Subclasses (most widely used)
  - Level 3: up to 72 Variant level (requires special arrangement with CEH staff)
  - Standard vector format is ESRI shapefile (ArcGIS may require Spatial Analyst extension)
- Raster data formats (derived from the vector DB):
  - 25 m: 26 Subclasses
  - 1 km: derived at Subclass level with options for Dominant values and Percentage values; also supports Aggregate class level with Dominant and Percentage
- Raster data are GeoTIFF; not directly comparable with LCM1990 for change estimation over a decade.

## Dataset coverage

- Compiled on a 100 km tile basis; parcels classified per tile and added to the corresponding tile.
- Some tiles merged for construction efficiency; 100 km tiles are vector-based with potential overlaps at tile edges.

## Hierarchical nomenclature

- Vector data provide Subclass and Variant detail (Level 2 and Level 3 respectively).
- Subclass and Variant codes map to a predefined hierarchical classification (26 Subclasses at Level 2; Level 3 Variants provide finer detail).

## Vector polygon attributes

- Each land parcel (SegID) carries a set of attributes, including:
  - BHSub: Dominant land cover type (Level 2 subclass)
  - BHSubVar: Dominant land cover type (Level 3 variant)
  - PerPixList: Per-pixel percentages for top five spectral subclasses (Level 3)
  - OpHistory: Processing history descriptor detailing input data, dates, and classification steps
  - TotPixels: Total pixels in the parcel
  - CorePixels: Pixels in the core area used for maximum likelihood classification
- SegID is a unique parcel label, recommended to be retained to preserve lineage and communications with data management.

## OpHistory Attribute

- The OpHistory (PHD) provides a five-field (plus sixth field) descriptor of input data and the classification workflow, including:
  - Scene number and input image data (sensor, acquisition dates)
  - Single date cloud hole patch indicators (S, W, or X)
  - Spectral probability (scaled 0–100) reflecting the closeness to the dominant Broad Habitat
  - Probability aggregation flag (0 = none, 1 = applied)
  - Phase 1 KBC rules (scene-dependent) and Phase 2 KBC rules (UK-wide)
  - A sixth field with additional indicators (e.g., eroded/merged at tile edges, training data usage)
- Example and table mappings describe how scenes, sensors, and dates are recorded and interpreted.

## Colour recipes for LCM2000 mapping

- Colour mappings provided for each of the 26 Subclasses to aid display and interpretation (H, S, V and RGB equivalents).
- Color assignments are designed to enable clear visual discrimination of land cover classes in maps and GIS work.

## LCM2000 Broad Habitat descriptions

- Provides 16 Broad Habitats with detailed descriptive guidance, including:
  - Broad-leaved/mixed woodland and yew woodland
  - Coniferous woodland
  - Boundaries and linear features
  - Arable and horticulture
  - Improved grassland
  - Neutral and Calcareous grassland
  - Acid grassland
  - Bracken
  - Dwarf shrub heath
  - Fen, marsh and swamp
  - Bog
  - Standing water and canals
  - Rivers and streams
  - Montane habitats
  - Inland rock
  - Built-up areas and gardens
  - Coastal/sea-related habitats (supra-littoral, littoral)
- Distinctions are made at subclass level where possible; certain coastal regions use maritime masks to separate habitat types.

## Appendix 1: Dealing with edge overlap problems

- Edge overlaps arise from mosaicked imagery and cloud-hole patches; 100 km tiles may contain multiple overlapping parcel layers.
- Artefacts are infrequent (<0.1% of parcels) and can be addressed by:
  - Visual tidying, such as dissolving boundaries between adjacent parcels of the same class (without removing parcel-level metadata)
  - Clipping tiles to edges, merging tiles, or dissolving to remove edge boundaries (not across entire dataset to preserve attribute information)
  - Using selection tools to limit dissolves to edge areas
- When merging tiles, the first input tile often takes precedence for edge parcels; anomalies occur if classifications differ at the edge.

## Appendix 1 (continued): Handling edge artefacts visually and technically

- Recommendations for ArcMap workflows to minimize data degradation, including cautions about loss of source attributes when dissolving or merging.
- Level 3 data requires careful handling of bhsubvar during dissolves to avoid loss of important classification information.

## Customisation and production philosophy

- LCM2000 is designed as an information-rich data storage and analysis framework, not just a map.
- Users are encouraged to customize and expand their version, while preserving parcel-level meta-data to document lineage and changes.
- Unique Segid labels support unambiguous communication with data managers and between users.
- Whenever altering attributes, retain original values in new attributes to preserve provenance.

## Accuracy and interpretation

- LCM2000 acknowledges inherent inaccuracies due to data model, scale, resolution, interpretation, and definitions.
- Differences from user expectations should consider these factors rather than viewing inaccuracies as absolute errors.

## Further information

- Contact: Land Cover Map (CEH) via spatialdata@ceh.ac.uk or 01491 692315; data homepage at www.ceh.ac.uk/data/lcm
- Key references:
  - Fuller et al. 2002; Fuller et al. 2001 on construction of parcel-based vector maps from satellite images
  - Jackson 2000; JNCC guidance on Broad Habitat classification
- The methodology supports the broader aim of environmental monitoring and policy performance analysis by providing standardized, traceable land cover data.