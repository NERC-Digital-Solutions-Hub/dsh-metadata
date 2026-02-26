# Mapping Quality Assurance Exercise

## Purpose and Context
- Evaluates the quality and consistency of digital mapping data from Countryside Survey 2007.
- Aims to produce high-quality, analysable data that can be integrated into a geodatabase and used alongside national spatial datasets.
- Implements a digital workflow (Surveyor software) to reduce interpretation errors and improve data clarity and attribute completeness.
- Uses an interactive wiki for early data checks and communication among surveyors, QA staff, and analysts.

## Methods: QA Process and Data Flow
- Field data collected with Surveyor software; mandatory feature fields and prompts; visit status tracking.
- Post-survey data uploaded to a wiki for rapid QA and guidance; QA teams conducted hands-on checks in the field.
- QA approached via three complementary methods:
  - Direct comparison of aggregated areas/lengths/points per 1 km square.
  - Raster comparison: convert polygons to 10 x 10 m raster cells to compare dominant Broad Habitats and spatial locations.
  - 100-point grid analysis to assess concordance of Broad Habitats at a fixed resolution.
- Additional analyses on attributes (areas, lines, points) with reference ID layers for feature-by-feature comparison.
- Surveyor efficiency assessed via metrics like visit rates, recorded species richness, and presence/absence of refused-access areas.

## Coverage and Sampling
- QA mapped 23 1 km squares (across various land classes), supplemented by cross-squares to ensure diverse representation.
- Comparisons were restricted to common surveyed areas to avoid bias from areas with access refusals.

## Analysis Techniques
- 4 main analyses:
  - 4.1 Direct square-level comparisons of aggregate habitat/linear/point data (exported to SAS for statistical summaries).
  - 4.2 Raster-based comparisons (dominant Broad Habitats per 10 x 10 m cell, with sampling grid).
  - 4.3 100-point concordance analysis for primary land cover codes and habitats.
  - 4.4 Polygon-level analysis of species attributes (dominant species per polygon) and habitat allocations.
- Additional analyses covered linear feature land-use themes, point and line feature habitat codes, and change recording consistency.

## Key Findings

- Habitat proportions and areas (6.1)
  - In 81% of squares, Broad Habitats were recorded by both CS and QA teams.
  - Mean differences for most Broad Habitats were typically under 1–3.5%, with small standard deviations; some habitats showed larger discrepancies (e.g., Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Urban).
  - Notable complexities around Blanket Bog definitions and upland mosaic habitats contributing to misclassifications (e.g., Dwarf Shrub Heath vs Blanket Bog, and machair-related anomalies).

- Raster data agreement (6.2)
  - Overall raster agreement averaged around 76%, with some squares very high (e.g., 364, 488) and others lower (e.g., 261, 773).
  - Agreement by Broad Habitat varied by square, highlighting where habitat coding diverged between teams.

- 100-point concordance (6.3)
  - Most squares showed good concordance, but several squares had notable mismatches (e.g., 773 only 19% concordance; 261 around 41%).

- Species attributes in polygons (6.4)
  - 45% of QA polygons had at least one listed species matching the matched CS polygon.
  - Concordance varied by Broad Habitat; highest for woodlands and Improved Grassland.
  - Species-level concordance overall around 40%; QA tended to record more species than CS.
  - For common species (e.g., Lolium perenne), concordance was higher (66%).

- Linear features (7.1)
  - Aggregate lengths per square showed minor differences; high consistency in land-use theme classifications (e.g., fences, walls, hedges).
  - Some confusions between closely related feature types (e.g., belts of trees vs woody linear features).

- Points data (8.1)
  - Overall small differences in total points per square; veteran trees showed the largest disparity due to field instruction limits (two relevant trees per species).

- Change recording (9)
  - Digital recording allowed more detailed change information (Real change, Error Change, No change).
  - Generally high agreement on change coding across Broad Habitats and linear features; some complexity remains for habitat-level change.

## Challenges and Observations
- Habitat definitions and key updates (e.g., Blanket Bog) impacted consistency; training and handbook revisions are important for reducing future misclassifications.
- Upland mosaics and mosaic-rich landscapes complicate direct one-to-one habitat matching between CS and QA data.
- Machair and specific regional habitats require localized considerations.
- Urban area recording ambiguities (e.g., amenity grass vs Improved Grassland) require clearer guidance.
- Species concordance is influenced by the dominance-driven selection of “dominant” species per polygon; broader species diversity in some habitats reduces match likelihood.

## Implications for Environment Monitoring Analysts
- Digital QA workflow substantially improves data quality and makes datasets more reusable for cross-dataset analysis.
- Overall agreement between QA and CS data is strong, but targeted improvements are needed for certain habitats, upland mosaics, and habitat definitions.
- The QA process provides actionable insights for standardizing habitat allocation, refining field protocols, and enabling reliable long-term trend analyses.
- The approach demonstrates how QA can support transparency, reproducibility, and data-sharing capabilities essential for environmental monitoring and policy scrutiny.

## Conclusions and Recommendations
- The digital QA framework enhanced data reliability and field-data integrity, enabling robust monitoring over time.
- Key areas for refinement include habitat definitions (notably Blanket Bog and conifer vs broadleaved woodland), training to reduce inter-operator variability, and improved handling of upland mosaics.
- Continued use of paired CS and QA analyses, with adjustments to key definitions and field-handbook guidance, will further increase reproducibility and data value.
- Emphasis should remain on making QA data and methods accessible to analysts, ensuring the long-term value and interoperability of environmental datasets.