# Mapping Quality Assurance Exercise

- Introduces digital field mapping for Countryside Survey 2007 using Surveyor software to map in the field, with QA to validate data quality across mapping, plots, and related datasets.
- Data were stored in a geodatabase and checked via an interactive wiki soon after collection, enabling early data validation and communication among surveyors and staff.
- QA employed multiple approaches to assess data quality and consistency across surveyors and QA teams, aiming to ensure data are suitable for fast analysis and integration with other national spatial datasets.

## Context and Objectives

- Move from post-survey digitisation of paper maps to in-field digital mapping to reduce interpretation errors and handwriting issues.
- Use QA to evaluate the mapping output against prior data (1998 baseline) and against independent QA collection across different squares, land classes, and habitat types.
- Assess mapping accuracy at multiple scales (aggregate habitat areas, rasterized species/habitat distribution, and 100-point samples) and validate attribute data (e.g., primary vs secondary attributes, dominant species).

## Digital Mapping and Data Architecture

- Deployment of Surveyor software with mandatory fields to standardize feature data and improve data quality.
- Immediate upload of field data to a wiki for early QA and guidance, enabling rapid feedback and issue resolution.
- QA teams conducted visits to survey teams to ensure protocol adherence and consistency across teams.
- Data were consolidated into a single geodatabase for cross-dataset comparisons (surveyors vs QA).

## QA Scope and Extent

- QA coverage: 23 x 1 km squares, representing diverse land classes across Great Britain; common areas were used where access was refused.
- QA was designed to parallel the survey, enabling direct comparisons between surveyors and QA across multiple data layers (areas, lines, points).

## Methodology

- 4.1 Direct comparison of aggregated areas/lengths/points per square; data exported to SAS to analyze by Square, Land Class, and Broad Habitat.
- 4.2 Raster data comparisons: polygons reclassified to 10,000 10x10 m cells per square; dominant Broad Habitat assigned per cell; analyzed with raster sampling.
- 4.3 100-point grid overlaid to assess concordance of Broad Habitats at ~1 ha resolution; positive/negative scoring of concordance per square.
- 4.4 Attribute-level analyses using reference IDs to compare species-related attributes for matched areas/lines/points.
- Overall, analyses explore agreement by habitat type, differences in patch-level vs mosaic mapping, and the impact of data structure (BH definitions, woodland classifications, etc.).

## Surveyor Efficiency

- Use of visit status layers was generally effective; very small percentage of land not visited (average around 0.4% in QA squares; often due to land access refusals).
- Mandatory fields increased the completeness of attribute data, notably the recording of dominant plant species per area, with a rise in species recorded per area over time.

## Key Findings by Analysis Type

- 6.1 Direct aggregate comparison
  - 81% of squares had the Broad Habitat (BH) present recorded by both CS and QA teams.
  - Mean differences in BH extent were generally under 3.5% across most habitats; some habitats showed larger differences (e.g., Improved/Neutral Grassland, Dwarf Shrub Heath, Bog).
  - Differences often reflect habitat definitions, mosaics, and classification boundaries; notable issues in upland/mosaic areas and with urban grassland coding.

- 6.2 Raster data comparisons
  - Overall raster agreement averaged around 76% across squares, with higher concordance in many squares (e.g., 364, 488) and notable low agreement in others (e.g., 261, 773).
  - Per-square, per-habitat agreement highlighted specific differences in Neutral vs Improved Grassland, Broadleaf vs Coniferous woodland, upland bogs, urban areas, and machair-related grasslands.

- 6.3 100-point concordance
  - Most squares showed good concordance; some squares displayed substantial mismatches (e.g., 773 with very low concordance, 261 with moderate).
  - The 100-point habitat matrix (BH/PH) indicated good overall alignment for many habitats but highlighted specific conflicts (e.g., Sand Dune/Strandline habitats, Blanket Bog vs Dwarf Shrub Heath, urban vs grassland overlaps).
  - Issues tied to landscape context (machair, upland bogs) and to habitat definitions and transition zones.

- 6.4 Polygon species attributes
  - 1081 QA polygons and 998 CS polygons matched spatially; only 45% had at least one species common to both polygons.
  - For habitat types, 77% of polygons with matching species also had matching Broad Habitat, but overall species concordance was about 40%.
  - Dominant species exhibited variable concordance; Lolium perenne showed comparatively higher agreement when present.
  - Indicates species-level concordance lags habitat-level concordance in mosaicked or diverse habitat areas; reflects differences in species lists and dominance decisions tied to habitat coding.

- 6.5 Species and habitat insights (implicit)
  - Species lists and habitat allocations are interrelated; discrepancies in habitat assignment can influence which species are recorded as dominant.
  - Training and experience (notably in upland squares with complex mosaics) affected consistency; improved guidelines for Blanket Bog and upland habitat definitions are recommended.

## Linear, Point, and Change Recording

- 7.x Linear features
  - High consistency in choosing land-use themes for linear features; small set of mismatches expected (e.g., fence vs wall).
  - Some potential confusion between belt-like forestry features (FO) vs woody linears (WNS, WUS), but overall alignment was strong.

- 8.x Points
  - Point feature analysis showed similar high consistency when reconciling QA and CS data, with the caveat that some point types (e.g., veteran trees) showed greater discrepancy due to interpretation and limited options per species.

- 9.x Change recording
  - Digital field recording enabled more detailed change classification: Real change, Error Change, No Change.
  - Some early survey confusion; overall change coding aligned well with QA for many broad habitats and linear/point features.
  - The change field supported data lineage and updates to previous maps, though complexity increased with habitat-level interpretation.

## Implications for Data Leaders

- Demonstrates a robust, multi-layer QA framework for large-scale, national spatial datasets, combining in-field digital mapping with independent QA checks.
- Highlights the value of:
  - In-field data capture with mandatory attributes to improve data completeness and consistency.
  - Real-time QA via a wiki and geodatabase integration to identify issues early.
  - Cross-scale quality assessments (aggregate, raster, 100-point) to surface both general reliability and localized problem areas.
  - Detailed change-tracking to manage data lineage and update previous datasets accurately.
- Key data governance considerations:
  - Need for standardized habitat definitions and clear criteria for ambiguous categories (e.g., Blanket Bog, Neutral vs Improved Grassland, Urban Grassland).
  - Better handling of mosaics and transition zones in upland and complex landscapes to reduce misclassification.
  - Ongoing training and handbook refinement to ensure consistent interpretation across survey teams and QA.
  - Documentation of data provenance, metadata quality, and cross-dataset compatibility to facilitate integration with other national datasets.
- Practical takeaways for future programs:
  - Maintain digital field tools with enforced metadata and prompts to minimize uncertainty.
  - Apply multi-method QA (direct, raster, 100-point) to capture both area- and location-based accuracy.
  - Use change recording to correct historical maps, ensuring data lineage and auditability.
  - Invest in targeted training for difficult habitats (e.g., Blanket Bog, high-midelity woodland classifications) and for mosaic landscapes.

## Conclusion

- The 2007 mapping QA exercise shows strong overall data quality and substantial alignment between surveyors and QA across multiple dimensions (BH extents, raster habitat distribution, linear and point features, and change recording).
- Some habitat-definition challenges persist, particularly in upland mosaics, Blanket Bog, machair-related grasslands, and urban-grassland distinctions, indicating a need for ongoing refinement of habitat keys, training, and consistency checks.
- The study provides a replicable QA framework and concrete metrics to guide data governance, data quality improvement, and scalable data management for data-led organizations.