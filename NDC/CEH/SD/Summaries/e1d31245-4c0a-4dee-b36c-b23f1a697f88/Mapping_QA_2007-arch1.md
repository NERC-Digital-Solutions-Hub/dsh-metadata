# Mapping Quality Assurance Exercise

- Purpose: Assess quality of the 2007 Countryside Survey mapping by comparing field surveyors (CS) with QA assessors using a digital workflow; evaluate mapping accuracy across habitats, features, and change records; inform improvements and data integration with national datasets.

- Data scope: 23 x 1 km squares; all mapping conducted digitally with Surveyor software; data uploaded to a wiki for early QA; common surveyed areas between CS and QA used for comparisons; access refusals noted.

- Key methodologies:
  - Direct comparison of aggregate areas/lengths/points per square (CS vs QA).
  - Raster comparison: convert polygons to 10 x 10 m raster cells to compare Broad Habitats (BH) and locations; sample with resolution-based points.
  - 100-point grid analysis: overlaid points to assess concordance of BH/PH between CS and QA at ~100-point resolution.
  - Attribute and polygon analyses: matched reference IDs to compare species attributes and habitat codes; spatially matched polygons for species concordance.
  - Land-use/linear feature analysis: buffering QA linears to compare land-use themes with co-located CS linears; point and polygon analyses for accuracy.

- Quality and efficiency indicators:
  - Surveyor efficiency: low not-visited land (avg ~0.4% of available area; some squares higher due to access issues); mandatory in-field data fields increased species recording.
  - Change recording: use of an "error change" field to flag previous mapping mistakes and update accordingly; complexity required substantial training and QC support.

- Main findings (by analysis type):

  - Direct comparison of aggregate areas (6.1)
    - 81% of squares had BH presence recorded by both CS and QA.
    - Mean differences between QA and CS for BH extent generally small: mostly under 1–3.5%, with a few habitats showing larger deviations.
    - Notable potential issues in certain habitats (e.g., Improved/Neutral Grassland, Dwarf Shrub Heath vs Blanket Bog, Urban vs Grassland, upland mosaics) often tied to scale, boundary definitions, or habitat overlap.
    - Blanket Bog particularly challenging; disagreements often between Dwarf Shrub Heath and Blanket Bog; training and revised key definitions mitigated some differences but remain a concern for upland areas.

  - Raster data comparisons (6.2)
    - Overall raster agreement across BHs per square averaged about 76%, with some squares much higher (e.g., 364, 488 at ~98%) and others lower (e.g., 261, 773 around 49–66%).
    - Differences by BH type highlighted where misclassifications occur in specific squares, informing targeted definition refinements.

  - 100-point concentration analysis (6.3)
    - Concordance across BHs generally good for many squares; some squares showed notable mis-matches (e.g., 773 with very low concordance; 261 with modest concordance).
    - Overall, most squares demonstrated good agreement, but mosaicked or upland areas with complex transitions posed more challenges.

  - Polygon species attributes (6.4)
    - 1081 QA polygons and 998 CS polygons matched spatially; only about 45% of QA polygons contained at least one species also observed in the matched CS polygon.
    - Species concordance varied by habitat type; woodland and Improved Grassland showed higher species concordance; Bracken, upland mosaics, and complex bog/dwarf heath boundaries showed lower concordance.
    - 77% of polygons with matching species also had matching BH, indicating habitat allocation often aligned with species lists but not universally.

  - Point features (6.4 table on points)
    - Habitat code agreement for points generally high; some inconsistencies between woodland/forest codes attributed to historical coding practices.

  - Linear features (7.1)
    - Overall small differences in total linear lengths per square; high consistency in land-use theme assignment for linears (e.g., fences vs walls, belts of trees vs WO), with a few ambiguous cases in forestry-related classes.

  - Points (8.1)
    - Very small differences in total points per square; consistency across major themes (Forestry, Inland Physiography, Inland Water, Structures, Veteran Trees), with veteran trees showing notable disparities due to multiple possible selections per species.

  - Change recording (9)
    - Digital change coding enabled detailed change descriptions (Real change, Error change, No change); QA and CS agreement on change codes was generally strong across broad habitats and linears, though some habitat-specific issues persisted.
    - Agreement on change for linear and point features was higher than for broad habitats, reflecting easier, clearer change signaling in discrete features.

- Notable implications for practice:
  - Digital data collection and early wiki-based QA substantially improve data traceability, timeliness, and consistency; mandatory fields enhance data completeness, especially for species.
  - Broad Habitat definitions remain a major source of discrepancy in upland/mosaic contexts and for complex habitats like Blanket Bog; ongoing refinement of habitat keys and training is recommended.
  - Urban vs agricultural classifications can cause misallocations; clarify urban boundary definitions and apply consistent interpretation across teams.
  - 1 km square scale is effective for broad comparability, but some habitat overlays and mosaics at small scales require careful interpretation and potential multi-scale analysis.
  - The 100-point and raster approaches provide complementary views of accuracy; use both to identify systematic issues and to guide targeted re-coding or redefinition efforts.
  - Species concordance in polygons is moderate; emphasis on standardizing dominant-species selection criteria could improve cross-team consistency.

- Overall assessment:
  - The 2007 digital mapping QA exercise demonstrates generally good agreement between CS and QA across most habitat types, with higher consistency for linear and point features than for some broad habitat allocations.
  - Key discrepancies are concentrated around complex upland and boundary habitats (notably Blanket Bog vs Dwarf Shrub Heath, Neutral vs Improved Grassland, and urban classifications), underscoring the need for ongoing habitat-definition refinement and targeted training.
  - The exercise provides a robust framework for ongoing QA, reproducible analytics, and data integration in national-scale habitat and landscape datasets.