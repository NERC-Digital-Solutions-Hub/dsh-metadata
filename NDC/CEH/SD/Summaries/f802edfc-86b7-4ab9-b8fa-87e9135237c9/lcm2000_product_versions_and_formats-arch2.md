# LCM2000 specification

- LCM2000 is a parcel-based thematic classification of satellite image data covering the entire United Kingdom, updating and substantially upgrading the Land Cover Map of Great Britain (LCMGB) from 1990.
- It is derived mainly from Landsat satellite imagery, includes Northern Ireland for the first time, and incorporates information from ancillary datasets.
- The classification uses a hierarchical nomenclature aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats, capturing the full range of UK habitats and providing additional detail where possible.
- Available in both vector and raster formats, with multiple product versions offering different levels of detail and spatial resolutions; vector data is delivered as land parcels with attached attributes; raster data is provided at 25 m and 1 km resolutions.
- Key caution: the LCM2000 raster dataset is not directly comparable with the LCM1990 dataset and is not suitable for estimating change over the 10-year period.

- Data minimum mapping unit and processing:
  - Minimum mappable area is greater than 0.5 ha; parcels under 0.5 ha are dissolved into surrounding areas during production.
  - Class hierarchy prioritises Broad Habitats (for widespread examples) and extends the classification for wider use; Variant classes add detail but may vary in accuracy.

## Product versions overview

- Vector data (polygons, land parcels) with attributes:
  - Level 2: 26 LCM2000 Subclasses (most widely used).
  - Level 3: up to 72 Variant level (requires special arrangement and more user support).
  - Standard vector format is ESRI shapefile; ArcGIS users may require Spatial Analyst for advanced analysis.
- Raster data (GeoTiff) at:
  - 25 m resolution: 26 Subclasses.
  - 1 km resolution: derived from 25 m data; includes Subclass level (26 Subclasses) and aggregated outputs:
    - Dominant values per 1 km pixel (Subclass level)
    - Percentage values per 1 km pixel (Subclass level)
    - Aggregate class level (10 Aggregates derived from 26 Subclasses)
    - Dominant and percentage values at Aggregate level
- Raster formats noted as not directly comparable to LCM1990 for change detection.

## Dataset coverage and structure

- Data compiled on a 100 km tile basis; imagery classified on a per-parcel basis and aggregated into 100 km tiles.
- Tiles are mosaicked; some edge tiles may be merged or simplified to produce a single layer of parcels.
- The dataset is designed to be stored and uploaded to appropriate data portals; parcel-level attributes maintain rich metadata.

## Hierarchical nomenclature

- Vector data provides Subclass and Variant detail; mapping table links codes to real-world classes.
- Subclasses and Variant codes are defined (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, etc.), with Alpha and Variant codes used for compact labeling.
- Variant level (Level 3) yields more detailed classifications (e.g., deciduous, mixed, conifers, specific crop types) but accuracy varies by area.

## Vector polygon attributes and OpHistory

- Each parcel (SegID) includes:
  - BHSub: Dominant land cover type at Subclass level (Level 2).
  - BHSubVar: Dominant land cover type at Variant level (Level 3) when present.
  - PerPixList: Top five spectral subclasses within the parcel (not always present at Level 2; present at Level 3).
  - OpHistory: Processing history details for the parcel, including image dates and knowledge-based correction (KBC) steps.
  - TotPixels and CorePixels: Total pixels in the parcel and in the core area used for maximum-likelihood classification.
- OpHistory detail:
  - Encodes a five-field descriptor per parcel: scene number, sensor, acquisition dates, cloud-hole patch indicator, spectral probability data, aggregation flags, and KBC rule counts (Phase 1 and Phase 2).
  - Additional sixth field captures other information (e.g., eroded/merged artefacts, training data usage).
- The dataset includes guidance on interpreting and managing edge overlaps, cuts, and classification history for reproducibility.

## Colour mapping and Broad Habitat descriptions

- Colour recipes provide display colors for the 26 Subclasses to support consistent visualization (exact RGB/Hue/Saturation values listed per subclass).
- Broad Habitat descriptions (28+ categories) define typical vegetation structure and habitat types, including:
  - Broad-leaved/mixed woodland, Coniferous woodland
  - Arable and horticulture, Improved grassland, Neutral grassland, Calcareous grassland, Acid grassland
  - Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog
  - Standing water and canals, Rivers/streams
  - Montane habitats, Inland rock, Built-up areas and gardens
  - Coastal habitats ( Supra-littoral/ Litoral rock and sediment, sea/estuary, etc.)
- Each Broad Habitat has a descriptive definition to aid interpretation and consistency with biodiversity and habitat classifications.

## Edge overlaps, slivers, and artefact handling

- Edge overlap issues arise from mosaicked, multi-date imagery; an erosion/merging process produces a single parcel layer, but edge parcels may straddle tile boundaries.
- Artefacts at edges are rare (typically <0.1% of parcels) and can be addressed by users as needed.
- Practical guidance includes:
  - Visual tidying by dissolving boundaries between adjacent parcels of the same class (without dissolving across the entire map to preserve parcel-level metadata).
  - Clipping data to 100 km tile edges, merging tiles with caution (preserves attribute integrity but can invalidate some parcel-level metadata).
  - Using Union and then selectively dissolving to preserve Level 3 (Variant) information when needed.
  - For Level 3 data, use bhsubvar during dissolving to avoid losing key classification details.
  - When merging tiles, priority may be given to the first input tile; edge parcels may reflect slight classification differences.
- Slivers and parcels smaller than 0.5 ha can be dealt with via visual removal, dissolving with adjacent same-class parcels, or intelligent dissolution based on shared boundaries.

## Customisation, provenance, and production philosophy

- LCM2000 acts as both a map and a data storage/analysis framework; users are encouraged to modify and expand while preserving provenance.
- Unique labeling: each parcel has a SegID for unambiguous communication with data managers and other users; SegID should be retained.
- Production philosophy emphasizes retaining as much information as possible; preserve metadata to document lineage and processing history.
- Fully document changes to support data management, security, and feedback to the data management team.
- Caution to users: avoid mislabeling differences due to data model, scale, resolution, interpretation, class definitions, or target classes as inaccuracies.

## Further information, access, and references

- For data access and methodology details, see the Land Cover Map home page and contact CEH spatialdata@ceh.ac.uk.
- Key literature:
  - Fuller et al. (2002): The UK Land Cover Map 2000 – construction of a parcel-based vector map from satellite images.
  - Smith et al. (2001, 2002): Land Cover Map 2000 – parcel-based map from satellite images; remote sensing conference proceedings.
  - Jackson (2000): JNCC Report No. 307 – guidance on Broad Habitat interpretation and relationships with other habitat classifications.

## Appendix highlights

- Appendix 1: Dealing with edge overlap problems
  - Details reasons for edge artefacts and recommended remedial steps with ArcMap workflows (clip, merge, dissolve) and cautions about data integrity and attribute loss.
  - Discusses priority rules when merging tiles and how to handle edge classifications, including Level 2 vs Level 3 considerations.
- Appendix 2: Good practice
  - Indicates there is guidance on good practice for handling data, metadata, and change management (content not fully shown in the provided text).