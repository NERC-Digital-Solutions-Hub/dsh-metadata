# Mapping Quality Assurance Exercise

- Overview
  - Evaluation of the 2007 Countryside Survey mapping using a digital, field-based approach to improve data quality, speed of analysis, and integration with national datasets.
  - Introduction of Surveyor software enabling in-field mapping with mandatory fields; data uploaded to an interactive wiki for early data checking; QA teams conducted independent quality assurance.

- Data and Methodology
  - Digital mapping in the field to reduce subjectivity and handwriting errors; standardized attributes and visit status layers.
  - QA approach included: 
    - Direct comparison of aggregate areas/lengths/points for 1 km squares.
    - Raster data comparisons: converting polygons to 10 x 10 m raster cells per square and assessing dominant Broad Habitat (BH).
    - 100-point grid analysis to assess concordance of BH mappings at a fixed resolution.
    - Attribute-level comparisons for areas, lines, and points using reference IDs.
  - Data governance and sharing: QA and CS data were aligned and integrated into a single geodatabase; unsurveyed and refused-access areas excluded from comparisons.

- QA Extent and Approach
  - QA mapping covered 23 1 km squares (target exceeded previously; access refusals limited the coverage).
  - Squares were selected to represent different land classes and locations across Great Britain; QA teams often mapped in squares differing from survey squares to broaden coverage.
  - Temporal alignment: QA teams visited squares concurrently with survey teams where possible to minimize vegetation changes.

- Analysis Methods
  - 4.1 Direct aggregate comparison: CS vs QA across square extents and broad habitat types.
  - 4.2 Raster data: 1 km squares subdivided into 10,000 cells; dominant BH per cell compared between datasets.
  - 4.3 100-point grid: positive concordance vs negative; evaluation across BH/PH and mosaics.
  - 4.4 Attribute comparisons: cross-check on species attributes within matched polygons using reference IDs.

- Surveyor Efficiency and Data Quality
  - Visit coverage: small proportion of land not visited on average (typical cases near zero or very small).
  - Mandatory fields improved data capture; more species recorded per area on average (increase observed in 2007).
  - Efficiency and data consistency: high alignment between QA and CS teams for many attributes, but some areas remained challenging due to habitat definitions and mosaics.

- Findings: Habitat and Land Cover Comparative Outcomes
  - Direct aggregate comparisons (Table 6.1):
    - 81% of squares recorded a BH in common by CS and QA.
    - Mean differences between QA and CS BH proportions typically under 3.5%; most BHs showed small differences, but notable variability existed for Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Urban, and sub-littoral habitats.
    - Some consistent directional biases observed (e.g., QA vs CS allocations for certain BHs), highlighting definitional and mapping challenges.
  - Raster data comparisons (Table 6.2):
    - Overall raster agreement across squares averaged around 76%, with notable outliers: squares 364 (98%), 261 (49%), 773 (23%).
    - Agreement by BH per square revealed varying levels of concordance; some BHs showed high agreement (e.g., Broadleaved Woodland, Urban, Sea), others low depending on square.
  - 100-point concordance (Table 6.3a/b):
    - Majority of squares showed good concordance; some squares had substantial mis-matches (e.g., squares 773 and 261).
    - Overall, the 100-point analysis indicated substantial agreement for many BH/PH but highlighted specific problem squares.
  - Key habitat issues discussed (6.3b):
    - Neutral vs Improved Grassland: overlapping species; misclassifications balanced between QA and CS.
    - Woodland classification: confusion around Broadleaf vs Coniferous definitions; mosaics of woodland types complicate strict binary allocations.
    - Upland mosaics: fine-scale heterogeneity caused mismatches when mosaics of BHs were disaggregated.
    - Urban misclassification: some Urban areas recorded as Improved Grassland; ongoing clarification needed.
    - Blanket Bog vs Dwarf Shrub Heath: major source of mismatches in certain squares (notably square 773); definitional refinements and training suggested.
  - Species-level polygon analysis (6.4):
    - 1,081 QA polygons and 998 CS polygons matched spatially; about 45% had at least one listed species in common.
    - Among matched polygons, species concordance was about 40%; higher for some habitats (woodlands, Improved Grassland) where dominant species are more recognizable; lower for Bracken and upland mosaic habitats.
  - Species-level within-sample results (6.5):
    - Across commonly recorded species, concordance varied by species; Lolium perenne showed relatively higher concordance (66%), others varied widely.
    - Overall pattern: species lists tended to be richer in QA data, reflecting broader observation in field, but cross-dataset matches remained moderate.

- Change Recording and Data Stewardship
  - 2007 introduced more detailed change codes to distinguish real changes, error changes, and no changes; included an "error change" field to correct previous mappings.
  - Change coding generally aligned between CS and QA for most broad habitats and features, though some discrepancies persisted.
  - Change assessment was more challenging for habitat-based changes than for linear or point features.

- Implications for Monitoring Frameworks
  - The digital approach enabled closer integration, faster QA, and clearer data governance, aligning with monitoring framework needs for timely, auditable environmental data.
  - The exercise exposed ongoing challenges that a monitoring framework must address:
    - Data standardization: habitat definitions (e.g., Blanket Bog, Coniferous vs Broadleaved Woodland) require clear, consistent guidelines and ongoing training.
    - Handling mosaic and transition habitats: mosaics complicate strict category allocations; frameworks should accommodate continuum mapping and cross-walking between habitat classes.
    - Metadata quality and data provenance: reliable metadata is essential to verify data quality and to support end-user confidence.
    - Data sharing and governance: balancing openness with protection of data; ensuring data are stored, versioned, and accessible with clear governance rules.
    - Training and capacity building: variability in surveyor QA alignment underscores the need for comprehensive training and calibration exercises.

- Challenges and Barriers (as highlighted by the authors)
  - Data availability and standard quality: issues with data at a good-enough standard and timely access.
  - Organizational silos: barriers to cross-department collaboration and data sharing.
  - Public sharing of datasets: governance constraints can limit data reuse.
  - Metadata inadequacy: poor metadata hampers verification and reuse.
  - Data transformation: data formats often require effortful transformation for use in QA and analysis.
  - Communicating complex findings: ensuring that QA results and habitat classifications are clearly interpretable for policy makers and stakeholders.
  - Governance processes: implementing robust data governance to ensure datasets meet standards and are maintained.

- Conclusions and Recommendations for Monitoring Framework Authors
  - Digital QA processes can substantially improve data quality and timeliness in monitoring frameworks, but require ongoing definitional clarity, standardized training, and robust metadata practices.
  - Expect and plan for mosaic and continuum habitats; avoid over-reliance on rigid binary classifications for complex landscapes.
  - Invest in cross-institution data governance to reduce silos and enable responsible data sharing with appropriate metadata standards.
  - Use multi-faceted QA methods (aggregate, raster, point-grid, and attribute analyses) to triangulate data quality and identify specific problem areas.
  - Reflect on change-recording protocols to differentiate real change from historic mapping errors; ensure field staff are trained in applying change codes consistently.