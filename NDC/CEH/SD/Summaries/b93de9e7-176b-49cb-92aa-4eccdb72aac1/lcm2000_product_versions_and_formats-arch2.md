# LCM2000 specification

- LCM2000 is a parcel-based thematic land cover map of the United Kingdom, derived mainly from Landsat satellite imagery, covering all of the UK including Northern Ireland.
- It is produced in both vector (land parcels with attributes) and raster formats, with multiple product versions offering different levels of detail and spatial resolutions.
- The classification uses a hierarchical nomenclature aligned to the Joint Nature Conservation Committee (JNCC) Broad Habitats, creating a broad, consistent basis for environmental health monitoring and policy performance over time.

## What the data map and how it is structured

- Minimum mappable parcel area is >0.5 hectares; parcels smaller than 0.5 ha are dissolved into surrounding classes during production.
- The classification hierarchy focuses on Broad Habitats (Target and Subclasses) and optionally Variant level; Variant detail (Level 3) is available but may vary in accuracy and consistency.
- Raster data come in two resolutions (25 m and 1 km) and provide Subclass- and Aggregate-level outputs (dominant values and percentages at 1 km; 25 m at Subclass level).
- Raster data are not directly comparable with the earlier LCM1990 dataset due to different construction methods.

## Product versions overview

- Vector data formats:
  - Level 2: 26 Subclasses (standard, most widely used).
  - Level 3: 72 Variant level details (requires special arrangement and more user support).
  - Standard vector format is ESRI shapefile; may require Spatial Analyst for advanced ArcGIS use.
- Raster formats (25 m and 1 km):
  - 25 m: 26 Subclasses.
  - 1 km: Subclass and Aggregate outputs, including Dominant and Percentage values.
- Note: Raster and vector products are provided in multiple combinations of detail, and the 1 km raster outputs are derived from the 25 m data.

## Dataset coverage and tile structure

- Data compiled on a 100 km tile basis; imagery classified per parcel and then assigned to the appropriate 100 km tile.
- Tiles can be merged for visualization or analysis, but edge handling must be treated carefully to preserve attribute integrity.

## Hierarchical nomenclature

- Vector data provide Subclass and, where available, Variant detail; codes map to an alpha code and a numeric Variant code.
- The ability to distinguish Variant level depends on the dominant land cover at the imaging time; some distinctions (e.g., crops post-harvest) are not always attempted.
- A wide range of land-cover types is represented through detailed Subclasses and Variants, as defined in accompanying tables.

## Vector polygon attributes

- Each land parcel (SegID) carries:
  - BHSub: Dominant land cover at Subclass level (level of detail 2).
  - BHSubVar: Dominant land cover at Variant level (if present).
  - PerPixList: Top-five spectral subclasses by pixel percentage within the parcel (level 3 only).
  - OpHistory: Processing history (image date(s), KBC rules, etc.).
  - TotPixels and CorePixels: Total pixels in the parcel and in its core classification area.
- OpHistory (processing history descriptor) includes fields for scene number, sensor, acquisition dates, and KBC (knowledge-based correction) details, plus flags indicating data peculiarities (e.g., edge eroding, training data, data from LCMGB 1990, cloud patches).

## Colour recipes and broad habitat descriptions

- 26 Subclasses each have specified display colors (RGB or HSV equivalents) to support consistent visual interpretation.
- Broad Habitat descriptions provide operational definitions for major habitat groups (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Water, Montane, Inland rock, Built-up areas, Coastal habitats, etc.).
- These descriptions underpin the interpretation of the 26 Subclasses and support cross-walker consistency with biodiversity and habitat classifications.

## Appendix highlights: edge overlaps and good practice

- Edge overlap problems arise because of mosaicked imagery and cloud-hole patches; tiles may retain multiple overlapping parcel layers.
- Artefacts are generally rare (<0.1% of parcels) but can occur at tile edges; guidance is provided to visually tidy or statistically dissolve boundaries between like classes, without degrading parcel-level attributes.
- Approaches include clipping to tile edges, merging tiles, or dissolving boundaries between identical classes at Level 2 (with careful handling of Level 3 data).
- When merging tiles, the first input tile often takes precedence at edges; some edge parcels may be classified differently between tiles, requiring user awareness.

## Customisation, production philosophy and data lineage

- LCM2000 is designed as a data storage and analysis framework, not just a map; users are encouraged to modify and expand their local database.
- Each parcel has a unique SegID to support clear communication with the data management team and between users.
- A production philosophy of retaining as much information as possible encourages maintaining parcel-level metadata to document lineage and processing history.
- Fully documenting changes is essential for data management and quality assurance.
- Users should carefully consider accuracy and compatibility; differences due to data model, scale, resolution, or interpretation are not necessarily errors.

## Further information and references

- Access and inquiries: Land Cover Map data page, CEH, spatialdata@ceh.ac.uk.
- Key references include Fuller et al. (2002) on the construction of parcel-based maps from satellite images and Jackson (2000) on broad habitat classification definitions.
- The broad habitat framework aligns with biodiversity classifications for UK landscapes.

## Summary for environmental health monitoring

- LCM2000 provides a comprehensive, UK-wide, parcel-based land cover dataset suitable for monitoring environmental health and policy performance over time.
- It offers standardized, hierarchical classification linked to biodiversity habitat frameworks, with both vector and raster formats to support a range of analyses.
- Provenance, processing history, and parcel-level attributes enable reproducibility and data integration with other environmental datasets.
- Users should be mindful of edge artefacts, slivers, and non-comparability with older datasets, and should document changes to maintain data integrity over time.