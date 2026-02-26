# Mapping Quality Assurance Exercise

- Purpose and context
  - Report on the 2007 Countryside Survey mapping QA, aimed at producing high-quality habitat and landscape data compatible with national spatial datasets.
  - Introduced digital field mapping (Surveyor software) to reduce interpretation errors, enable early data checks via a wiki, and implement in-field data prompts and mandatory fields.
  - QA process involved independent verification by QA teams against surveyor data to assess accuracy, consistency, and data handling at multiple scales.

- Scope and data coverage
  - QA surveyed 23 1-km squares, selected to cover diverse land classes and locations across Great Britain.
  - Areas with refused access or not visited were excluded from analyses; common surveyed areas between CS and QA were used for comparisons.
  - Data collected and stored in a shared geodatabase, enabling direct comparison of habitat, linear, and point features.

- QA methodologies and analyses
  - Three main QA approaches:
    - 4.1 Direct comparison of aggregate areas/lengths/points for whole squares.
    - 4.2 Raster data comparison: polygons converted to 10 x 10 m rasters within each 1-km square to compare dominant Broad Habitats (BH) and their locations.
    - 4.3 100-point grid comparisons: overlaid grids to assess concordance of BH at a fixed resolution; plus 6.3 and 6.4 extended analyses.
  - Additional analyses:
    - 4.4 Attribute comparisons for areas, lines, and points using reference ID layers.
    - 5.1 Surveyor efficiency metrics (visit status, not-visited vs visited areas) and 5.2 changes in plant species recording due to mandatory fields.

- Key findings: broad habitat (BH) mapping quality
  - 6.1 Direct comparison of aggregate square areas:
    - 81% of squares had BH presence recorded by both CS and QA.
    - Mean differences between QA and CS for BH proportions were mostly under 3.5% across most BH types; a few BHs showed larger SDs indicating potential misallocation (e.g., Improved/Neutral grassland, Dwarf Shrub Heath, Bog, Urban, Sub-littoral sediment).
    - Notable issues discussed for Blanket Bog and upland mosaics, with some misalignment between field definitions and mosaic mapping.
  - 6.2 Raster data comparisons:
    - Overall, good agreement in many squares; average agreement around 76%, with some squares notably higher or lower (e.g., 364 and 488 high; 261 and 773 lower).
    - Per-BH agreement highlighted variability; notable discrepancies between Neutral and Improved Grassland, Broadleaf vs Coniferous Woodland, urban/BH allocations, and machair-related anomalies in Scotland.
  - 6.3 100-point grid concordance:
    - General good agreement for most squares; some notable mis-matches (e.g., squares 773 with very low concordance; 261 with moderate concordance).
    - Table 6.3b showed cross-tabulations of BH/PH codes; overall, most BH/PH allocations aligned, but certain habitats exhibited higher discordance due to definitions, mosaics, or landscape-specific issues.
- Key findings: species attributes and polygon analysis
  - 6.4 Polygon analysis of species attributes:
    - 1081 QA polygons and 998 CS polygons matched spatially; about 45% of matched polygons contained at least one common listed species.
    - Concordance by BH varied, with higher matching for woodlands and Improved Grassland; lower for Bracken, fen/marsh, and upland mosaics.
    - About 77% of polygons with matched species also had a matched BH, indicating species composition often aligned with the chosen habitat, but not universally.
  - 6.5 Listed species concordance:
    - Overall species concordance around 40% for commonly recorded species; QA tended to record more species.
    - Certain species showed higher agreement (e.g., Lolium perenne, Calluna vulgaris, Juncus species) while others showed substantial divergence due to identification or dominance differences.
- Key findings: linear and point features
  - 7.1 Direct comparison of aggregate linear features:
    - Lengths of linear features per square generally similar between QA and CS; minor differences in most squares.
    - Theme-based breakdown (banks, fences, forestry belts, etc.) showed strong overall alignment, with few cases of mismatches (e.g., fence vs wall) and some confusion between related forestry/wildlife tree categories.
  - 7.2 Land use themes for linear features:
    - Very high consistency in choice of land-use themes between QA and CS; minimal instances of QA-recorded features without CS counterpart.
  - 8.1 Points:
    - Total points per square showed only minor differences; major land-use themes (forestry, inland physiography, urban, etc.) aligned well.
    - Veterans trees produced the largest disparity, reflecting counting and definition differences in selecting representative trees.
- Change recording and data stewardship
  - 9. Change coding introduced in 2007 allowed distinguishing Real Change, Error Change, and No Change, with an explicit error-change field to update previous maps.
  - Overall, change coding showed good agreement across broad habitats and linear/point features, though habitat-based change assessment was more challenging (some discrepancies in BH-level change coding).
  - The digital workflow aided data tidying in the field, but added complexity and training needs for surveyors.

- Conclusions and implications
  - The digital Surveyor-based mapping and wiki-enabled QA processes yielded high overall data quality and strong alignment between QA and CS datasets across multiple dimensions (BHs, linears, points, and change records).
  - Most BH allocations and habitat classifications were consistent, with only a subset showing meaningful discrepancies tied to habitat definitions, upland mosaics, and local habitat peculiarities (notably Blanket Bog, Neutral vs Improved Grassland, urban classifications, and machair areas).
  - Differences highlight the need for ongoing refinement of habitat definitions, improved handling of mosaics, and enhanced training for field teams to ensure consistent application of definitions, especially for complex upland and transitional habitats.
  - The QA workflow demonstrated the value of in-field data validation and metadata-rich datasets, with an emphasis on making derived datasets discoverable and usable, and on documenting data sources and methodological choices for future surveys.