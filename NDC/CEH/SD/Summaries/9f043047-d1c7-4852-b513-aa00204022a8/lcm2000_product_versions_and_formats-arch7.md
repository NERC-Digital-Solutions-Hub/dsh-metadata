# LCM2000 specification

- A parcel-based thematic land cover map for the United Kingdom, derived from satellite imagery (primarily Landsat) with all-UK coverage including Northern Ireland.
- Classified using a hierarchical nomenclature aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats; aims to support broad habitat mapping and extend detail for wider user needs.
- Available in vector and raster formats with multiple product versions offering different levels of detail and spatial resolutions.

## Product formats and versions

- Vector data format (polygons, land parcels) with attached attribute lists.
  - Level 2: standard detail with 26 LCM2000 Subclasses (most widely used).
  - Level 3: detail down to 72 Variant level; higher complexity and support needs; available by special arrangement.
  - Standard vector format is ESRI shapefile; ArcGIS users may require Spatial Analyst for analysis.
- Raster data format (derived from the vector dataset) at two resolutions:
  - 25 m grid: 26 Subclasses.
  - 1 km grid: derived from 25 m; two levels of detail:
    - Subclass level (26 Subclasses).
    - Aggregate level (10 simpler aggregates) with Dominant values and Percentage values.
- Note: Raster data is not directly comparable with LCM1990 due to different construction methods.

## Dataset coverage and structure

- Compiled on a 100 km tile basis; parcels classified per tile and added to the corresponding 100 km tile.
- Edge overlaps removed through erosion/merging; parcels straddling tile edges may be retained in both adjoining tiles.
- 0.5 ha is the minimum mappable unit; parcels smaller than this are dissolved into surrounding parcels based on proximity or spectral/thematic rules, with occasional remnants possible.

## Hierarchical nomenclature

- Vector data offers Subclass detail and optional Variant detail (Level 3).
- Subclass and Variant codes map to 26 Subclasses and numerous Level 3 Variants (illustrative examples provided, e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable crops, etc.).
- Class variants depend on dominant land cover at imaging time; some distinctions (e.g., post-harvest) may not be captured.

## Vector polygon attributes

- SegID: Unique parcel identifier (e.g., TQ005232).
- BHSub: Dominant land cover type (Level 2) as WidespreadBH.LCMSubclass.
- BHSubVar: Dominant land cover type (Level 3) as WidespreadBH.LCMSubclass.Variant.
- PerPixList: Per-pixel list by percentage area of top spectral subclasses (Level 3 only).
- OpHistory: Processing history of each parcel (image dates, KBC rules, etc.) (Level 2 and Level 3).
- TotPixels: Total pixels in the segment.
- CorePixels: Pixels in the core area used for maximum likelihood classification.

## OpHistory Attribute (processing history)

- Five fields describe input data and classification stages (plus a sixth field for other information).
- Example structure includes scene number, sensor, acquisition dates, and flags indicating cloud/patch status.
- Layered details (Table 4) map scenes/sensors/dates, e.g., TM, IRS sensors and various summer/winter dates.

## Colour mapping for display

- 26 Subclasses each have recommended display colors (Hue, Saturation, Value and approximate RGB equivalents).
- Colour recipes facilitate consistent map visualization across software; primarily for display, not analysis accuracy.

## Broad Habitat descriptions

- Broad Habitats are described as:
  - 1 Broad-leaved/mixed woodland
  - 2 Coniferous woodland
  - 3 Boundaries and linear features
  - 4 Arable and horticulture
  - 5 Improved grassland
  - 6 Neutral grassland
  - 7 Calcareous grassland
  - 8 Acid grassland
  - 9 Bracken
  - 10 Dwarf shrub heath
  - 11 Fen, marsh and swamp
  - 12 Bog
  - 13 Standing open water
  - 14 Rivers, streams
  - 15 Montane habitats
  - 16 Inland rock
  - 17 Built-up areas and gardens
  - 18 Supra-littoral rock
  - 19 Supra-littoral sediment
  - 20 Littoral rock
  - 21 Littoral sediment
  - 22 Inshore sublittoral sediment
  - 23-27 Not distinguished in LCM2000 (varied coastal/offshore categories)
- Descriptions emphasize vegetation structure, management, and distinguishing factors at subclass level where possible.

## Further information and methodology

- Data and methodology resources:
  - Land Cover Map home page: www.ceh.ac.uk/data/lcm
  - Contact: spatialdata@ceh.ac.uk; phone 01491 692315
  - Key methodological references for LCM2000 construction and Broad Habitat guidance (Fuller et al. 2002; Smith et al. 2001; Jackson 2000).
- Production philosophy:
  - Retain as much information as possible; parcel-level metadata should document lineage and processing history.
  - Encourage users to customize and expand the database while preserving Segid and primary attributes for traceability.
- Customisation and data integrity:
  - LCM2000 is intended as an extensible data framework, not just a map; maintain parcel-level metadata when altering data.
  - Document changes thoroughly to support data management and user feedback.
- Accuracy and interpretation:
  - Recognize inherent inaccuracies due to data models, scale, resolution, and interpretation.
  - Distinctions may not reflect all user needs; avoid misattributing changes to data quality without context.

## Appendix topics (overview)

- Appendix 1: Dealing with edge overlap problems
  - Edge overlaps arise from multiple source images; methods include erosion/merging, clipping, and dissolving boundaries between like classes, with caution about preserving parcel-level attributes.
  - Edge priority rules can affect attribute data; guidance for handling 100 km tile merges and edge artifacts is provided, including practical steps for ArcMap.
  - Slivers and small parcels can be removed or dissolved using context-based approaches (longest shared boundary, visual tidying).
- Appendix 2: Good practice
  - Indicates there is additional guidance on good practice (content not reproduced here).

## Summary for GIS practice

- LCM2000 provides a comprehensive, multi-format UK land cover dataset suitable for map-based GIS products, with robust vector and raster options and detailed attribute metadata.
- Users should plan for data management and quality control that preserves parcel-level lineage while allowing sensible edge artefact handling in tile mosaics.
- The dataset supports hierarchical classification (Subclasses and Variants) aligned with Broad Habitat concepts, enabling both broad and detailed habitat analysis.
- Practical considerations include minimum mapping unit, edge artefact management, and the need for appropriate software extensions for analysis (e.g., Spatial Analyst for ArcGIS).
- Ongoing documentation and provenance are emphasized to support data reuse, reproducibility, and collaboration.