# LCM2000

- LCM2000 is a parcel-based thematic map of land cover for the United Kingdom, produced mainly from Landsat and supplemented with ancillary data. It supports UK-wide habitat classification aligned to JNCC Broad Habitats, and is available in both vector and raster formats with multiple detail levels and resolutions.
- It updates and upgrades the Land Cover Map of Great Britain (LCMGB) from 1990 and includes Northern Ireland, enabling an all-UK dataset. It is not directly comparable to LCM1990 for change detection.

## Data formats, coverage and scale

- Formats:
  - Vector: polygons (land parcels) with attached attributes; standard ESRI shapefile.
  - Raster: 25 m grid (26 Subclasses) and 1 km grid (derived from 25 m; Subclass and Aggregate levels, with Dominant and Percentage values).
- Spatial detail:
  - Minimum mappable area: greater than 0.5 ha; parcels ≤ 0.5 ha dissolved into surrounding areas during production.
  - Raster data are not directly comparable with LCM1990 due to different construction methods.
- Coverage:
  - 100 km tile basis mosaic across the UK; tiles may be edge-merged, with some artefacts possible at tile edges (<0.1% of parcels).
- Product variants:
  - Vector Level 2: 26 Subclasses (most widely used).
  - Vector Level 3: up to 72 Variants; available by special arrangement with CEH staff.
  - Raster: 25 m (26 Subclasses) and 1 km (Subclass and Aggregate with Dominant and Percentage values).

## Hierarchical nomenclature and attributes

- Classification:
  - Subclass level (Level 2) and Variant level (Level 3) provide increasing detail; level 3 detail quality may vary geographically.
- Key vector attributes:
  - SegID: unique parcel identifier.
  - BHSub: dominant land cover at Level 2 (hierarchical code).
  - BHSubVar: dominant Level 3 variant (if present).
  - PerPixList: top-five per-pixel subclass percentages (Level 3 only).
  - OpHistory: processing history for the parcel (image dates, KBC rules, etc.).
  - TotPixels: total pixels in the parcel.
  - CorePixels: pixels in the core area used for classification.
- Note: Some attributes appear only in Level 3 data; others are present in Level 2.

## OpHistory and provenance

- The OpHistory (PHD) on each parcel records input data and the progression through classification, knowledge-based corrections (KBC), and final compilation. It contains:
  - Scene number, sensor, and image acquisition dates.
  - Information on KBC rules applied (phase 1 and phase 2).
  - Indicators of data patching, cloud-hole filling, and other processing details.
  - A sixth field for other information and a short legend of codes describing processing steps.

## Colour mapping and habitat descriptions

- Colour mapping:
  - 26 Subclasses each have recommended display colors (Hue/Saturation/Value or RGB approximations) to aid visualization.
- Broad Habitats (descriptions provided for the 16+ Broad Habitat groups, e.g., Broad-leaved/mixed woodland; Coniferous woodland; Arable and horticulture; Improved/Neutral/Calcareous/Acid grassland; Bracken; Dwarf shrub heath; Fen/marsh/swamp; Bog; Standing water; Montane habitats; Inland rock; Built-up areas; Coastal habitats; etc.).
- Notable nuances:
  - Some classes distinguish at subclass level; others use broader categories.
  - The Broad Habitat descriptions explain typical vegetation and management considerations that influence classification.

## Edge overlaps, artefacts and data cleaning

- Edge overlap issues:
  - Edge overlaps occur due to mosaic of multiple overlapping scenes; artefacts can arise at 100 km tile edges.
  - Artefacts are rare and represent less than ~0.1% of parcels.
- How to deal with edge artefacts visually and computationally:
  - Visual tidy-up by dissolving boundaries between adjacent parcels of the same class using GIS legend tools (preserve parcel metadata).
  - Clipping or merging 100 km tiles can incur loss of parcel-level metadata; merging retains attributes but may cause inaccuracies in edge parcels.
  - For Level 3 data, preserve bhsubvar during dissolves to avoid losing key Level 3 information.
  - Data selection (e.g., select edge areas) before dissolving can speed up processes.
  - Order of tile input matters; the first input tile often has precedence at edges.
- Slivers and small parcels:
  - Parcels smaller than the minimum mappable unit may exist; handled via visual removal, dissolving with adjacent similar parcels, or “intelligent” dissolve along the longest shared boundary to preserve context.

## Customisation, labeling and governance

- Customisation:
  - LCM2000 is designed as a data storage and analysis framework; users are encouraged to modify and expand the dataset while preserving parcel-level meta-data for lineage.
- Unique labeling:
  - Each parcel has a unique SegID; users should retain this to maintain traceability with data management and other users.
- Production philosophy:
  - The process preserves as much information as possible; retain lineage by recording metadata and changes in new attributes when modifying data.

## Documentation, accuracy and usage notes

- Documentation and change tracking:
  - Fully document data changes to support data management, security, and feedback to the data team.
- Accuracy and interpretation:
  - Accept that LCM2000 contains inevitable inaccuracies due to data model, scale, resolution, and interpretation.
  - Differences from other datasets or classifications should be described in terms of data model and methodological reasons, rather than as simple inaccuracies.

## Additional references and contact

- Further information and methodology references are provided (e.g., Fuller et al. 2002; Smith et al. 2001) and the CEH Land Cover Map pages for access and inquiries.
- Contact: CEH Spatial Data team (spatialdata@ceh.ac.uk) for data sales or more details.