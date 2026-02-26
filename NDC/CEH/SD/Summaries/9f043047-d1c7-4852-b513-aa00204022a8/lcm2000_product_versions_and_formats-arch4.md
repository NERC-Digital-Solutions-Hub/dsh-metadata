# LCM2000 specification

- LCM2000 is a parcel-based thematic land cover map for the entire United Kingdom, derived mainly from Landsat imagery and incorporating additional ancillary datasets. It covers Great Britain and Northern Ireland all-UK for the first time, in both vector and raster formats, and is aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats classification. It is not directly comparable with the 1990 dataset for change estimation.

## Product versions overview
- Vector data (parcels) at Level 2: 26 LCM2000 Subclasses.
- Vector data at Level 3: down to 72 Variant level details; available by special arrangement with CEH.
- Standard vector format: ESRI shapefile; ArcGIS users may need Spatial Analyst for advanced analysis.
- Raster data at 25 m resolution: 26 Subclasses.
- Raster data at 1 km resolution: derived from the 25 m raster with two detail options:
  - Subclass level: 26 Subclasses.
  - Aggregate level: 10 simplified aggregates; Dominant values and Percentage values per 1 km pixel.
- Raster formats: GeoTiff; ArcGIS Spatial Analyst may be required for analysis.
- Note: Raster data are not directly comparable with LCM1990 due to differing construction methods; not suitable for 10-year change estimation.

## Dataset coverage and structure
- Data compiled on a 100 km tile basis; parcels classified per tile and then aggregated into tiles.
- Tiles may be merged to simplify construction; some parcels near tile edges may be retained in adjacent tiles.

## Hierarchical nomenclature
- Vector data provide Subclass (and Level 3 Variant) details; codes are standardized (e.g., broad-leaved/mixed woodland, coniferous woodland, arable crops, etc.).
- Subclass and Variant codes (Level 2 and Level 3) are provided and may display differently in some GIS packages.

## Vector polygon attributes
- Each parcel carries a set of attributes:
  - SegID: Unique segment identifier (combines OS 100 km square and segment number).
  - BHSub: Dominant land cover type at Subclass level.
  - BHSubVar: Dominant land cover type at Variant level (Level 3 only).
  - PerPixList: Top-five spectral subclasses per pixel within the segment.
  - OpHistory: Processing history details; see below.
  - TotPixels: Total pixels within the segment.
  - CorePixels: Pixels within the core area used for maximum likelihood classification.

## OpHistory Attribute (processing history)
- The OpHistory (PHD) provides five fields describing input data and classification stages, plus a sixth field for other information:
  - Scene number and sensor/date details (image data used).
  - Cloud hole patch indicators (S, W, or none) and whether single-date imagery was used.
  - Spectral probability and probability aggregation flags.
  - Phase 1 and Phase 2 KBC (knowledge-based correction) rules applied.
  - Additional status flags for edge handling, training data, and data provenance.

## Colour recipes for LCM2000 mapping
- A predefined colour table assigns display colours to the 26 Subclasses (and related categories) to aid visualization (examples include Broad-leaved/mixed woodland, Coniferous woodland, Arable cereals, Arable horticulture, Improved grassland, Neutral grassland, Calcareous/acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Inland water, Montane habitats, Inland bare ground, Suburban/urban areas, and coastal/seaside habitats).

## Broad Habitat descriptions
- Provides definitions for the 16 Broad Habitat groups, including:
  - Broad-leaved/mixed woodland and coniferous woodland
  - Boundaries/linear features
  - Arable and horticulture, including set-aside
  - Various grasslands (improved, neutral, calcareous, acid)
  - Bracken and dwarf shrub heath
  - Fen/marsh/swamp and bog
  - Standing water and inland water
  - Montane habitats
  - Inland rock and built-up areas
  - Coastal/habitat categories (supra-littoral and littoral zones)

## Appendix 1: Dealing with edge overlap problems
- Edge overlaps occur because 100 km tiles were constructed from multiple overlapping images; overlaps removed by erosion/merging to a single parcel layer.
- Artefacts near tile edges are rare (usually <0.1%) and may include:
  - Differing classifications across overlapping imagery
  - Slivers or parcels smaller than minimum mappable units
- Guidance for handling visually:
  - Visual tidying by dissolving boundaries between adjacent parcels of the same class (recommended only at the edge, not across the entire dataset to preserve parcel-level metadata).
  - In ArcMap, dissolve operations can degrade source attributes; for Level 3, preserve bhSubVar during dissolve to avoid loss of Level 3 information.
- Approaches for edge artifact resolution in practice:
  - Clip to tile edges, or merge tiles with caution (may invalidate parcel-level attributes like SegID lineage and per-pixel data).
  - Use select-then-dissolve to target edge regions for speed and to minimize attribute loss.
  - Priority of input tile during merge can affect edge results; typically first input tile takes precedence, but differences may occur if classifications differ.

## Appendix 2: Good practice
- (Not fully detailed in the provided text; core principles are preservation of metadata, lineage, and class boundaries; use of structured documentation for changes.)

## Customisation and production philosophy
- LCM2000 is designed as a data storage and analysis framework, not just a map; users are encouraged to modify and expand their version.
- Maintain unique parcel labels (SegID) and preserve metadata to enable traceability and communication with data management.
- Production philosophy emphasizes retaining as much information as possible; preserve parcel-level metadata and lineage when altering data.

## Documenting changes and accuracy
- Fully document all changes to maintain data management efficiency, traceability, and feedback loops with the data management team.
- Recognize that LCM2000 embodies inevitable inaccuracies due to data model, scale, resolution, interpretation, and target-class definitions; differences should be understood in context rather than automatically deemed errors.

## Further Information
- Land Cover Map homepage: www.ceh.ac.uk/data/lcm
- Contact: spatialdata@ceh.ac.uk; +44 (0)1491 692315
- Key references for methodology and broad habitat classification:
  - Fuller et al. (2002) The UK Land Cover Map 2000: construction of a parcel-based vector map from satellite images
  - Smith et al. (2001) Land Cover Map 2000: a parcel-based map from satellite images
  - Jackson (2000) JNCC Report No. 307: Guidance on interpretation of the Biodiversity Broad Habitat Classification