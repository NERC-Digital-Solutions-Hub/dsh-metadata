# LCM2000 specification

- LCM2000 is a parcel-based thematic classification of satellite imagery covering the entire United Kingdom, producing an all-UK land cover dataset derived mainly from Landsat imagery plus ancillary data.
- It uses a hierarchical nomenclature aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats to cover the full range of UK habitats, with additional detail where possible.
- Available in both vector and raster formats, with multiple product versions offering different levels of detail and resolutions.
- Designed to support environmental monitoring and policy performance assessment by providing standardized outputs and traceable provenance.

## Data structure and classification

- Minimum mappable unit is greater than 0.5 hectares; parcels smaller than 0.5 ha are dissolved into surrounding land where possible.
- Classification hierarchy focuses on Broad Habitats (Target/Subclasses) with optional Level 3 Variants for more detail; Levels are designed to balance broad mapping utility with finer distinctions where feasible.
- Vector data: polygons representing land parcels with a set of attached attributes.
- Raster data: generated from the vector database at two resolutions (25 m and 1 km) with two levels of detail for the 1 km grid (Subclass and Aggregate class levels), plus dominant and percentage-valued outputs.
- Note: Raster data are not directly comparable with the 1990 LCMGB dataset due to different construction methods; not suitable for estimating 10-year change.

## Product versions and formats

- Vector data (detail options):
  - Level 2: Standard level with 26 Subclasses (most widely used).
  - Level 3: Detailed to 72 Variants; requires special arrangement and additional user support.
  - Standard vector format is ESRI Shapefile; ArcGIS users may need Spatial Analyst for advanced analysis.
- Raster data (2 resolutions):
  - 25 m: 26 Subclasses.
  - 1 km: Derived from the 25 m raster; includes Subclass-level, Dominant-values, and Percentage-values; aggregates to 10 Aggregate classes for some outputs.
- The vector and raster outputs provide both broad consistency for monitoring and mechanisms to drill down into details where needed.

## Dataset coverage and tile structure

- LCM2000 data are compiled on a 100 km tile basis; imagery is classified per parcel and then attributed to the 100 km tiles.
- Acknowledges edge overlaps between tiles and notes artefacts may occur at tile boundaries; procedures exist to manage overlaps during production.

## Vector polygon attributes and provenance

- Each parcel carries:
  - SegID: unique parcel identifier.
  - BHSub: hierarchical code for the dominant land cover (Level 2).
  - BHSubVar: Level 3 variant code (where present).
  - PerPixList: per-pixel breakdown of top spectral subclasses (Level 3 only).
  - OpHistory: processing and classification history, including image dates and Knowledge-Based Corrections (KBC) applied (Level 2 and Level 3).
  - TotPixels and CorePixels: pixel counts for the parcel and its core area used in max-likelihood classification.
- OpHistory (PHD) details input data and classification steps across multiple fields (scene number, sensor, acquisition dates, cloud-hole patches, KBC counts, etc.), enabling traceability of the production chain.

## Colour mapping and habitat descriptions

- Color recipes (for display) are provided for all 26 Subclasses to aid interpretation and visual consistency.
- Broad Habitat descriptions (Table 6) cover categories such as Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Various grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Water bodies, Montane habitats, Inland bare ground, Built-up areas, and Coastal/shoreline habitats.
- Descriptions emphasize practical criteria for class assignment (e.g., canopy cover, land management, spectral signals) and note where distinctions may be challenging or context-dependent.

## Edge overlaps and artefacts (Appendix 1)

- Edge overlap problems arise from mosaicked imagery and cloud-hole patches; a single-layer parcel map is produced by erosion and merging operations.
- Artefacts can include differing classifications at tile edges, slivers, or parcels split across edges; typically less than 0.1% of parcels are affected.
- Visual tidying options:
  - Dissolve boundaries between adjacent parcels of the same class (preferable when not losing parcel-level metadata).
  - Clip or merge tiles with caution, understanding that edge processes can invalidate some attribute data.
  - For Level 3 data, preserve bhsubvar during dissolves to retain important detail.

## Dealing with edge artefacts (practical guidance)

- Clip to 100 km square edges or use Merge themes and then dissolve like classes, aware of impact on parcel metadata.
- Use Union when merging tiles; note that edge parcels may retain attributes from the first input tile, and some data may become inconsistent.
- In cases with multiple edge artefacts, selective dissolution and data selection can speed processing.
- For Level 3 data, ensure bhsubvar is retained to avoid loss of critical classification detail.

## Slivers and small parcels

- Small parcels (< minimum mappable unit) and slivers are addressed through:
  - Visual removal of boundaries between same-class parcels.
  - Dissolving parcels with adjacent similar-class parcels.
  - Intelligent dissolving based on the longest shared boundary with surrounding parcels.
- Recommend cautious dissolution to avoid erasing important attribute information.

## Customisation and production philosophy

- LCM2000 is an information-rich data storage and analysis framework intended for repurposing and expansion by users.
- Users are encouraged to retain parcel-level metadata (e.g., SegID) to preserve lineage and facilitate communication with data managers.
- When altering data, maintain copies of original attributes or document changes in new attributes to preserve provenance.

## Documentation, accuracy, and usage notes

- Fully document changes to support data management, security, and feedback to the data management team.
- Use precise language: differences may arise from data model, scale, resolution, interpretation, or class definitions; LCM2000 acknowledges inherent inaccuracies and emphasizes appropriate framing of accuracy.
- The dataset is designed to support monitoring and policy evaluation, with standardized formats and clear provenance to enable scrutiny over time.

## Further information and references

- Land Cover Map home page: www.ceh.ac.uk/data/lcm
- Contact: spatialdata@ceh.ac.uk; 01491 692315
- Key methodological references:
  - Fuller et al. (2002) The UK Land Cover Map 2000: construction of a parcel-based vector map from satellite images.
  - Smith et al. (2001) Land Cover Map 2000: a parcel-based map from satellite images.
  - Jackson (2000) JNCC Report No. 307: Guidance on interpretation of the Biodiversity Broad Habitat Classification.
- Appendices: Appendix 1 – Dealing with edge overlap problems; Appendix 2 – Good practice.

## Appendices

- Appendix 1: Dealing with edge overlap problems (edge artefacts, tile merging, and guidance on tidying).
- Appendix 2: Good practice (high-level guidance for responsible data handling and customization).