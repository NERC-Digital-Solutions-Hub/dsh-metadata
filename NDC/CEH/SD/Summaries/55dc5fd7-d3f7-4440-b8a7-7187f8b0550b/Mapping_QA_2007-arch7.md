# Mapping Quality Assurance Exercise

- Purpose and context
  - 2007 Countryside Survey aimed to produce high-quality habitat/landscape data compatible with national spatial datasets in a geodatabase for rapid analysis.
  - Shift to digital mapping in the field using Surveyor software to reduce interpretation errors and avoid post-survey digitisation.
  - QA integrated early via a wiki for in-field data checks; QA teams visited survey teams to ensure protocol adherence.

- Data collection and workflow
  - Surveyors mapped in the field with mandatory fields and prompts; visit status layers helped track visited/unvisited features.
  - Data uploaded to an interactive wiki for early office-based data checks and guidance.
  - QA compared surveyor data with QA datasets using multiple digital approaches; analyses covered areas, lines, points and attributes.

- Extent and sampling
  - QA mapped 23 1km squares, selected to cover land classes and locations across Great Britain; access refusals noted.
  - Analyses focused on common surveyed areas between QA and survey data, excluding unsurveyed/refused areas.

- Analytical approaches (section 4)
  - 4.1 Direct comparisons of aggregate areas/lengths/points per square.
  - 4.2 Raster data comparisons: polygons converted to 10x10 m rasters (10,000 cells per 1km square); dominant Broad Habitat assigned for comparison; sampling via resolution grids.
  - 4.3 100-point grid: overlaid points to assess concordance of Broad Habitats; positive/negative scoring per square.
  - 4.4 Attribute analysis: reference ID layers enabled cross-checks of species attributes for matched features.

- Surveyor efficiency and data quality (sections 5–6)
  - Efficiency and data completeness improved by digital system; very small areas not visited (average ~0.4%, often due to access issues).
  - Mandatory fields increased species data capture; more species recorded per area than in earlier surveys.
  - Direct comparisons (6.1): most Broad Habitats showed minimal differences between CS (surveyors) and QA; 81% agreement on BH presence within a square; mean differences for many BHs typically <1–3.5% of area.
  - Notable discrepancy areas: Improved/Neutral Grassland overlap; Broadleaf vs Coniferous woodland definitions; upland habitat mosaics; urban vs grassland allocations; machair on Scottish dunes; Blanket Bog definitions (linked to 2007 field handbook revisions).
  - Raster comparisons (6.2): overall raster agreement averaged around 76%, with some squares high (e.g., 364, 488) and others lower (e.g., 261, 773).
  - 100-point Concordance (6.3): good concordance for many squares; some squares showed substantial mismatches (e.g., 773, 261).
  - Species and polygon analyses (6.4):
    - 45% of QA polygons matched a CS polygon for listed species; species concordance varied by habitat type.
    - Among matched polygons, 77% also had matching Broad Habitat; species concordance around 40% overall.
    - Lolium perenne and other common species showed varying levels of agreement, with higher concordance for easily identifiable, dominant species.

- Linear features and points analyses (sections 7–8)
  - 7.1 Linear features: high consistency in land-use themes for lines; CS and QA generally align on most feature types; some ambiguity between belts of trees (FO) and other woody features (WNS/WUS).
  - 7.2 Land-use themes for linear features show strong agreement; few cases where QA captured a feature CS did not.
  - 8.1 Points: overall small differences in total points per square; most point features aligned with similar land-use themes; veteran trees showed greatest discrepancy due to field-choice limitations.

- Change recording (section 9)
  - 2007 introduced more detailed change codes: Real change, Error Change, No change.
  - Change field analysis (Tables 9.1–9.3) shows broad agreement between CS and QA across habitat types, linear features, and point features, though change assessment remains challenging in habitat-rich mosaics.
  - Digital workflow enabled surveyors to update/change data in-field; overall change coding aligned with protocols, with some nuances in complex habitat contexts.

- Key findings and implications for GIS practice
  - Digital mapping markedly improved data quality control, timeliness, and consistency with national datasets.
  - High overall agreement between surveyors and QA for many habitat classes and linear/point features, validating the in-field Surveyor/QA workflow.
  - The largest definitional challenges relate to Blanket Bog, upland habitat mosaics, and the overlap between Neutral/Improved Grassland and between Broadleaf/Coniferous woodland definitions.
  - Training and experience significantly influence land-cover classification in complex habitats; targeted guidance on habitat definitions is recommended.
  - 100-point and raster concordance analyses provide valuable diagnostics to identify and investigate specific squares with mis-matches, guiding future QA focus and habitat-definition refinement.
  - Change recording in a digital environment supports clearer data provenance and updating previous data where necessary.

- Relevance for GIS specialists
  - Demonstrates effective integration of field data collection, geodatabase management, and QA analytics to produce reliable map-based data products.
  - Validates the use of multi-scale QA approaches (per-square, raster, and point-grid) to assess both extent and spatial accuracy.
  - Highlights practical considerations when reconciling habitat classifications across teams, including the importance of clear definitions, training, and documentation.
  - Provides a framework for ongoing QA in future GIS-enabled habitat surveys, including change tracking, data integrity checks, and cross-dataset compatibility with national datasets.