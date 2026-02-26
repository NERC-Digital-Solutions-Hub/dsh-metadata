# Mapping Quality Assurance Exercise

- Aims and scope
  - Assess and compare mapping data collected in the 2007 Countryside Survey (CS) with QA assessments to evaluate data quality, consistency, and reliability across habitats, linear features, and points.
  - Use digital field mapping to reduce errors, enable rapid QA, and create a connected geodatabase for integration with national datasets.
  - Identify areas where discrepancies arise to inform definitions, training, and future survey methods.

- Context and QA approach
  - In 2007, field mapping shifted from post-survey digitising to in-field digital mapping using the Surveyor software with mandatory fields and prompts to reduce handwriting and interpretation errors.
  - An interactive wiki facilitated early data checks, while QA teams conducted visits to ensure adherence to protocols.
  - QA examined data at multiple scales and levels of attribute detail, from broad habitat extents to secondary attributes such as species.

- Extent and data workflow
  - QA covered 23 1-km squares, selected to represent land classes and locations across Great Britain; common surveyed areas were used to align QA and CS data due to access/refusal issues.
  - Data sources were uploaded into a single geodatabase; unsurveyed or refused areas were excluded from comparisons.
  - Both CS surveyor data and QA data were aligned to provide two comparable datasets (areas, lines, and points).

- Analysis methods
  - 4.1 Direct comparison of aggregates (areas/lengths/points) for entire squares using SAS.
  - 4.2 Raster comparison: convert polygons to 10,000 x 10 m2 cells per square; compare dominant Broad Habitats and locations; sample with a resolution grid.
  - 4.3 100-point grid: overlay 10x10 point grid per square to test concordance of Broad Habitats; compile concordance and discrepancy counts.
  - 4.4 Attribute analysis: match reference IDs to compare species attributes within matched polygons.
  - 5. Surveyor efficiency: evaluate use of visit-status layers, access refusals, and species recording activity.

- Key findings: habitat mapping and agreement
  - Direct comparison of aggregate broad habitats (BH) in square-scale data
    - In 81% of cases, both CS and QA recorded the same BH in a square.
    - Mean differences between CS and QA BH proportions were typically small: often less than 1% for many BHs; 1–2% for several others; up to around 3.5% for the remaining two BHs.
    - Notable potential issues flagged in certain BHs (e.g., Improved Grassland, Acid Grassland, Dwarf Shrub Heath, Bog, Urban, Sub-littoral sediment) indicating differences in allocation between CS and QA.
  - Raster data comparisons
    - Overall raster agreement across squares averaged around 76%, with some squares showing high concordance (e.g., 364, 488) and others much lower (e.g., 261, 773).
    - Agreement by BH varied by square; some squares showed strong matches across most BHs, while others exhibited substantial mismatches in particular habitats.
  - 100-point grid analysis
    - Concordance varied by square; generally high in many squares but some notable exceptions (e.g., 773 only 19% concordance; 261 around 41%).
    - The 100-point matrix highlighted that some habitat/matrix combinations had high agreement while others showed substantial mismatch, reflecting complexities in mosaicked upland areas and rare/localized habitats (e.g., machair, Blanket Bog, and certain dune habitats).
  - Habitat coding issues and interpretation
    - Some discrepancies arose from overlapping or transitioning habitat definitions (e.g., Neutral vs Improved Grassland; Broadleaf vs Coniferous woodland) and from how mosaic habitats were disaggregated for comparison.
    - Blanket Bog was particularly challenging due to evolving definitions; mis-matches often occurred with Dwarf Shrub Heath in upland squares. Training and clearer field guidance were identified as key areas for improvement.
  - Species attributes within polygons
    - 45% of QA polygons, when spatially matched with CS polygons, had at least one common species listed.
    - Among polygons with matched species, 77% also had matching Broad Habitats, suggesting species composition influences habitat allocation but is not uniformly predictable across habitat types.
    - Overall concordance for listed species within matched polygons was around 40%; species lists tended to be more divergent in more species-rich habitats.
    - Some species were more consistently recorded (e.g., Lolium perenne, Calluna vulgaris, Molinia caerulea) than others, reflecting identification ease and dominance, while many taxa showed substantial divergence between QA and CS records.
  - Points and linear features
    - Point-feature habitat codes showed high consistency between QA and CS; some minor divergences occurred in woodland/forest coding.
    - Linear features demonstrated high consistency in land-use theme classifications; few cases where QA recorded a feature that CS did not in the same location.
- Change coding and assessment
  - 2007 introduced more detailed change-coding (Real change, Error Change, No change) to capture updates and corrections to prior maps.
  - Overall, there was broad agreement between CS and QA on change coding for most habitat types and linear features; some discrepancies occurred for complex habitat categories (notably Blanket Bog and certain upland mosaics).
  - The digital workflow helped surveyors tidy data in the field and verify prior maps, though it added complexity to the process.
- Surveyor efficiency and data quality considerations
  - Not-visited areas were generally minimal (around 0.4% in most squares); refused access areas were more variable and could introduce sampling bias.
  - Mandatory attribute fields improved data completeness; increased recording of dominant species in many cases.
  - Training and experience influenced QA-CS concordance, particularly in challenging habitat types (e.g., Blanket Bog, upland mosaics, machair-like dune habitats).

- Implications for data quality and future work
  - The digital mapping and QA framework materially improved data clarity, traceability, and the ability to compare CS data with other national datasets.
  - While overall agreement is solid for many habitat classes and feature types, notable discrepancies in particular habitats and upland mosaics indicate a need for:
    - Clearer, more consistent definitions (especially Blanket Bog, dune/machair habitats, and woodland types).
    - Enhanced training for survey teams on problematic habitats and mosaic classifications.
    - Ongoing refinement of QA methods to better accommodate mosaic landscapes and to improve concordance for species lists.
  - The exercise demonstrates the value of in-field data capture, metadata-rich records, and cross-team verification to support reliable landscape-scale analyses.

- Conclusion
  - The 2007 Mapping Quality Assurance Exercise shows a high level of overall agreement between surveyors and QA assessments across habitats, lines, and points, with some habitat-specific discrepancies and challenges driven by complex mosaics and evolving habitat definitions.
  - The digital QA framework facilitated robust cross-validation, highlighted areas for definitional refinement, and provided actionable insights to improve future survey design, training, and data processing.