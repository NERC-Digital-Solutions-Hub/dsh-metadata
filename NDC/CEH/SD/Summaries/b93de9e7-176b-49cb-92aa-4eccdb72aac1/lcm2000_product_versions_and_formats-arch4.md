# LCM2000 specification

- LCM2000 is a UK-wide parcel-based land cover map, derived from satellite imagery (mainly Landsat), available in vector and raster formats, produced on a 100 km tile basis, and linked to the Joint Nature Conservation Committee (JNCC) Broad Habitats classification.
- It covers Northern Ireland and Great Britain (all-UK) with additional ancillary data; not directly comparable with LCM1990 for change estimation.

## Product versions and formats

- Vector data (parcels with attributes)
  - Level 2: standard 26 Subclasses (most widely used).
  - Level 3: 72 Variant level (more detailed; quality varies regionally; requires special arrangement with CEH staff).
  - Standard vector format is ESRI shapefile (ArcGIS users may need Spatial Analyst for advanced analysis).
- Raster data (derived from vector)
  - 25 m: 26 Subclasses (full detail).
  - 1 km: derived from 25 m with two levels of detail:
    - Subclass level (26 Subclasses)
    - Aggregate level (10 simplified Aggregate classes) with Dominant values and Percentages per pixel
- Quick note: LCM2000 rasters are not directly comparable to LCM1990 due to different construction methods; not suitable for 10-year change estimates.

## Dataset coverage and structure

- Compiled on a 100 km tile basis; parcels added to respective tiles after per-parcel classification.
- Some tiles were merged for construction efficiency (see Figures in the document).
- Edge overlaps between tiles were resolved to create a single layer of land parcels per tile; edge artefacts are rare (generally <0.1% of parcels).

## Hierarchical nomenclature

- Vector data supports Subclass (Level 2) and Variant (Level 3) details; codes provided (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable cereals, etc.).
- Subclass and Variant codes enable detailed classification and cross-referencing with the Broad Habitat framework.

## Vector polygon attributes

- SegID: unique parcel identifier (includes OS 100 km square and segment number).
- BHSub (Level 2) and BHSubVar (Level 3): dominant land cover type as hierarchical codes.
- PerPixList: per-pixel list of top spectral subclasses within the parcel (Level 3 only).
- OpHistory: processing history details, including image dates, KBC rules applied, etc. (see below).
- TotPixels and CorePixels: total pixels in the parcel and pixels used for maximum likelihood classification.
- Notes: Unique SegID should be retained to preserve lineage and communications with data management.

## OpHistory Attribute (processing history)

- OpHistory (PHD) contains five main fields (plus a sixth for other information) describing input data and processing stages:
  - Scene number, Sensor type, Acquisition dates (summer/winter), and whether single-date cloud-hole patches were used.
  - Probability aggregation flag and the number of Phase 1 and Phase 2 KBC (knowledge-based correction) rules applied.
  - A descriptor for other conditions (e.g., eroded, grown, voids filled, training data, etc.).
- A detailed table explains Scene/Sensor mappings and the meaning of each field.

## Colour recipes for LCM2000 mapping

- Table-driven color mappings provide display colors for the 26 Subclasses to assist visualization in GIS and mapping software.
- Each subclass has a defined Hue, Saturation, and Value (or approximate RGB equivalent) to support consistent display.

## LCM2000 Broad Habitat descriptions

- Broad Habitats are organized into major groups (e.g., Broad-leaved/mixed woodland; Coniferous woodland; Arable and horticulture; Improved/Neutral/Calcareous/Acid grasslands; Bracken; Dwarf shrub heath; Fen/marsh/swamp; Bog; Water bodies; Montane habitats; Inland bare ground; Built-up areas; Coastal/Marine habitats).
- Descriptions explain the ecological interpretation, vegetation structure, and notable considerations for each Broad Habitat type.
- The classification supports alignment with biodiversity and habitat planning standards (e.g., Biodiversity Broad Habitat Classification).

## Appendix 1: Dealing with edge overlap problems

- Edge overlaps arise from mosaicking multiple images within 100 km tiles and cloud-hole patching; a single-layer parcel map is produced by erosion and merging, with edge parcels retained in adjacent tiles.
- Artefacts are infrequent and generally less than 0.1% of parcels.
- Visual tidying and pragmatic corrections:
  - Dissolve boundaries between adjacent parcels of the same class (preferably only at the Level 2 subclass) to create a cleaner join.
  - Do not dissolve boundaries across the entire dataset if attribute integrity must be preserved.
  - For Level 3 data, ensure bhsubvar information is retained during dissolves.
- Practical guidance for ArcMap workflows (clip, merge, dissolve) and strategies to preserve essential parcel-level metadata.

## Appendix 2: Good practice

- LCM2000 is designed as an extensible data storage and analysis framework, not just a map.
- Users are encouraged to customize, expand, and maintain parcel-level metadata to preserve lineage and facilitate communication with data managers.
- Unique labeling (Segid) should be retained to support unambiguous data management and traceability.
- Production philosophy emphasizes information richness; when modifying data, preserve original attributes and document changes comprehensively.

## Production philosophy and data governance

- Retain as much information as possible; document lineage and processing history.
- If attributes are changed, create new attributes or copies to preserve provenance.
- Fully document data changes to support data security and feedback to management teams.
- Acknowledge and communicate inherent inaccuracies due to data models, scale, resolution, and classification definitions.

## Practical takeaway for Data Leaders

- LCM2000 provides a comprehensive, lineage-rich UK land cover dataset in both vector and raster formats, tied to the Broad Habitat framework.
- Key governance points: retain Segid and OpHistory; manage edge artefacts with well-documented, section-level dissolves; balance data richness with practical usability; understand format-specific limitations (e.g., Level 3 variability, 1 km vs 25 m rasters, and non-changeable comparison with LCM1990).
- The dataset supports flexible use, cross-institution collaboration, and potential customization to fit organizational data systems, with explicit guidance on metadata, quality, and provenance.