# LCM2000 specification

- LCM2000 is a parcel-based thematic classification of satellite imagery covering the entire United Kingdom, upgrading the Land Cover Map of Great Britain (LCMGB) 1990 and producing an all-UK dataset that includes Northern Ireland. It is derived mainly from Landsat imagery, integrates ancillary data, and uses a hierarchy linked to the JNCC Broad Habitats.

- Available in both vector and raster formats, with multiple product versions offering varying levels of detail and spatial resolutions.

Overview of data and classification
- Minimum mappable unit is greater than 0.5 hectares; parcels 0.5 ha or smaller are dissolved into surrounding areas during production, with rare exceptions.

- Classification hierarchy:
  - Level 2: 26 Subclasses (primary targets for broad mapping)
  - Level 3: up to 72 Variant level details (more detailed, may vary in accuracy by area)
  - Vector data are provided as land parcels (polygons) with attached attributes; standard vector format is an ESRI shapefile. Raster formats include 25 m and 1 km resolutions derived from the vector data, with 1 km raster providing Subclass, Aggregate, Dominant, and Percentage values.

- Raster data caveat: LCM2000 raster data are not directly comparable with LCM1990 due to different construction methods and should not be used for estimating change over the 10-year period.

- Product versioning:
  - Vector, Detail level Level 2 (Aggregate level) and Level 3 (Variant level) available; Level 3 available by special arrangement with CEH staff.
  - Raster, 25 m: 26 Subclasses; Raster, 1 km: Subclass and Aggregate detail with Dominant and Percentage values.

Dataset coverage and spatial structure
- Data compiled on a 100 km tile basis; parcels are classified per tile and then added to their appropriate tile. Some tiles were merged for construction efficiency; edge overlaps exist where parcels straddle tile boundaries.

Hierarchical nomenclature and attribute codes
- Vector data include Subclass and Variant detail. Codes are provided to map Subclasses and Variants (e.g., broad-leaved/mixed woodland, coniferous woodland, arable cereals, etc.). A note explains that some GIS packages may display codes as data values rather than Subclass codes.

- The classification is designed to emphasize Broad Habitats for wide-scale use and to extend detail where possible; however, Level 3 accuracy can vary by area, and some details may not be up to date.

Vector polygon attributes and processing history
- Each parcel carries a set of attributes:
  - SegID: unique parcel identifier (including OS 100 km square and segment number)
  - BHSub: dominant land cover (Level 2 subclass code)
  - BHSubVar: dominant land cover variant (Level 3)
  - PerPixList: top five spectral subclasses within the segment (when available)
  - OpHistory: processing history for each segment (image dates, sensors, KBC rules applied)
  - TotPixels, CorePixels: pixel counts for the segment and its core area

- OpHistory (the processing history descriptor) documents input data, processing stages, knowledge-based corrections (KBC), and dataset compilation; fields include scene number, sensor, acquisition dates, cloud-hole patch indicators, spectral probabilities, and KBC rule applications.

Colour mapping and Broad Habitat descriptions
- Colour recipes provide display colors for the 26 Subclasses (and associated Broad Habitats) to support consistent visualization in GIS. Each subclass is assigned specific Hue, Saturation, Value (and approximate RGB) values to aid interpretation.

- Broad Habitat descriptions (JNCC framework) cover categories such as Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Various grasslands (improved, neutral, calcareous, acid), Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Water bodies, Montane habitats, Inland rock, Built-up areas, and coastal/littoral habitats. These descriptions explain the target habitat concepts and distinctions used in LCM2000.

Further information and key references
- Data access and enquiries: CEH Land Cover Map data page and contact details.
- Core methodology references:
  - Fuller et al. (2002) on construction of a parcel-based vector map from satellite images
  - Smith et al. (2001) on Land Cover Map 2000: parcel-based map from satellite images
  - Jackson (2000) on Broad Habitat classification guidance

Appendix 1: Dealing with edge overlap problems
- Edge overlaps arise from mosaicking multiple images and patching cloud holes; 100 km tiles may contain multiple overlapping parcels. Artefacts are infrequent (typically <0.1% of parcels) and can occur due to different imagery at tile edges, erosion/merging differences, or residual slivers.
- Visual tidying options include dissolving boundaries between adjacent parcels of the same class, using ArcMap legend tools to render cleaner joins without degrading source attributes.
- For edge-handling in GIS:
  - Clip to the 100 km edge (note: clipping invalidates parcel-level attributes derived from source data)
  - Merge tiles with caution; dissolving after merging can lose some source metadata
  - For Level 3 data, ensure bhsubvar is preserved during dissolves
  - Use selective dissolves or data selections to limit impact on attributes
- Priority of input tiles can affect edge outcomes; generally the first input tile takes precedence, though identical classifications minimize differences.

Appendix 2: Good practice
- Not detailed in the provided text, but the appendix exists to outline recommended practices for handling LCM2000 data and workflows.

Production philosophy and data governance
- The production approach aims to retain as much information as possible; parcel-level metadata should be preserved to document lineage and processing history.
- When altering data, maintain copies of original attributes and document changes clearly.
- Unique Segid labeling is recommended for clear communication with data management and among users.
- The dataset is designed to be customizable and extensible as a research and applications foundation.

Accuracy and interpretation
- LCM2000 acknowledges inevitable inaccuracies related to data models, scale, resolution, interpretation, and target definitions. Differences from user needs may reflect these fundamental limitations as well as gap-filled data or context changes.