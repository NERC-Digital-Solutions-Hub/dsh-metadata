# Mapping Quality Assurance Exercise

- Purpose: Report on 2007 Countryside Survey digital mapping QA to ensure high-quality, analysis-friendly habitat data compatible with national spatial datasets (geodatabase) and to explore data quality across multiple scales and feature types.

## Methods and Workflow

- Digital mapping in the field using Surveyor software with mandatory fields, prompts, and visit-status tracking to reduce interpretation subjectivity and improve data clarity.
- Early QA via an interactive wiki for data checks; QA teams conducted field visits to ensure protocol adherence.
- Data uploaded to a geodatabase; unsurveyed and refused areas excluded prior analysis.
- QA compared surveyor data (CS) with QA data using multiple methods (aggregate areas, raster, 100-point grid, and attribute comparisons).
- Analyses applied to areas, lines, and points; used reference IDs to align datasets and enable attribute comparisons.
- 2007 QA in 23 1-km squares; squares chosen by land class and location to cover GB diversity; field timing aligned to minimize vegetation change.

## Data Processing and Alignment

- Two comparable datasets created for each square: common surveyed areas between CS and QA, aligned via mask overlays.
- Focus on habitat categories (Broad Habitats, BH) and higher-level attributes; included dominant species where recorded.
- Used rasterization (10,000 cells per 1-km square, 10 x 10 m cells) to compare absolute amounts and spatial locations of Broad Habitats.
- 100-point grid analyses overlayed on squares to assess spatial concordance of BH mappings.

## Key Analysis Approaches

- 4.1 Direct comparison of aggregate areas/lengths/points per square (CS vs QA).
- 4.2 Raster data comparisons (dominant BH per 10 x 10 m cell; grid-based sampling).
- 4.3 100-point grid analysis for BH concordance at ~100-point resolution.
- 4.4 Attribute analyses (reference IDs and species attributes) for areas, lines, and points.
- 7.1 Linear features analysis using buffers to compare land-use themes between QA and CS.
- 8.1 Points analysis (buffering points to compare habitat codes with CS points).
- 9 Change recording: digital change codes (Real change, Error change, No change) and agreement between CS and QA on change assignments.

## Major Findings

- Overall habitat mapping agreement
  - 81% of squares showed CS and QA both recording the same Broad Habitat in at least part of the square.
  - Mean differences in BH extent between CS and QA typically under 1–3.5% across many BH types; some habitats showed larger SDs indicating potential differential allocation (e.g., Improved/Acid Grassland, Dwarf Shrub Heath, Bog, Urban).
  - Notable hotspot disagreements linked to Blanket Bog vs Dwarf Shrub Heath in upland contexts and to Scottish machair (neutral vs improved grassland definitions).
- Raster data concordance
  - Average overall agreement across squares: 76%, with higher concordance in some squares (e.g., 364, 488) and notably lower in others (e.g., 261, 773).
- 100-point grid concordance
  - Generally good concordance across squares; however, some squares showed substantial mismatches (e.g., 773 with low concordance; 261 and 355/359 showing issues).
- Habitat vs species attributes
  - 45% of polygons with matched location contained at least one matching listed species between QA and CS polygons.
  - Species concordance overall around 40% for commonly recorded species; Improved Grassland and woodlands showed higher concordance due to dominant species; Bracken showed lower concordance due to sensitivity to threshold/categorization.
  - For matched polygons, 77% had matching Broad Habitat as well as species lists.
- Points and linear features
  - Point features: high agreement in habitat codes for points; some minor woodland-code confusion.
  - Linear features: high consistency in land-use themes; robust across most categories; minor confusion between certain forestry/woody-category codes (FO vs WNS/WUS) but overall strong agreement.
- Change recording
  - Digital change field generally consistent with QA; most habitat change assessments aligned with protocols, though some surveyors initially struggled with the complexity of change coding.
  - Change coding allowed updating previous maps and provided a mechanism for error-correction in conjunction with new data.

## Notable Challenges and Interpretations

- Definitions and classification
  - Woodland definitions and the 80% coniferous cover threshold caused some misclassifications between Broadleaf and Coniferous woodland.
  - Blanket Bog: revised field-key descriptions and debates around bog vs wet heath, especially in upland areas; mismatches clustered in squares with mosaics or complex peatland structures.
- Upland mosaics
  - Many upland squares contained mosaics of multiple BHs; disaggregation into component BHs could create mismatches when like BHs occurred within a mosaic.
- Scotland-specific habitats
  - Machair habitats on Scottish dunes caused inconsistencies due to their hybrid nature with Neutral/Improved Grassland classifications.
- Data standards and training
  - Training and experience strongly influenced consistency, particularly for complex habitats and mosaicked landscapes.
- Data scale and resolution
  - Differences between 1-km square-level summaries and high-resolution 10 x 10 m rasters revealed scale-related discrepancies that require careful interpretation in GIS applications.

## Implications for GIS Practice

- Digital workflow benefits
  - In-field data capture with mandatory fields reduces handwriting/entry issues; real-time QA via wiki supports early issue detection.
  - Immediate final data (no prolonged post-processing digitisation) improves data timeliness and consistency for geodatabases.
- Data quality and standards
  - Need for ongoing refinement of habitat definitions (especially for Blanket Bog, upland mosaics, and woodland classification) to minimize cross-team misclassification.
  - Consistency in handling refused access and the effect on area calculations; use of masks to ensure fair comparisons.
- Data integration and analysis
  - Rasterization and 100-point sampling are useful for QA assessments, but care must be taken with mosaics and scale to avoid over-interpreting minor differences.
  - Integrating species attributes with BH mappings remains challenging; results suggest focusing on dominant species patterns and standardized vocabularies.
- Training and resource considerations
  - Enhanced training for field teams on complex habitat keys, especially upland and peatland systems, will reduce mismatches.
  - Clear guidance to distinguish urban vs. improved grassland and to correctly classify coniferous vs broadleaved woodlands.

## Conclusions

- The 2007 Mapping Quality Assurance Exercise demonstrates substantial alignment between field surveyors and QA assessments using a fully digital GIS workflow.
- High levels of concordance across many habitat types and feature classes, with meaningful improvements over previous paper-based approaches.
- Remaining discrepancies are concentrated in complex upland mosaics, Scottish peatland/bog classifications, and Scotland-specific habitats, highlighting areas for definitional refinement and targeted training.
- Overall, the digital approach provides robust, analysable geospatial data suitable for integration with national datasets, while also offering actionable feedback to improve data standards, classification schemes, and future survey design.