# LCM2000 specification

- LCM2000 is a parcel-based thematic classification of UK satellite imagery, delivering an all-UK dataset in both vector and raster formats.
- Built from Landsat imagery with additional ancillary data; aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats classification.
- Available in multiple product versions and formats, with varying detail levels and resolutions to suit different GIS analyses.

## Product versions overview

- Vector data: polygons representing land parcels with attached attributes.
  - Level 2: 26 LCM2000 Subclasses (standard, widely used).
  - Level 3: up to 72 Variant level detail; higher detail may vary by area and requires CEH specialist involvement.
  - Standard vector format is ESRI shapefile; ArcGIS users may need Spatial Analyst for advanced analyses.
- Raster data (derived from the vector base): two resolutions.
  - 25 m raster: 26 Subclasses (with full 26-class detail).
  - 1 km raster: summarised at Subclass and Aggregate levels; includes Dominant and Percentage values for each 1 km cell.
  - Raster formats are GeoTIFF; Spatial Analyst may be required for some analyses.
- Note: Raster data are not directly comparable with LCM1990 due to different construction methods; not suitable for estimating 1990–2000 change.

## Dataset coverage

- Compiled on a 100 km tile basis; land parcels are classified per parcel and added to their corresponding 100 km tile.
- Some edge/overlay tiles were merged to simplify construction; tiles may be merged or overlapped to ensure continuity.

## Hierarchical nomenclature

- Vector data provide both Subclass and Variant detail.
- Codes map to Broad Habitat concepts (e.g., Broad-leaved/mixed woodland; Coniferous woodland; Arable crops; etc.).
- Subclass and Variant codes enable detailed, hierarchical labeling; Variant level depends on dominant land cover at imaging time and may not always be fully available everywhere.

## Vector polygon attributes

- Each parcel (SegID) carries a set of attributes:
  - BHSub: dominant land-cover subtype code (Level 2/3).
  - BHSubVar: dominant subtype and Variant code (Level 3).
  - PerPixList: per-pixel top five spectral subclasses (Level 3).
  - OpHistory: processing history string (image dates and KBC rules applied) (Level 2 and Level 3).
  - TotPixels: total pixels in the parcel.
  - CorePixels: pixels used for maximum likelihood classification.
- SegID is a unique parcel identifier; recommended to retain for traceability.

## OpHistory Attribute

- Contains a five-field processing history descriptor per parcel, plus a sixth field for other information.
- Fields capture: scene number, sensor type, imaging dates, single-date cloud-hole patches, spectral probabilities, aggregation flags, phase 1 and phase 2 KBC rules, and various special markers (e.g., edge eroded, data from LCMGB 1990, voids filled).

## Colour recipes for LCM2000 mapping

- A predefined color scheme for the 26 Subclasses to support map design and interpretation.
- Each subclass/subclass variant has specific Hue, Saturation, Value (HSV) and equivalent RGB values to aid consistent visualisation.

## LCM2000 Broad Habitat descriptions

- Broad Habitat categories and definitions cover woodland (broad-leaved, coniferous), arable and horticulture, various grassland types, heath and dwarf shrub, fen/marsh/swamp, bog, standing water, rivers/streams, montane habitats, inland bare ground, built-up areas, coastal/intertidal habitats, and marine-related classes.
- Each description provides practical mapping guidance and distinctions (e.g., how management or spectral characteristics affect class assignment).

## Further Information

- Contact and data access: CEH Land Cover Map data page, spatialdata@ceh.ac.uk, phone numbers listed.
- Methodology references for construction and broad habitat classification are provided (full papers and conference proceedings).

## Appendix 1: Dealing with edge overlap problems

- Edge overlaps occur because 100 km tiles use multiple overlapping source images and cloud-hole filling.
- Overlaps were removed via erosion and merging to create a single parcel layer per tile; some parcels straddle tile edges and may be duplicated across tiles.
- Artefacts are rare (generally <0.1% of parcels) and users can tidy visually or programmatically:
  - Clip to tile edges or merge tiles with caution; be aware that some parcel-level attributes may become invalid after clipping or merging.
  - Use dissolve to remove boundaries between like classes at Level 2; for Level 3, preserve bhsubvar during dissolves to retain important detail.
  - Use selective dissolution or the ArcMap select-feature tool to focus on edge areas and preserve attribute integrity.
- Slivers and very small parcels can be addressed by visual removal, dissolving with adjacent parcels of the same class, or intelligent dissolution based on the longest shared boundary, with caution to preserve important metadata.

## Appendix 2: Good practice

- (Not detailed in the provided text; referenced in contents. Intended to describe recommended practices for maintaining lineage, metadata, and data integrity when modifying LCM2000.)

## Production philosophy and data management

- Emphasis on retaining as much information as possible; parcel-level metadata should be preserved to maintain data lineage.
- Encourages customization and expansion of the dataset by users, while retaining a stable Segid for communication with the data management team.
- Clear guidance on documenting changes and acknowledging inevitable inaccuracies due to data model, scale, resolution, and interpretation differences.