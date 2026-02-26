# Mapping Quality Assurance Exercise

- Overview and aims
  - Evaluates quality of Countryside Survey 2007 data, focusing on habitats and landscape features mapped digitally in the field.
  - Aims to ensure data are high-quality, quickly analysable, and compatible with national datasets via a geodatabase.
  - Digital mapping (Surveyor software) reduced interpretation subjectivity, improved data clarity, and enabled early data checks via an interactive wiki.
  - QA checks conducted by CEH staff and survey teams to validate protocols and data integrity; visit status and mandatory fields improved data capture.

- Methodology and scope
  - Extent: QA covered 23x1km squares across GB, with data masking to common surveyed areas when access was refused.
  - QA approaches (three core analyses):
    - 4.1 Direct comparisons of aggregate areas/lengths/points per square (surveyors vs QA).
    - 4.2 Raster data comparisons: converting polygons to 10x10 m raster cells, comparing dominant Broad Habitats within 1 km squares.
    - 4.3 100-point grid:, overlaid points to assess concordance of Broad/Priority Habitats; provides concordance scores and SDs.
    - 4.4 Attribute analysis: generated reference ID layers to compare species attributes within matched features.
  - Additional analyses encompassed surveyor efficiency (visit coverage, data completeness), and polygon-level species attributes.

- Key findings: habitat mapping and data concordance
  - Broad Habitats (BH) agreement
    - In about 81% of squares, BH presence was recorded by both CS and QA.
    - Mean differences in BH proportions between QA and CS data were generally small:
      - Most BHs had mean differences under 1–2%; a few reached up to about 3.5%.
    - Some BHs showed greater variability (SD > 5%), indicating potential differential allocation (e.g., Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Urban, and some upland habitats).
  - Raster data comparisons (4.2)
    - Overall raster agreement across squares averaged around 76%, with some squares very high (e.g., 364: 98%) and others lower (e.g., 261: 49%, 773: 23%).
    - Agreement by BH varied by square; a number of squares showed strong concordance, while a few exhibited notable discrepancies.
  - 100-point concordance (6.3)
    - Majority of squares showed good concordance between QA and CS BH mappings at the 100-point level.
    - Some notable exceptions: squares 773 and 261 had low concordance (19–41%), while others like 364, 359, 355, 434, 488 showed high concordance (around 80–95%).
    - Concordance and discrepancies discussed per BH/PH, highlighting issues in Neutral vs Improved Grasslands, Broadleaf vs Coniferous woodland, and upland mosaic mappings.
  - Polygon and species attributes (6.4)
    - Species concordance within spatially matched polygons was 45% (i.e., at least one matching species listed in both CS and QA polygons).
    - BH concordance within matched polygons was 77% (i.e., 77% of matched polygons also had matching BH).
    - Common species lists showed varying levels of agreement; Lolium perenne had higher concordance (66%), while many other species showed lower agreement due to dominance and identification challenges.
  - Points and linear features (7.1, 8.1)
    - Linear features: generally high consistency in land-use theme classifications (e.g., fences, walls, belts of trees) with few mismatches.
    - Some cross-category confusion between related feature types (e.g., FO belts vs WNS/WUS woody features) but overall high agreement.
    - Point features: most cases showed consistent habitat codes with CS data; minimal cases of mixed coding between woodland/forest categories.
  - Change recording (9)
    - Digital change-coding allowed more detailed categorisation (Real change, Error Change, No change).
    - Agreement on change coding between CS and QA was high across many broad habitats and linear/point features.
    - Complexity remained for habitat-based change due to interpretation of habitat boundaries.

- Notable issues and explanations
  - Habitat definitions and definitions revision
    - Blanket Bog vs Dwarf Shrub Heath: key definitions updated for 2007; main mis-matches arose where bog/heath boundaries blur, especially in upland areas (e.g., square 773).
  - Upland mosaics
    - Upland habitats mapped as mosaics across multiple BHs; disaggregation into component BHs could inflate mismatches.
  - Machair and regional variation
    - Scotland machair on sand dunes caused discrepancies due to localised presence; often classified within Neutral/Improved Grassland rather than a dedicated machair category.
  - Urban vs grassland classification
    - Unclear guidance on whether urban amenity areas should be recorded as Improved Grassland; ongoing analysis.
  - Woodland classification
    - Earlier handbooks used mixed allocation matrices; updated definitions and back-allocation issues affected woodland categories (Broadleaf vs Coniferous).

- Species-focused analysis (6.4)
  - 1,081 QA polygons and 998 CS polygons spatially matched.
  - 45% matched polygons had at least one common listed species; concordance varied by BH type.
  - Woodland and Improved Grassland showed higher species concordance; Bracken and upland mosaics showed lower concordance due to species diversity and habitat complexity.
  - Dominant species lists had about 40% concordance; some highly recognizable species (e.g., Lolium perenne) showed higher cross-survey concordance.

- Change recording: detail and consistency
  - Change coding generally aligned with QA protocols; most Broad Habitats showed strong agreement.
  - Some categories (e.g., Blanket Bog vs Dwarf Shrub Heath) highlighted the need for clearer habitat-specific change guidelines.
  - Digital capture enabled more precise change logging but added complexity for surveyors.

- Surveyor efficiency and data capture
  - Digital workflow improved data completeness and consistency through mandatory fields and real-time checks.
  - Not visited areas were low on average (around 0.4% of available survey area in many squares).
  - Visit status layers aided rapid QA feedback and data validation, reducing retrospective data corrections.

- Conclusions and implications for data leadership
  - The digital Surveyor-based mapping and integrated wiki QA framework substantially improved data quality control, traceability, and timeliness of QA feedback.
  - Across most habitat types, CS and QA data showed high concordance, indicating robust data collection and QA processes.
  - Key challenges remain in upland mosaic mapping, Blanket Bog vs Dwarf Shrub Heath definitions, and region-specific habitats (e.g., machair); ongoing refinement of habitat definitions and training is recommended.
  - The QA exercise demonstrates the value of:
    - An integrated geodatabase with standardized metadata and provenance.
    - In-field data validation and real-time change coding.
    - Cross-site QA to ensure consistency across networks and partners.
    - Documentation and training to minimize classification ambiguities (woodland types, grassland boundaries, urban vs grassland classification).
  - For data leaders, the report reinforces the importance of: governance around data standards, ongoing calibration of classification schemes, and investing in digital QA and metadata to support reliable, scalable data for policy and networked analyses.