# Mapping Quality Assurance Exercise

- Aims and scope
  - Evaluate quality and consistency of Countryside Survey 2007 mapping by comparing field surveyors’ data (CS) with QA assessments.
  - Use digital field mapping (Surveyor software) to reduce interpretation error and enable in-field QA via wiki and geodatabase.
  - Assess across multiple scales and feature types (areas, lines, points) and examine change recording.

- Key methods and workflow
  - Digital field mapping with Surveyor; mandatory attribute fields; ‘visit status’ layers to track coverage; in-field wiki checks and QA visits.
  - QA coverage: 23 one-kilometre squares, selected to represent land classes and locations; emphasis on common areas where access allowed.
  - Data handling: two comparable datasets created per square by masking unsurveyed/refused areas; data consolidated into a single geodatabase for analysis.
  - Analysis toolbox (4 main approaches):
    - Direct aggregation comparisons (CS vs QA) for square extents and attributes.
    - Raster comparisons: convert polygons to 10 x 10 m grid cells, compare dominant Broad Habitats per cell.
    - 100-point grid analysis: overlay 100 points per square to assess concordance of Broad Habitats at comparable resolution.
    - Polygon-level analysis of species attributes linked to mapped habitats.

- Surveyor efficiency and data quality indicators
  - Visit coverage: very small areas not visited (average around 0.4% in QA squares); most land accessible.
  - Data richness: mandatory fields led to more comprehensive recording of dominant species per area; increased species counts relative to earlier surveys.

- Direct comparisons of aggregated areas (6.x sections)
  - Broad Habitat (BH) agreement: 81% of squares showed CS and QA both recording the same BH presence.
  - Mean differences by BH generally small (often <1–3.5% of square area); some habitats showed larger SDs signaling potential allocation issues (e.g., Improved/Neutral Grasslands, Dwarf Shrub Heath, Bog, Urban).
  - Noted areas for more scrutiny: Blanket Bog (definitions revised in 2007), upland mosaic mappings, and distinctions between Broadleaf vs Coniferous woodland.

- Raster data comparisons (6.2)
  - Overall raster agreement across squares averaged around 76%, with variability by square.
  - High concordance in many squares (e.g., 364: ~98%, 488: ~94%), but notable lower agreement in others (e.g., 261: ~49%, 773: ~23%).
  - Table-level details show differences in specific BHs driving misalignment; results suggest raster method captures spatial patterns but is sensitive to habitat coding decisions.

- 100-point grid comparisons (6.3)
  - Concordance across 100-point samples averaged about 76.8% overall.
  - Some squares showed strong concordance (e.g., 364: ~95.7%), others substantial mismatches (e.g., 261: ~41%, 773: ~19%).
  - Result indicates good general alignment but concrete mis-matches in certain squares and habitat combinations.

- Polygon species attributes (6.4)
  - Matched polygons (CS vs QA) after spatial alignment: 45% of QA polygons had at least one listed species present in the matched CS polygon.
  - Species concordance varied by BH type; improved grassland and woodlands tended to show higher matching of listed species.
  - Overall species concordance within spatially matched polygons ~40% for the most commonly recorded species; QA tended to record more species than CS.
  - Notable species-level findings: Lolium perenne and other common grasses showed higher concordance; many woodland species showed substantial matches, but mosaics (polygons spanning multiple BHs) complicated comparisons.

- Linear features (7.1)
  - High consistency in land-use themes between QA and CS for linears; generally small numbers of features recorded by QA not present in CS (expected discrepancies in feature type naming e.g., FO vs WNS/WUS).
  - Some confusion between certain forestry-related categories, but overall strong alignment.

- Points (8.1)
  - Point feature analysis showed generally good agreement in habitat codes between QA and CS point data after buffering/overlay.
  - Veteran trees displayed the greatest disparity due to field instructions limiting to a small number of trees, highlighting sampling differences for that category.
  - Point feature habitat coding largely aligned across the two datasets with minor inconsistencies.

- Change recording assessment (9)
  - Change coding (areas, lines, points) largely aligned between CS and QA survey teams (high agreement for many BHs and feature types).
  - 9.1 Broad Habitats: substantial agreement, but some mismatches tied to habitat overlaps and evolving habitat definitions (e.g., Blanket Bog vs Dwarf Shrub Heath).
  - 9.2 Linear features: very high agreement on change coding between teams.
  - 9.3 Point features: strong agreement on change coding; some complexities remain for habitat-based change assessment.
  - Digital recording facilitated better documentation of change types (Real Change, Error Change, No Change) but required careful interpretation and training; overall a positive effect on data maintenance.

- Notable challenges and interpretations
  - Habitat definitions and mapping boundaries: Blanket Bog and other upland habitats posed definitional challenges, causing mismatches between CS and QA.
  - Woodland classification: ambiguity in broad vs coniferous woodland definitions; the 2007 field handbook revisions highlighted the need for consistent application and potential reallocation in future surveys.
  - Mosaic mappings in uplands: mosaics of BHs complicate one-to-one BH allocations when comparing CS and QA; disaggregation into components can introduce mismatches.
  - Machair on Scottish dunes (neutral vs improved grassland) illustrates location-specific habitat variability and how localized special cases affect cross-square comparisons.
  - Change assessment relies on consistent interpretation of prior maps and field observations; ongoing refinement of change coding is needed to maximize accuracy.

- End-of-document conclusions (implications for analysts)
  - Overall, the 2007 QA exercise shows substantial agreement between QA and CS data across habitats, linear features, and points, with robust use of digital data collection enhancing data quality and traceability.
  - Remaining discrepancies are largely explainable by definitional nuances, mosaic landscapes, and local habitat peculiarities; targeted training and clearer definitions are recommended for future surveys.
  - The project demonstrates the value of multi-scale QA (square-level, raster, 100-point grids, polygons) for diagnosing data quality and guiding improvements in habitat classification and mapping workflows.
  - The QA process provides a framework for making CS data more discoverable and usable, with transparent metadata and versioning to support cross-dataset analyses.