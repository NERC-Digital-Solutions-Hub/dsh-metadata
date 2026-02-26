# LCM2000 specification

- Overview
  - LCM2000 is a parcel-based thematic classification of UK satellite imagery, producing an all-UK land cover dataset (including Northern Ireland) derived mainly from Landsat and supplemented with ancillary data.
  - Classified to the Joint Nature Conservation Committee Broad Habitats, with added detail for wider use; available in vector and raster formats and in several detail/resolution versions.

- Classification and scope
  - Minimum mappable parcel size: greater than 0.5 hectares (smaller parcels are dissolved into surrounding areas).
  - Uses a hierarchical nomenclature tied to Broad Habitats; includes Level 2 Subclasses and Level 3 Variants (the latter may vary in accuracy across the country).
  - Vector and raster formats; Vector is polygonal parcels with attributes; Raster includes 25m and 1km grids with Subclass, Aggregate, and Variant representations.
  - Raster data are not directly comparable to LCM1990 due to differing construction methods; not suitable for estimating change over the 10-year period.

- Product versions
  - Vector, Level 2: 26 Subclasses (standard, widely used).
  - Vector, Level 3: 72 Variants (requires special arrangement and additional support).
  - Raster, 25m: 26 Subclasses; Raster, 1km: Subclass, Dominant values, and Percentage values; also 10 Aggregate classes with Dominant/Percentage.
  - Standard outputs are GeoTiff for rasters; Vector outputs are ESRI shapefiles (ArcGIS compatibility may require Spatial Analyst for certain analyses).

- Dataset coverage and structure
  - Compiled on a 100km tile basis; images are classified per parcel and added to the corresponding tile.
  - Vector data provide a detailed Hierarchical nomenclature for Subclass and Variant codes; a cross-reference table lists codes and descriptions.

- Vector polygon attributes
  - SegID: unique parcel identifier (OS 100km square + sequential segment).
  - BHSub: dominant Subclass code (hierarchical).
  - BHSubVar: dominant Variant code (Level 3).
  - PerPixList: top-five spectral Subclasses by pixel percentage (Level 3 only).
  - OpHistory: processing history details (dates, sensors, KBC steps, etc.).
  - TotPixels: total pixels in the parcel; CorePixels: pixels used for maximum likelihood classification.
  - Some attributes (e.g., PerPixList, BHSubVar) are Level 3 only or conditional depending on data level.

- OpHistory attribute (processing history)
  - Each parcel includes a processing history descriptor (PHD) with fields describing:
    - Scene number, sensor, acquisition dates, cloud-hole patches, and a 6th field for other information.
    - Spectral probability: a score indicating how close the segment’s spectral data were to the expected Broad Habitat.
    - Probability aggregation flag: indicates whether probability aggregation rules were applied.
    - Phase 1 KBC rules: number of knowledge-based corrections applied (scene-dependent).
    - Phase 2 KBC rules: UK-wide corrections.
    - Various flags indicating edge conditions, training data usage, prior datasets, etc.
  - The table and example explain how to interpret the PHD fields and how they influence data interpretation.

- Colour recipes and Broad Habitat descriptions
  - Colour display guidelines are provided for all 26 Subclasses to aid visualization and interpretation.
  - Broad Habitat descriptions (16 categories) define high-level groupings such as Broad-leaved/mixed woodland, Coniferous woodland, Arable/horticulture, Improved/Neutral/Calcareous/Acid grasslands, Bracken, Dwarf shrub heath, Fen/marsh/swamp, Bog, Waters (inland), Montane habitats, Inland bare ground, Suburban/rural developed, Continuous urban, and coastal/marine habitats (with formal definitions and notes).

- Further information and references
  - Contact details for Land Cover Map data and sales.
  - Key publications detailing the methodology and construction of Land Cover Map 2000 and related classifications.
  - References for the Broad Habitat classification guidance.

- Appendix 1: Dealing with edge overlap problems
  - Edge overlaps arise from mosaic construction and cloud-hole patching; 100km tiles include multiple overlapping parcels that were eroded/merged to form a single layer.
  - Artefacts are rare (typically <0.1% of parcels); edge parcels may be duplicated across adjacent tiles and may show boundary artefacts.
  - Visual tidying tips:
    - Dissolve boundaries between adjacent parcels with the same class using legend tools (ArcMap) to produce a cleaner join without altering underlying attribute data.
  - How to deal with edge artefacts in practice:
    - Clip data to tile edges or merge tiles (noting that editing may invalidate some parcel-level attributes).
    - Use Union to merge tiles while retaining attribute copies (with caveats about edge parcel attributes).
    - When dissolving, preserve Level 3 BHSubVar data to avoid losing important information.
    - Use selective dissolving around edges to speed up processing (e.g., select edge parcels and dissolve only those).
  - Precedence rules during tile merging:
    - The first input tile often takes precedence for edge parcels; some edge parcels may differ between tiles, leading to subtle differences in the output.

- Appendix 1: Dealing with "slivers"
  - Very small parcels and slivers (often from patching cloud holes) can be:
    - Visually removed by dissolving boundaries between like classes.
    - Intelligently dissolved into adjacent parcels with the longest shared boundary when appropriate.
  - The approach should consider preserving important class information and not over-dissolving.

- Appendix 2: Good practice
  - Guidance on best practices for handling data, maintaining data integrity, and ensuring traceability and provenance.

- Customisation, provenance, and production philosophy
  - LCM2000 is designed as a data storage and analysis framework; users are encouraged to modify and expand their version while preserving lineage.
  - Unique Segid labels should be retained to enable traceability and communication with the data management team.
  - The production philosophy emphasizes retaining as much information as possible and documenting changes to preserve data integrity and explainability.
  - Users should document changes and be mindful of differences between data models, scale, resolution, interpretation, and target class definitions when assessing accuracy.

- Accuracy and correspondence
  - Acknowledges inevitable inaccuracies due to data models, scale, resolution, and interpretation.
  - Differences from other datasets may reflect methodological choices rather than true inaccuracies; care should be taken in interpreting mismatches.