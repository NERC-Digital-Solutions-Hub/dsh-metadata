# Mapping Quality Assurance Exercise

## Aim and Context
- Countryside Survey 2007 produced high-quality habitat and landscape data aligned with previous approaches.
- Transition to digital mapping in the field (Surveyor software) to reduce post-survey interpretation errors and speed analysis.
- Data stored in a geodatabase; early digital QA checks via an interactive wiki; QA teams conducted field visits to ensure protocol adherence.

## Digital Mapping, Data Management and QA Setup
- Digital mapping eliminated handwriting/interpretation issues; mandatory fields and prompts improved data quality; visit status layers helped track visited features.
- Datasets uploaded to a wiki for early office-based data checking; QA teams visited survey teams to ensure protocol compliance.
- QA compared mapped data against 1998 data using digital tools, enabling digital QA of final data without an intermediate digitisation step.

## QA Approaches and Methodology
- 4.1 Direct comparison of aggregate areas/lengths/points per 1km square (CS vs QA data).
- 4.2 Raster comparisons: convert polygons to 10x10 m cells to assess absolute abundance and spatial location of Broad Habitats.
- 4.3 100-point grid: overlay to evaluate concordance of Broad Habitats at ~100-point resolution; calculates agreement and deviations.
- 4.4 Attribute analysis: matched reference IDs allow comparison of species attributes within corresponding areas/lines/points.
- 5 Surveyor efficiency: evaluation of visit coverage, use of visit-status layers, and recording of dominant species.

## Key Findings: Data Quality and Agreement
- 6.1 Direct comparison of aggregate square data:
  - In 81% of squares, Broad Habitat (BH) presence was recorded by both CS and QA.
  - Mean differences in BH proportions were typically under 1–3.5% across most BH types; some habitats showed larger variation (e.g., Improved/Acid Grassland, Dwarf Shrub Heath, Bog, Urban, Sub-littoral sediment).
  - Notable issues identified with Blanket Bog (definitions updated for 2007), and mosaic upland habitats complicating precise allocation.
- 6.2 Raster data comparisons:
  - Overall raster agreement across squares averaged 76%, with some squares high (e.g., 364, 488) and others low (e.g., 261, 773).
  - Agreement by BH varied by square; some areas showed strong concordance, others substantial misclassification.
- 6.3 100-point grid analysis:
  - Concordance generally high across many squares; some notable mismatches in squares 773 (19% concordance) and 261 (41% concordance).
  - Overall, 76–78% concordance on broad habitat mapping at the 100-point resolution; certain habitats showed higher mismatch due to mosaic or definitional issues.
- 6.4 Polygon-based species attributes:
  - 45% of QA polygons matched a listed species with a CS polygon at the same location.
  - Species concordance varied by habitat; woodland and Improved Grassland tended to have higher species-match rates; upland and mosaic habitats showed more variability.
  - Within matched polygons, 77% also had matching BH; overall species concordance around 40%.
  - Dominant species (e.g., Lolium perenne) more consistently identified across datasets than many others.
- 7.1 Linear features:
  - Lengths of linear features per square generally aligned; high consistency in land-use themes (e.g., fences, walls, hedgerows).
- 8.1 Points:
  - Total points per square showed only minor differences; most points aligned with CS data in land-use theme, with some discrepancies in veteran trees due to the field instruction cap (two large trees per species).
- 9 Change recording:
  - Change coding included Real Change, Error Change, and No Change.
  - High agreement for change coding across broad habitats and linear/point features; some complexities arose in habitat-related changes (notably Blanket Bog) due to evolving definitions and mapping approaches.
  - Digital recording allowed more detailed change information but required additional training and interpretation to ensure consistency.

## Habitat-Specific and Training Implications
- The most significant discrepancies occurred in:
  - Blanket Bog and Dwarf Shrub Heath allocations, partly due to definitional updates and complex boundary cases.
  - Urban vs. Improved Grassland allocations, suggesting need for clearer urban grassland guidelines.
  - Sand Dune/ machair habitats in Scotland, highlighting localised habitat differences.
- Upland mosaics and area-by-area mosaics introduced matching challenges; cross-walking between mosaic BHs and single BH allocations can yield mismatches.
- Training and clearer field handbooks were identified as important to reduce misclassification and improve consistency in future surveys.

## Change Recording, Data Integration and Accessibility
- The inclusion of a formal change field improved the ability to correct past mappings using an error-change designation, though it added complexity.
- The digitally integrated workflow (field mapping, wiki-based checks, and geodatabase storage) demonstrated the value of making underlying data accessible for cross-survey analyses and future monitoring.
- Overall, the QA exercise demonstrates a high level of data integrity and consistency, while also highlighting areas where definitions, training, and local habitat variability require ongoing refinement.

## Conclusions for Analysts Monitoring the Environment
- Digital mapping and integrated QA processes substantially improve data quality, enabling consistent, auditable environmental monitoring over time.
- Agreement between surveyors and QA is strong for many habitat types and feature classes, but certain habitats and mosaics require clarified definitions and targeted training.
- The QA framework provides a robust basis for validating and reconciling large spatial datasets, supporting cross-dataset analyses and policy performance monitoring.
- To maximize value and accessibility, datasets and underlying QA data should continue to be stored in interoperable formats (geodatabases) and shared via accessible portals, enabling broader data integration and scrutiny.