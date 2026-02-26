# Mapping Quality Assurance Exercise

- Purpose: Assess the quality and reliability of digital mapping data from Countryside Survey 2007 by comparing surveyor-collected data with QA team data, using a digital workflow designed to reduce prior mapping errors and enable rapid analysis alongside other national datasets.

## Key context and approach

- Transition to digital mapping in 2007 to avoid subjectivity and errors from post-survey digitisation of paper maps.
- Use of a dedicated Surveyor software with mandatory fields and prompts to capture feature-level data directly in the field.
- Early data checking via an interactive wiki, enabling rapid communication of issues between surveyors and staff.
- QA strategy involved testing data in multiple ways, including field QA in different 1 km squares, to avoid bias toward any single QA approach.

## Data, extent, and workflow

- QA coverage: mapped data QA across 23 1 km squares; selections aimed to represent land classes and locations across GB.
- Parallel data streams:
  - CS surveyors collected in-field data with mandatory fields and visit-status tracking.
  - QA teams re-mapped or validated mapped areas using standard CS tablets/software, producing a single geodatabase for cross-dataset comparison.
- Data handling: unsurveyed areas and areas with refused access were masked; common surveyed areas were used for direct comparisons.

## Analytical approaches

- 4.1 Direct comparison of aggregate areas/lengths/points for whole squares.
- 4.2 Raster data comparisons: polygons converted to 10 x 10 m raster cells; dominant Broad Habitat per cell used to assess absolute amounts and spatial locations; resolution enabled sampling across grids.
- 4.3 100-point grid: overlaid on each square to assess concordance of Broad Habitats at a fixed spatial resolution; positive/negative scoring based on matches.
- 4.4 Attribute comparisons: reference ID layers enabled comparing species attributes across matched areas/lines/points.

## Surveyor efficiency and data quality

- Digital workflow improved deployment of visit-status layers and reduced undetected areas; average not-visited land was very low (often near 0.0–0.4%).
- Increased recording of plant species due to mandatory fields; broader and more consistent species coverage recorded in 2007.
- Some challenges persisted in locating and classifying certain land types, especially where access limitations or land ownership issues existed.

## Key findings on data agreement and discrepancies

- Overall raster and aggregate-area concordance: generally high, with many squares showing strong agreement between CS and QA data; raster agreement often above 70–90% in many squares.
- Variability by habitat type:
  - Most Broad Habitats showed minor mean differences (~<3.5% in many cases) with small standard deviations, indicating good overall alignment.
  - Notable discrepancies identified in specific habitats and contexts (e.g., Improved vs Neutral Grassland, Broadleaf vs Coniferous Woodland, Urban vs Grassland classifications, and Sand Dune habitats due to machair in Scotland).
  - Blanket Bog presented significant definitional challenges, especially when mapping in upland areas; Dwarf Shrub Heath vs Blanket Bog disagreements were prominent in some squares.
- Mosaic and upland complexities: mosaics and small-scale variability in upland areas complicated precise habitat delineation and contributed to some spatial mismatches between CS and QA datasets.
- 100-point and raster analyses: most squares demonstrated good concordance, but a few squares showed substantial mismatches (e.g., squares 261, 773, 935) due to habitat definition issues or localized landscape features.
- Species-level concordance: matched species lists in spatially joined polygons were about 45%, lower than ideal, reflecting the complexity of translating dominant species into consistent Broad Habitat allocations; some taxa showed higher concordance when species were clearly dominant (e.g., Lolium perenne, Calluna vulgaris, etc.).
- Change coding: overall good agreement across habitat and linear/point features, though change assessment on Broad Habitats was more challenging; digital recording facilitated clearer differentiation between Real changes, Error changes, and No Change, but some surveyors needed guidance to apply change codes consistently.

## Notable methodological observations

- Use of multiple analytic modalities (direct square comparisons, raster habitat concordance, 100-point grid, and attribute matching) provided a robust framework to detect both extent and spatial arrangement differences.
- Training and field experience influenced consistency, particularly for complex or less common habitats (e.g., Blanket Bog, machair, urban-forest interfaces, and upland mosaics).
- Differences in habitat definitions and classification rules (e.g., coniferous vs broadleaf woodland definitions) highlighted the need for clear, updated field keys and ongoing harmonization across surveys.

## Change recording and assessment

- Digital change fields enabled richer categorization of changes and potential corrections to past mappings.
- High agreement in change coding for linears and points; habitat-based change assessment remained more challenging due to ecological nuance and habitat overlap.
- The transition to digital change logging supported later data governance and potential data correction workflows.

## Implications for monitoring framework designers

- Embrace digital data capture with built-in validation to improve data quality, consistency, and timeliness of QA checks.
- Implement iterative QA loops combining in-field QA, wiki-based collaboration, and cross-dataset validation to identify and address errors early.
- Use multi-faceted comparison frameworks (direct square-level metrics, raster-based spatial concordance, and fixed-point grids) to capture both area accuracy and spatial arrangement.
- Define and document habitat/classification keys clearly; anticipate mosaic and upland complexity, and plan for targeted training to reduce misclassification across habitat types.
- Maintain explicit change-coding schemes (Real Change, Error Change, No Change) with guidance to ensure consistent application across teams.
- Ensure data governance, metadata, and openness considerations are addressed from the outset to facilitate reuse, transparency, and accountability in monitoring outputs.
- Recognize that certain habitat definitions (e.g., Blanket Bog, machair) may require ongoing refinement and stakeholder consensus to minimize cross-team discrepancies.
- Use the findings to calibrate and refine monitoring frameworks over time, integrating QA findings into policy evaluation and future decision-making processes.