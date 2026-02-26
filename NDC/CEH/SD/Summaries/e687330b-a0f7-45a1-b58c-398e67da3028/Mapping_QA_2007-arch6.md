# Mapping Quality Assurance Exercise

- Aims and context
  - Assess quality of digital habitat and landscape mapping from Countryside Survey 2007.
  - Ensure data are compatible with previous approaches and suitable for rapid analysis in a geodatabase with other national datasets.
  - Use digital mapping (Surveyor) to reduce interpretation error, enable timely data checks, and support QA across a broad range of topics.

- Data collection and workflow
  - Field mapping performed with Surveyor software, requiring mandatory fields and prompts for each feature type.
  - In-field data uploaded to an interactive wiki for early data checking by office staff; QA teams visited survey teams to ensure protocol adherence.
  - Digital geodatabase integration allowed direct comparison between surveyors’ data and QA data, across areas, lines, and points.

- QA extent and design
  - QA covered 23 1km squares (with refusals noted); goal was broad representation across land classes and locations, not full square coverage.
  - QA squares selected based on land class and location; analyses focused on common surveyed areas between CS and QA.

- Analytical approaches
  - Direct comparison of aggregate areas/lengths/points per square (CS vs QA).
  - Raster comparison: convert polygon data to a 10,000-cell (10x10 m) grid per 1km square; compare dominant Broad Habitat in each cell.
  - 100-point grid: overlay 10x10 point grid per square; compare Broad Habitat matching at 100 points.
  - Attribute-level comparisons: reference IDs used to compare species attributes for matched areas/lines/points.
  - Surveyor efficiency: evaluation of visit-status layers, coverage, and species recording frequency.

- Key findings: habitat mapping accuracy and discrepancies
  - Direct aggregate comparisons (6.1)
    - In 81% of cases, both CS and QA recorded the same Broad Habitat (BH) in a square.
    - Mean differences between QA and CS BH proportions were generally small: most BHs showed differences under 3%, with a few exceptions.
    - Notable potential issues for Improved grassland, Neutral grassland, Dwarf Shrub Heath, Bog, Urban, and Sub-littoral/Machair-type habitats in certain squares.
    - Upland mosaics and peatland (e.g., Blanket Bog) proved particularly challenging; definitional updates and training affected consistency.
  - Raster data comparisons (6.2)
    - Overall raster agreement across squares averaged around 76%, with some squares much higher (e.g., 364, 488) and others lower (e.g., 261, 773).
    - Some BH-level disagreements highlighted by per-square agreement measures.
  - 100-point concordance (6.3)
    - Concordance across Broad Habitats generally good, with many squares above ~70–80%, but some notable exceptions (e.g., squares 773 and 261 showed low concordance).
  - Habitat definitions and definitional issues
    - Blanket Bog disagreements were prominent, linked to updated field handbook definitions and complex peatland mosaics (e.g., Dwarf Shrub Heath vs Blanket Bog, especially in Scotland).
    - Urban vs Improved Grassland recording ambiguities noted; machair-related anomalies in Scottish dunes discussed.
  - Species attributes within polygons (6.4)
    - 1,081 QA polygons matched to 998 CS polygons; 45% of QA polygons had at least one listed species present in the matched CS polygon.
    - Among matched polygons, 77% also shared the same BH, suggesting species choice often aligns with habitat allocation but not universally.
    - Species concordance across commonly recorded species was around 40%; QA tended to record more species than CS.
    - Examples of commonly recorded species and trends provided, with some species showing higher CS-vs-QA concordance than others.
- Change recording and analysis (9)
  - Change coding allowed Real change, Error Change, and No Change; an explicit “error change” field supported data corrections.
  - Overall, high agreement between CS and QA on change assignments for most habitat types and linear/point features.
  - Some complexity remained, particularly for habitat-level change interpretations; the digital workflow helped improve change recording but added training needs.

- Linear and point feature analyses (7–8)
  - Linear features: strong overall agreement in land-use theme classification (e.g., boundaries, fences, walls, arable, etc.); very few cases where QA recorded a feature not replicated by CS.
  - Some potential confusion between certain forestry/woody categories (e.g., belts of trees vs woody linear features), but no major systemic issues detected.
  - Points: overall minor differences in total counted points; land-use themes captured similarly across CS and QA; some differences observed in veteran trees due to field selection limits.

- Data quality implications and recommendations
  - The shift to digital data collection and in-field verification improves data quality, timeliness, and consistency, enabling more robust cross-dataset analyses.
  - Definitional clarity and training are critical, especially for peatland (Blanket Bog), urban vs grassland classifications, and dune-associated habitats (machair).
  - Ongoing refinement of habitat definitions and field-handbook guidelines is recommended to minimize misclassification in future surveys.
  - The QA framework demonstrated effective error detection and opportunities to iterate on data collection protocols, feature definitions, and change-tracking practices.

- Overall takeaway for Data Support
  - Digital mapping and QA processes substantially enhance data quality and interoperability, while also revealing specific areas where habitat definitions and field practices can be refined.
  - The combination of direct, raster, and 100-point analyses provides a comprehensive view of data consistency, enabling targeted improvements and informing future data products and analyses.