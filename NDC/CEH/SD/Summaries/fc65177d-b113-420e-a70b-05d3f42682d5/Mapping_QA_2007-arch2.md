# Mapping Quality Assurance Exercise

- Purpose: Assess quality of digital mapping and QA processes for Countryside Survey 2007, ensuring data are compatible with previous approaches, analysable in a national geodatabase, and suitable for cross-dataset comparisons.

- Key shift: Move from post-survey lab digitisation of paper maps to field mapping with a dedicated Surveyor software, reducing subjectivity and improving data clarity and attribute recording.

- QA workflow: Data uploaded to an interactive wiki for early checks; Quality Control teams conducted on-site visits to ensure protocol adherence; multiple QA approaches implemented to test mapping efficacy.

- Data and outputs: Emphasis on high-quality habitat and landscape feature data, with outputs suitable for analysis against standards and for integration with other national spatial datasets.

- Scope of QA exercise: Mapped data QA conducted in 23 1km squares, chosen to represent land classes and locations across GB; common areas between QA and survey data excluded where access was refused.

- Methods used in analysis:
  - Direct comparison of aggregate areas/lengths/points per square (CS vs QA data).
  - Raster data comparison: convert polygons to 10x10 m raster cells, assign dominant Broad Habitat, compare QA vs CS raster maps.
  - 100-point grid overlap: 10x10 point grid per square to assess concordance of Broad Habitats.
  - Attribute analysis: reference ID layers created to compare species/attributes within matched features.
  - Surveyor efficiency metrics: use of visit-status layers, rate of land visited, and richness of recorded species.

- Surveyor efficiency and data quality:
  - Low non-visited land fraction overall (average around 0.4% in many squares).
  - Mandatory fields increased the number of recorded records and species per area compared with earlier surveys.
  - Digital workflow improved immediate data checks and field-to-database integrity.

- 6.1 Direct comparison of aggregate areas (square-level):
  - In 81% of squares, Broad Habitats (BH) recorded by CS and QA agreed.
  - Mean differences between CS and QA BH extents generally under 3.5% across BHs; most standard deviations under 5%.
  - Notable potential issues identified for Improved grassland, Neutral grassland, Dwarf Shrub Heath, Bog, Urban, and several upland habitats.
  - Blanket Bog discrepancies highlighted; 2007 Field Handbook revisions and training were aimed at clarifying definitions.

- 6.2 Raster data comparisons:
  - Average raster agreement across squares around 60–90%, with several squares showing very high concordance (e.g., 364, 488) and some poorer performers (e.g., 261, 773).
  - Table 6.2b details agreement by BH per square, illustrating where discrepancies arose (e.g., Urban vs grassland allocations, acid/neutral grassland overlaps).

- 6.3 100-point analysis:
  - Overall good concordance for many squares; some squares showed substantial mismatch (e.g., 773 with only ~19% concordance; 261 around 41%).
  - Table 6.3a provides concordance/ discrepancy counts by BH; Table 6.3b shows a matrix of BH/PH matches and mis-matches, illustrating areas where misclassification occurred (notably in blankets bog vs dwarf shrub heath, upland mosaics, and machair-related variations).

- 6.4 Polygon analysis of species attributes:
  - 1081 QA polygons and 998 CS polygons matched by location; about 45% of matched QA polygons shared at least one listed species with the CS polygon.
  - Concordance for species within matched polygons varied by BH; woodland and Improved Grassland showed higher species-match rates; upland mosaics and Bracken had lower concordance due to fine-scale variability and definition differences.
  - 77% of polygons with matching species also shared the same BH, indicating species composition influenced habitat coding in many cases.
  - Species-level concordance for the most common species (e.g., Lolium perenne) varied, generally lower than habitat concordance due to multiple co-dominant species and identification challenges.

- 7.x Linear features analysis (7.1):
  - High consistency in land-use theme choices for linear features between QA and CS; small number of cases where QA recorded a feature and CS did not.
  - Some confusion between belts of trees (FO) vs woody features (WNS, WUS), but overall robust agreement.

- 8.x Point features analysis (8.1):
  - Overall, minor differences in total points; veteran trees showed the greatest discrepancy, due to field instruction to select up to two trees per species and possible multiple candidate trees in a location.

- 9 Change recording:
  - Change types recorded: Real change, Error change, No change.
  - Tables 9.1–9.3 show generally good agreement on change coding across broad habitats, linears, and point features; some complexity remained for habitat-level changes.
  - Digital workflow enabled in-field updating and verification of change, though some surveyors needed time to adapt to the new change-coding approach.

- Main conclusions:
  - The 2007 digital mapping and QA framework produced generally high alignment between CS surveyors and QA assessments across most habitat types and feature classes.
  - The largest discrepancies occurred in specific habitat classes (notably Blanket Bog, Neutral vs Improved Grassland, Broadleaf vs Coniferous woodland) and certain upland mosaics, driven by definitional differences and the continuum of habitat types.
  - Training, clearer habitat definitions, and continued refinement of the field handbook are recommended to improve consistency in future efforts.
  - The inclusion of change-recording fields and real-time QA checks demonstrably improved data integrity and offered a framework to align past maps with updated field observations.

- Overall takeaway for environment monitoring analysts:
  - Digital field mapping and integrated QA workflows enable standardized, scrutinizable data outputs over time.
  - Systematic multi-scale QA (square-level, raster, and 100-point analyses) identifies where definitions and mapping practices diverge, guiding targeted improvements.
  - While high concordance is achievable across most habitat classes, careful management of edge cases (e.g., Blanket Bog, upland mosaics, and complex grassland boundaries) is essential for maintaining long-term data comparability and policy-relevant monitoring.