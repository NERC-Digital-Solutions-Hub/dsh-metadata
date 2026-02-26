# LCM2000 specification

- LCM2000 is a UK-wide parcel-based land cover map derived mainly from Landsat imagery, updating LCMGB 1990 and including Northern Ireland for the first time. It uses a hierarchical Broad Habitat classification (JNCC) and is produced in both vector and raster formats with multiple detail levels and resolutions. It is not directly comparable to LCM1990 for change analysis.

## Product formats and versions

- Vector data (parcels with attributes)
  - Level 2: standard detail with 26 Subclasses (most widely used)
  - Level 3: up to 72 Variant level detail; available by special arrangement (requires more user support)
- Raster data (GeoTiff)
  - 25 m resolution: 26 Subclasses
  - 1 km resolution: aggregates from 25 m with Subclass level, Dominant values, and Percentage values; also 10 Aggregate classes with Dominant and Percentage
- Minimum mappable parcel size: >0.5 ha (smaller parcels are dissolved into surrounding land)
- ArcGIS compatibility: Vector uses ESRI shapefile; Spatial Analyst extension may be required for analysis
- Raster datasets are derived from the vector database

## Dataset coverage and tiling

- Coverage is organised on a 100 km tile basis; parcels are classified per tile and then assembled into a UK-wide dataset
- Some edge parcels straddle tile boundaries; edge overlaps were removed through erosion/merging to produce a single layer per tile, with parcels crossing edges retained in adjacent tiles
- Note: tiles are vector-based; merging can affect parcel-level attributes and performance

## Hierarchical nomenclature (Subclass and Variant)

- Vector data provides Subclass (Level 2) and Variant (Level 3) detail
- Subclass and Variant codes are used to describe land cover types (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable cereals, etc.)
- A detailed code table maps Subclass codes to Level 3 Variant codes; the dominant land cover at the time of imaging determines Variant availability
- Some areas may not have Level 3 variants due to imaging conditions

## Colour recipes and Broad Habitat descriptions

- 26 Subclasses have predefined display colours (Table 5), enabling consistent map rendering in GIS
- Broad Habitat descriptions (Table 6) provide definitions for each habitat category (e.g., Broad-leaved woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grassland, Bracken, Heath, Fen/marsh/swamp, Water, Montane habitats, Inland bare ground, Built-up areas, Coastal habitats)

## Vector polygon attributes and OpHistory

- Each land parcel (SegID) carries:
  - BHSub: dominant land cover (Level 2 code)
  - BHSubVar: Level 3 variant code (if present)
  - PerPixList: top five spectral subclasses by pixel percentage (Level 3)
  - OpHistory: processing history of the segment (image dates, KBC rules applied)
  - TotPixels: total pixels in segment
  - CorePixels: pixels in the core area used for maximum likelihood classification
- OpHistory field encodes scene number, sensor, image dates, cloud-hole patches, spectral probability, aggregation rules, and KBC rule counts (Phase 1 and Phase 2)
  - Scene data includes sensor type (TM, IRS) and acquisition dates
  - Single date cloud-hole patch indicators (S, W, X)
  - A multi-field descriptor provides a compact processing history per parcel

## Edge overlaps, artefacts, and handling (Appendix 1)

- Edge overlaps arise from mosaicking multiple images; overlaps were removed to produce a single parcel layer per 100 km tile
- Artefacts at tile edges can occur due to different imagery or merging decisions; small parcels and slivers (<0.5 ha) may remain
- Visual tidy-up options:
  - Dissolve boundaries between adjacent parcels with the same class (via legend tools)
  - Clip data to 100 km edges or merge tiles, noting that parcel-level attributes may be invalidated
  - Use selective dissolving (e.g., target edge areas) to preserve important source attributes
- When merging tiles, the first input tile often takes precedence for edge parcels; there may be differences if edge classifications differ
- Slivers can be removed by dissolving with adjacent similar-class parcels or by intelligent dissolution using the longest shared boundary
- Users should consider artefacts in context of the whole dataset and preserve Segid for traceability

## Customisation and production philosophy

- LCM2000 is designed as an information-rich data storage and analysis framework, not just a map
- Users are encouraged to modify and expand their version while preserving provenance
- Unique Segid labels should be retained to maintain unambiguous communication with the data management team
- When altering attributes, maintain copies or create new attributes to record changes
- Documenting changes is essential for data management and traceability
- Be mindful of inaccuracies: differences due to model, scale, resolution, or interpretation are expected; use the dataset accordingly

## Further information and contacts

- For access and sales: Land Cover Map information via CEH contact (spatialdata@ceh.ac.uk)
- Refer to published methodology papers for construction details and Broad Habitat classification guidance