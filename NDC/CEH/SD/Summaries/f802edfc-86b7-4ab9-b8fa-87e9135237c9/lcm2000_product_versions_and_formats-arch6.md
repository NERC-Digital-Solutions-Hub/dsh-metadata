# LCM2000 specification

- Overview
  - LCM2000 is a parcel-based thematic classification of satellite imagery covering the entire United Kingdom, updating the Land Cover Map of GB (LCMGB) 1990 and extending to Northern Ireland for an all-UK dataset.
  - Classified with a hierarchical nomenclature aligned to the JNCC Broad Habitats, aiming to support a wide range of users and applications.
  - Available in vector and raster formats, with multiple versions offering varying detail and resolutions; not directly comparable with LCM1990 due to differing methods.

- Product versions and formats
  - Vector data (polygons): Standard Level 2 (26 Subclasses) and Level 3 (72 Variants); Level 3 available by special arrangement.
  - Vector format: ESRI Shapefile; optional Spatial Analyst extension in ArcGIS for advanced analysis.
  - Raster data (derived from vector): 25m resolution (26 Subclasses) and 1km resolution (aggregated details: Subclass level with Dominant values and Percentages; Aggregate class level with Dominant values and Percentages).
  - Raster format: GeoTiff; Spatial Analyst extension may be required in ArcGIS.
  - Note: Raster 2000 cannot be directly used to estimate changes since 1990 due to methodological differences.

- Dataset coverage and tile structure
  - Data compiled on 100km tiles; scenes classified per parcel and added to corresponding tile.
  - Edges may contain overlaps; tiles are merged/eroded to form a single layer, with some edge artefacts possible.

- Hierarchical nomenclature
  - Vector data provides Subclass (and Variant) detail; codes and descriptions map to broad habitat classifications.
  - Subclass and Variant codes are used in attributes (e.g., Level 2 subclass codes and Level 3 variant codes).

- Vector polygon attributes
  - SegID: Unique parcel identifier.
  - BHSub: Dominant land cover subtype (Level 2).
  - BHSubVar: Dominant land cover subtype variant (Level 3).
  - PerPixList: Top-five per-pixel subclass composition (Level 3 only).
  - OpHistory: Processing history details (input data, dates, KBC rules applied) with a compact encoding described in the document.
  - TotPixels / CorePixels: Pixel counts for full parcel and core classification area.

- OpHistory attribute details
  - Five fields: Scene number, Sensor(s), Acquisition dates, Single-date cloud-hole patch indicator, and an extended six-field descriptor for spectral and processing information.
  - The sixth field records miscellaneous information (e.g., edge merging, training data usage, etc.) with specific codes.

- Colour recipes and display
  - Table-based colour assignments for the 26 Subclasses to support consistent visualization in GIS.
  - Each Subclass has defined Hue, Saturation, Value (or RGB equivalents) for display.

- LCM2000 Broad Habitat descriptions
  - Broad habitat categories include: Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved grassland, Neutral/Calcareous/acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Standing water, Montane habitats, Inland bare ground, Suburban/rural developed, Continuous urban, Supra-littoral and Littoral habitats, among others.
  - Descriptions emphasize vegetation structure, management status, and constraints in remote sensing for certain classes (e.g., wetlands, bog depth).

- Edge overlap and artefact handling (Appendix 1)
  - Edge overlaps occur due to mosaic of multiple images; overlaps removed via erosion/merging to produce a single parcel layer per tile.
  - Artefacts are rare (<0.1% of parcels) but may occur; guidance provided to tidy visuals or dissolve boundaries between like classes.
  - Several approaches for handling edge issues in GIS (clipping, union, dissolve) with cautions about losing parcel-level metadata.
  - For Level 3 data, preserve bhsubvar during dissolving to avoid losing key classification detail.
  - Priority of first input tile can affect edge parcels during tile merges.

- Customisation and production philosophy
  - LCM2000 is designed as an extensible data framework, not just a map; users are encouraged to modify and expand with parcel-level metadata and lineage tracking.
  - Unique Segid labeling should be retained to maintain traceability and facilitate communication with data managers and other users.
  - Production philosophy prioritises retaining as much information as possible; changes to attributes should be documented with new attributes or lineage records.

- Documentation, usage, and references
  - Detailed methodology and construction references available (Fuller et al., 2002; Smith et al., 2001; Jackson, 2000) for broader habitat classification integration.
  - Further information and data access through the Land Cover Map homepage and CEH Spatial Data contact details.
  - Important caution: users should clearly distinguish data model/resolution differences when assessing accuracy and suitability for specific applications.

- Accuracy and usage notes
  - Users should avoid conflating inaccuracy with differences in data model, scale, resolution, or class definitions.
  - LCM2000 acknowledges inherent inaccuracies; users should consider these in the context of intended use and data lineage.