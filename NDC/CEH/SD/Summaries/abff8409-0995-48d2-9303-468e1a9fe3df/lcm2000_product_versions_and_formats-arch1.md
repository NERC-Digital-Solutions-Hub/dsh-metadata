# LCM2000 specification

- LCM2000 is a parcel-based, UK-wide land cover map that updates and upgrades the Land Cover Map of Great Britain (LCMGB) 1990, extending coverage to Northern Ireland for an all-UK dataset.
- Classifies land cover using a hierarchical nomenclature aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats, with detailed subclasses and variants where available.
- Produced in both vector (parcels/polygons) and raster formats, with multiple detail levels and resolutions to suit different user needs.

## Product versions and data formats

- Vector data (polygons, parcel-based) with attributes:
  - Level 2: 26 Subclasses (most widely used)
  - Level 3: 72 Variant level (more detail; available by special arrangement)
  - Standard vector format: ESRI shapefile (ArcGIS compatibility; Spatial Analyst recommended for advanced analysis)
- Raster data (derived from vector; 2 resolutions at 25m and 1km):
  - 25m: 26 Subclasses
  - 1km: 
    - Subclass level (26 Subclasses)
    - Dominant values and Percentage values for 1km cells
    - Aggregate class level (10 simplified aggregates)
- Important caveat: Raster data are not directly comparable with LCM1990 due to different construction methods and should not be used to estimate change over the 10-year period.

## Dataset coverage and nomenclature

- Coverage is organized on 100km UK tiles; parcels are classified per parcel and assigned to 100km tiles, forming an all-UK mosaic.
- Hierarchical nomenclature:
  - Subclass codes with corresponding Variant codes (Level 3) and alpha codes (e.g., 1.1 Broad-leaved / mixed woodland; 2.1 Coniferous woodland; 4.1 Arable cereals; etc.)
  - Variant level provides more specific classifications; database notes indicate that certain variants may vary in accuracy by area.
- Notes on usability:
  - The “Subdivision” (Variant) detail depends on the dominance of the land cover in the image; distinctions may be limited when crops are harvested or data are dated.

## Vector polygon attributes

- Each land parcel (SegID) includes:
  - BHSub: Dominant land cover type (Level 2/Subclass)
  - BHSubVar: Dominant land cover type (Level 3/Variant; present for Level 3)
  - PerPixList: Top-five spectral subclass percentages per pixel (Level 3 only)
  - OpHistory: Processing history (image dates, KBC rules applied)
  - TotPixels: Total pixels in the parcel
  - CorePixels: Pixels in the core area used for maximum likelihood classification
- SegID is a unique parcel identifier and is recommended to be retained for traceability.

## OpHistory attribute (production and classification trace)

- Each parcel carries a Process History Descriptor (PHD) with fields describing:
  - Scene number and sensor details (e.g., TM, IRS) and acquisition dates
  - Cloud hole patch status and related metadata
  - Spectral probability measures and aggregation flags
  - Phase 1 and Phase 2 knowledge-based corrections (KBC) rules applied
  - A sixth field for other information
- Tables in the document provide explicit mappings of sensor/date combinations and interpretation of these fields.

## Colour mapping and broad habitat descriptions

- Colour recipes are provided for displaying the 26 Subclasses (Level 2) to aid visual interpretation.
- Broad Habitat descriptions (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable, Improved grassland, Neutral grassland, Calcareous/Acid grassland, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Standing water, Montane habitats, Inland rock, Built-up areas, and coastal littoral habitats) define target habitat types and typical characteristics, with distinctions often made at the subclass level where possible.

## Edge overlaps, slivers, and artefacts (Appendix 1)

- Edge overlap issues arise from mosaicking multiple images; 100km tiles may contain overlapping parcels after patching cloud holes.
- Artefacts are rare (<0.1% of parcels) but can occur at tile edges due to different source imagery and erosion/merging processes.
- Guidance includes:
  - Visual tidying by dissolving boundaries between adjacent parcels of the same class
  - Clipping to 100km edges or merging tiles with attention to attribute loss
  - Using dissolve operations carefully to preserve Level 3 information
  - Handling slivers by visual removal, dissolving with neighbors of the same class, or intelligently dissolving based on boundary length
- Priority of first input tile can affect edge parcels when merging tiles, though differences may be minor.

## Good practice and production philosophy (Appendix 2 and related notes)

- LCM2000 is designed as a data storage and analysis framework, encouraging users to customize and extend with parcel-level metadata to record lineage and change.
- Preserve the Segid and original attribute information when making modifications; document changes thoroughly to maintain data provenance and usability.

## Usage notes, accuracy, and further information

- LCM2000 acknowledges inevitable inaccuracies due to data model, scale, resolution, interpretation, and target definitions; users should interpret differences with this in mind.
- The dataset is not a direct one-to-one change detector with LCM1990 and should be used with caution for change assessment.
- For further information, references are provided (e.g., Fuller et al. 2002; Smith et al. 2001) and contact details are given for data inquiries and methodology descriptions.
- The Broad Habitat classification guidance is supported by JNCC documentation (Jackson 2000).