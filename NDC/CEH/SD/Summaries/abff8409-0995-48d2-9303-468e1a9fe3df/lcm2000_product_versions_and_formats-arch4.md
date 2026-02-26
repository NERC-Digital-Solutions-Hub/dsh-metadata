# LCM2000 specification

- A parcel-based thematic map of land cover for the entire United Kingdom, updating and upgrading the Land Cover Map of Great Britain (LCMGB) 1990.
- Derived mainly from Landsat satellite imagery, with integration of ancillary datasets; covers Northern Ireland to provide an all-UK dataset.
- Classified using a hierarchical nomenclature aligned with the Joint Nature Conservation Committee (JNCC) Broad Habitats; aims to provide broad habitat classes while recording additional detail where possible.
- Produced in both vector and raster formats, with multiple product versions offering different levels of detail and spatial resolutions.

## Data formats and structure

- Vector data: polygons representing land parcels with attached attributes.
  - Level 2 (baseline): 26 Subclasses (widely used).
  - Level 3: 72 Variant classes; higher detail with variable accuracy; available by special arrangement.
  - Standard vector format: ESRI shapefile (ArcGIS may require Spatial Analyst extension).
- Raster data: derived from the vector dataset, available in two resolutions (25m and 1km).
  - 25m raster: 26 Subclasses.
  - 1km raster: Subclass level (26), Dominant values, and Percentage values; also Aggregated to 10 Aggregate classes with Dominant and Percentage options.
- Note: Raster data are not directly comparable with LCM1990 due to different construction methods; not suitable for estimating 10-year change.

## Dataset coverage and tile system

- Compiled on a 100km tile basis; imagery classified per parcel and added to the corresponding 100km tile.
- Tiles may be merged; parcels straddling tile edges are retained in both adjacent tiles.
- Overlaps and mosaic construction can introduce artefacts; generally <0.1% of parcels, but users may need to address visually if needed.

## Hierarchical nomenclature and codes

- Subclass and Variant detail levels define land cover types.
- Codes correspond to a hierarchical scheme (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable cereals, etc.).
- Subclass and Variant codes are referenced in the attribute fields (BHSub, BHSubVar) and are used to describe dominant habitat types per parcel.

## Vector polygon attributes

- SegID: Unique parcel identifier (includes OS 100km square and segment number).
- BHSub: Dominant land cover type as a hierarchical code (Subclass level).
- BHSubVar: Dominant land cover type as Variant code (Level 3).
- PerPixList: Top-five spectral subclass percentages within the parcel (Level 3 only).
- OpHistory: Processing history of each parcel (image dates, KBC rules, etc.).
- TotPixels: Total pixels within the parcel.
- CorePixels: Pixels within the parcel core used for maximum likelihood classification.

## OpHistory (processing history descriptor)

- Contains input data and stages of classification, knowledge-based correction (KBC), and final compilation.
- Fields document scene number, sensor data, acquisition dates, cloud hole patches, spectral probability, probability aggregation, and KBC rules applied (Phases 1 and 2).
- Sixth field encodes other conditions (e.g., edge erosion, void filling, training data, etc.).

## Colour mapping (display conventions)

- Table of 26 Subclasses with specific hue, saturation, value (or RGB equivalents) for visualization, enabling consistent color representation across the map.
- Colour assignments are provided for Broad Habitat groups (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable cereals, Grasslands, Urban/suburban areas, Coastal/bathymetric categories, etc.).

## Broad Habitat descriptions

- Broad habitat descriptions (e.g., Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved/Neutral/Calcareous/Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Standing water, Montane habitats, Inland rock, Built-up areas) with definitions and notes on distinctions and potential ambiguities.
- Also describes coastal and littoral habitats ( Supra-littoral and Littoral) and inland water classifications.

## Edge overlap and artefact handling (Appendix 1)

- Edge overlaps arise from mosaic of multiple overlapping images; 100km tiles were eroded/merged to a single parcel layer, with some parcels overlapping tiles retained in both.
- Artefacts near tile edges are rare but may include differing classifications, slivers, or edge boundaries.
- Visual tidying options:
  - Dissolve boundaries between adjacent parcels of the same class using legend tools (ArcMap) without altering core attribute data.
  - Clip data to tile edges or union tiles to merge, understanding that certain parcel-level attributes may be invalid after such operations.
  - For Level 3 data, preserve bhsubvar during dissolves to avoid losing Level 3 information.
- First-input tile precedence typically governs edge results; differences across tiles may lead to slight changes at the boundary.

## Slivers and small parcels

- Slivers and parcels below the minimum mappable unit can occur (often from patching with LCM1990 data).
- User options to address slivers:
  - Visual removal of small parcels.
  - Dissolve with adjacent like-class parcels.
  - Intelligent dissolution toward the adjacent parcel with the longest shared boundary.
- Users should consider the impact of such modifications on overall data context and attributes.

## Customisation and use as a data framework

- LCM2000 is not only a map but a data storage and analysis framework.
- Users are encouraged to adapt, expand, and build upon the dataset, retaining parcel-level metadata to document lineage and processing history.

## Production philosophy and data management

- Emphasizes retaining as much information as possible; maintain comprehensive parcel-level metadata for provenance.
- Changes should be documented and traceable; when altering data, preserve original attributes or create new attributes documenting changes.

## Accuracy and interpretation

- Acknowledge inevitable inaccuracies due to data model, scale, resolution, interpretation, and target class definitions.
- Differences from user needs may stem from methodological choices rather than pure inaccuracy; users should understand the data construction process when assessing suitability.

## Further information and contact

- Land Cover Map homepage and contact details for data sales and methodology references.
- Key references include Fuller et al. (2002, 2001) on construction of parcel-based vector maps from satellite images and related proceedings; Jackson (2000) on Broad Habitat guidance.