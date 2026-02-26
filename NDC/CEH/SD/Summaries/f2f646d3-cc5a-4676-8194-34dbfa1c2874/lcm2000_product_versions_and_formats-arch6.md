# LCM2000 specification

- Overview
  - LCM2000 is a parcel-based thematic classification of UK satellite imagery covering the entire United Kingdom, including Northern Ireland.
  - It updates and upgrades the Land Cover Map of Great Britain (LCMGB) from 1990 and is produced in both vector and raster formats with multiple detail levels.
  - Classified against a hierarchical nomenclature aligned with JNCC Broad Habitats; designed to support a wide range of users and applications.
  - Raster data are not directly comparable with LCM1990 due to different methods and are not suitable for estimating change over the 10-year period.

- Product formats and levels
  - Vector format: polygons (land parcels) with a rich attribute set.
    - Level 2: 26 LCM2000 Subclasses (standard, widely used).
    - Level 3: up to 72 Variant level (more detail, available by special arrangement and additional user support).
    - Standard vector format is ESRI shapefile; ArcGIS users may need Spatial Analyst for advanced analysis.
  - Raster format (GeoTIFF):
    - 25m resolution with 26 Subclasses.
    - 1km resolution with Subclass level (and Aggregate level) data, including Dominant values and Percentages.
  - Minimum mappable unit: parcels > 0.5 ha; features ≤ 0.5 ha dissolved into surrounding areas during production.

- Dataset coverage and structure
  - Data compiled on a 100 km tile basis; parcels are classified within tiles and then assembled into a UK-wide mosaic.
  - Some tiles were merged to simplify construction; edge parcels may appear in adjacent tiles.
  - Acknowledge edge overlaps and artefacts; users may visually tidy boundaries between same-class parcels without degrading source data.

- Hierarchical nomenclature
  - Vector data available at Subclass (Level 2) and Variant (Level 3) detail, encoded with standardized Subclass and Variant codes.
  - Subclass and Variant codes correspond to Broad Habitat categories; Level 3 Variant details depend on dominant land cover at imaging time and may be incomplete or up-to-date.

- Vector polygon attributes
  - Each parcel includes a set of attributes:
    - SegID: unique parcel identifier (important for lineage and communication with data managers).
    - BHSub: dominant land cover subclass (Level 2).
    - BHSubVar: dominant land cover variant (Level 3).
    - PerPixList: top-five spectral subclasses by pixel percentage (Level 3 only).
    - OpHistory: processing history of the parcel (image dates and KBC rules applied) (Level 2 and 3).
    - TotPixels: total pixels in the parcel.
    - CorePixels: pixels in the core area used for maximum likelihood classification.
  - OpHistory (PHD) details input data and the steps of classification and knowledge-based corrections; includes fields for scene, sensor, acquisition dates, cloud-hole patches, spectral probabilities, KBC rules, and extra flags.

- Colour recipes for mapping
  - 26 Subclasses have recommended display colors (Hue, Saturation, Value; or approximate RGB).
  - Recipes provide consistent visualization across the 26 Subclasses and support quick interpretation in GIS environments.

- LCM2000 Broad Habitat descriptions
  - Provides a description for 26 Broad Habitats, including:
    - Broad-leaved/mixed woodland, Coniferous woodland, Arable and horticulture, Improved grassland, Neutral/Calcareous/ Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Standing water and canals, Rivers/streams, Montane habitats, Inland rock, Built-up areas and gardens, Supra-littoral and Littoral habitats (rock/sediment), Inshore sublittoral and Offshore habitats, and others.
  - Each habitat includes definitions and notes on how land cover is interpreted and mapped, with attention to differentiating related classes and situations where imagery may limit distinctions.

- Appendix 1: Dealing with edge overlap problems
  - Edge overlaps arise from mosaicking multiple images and cloud-hole filling; a single parcel layer is produced by erosion/merging, but some artefacts can remain.
  - Artefacts are typically rare (usually <0.1% of parcels) but may require user tidying.
  - Guidance on visually tidying edges (dissolving boundaries between adjacent parcels of the same class) and on methods to handle edge overlaps when merging 100 km tiles:
    - Clipping to tile edges, merging tiles, or dissolving boundaries—all have trade-offs regarding parcel-level metadata preservation.
    - For Level 3, preserve bhsubvar during dissolves to avoid losing important detail.
    - Practical tips for speeding up edge-area dissolution and selecting edge parcels for targeted treatment.

- Appendix 2: Good practice
  - Indicates that practical good-practice guidelines are provided to support data users in handling and modifying LCM2000 data responsibly.
  - Content details are not fully shown in the extract but are intended to accompany the production and use of the data.

- Customisation and production philosophy
  - LCM2000 is designed as an extendable data framework, not just a static map.
  - Users are encouraged to customize while preserving lineage; retain SegID and related metadata to enable traceability and communication with data management.
  - Production philosophy emphasizes retaining as much information as possible and documenting changes to support data management and security.

- Documentation, accuracy, and usage notes
  - Fully document changes and maintain metadata to support data provenance.
  - Exercise care in using terms like "inaccuracy"—differences may reflect data model, scale, resolution, interpretation, or class definitions rather than true errors.
  - The dataset provides a robust basis for environmental applications and further research, with recommended references for methodology and broad habitat definitions.

- Further information and references
  - Contact: CEH Land Cover Map team (spatialdata@ceh.ac.uk; +44 (0)1491 692315).
  - Land Cover Map homepage: www.ceh.ac.uk/data/lcm.
  - Key references:
    - Fuller et al. 2002: The UK Land Cover Map 2000—construction of a parcel-based vector map from satellite images.
    - Smith et al. 2001: Land Cover Map 2000—parcel-based map from satellite images.
    - Jackson 2000: Guidance on interpretation of the Biodiversity Broad Habitat Classification (JNCC).
  - For Broad Habitat classifications, see JNCC guidance and related documentation.