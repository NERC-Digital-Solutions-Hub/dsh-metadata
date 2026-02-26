# Mapping Quality Assurance Exercise

- Purpose and context
  - 2007 Countryside Survey aimed to produce high-quality, GIS-ready data on habitats and landscape features, compatible with prior approaches.
  - Digital mapping in the field with Surveyor software reduced interpretation and handwriting errors; mandatory fields and visit-status layers aided data completeness.
  - Data uploaded to an interactive wiki for early QA; QA teams conducted field visits to ensure protocol adherence.

- Data workflow and QA methods
  - Outputs were transformed into a geodatabase to enable cross-dataset analysis and national-scale comparisons.
  - QA compared surveyor data (CS) with QA datasets across multiple scales and methods:
    - Direct comparison of aggregate areas/lengths/points per 1km square.
    - Raster comparison by converting polygons to 10 x 10 m cells (dominant Broad Habitat per cell) and sampling on a grid.
    - 100-point grid analysis to assess concordance of Broad Habitats at a fixed spatial resolution.
    - Polygon-level analysis of species attributes (dominant species within polygons) and matched habitat codes.
  - For linear and point features, data were spatially joined or buffered to enable robust comparisons.
  - Common surveyed areas were aligned using masks to ensure comparability; some areas were excluded due to access refusals.

- Key results and findings
  - Overall QA vs CS agreement
    - 81% of squares had the Broad Habitat (BH) in common between CS and QA data.
    - Differences in BH proportions between CS and QA were generally small; many BHs showed mean differences under 1–3.5% with relatively small standard deviations, indicating broadly similar classifications.
    - Some BHs showed larger discrepancies and higher variability, highlighting potential issues in coding certain habitats (e.g., Improved grassland vs Neutral grassland, Dwarf Shrub Heath vs Bog, and Blanket Bog in upland areas).
    - Specific habitat definition challenges included Blanket Bog terminology and the boundary between Dwarf Shrub Heath and Blanket Bog in some squares.
  - Raster data comparisons
    - Average raster agreement across squares varied; many squares achieved high concordance (e.g., 364, 488) but some performed poorly (e.g., 261, 773).
    - Overall, many BHs showed strong agreement, but discrepancies highlighted where habitat boundaries or mosaic classifications occurred.
  - 100-point analysis
    - Concordance between QA and CS across 100 points was generally high (typical squares around 70–90% concordance), with notable exceptions (e.g., squares 773 and 261 showing lower concordance).
    - The 100-point matrix revealed detailed agreement patterns among BHs and highlighted specific habitat-code confusion areas.
  - Species attributes within polygons
    - About 45% of QA polygons contained at least one species match with the corresponding CS polygon.
    - Of polygons with matching species, 77% also had a matching BH, suggesting species composition partly aligned with habitat classification but with notable divergences.
    - Species concordance overall around 40% for commonly recorded species; variability linked to habitat type (woodlands and Improved Grassland showed higher concordance).
  - Linear features and point features
    - Linear features showed strong consistency in land-use theme classifications between QA and CS, with relatively few mismatches (e.g., FO vs WNS/WUS were potential confusion points but overall low).
    - Aggregate lengths of linear features generally matched closely between datasets; some differences occurred but followed expected field-mapping variability.
    - Points: total counts and land-use distribution were broadly aligned; veteran trees showed the largest disparity between CS and QA in point data.
    - Point habitat codes were generally consistent between QA and CS; some occasional confusion between woodland/forest coding.
  - Change recording
    - In 2007, change coding included Real change, Error Change, and No change, with an additional error-change field to update mistakes from earlier maps.
    - The majority of change coding aligned between CS and QA, though some habitat-dependent discrepancies existed (e.g., between certain BHs where change interpretation is nuanced).
    - The digital workflow facilitated in-field change coding and subsequent verification, though it added complexity for surveyors.
  - Notable issues and interpretations
    - Upland mosaics: mapping mosaics of multiple BHs in upland squares increased mismatch potential when disaggregated into component BHs.
    - Blanket Bog: persistent definitional challenges between field keys and QA interpretations; significant in squares like 773 and 991/1034.
    - Machair on certain dunes created localized anomalies where Neutral vs Improved Grassland boundaries were affected.
    - Urban vs grassland distinctions occasionally lacked clarity in field handbooks, suggesting a need for clearer guidance on Amenity Grassland vs Improved Grassland classifications.

- Data quality implications for Data Support
  - Digital QA enables robust, multi-scale validation and supports “self-serve” data products by end users with confidence in HS/broad habitat classifications.
  - High overall agreement supports the viability of integrating CS and QA datasets for landscape-scale analyses.
  - Identified gaps (Blanket Bog definitions, upland mosaics, machair, urban-grassland ambiguities) provide concrete targets for refinement of definitions and training.

- Practical outcomes and recommendations
  - Continued refinement of habitat definitions, particularly Blanket Bog, Broadleaf vs Coniferous woodland, Neutral vs Improved Grassland, and urban grassland classifications.
  - Greater emphasis on training and experience in upland habitat interpretation to reduce mosaic-related mismatches.
  - Maintain digital change-coding workflow, while simplifying guidance to minimize confusion and improve consistency in future surveys.
  - Consider localized, square-specific calibration when mosaicked or rare habitats (e.g., machair) are present to prevent bias in broad-habitat allocation.
  - Leverage the geodatabase and wiki-based QA artifacts to build repeatable QA pipelines and dashboards for ongoing data quality monitoring.

- Data products and methodological notes
  - A geodatabase was produced to enable cross-dataset analyses and integration with national-scale spatial datasets.
  - QA outputs encompassed aggregated statistics, raster concordance metrics, 100-point concordance, species-polygon matching statistics, linear and point feature comparisons, and change-coding assessments.
  - The documentation highlights the value of early QA feedback and iterative refinement of data collection and habitat coding protocols.