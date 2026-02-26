# Mapping Quality Assurance Exercise

- Purpose: Evaluate the quality and consistency of digital mapping data collected for Countryside Survey 2007 by comparing field survey data (CS) with QA assessments, using a digital geodatabase approach to enable rapid analysis and integration with other national datasets.
- Context: Transition from post-survey lab digitisation to in-field mapping with Surveyor software; mandatory fields and visit status layers; early data checks via an interactive wiki; QA teams conducted extensive validation to ensure data quality, consistency, and reliability across habitat types and spatial scales.

## Methodology and Scope

- Extent and sampling
  - QA covered 23 x 1 km squares, representing diverse land classes across GB; access refusals limited actual survey coverage; analyses focused on common surveyed areas.
- QA approaches
  - Direct comparison of aggregates (areas/lengths/points) per square.
  - Raster data comparisons: convert polygons to 10x10 m rasters, assign dominant Broad Habitat (BH), compare QA vs CS raster coverage.
  - 100-point grid analysis: overlay 10x10 points per square to assess point-level agreement on BH; calculated concordance and mis-matches.
  - Attribute-level analyses: used reference ID layers to compare species attributes for matched features.
- Data processing and tools
  - Data from CS tablets aggregated into a single geodatabase; unsurveyed and refused areas excluded prior analysis; SAS used for aggregate statistics; GIS-based masking for common areas.
- Change recording
  - Introduced change codes to capture Real change, Error Change, and No change; QA evaluated agreement on change coding by habitat, linear, and point features.

## Key Findings and Insights

- Overall agreement and data quality
  - Habitat presence agreement between CS and QA was high in most squares (about 81% Agreement for BH presence in the 1 km squares); mean differences in BH extent were generally under 3.5% for most habitats.
  - Raster comparisons showed strong concordance in many squares (example: 364, 488 with >90% agreement), but notable exceptions existed (e.g., squares 261 and 773 with lower agreement).
  - 100-point concordance was strong for many habitats but revealed selective mismatches in a subset of squares (e.g., 773 and 261 showed lower concordance).
- Notable habitat-specific issues
  - Blanket Bog: frequent mis-matches with Dwarf Shrub Heath, particularly in upland areas; definitional revisions during 2007 contributed to discrepancies (square 773 notably affected).
  - Upland mosaics: mosaicked mappings led to mismatches when disaggregating mosaics into constituent BHs; more pronounced in squares with complex mosaics (261, 765, 1113).
  - Grasslands and woods: inconsistencies between Neutral vs Improved Grassland; between Broadleaf vs Coniferous woodland; urban vs grassland classifications; machair-related issues on Scottish dunes noted.
  - Habitat definitions and field guidance: gaps in Woodland definitions (Coniferous/Broadleaved) and legacy allocation matrices from earlier surveys complicated direct comparisons.
- Species attributes
  - 45% of polygons with matched location contained at least one shared listed species between QA and CS datasets; species concordance was around 40% overall for commonly recorded species, typically higher for woodlands and Improved Grassland due to dominant species.
  - Common species (e.g., Lolium perenne) showed higher concordance than many less dominant taxa.
- Linears and points
  - Linear feature comparisons showed high consistency in land-use theme classification (e.g., fences vs walls, etc.), with few cases where QA and CS differed on same features.
  - Point features: high consistency in habitat codes; some confusion between woodland/forest codes likely due to legacy coding; veteran trees exhibited large disparities due to field instruction limits (up to two trees per species).
  - Aggregate point totals per square generally aligned, with minor differences across themes like Fo, IL, IW, ST, VT.
- Change recording and governance
  - Change coding generally aligned between CS and QA across broad habitats and linear features; some habitat-specific nuances remained (habitat-level change assessment more challenging than linear/point changes).
  - Digital workflow helped surveyors tidy and validate change in-field, though it added complexity; overall, the change-recording process functioned effectively.

## Implications for Data Leadership and Strategy

- Data quality and interoperability
  - Demonstrates that a digital, field-to-database workflow with structured QA can yield high-quality, comparable data across multiple organizations and datasets, suitable for integration with national-scale spatial datasets.
- Habitat definitions and standards
  - Highlights the need for clearer, continually refined habitat definitions (e.g., Blanket Bog, upland mosaics, Neutral vs Improved Grassland, woodland typology) to minimize cross-team discrepancies.
- Training and guidance
  - Training gaps (especially for complex upland and mosaic habitats) can lead to misclassifications; targeted training and updated field handbooks are beneficial.
- Metadata, lineage, and governance
  - The QA process reinforces the importance of metadata, change-tracking, and audit trails to support data provenance, reproducibility, and governance across partners.
- Data products and user needs
  - Findings support the feasibility of producing reliable, co-owned data products that policy colleagues and partners can use for analysis, reporting, and decision-making, with documented uncertainties and areas for improvement.

## Recommendations and Next Steps

- Refine habitat definitions and documentation
  - Address key ambiguities identified (e.g., Blanket Bog vs. Dwarf Shrub Heath, upland mosaics, machair-related vegetation) and harmonize definitions across datasets.
- Enhance training and standard operating procedures
  - Provide targeted training on challenging habitats and update field manuals to align with digital QA practices.
- Improve handling of mosaics and spatial heterogeneity
  - Develop methods to better map and compare mosaic landscapes, possibly by maintaining richer within-square habitat sub-codes or gradient-based classifications.
- Strengthen urban vs grassland distinctions
  - Clarify criteria for classifying urban areas versus Improved Grassland to reduce urban-overlap misclassifications.
- Expand QA coverage and targeted sampling
  - Increase QA square coverage for problem domains (certain squares with lower raster/point concordance) to better quantify uncertainty and guide refinements.
- Continue change management and data governance
  - Maintain robust change-coding workflows, ensure consistent application across habitats, and publish change provenance alongside habitat maps.

## Conclusion

- The 2007 Mapping Quality Assurance exercise demonstrates that a digitally-enabled QA framework, with standardized protocols and cross-organization collaboration, delivers robust, field-validated ecological mapping data with high overall agreement to the prior (1998) baselines and substantial compatibility with other national datasets. While notable discrepancies remain in select habitats and upland mosaics, the findings offer clear directions for refining habitat definitions, training, and data governance to further improve data quality and usefulness for data-driven decision-making.