# Mapping Quality Assurance Exercise

- Purpose and context
  - Evaluates the quality of digital mapping data from Countryside Survey 2007, focusing on habitats and landscape features.
  - Aims to make CS data compatible with prior approaches and national-scale spatial datasets via a geodatabase, enabling rapid analysis and cross-dataset investigations.
  - Tests efficacy of the digital mapping approach in reducing errors associated with post-survey interpretation of paper maps.

- Key methods and workflow
  - Field mapping with a purpose-built Surveyor software allowing in-field digitising with mandatory fields and prompts; reduced handwriting/ spelling issues and included visit-status layers.
  - Early data checks via an interactive wiki, enabling rapid QA discussions and guidance; QA teams conducted field visits to ensure protocol adherence.
  - QA coverage in 2007: mapped 23 1-km squares for QA of mapped data; analyses used common surveyed areas to compare with CS data.
  - QA approaches:
    - Direct comparison of aggregate areas/lengths/points by square, land class, and Broad Habitat (BH).
    - Raster data comparison: convert polygons to 10,000 10x10 m cells per square and sample with a grid to assess absolute BH areas and spatial locations.
    - 100-point grid comparison: overlay 10x10 point grid to assess concordance of BH mapping at approximate prior QA resolution.
    - Attribute-level analyses using reference IDs to compare species attributes across matched features.
  - Data handling: unsurveyed or refused areas excluded; data from CS and QA aligned via masks to enable comparability.

- Surveyor efficiency and data capture
  - High use of visit-status layers; minimal non-visited land (average around 0.4% in many squares; majority 0%).
  - Mandatory fields led to improved attribute recording and a higher number of recorded species per area, compared with earlier surveys.

- Major findings by data type and analysis

  - Overall habitat (BH) agreement and accuracy
    - 81% of squares had BH present recorded by both CS and QA teams.
    - Mean differences in BH proportions were generally small: under 1% for most BH codes; up to 2-3.5% for the rest.
    - Some BHs showed larger differences and potential issues, notably Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Urban, and certain upland habitats.
    - Key interpretive challenges included: overlap between Neutral and Improved Grassland; definition differences between Broadleaf and Coniferous woodland; mosaics in upland habitats leading to mismatches; urban areas sometimes misclassified as Improved Grassland; machair on sand dunes causing locality-specific anomalies.
    - Blanket Bog emerged as a particularly difficult habitat due to definitional changes and field-handbook updates; some misclassifications involved Dwarf Shrub Heath vs Blanket Bog in upland squares.

  - Raster data concordance
    - Average raster agreement across squares: about 76% (range across squares from high to notably lower in some cases).
    - Some squares showed very high concordance (e.g., 364, 488); others showed poor agreement (e.g., 261, 773).
    - By BH category, agreement varied, with higher concordance in many common habitats and weaker in a few problematic ones (e.g., where mosaics or rare habitats occur).

  - 100-point analysis (BH concordance)
    - Overall concordance across squares: 77% of polygons with matching BH at matched locations.
    - Some squares had markedly lower concordance (e.g., 773 at 19%, 261 at 41%).
    - The BH/PH matrix highlighted particular difficulties in certain habitat pairs (e.g., sand dune-related habitats, Blanket Bog vs Dwarf Shrub Heath, Urban vs grassland interactions).

  - Polygon-based species attributes
    - Approximately 45% of QA polygons had at least one species listed that matched the corresponding CS polygon.
    - Species concordance varied by BH type; woodlands and Improved Grassland tended to show higher species-match rates, while upland/mosaic habitats showed lower concordance.
    - A notable portion of polygons did not match BH despite shared species, reflecting the complexity of habitat allocation.

  - Species-level concordance for listed species
    - For commonly recorded species, concordance was mixed; Lolium perenne showed higher agreement (approx. 66% when comparing common species between QA and CS).

  - Point features and linear features
    - Point feature habitat codes: high consistency between QA and CS; occasional confusion between woodland/forest coding likely due to legacy coding practices.
    - Linear features: generally high consistency in land-use theme allocations (e.g., fences vs walls) with few mismatches; some confusion between forestry belts and woody features with natural vs non-natural shapes, but overall robust agreement.
    - Change coding for linear features: very high agreement; indicates reliable application of change/change-type field across QA and CS.

  - Change recording
    - 2007 introduced more detailed change coding: Real Change, Error Change, No Change.
    - Most habitat-change coding showed broad agreement between CS and QA, though some discrepancies remained, particularly for habitat-related changes.

- Notable themes and implications for environmental analytics
  - Digital mapping and QA significantly improve data transparency, verifiability, and early error detection, facilitating integration with other national datasets.
  - Most habitat categories show strong CS/QA agreement, enabling reliable time-series analyses and policy evaluation.
  - Key definitional ambiguities (e.g., Blanket Bog, urban/grassland boundaries, conifer vs broadleaf woodland) require ongoing clarification, training, and field handbook refinements.
  - Upland mosaics and rare habitats (e.g., machair) pose particular challenges for pixel-level or point-level comparisons; methodological choices (disaggregation of mosaics) can influence agreement metrics.
  - The QA framework demonstrated here supports both data quality assurance and ongoing methodological refinement for landscape-scale monitoring programs.

- Recommendations for future monitoring and QA
  - Clarify and harmonize habitat definitions, especially for Blanket Bog, urban grassland classifications, and woodland categories; update field handbooks accordingly.
  - Provide targeted training for survey teams to handle upland mosaics and habitat boundaries more consistently.
  - Continue using digital field data capture with integrated QA workflows (wiki-based checks, mandatory fields) to maintain high data integrity and facilitate data sharing.
  - Maintain multi-scale QA analyses (aggregate, raster, 100-point, and polygon-level) to identify and address systematic biases.
  - Consider refining handling of specific locality-dependent habitats (e.g., machair) and continue cross-dataset calibration to improve consistency across time.

- Bottom-line takeaway for analysts monitoring the environment
  - The Mapping Quality Assurance Exercise demonstrates that a digital, standardized QA process yields robust, comparable habitat data across surveys, supporting reliable environmental health assessments and policy performance monitoring over time. While most habitat classes align well between surveyors and QA, targeted refinements in definitions, training, and handling of complex mosaics are needed to further improve consistency and data utility for long-term monitoring and integration with other datasets.