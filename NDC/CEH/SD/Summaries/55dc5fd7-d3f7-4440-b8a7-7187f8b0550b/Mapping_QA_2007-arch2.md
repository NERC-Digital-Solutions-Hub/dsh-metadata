# Mapping Quality Assurance Exercise

- Objective: Assess quality and consistency of digital mapping data from Countryside Survey 2007 by comparing surveyors' field data with QA assessments using a geodatabase, standardized QA methods, and multiple analytical approaches.
- Context: Transition from post-survey lab digitisation to in-field digital mapping (Surveyor software) to reduce subjectivity, improve data clarity, and enable rapid QA and analysis.

## Methodology and Data Flow

- Digital field mapping:
  - Surveyors used Surveyor software with mandatory fields, prompts, and visit-status layers.
  - Data uploaded to an interactive wiki for early data checks; QA teams conducted field visits to ensure protocol adherence.
- QA design and scope:
  - QA covered 23 1-km squares (common with survey areas where access was allowed).
  - QA mapping largely occurred in different squares from plot/freshwater QA to avoid owner bias and to enable deeper QA of mapped data.
  - Data from QA and CS were aligned to common surveyed areas via masking; unsurveyed or refused areas were excluded from analysis.
- Analysis approaches:
  - 4.1 Direct comparison of aggregate areas/lengths/points for whole squares.
  - 4.2 Raster comparison: convert polygons to 10x10 m raster cells, assign dominant Broad Habitat, compare HQ vs QA across squares.
  - 4.3 100-point grid: overlay a 10x10 point grid per square to assess concordance of Broad Habitats at points.
  - 4.4 Attribute comparison: create reference ID layers to compare species attributes for matched polygons.

## Key Findings: Data Quality and Consistency

- Surveyor efficiency and data capture
  - Very small proportion of land areas not visited (average around 0.4% in QA squares); most areas visited.
  - Mandatory fields increased the number of species recorded per area compared with previous surveys.
- Overall agreement on habitat mapping (6.x series)
  - 6.1 Direct aggregate areas per square: 81% of squares had BH present recorded by both CS and QA; mean differences across BH types mostly under 3.5%, with most BHs showing differences <1–2%. Some issues noted for Improved grassland, Neutral vs Acid grassland, Dwarf Shrub Heath, Bog, Urban, and Sub-littoral sediment.
  - 6.2 Raster data: average agreement across squares ~76%; some squares very high (364, 488) and others lower (261, 773).
  - 6.3 100-point grid: concordance varied by square; generally good, but notable problems in squares 773 (low concordance) and 261 (moderate concordance).
  - 6.4 Polygon species attributes: of 1,081 QA polygons and 998 CS polygons, about 45% had at least one matching species in matched polygons; 77% of those also had matching Broad Habitat. Higher concordance for woodlands and Improved Grassland; lower for Bracken and upland mosaics due to intrinsic habitat complexity.
  - 6.5 Species-level concordance within matched polygons was around 40% for the most commonly recorded species, with QA often recording more species; Lolium perenne showed relatively higher concordance where dominant.
- Linear features and point features (7.x and 8.x)
  - 7.1 Linear features: high consistency in land-use theme assignments (e.g., fences vs walls; forestry belts vs WO). Some confusion between FO vs WNS/WUS, but overall strong alignment.
  - 8.1 Points: small differences in total points; veteran trees showed large discrepancy due to counting decisions (surveyors allowed multiple trees per species); overall high consistency in point feature habitat codes, with minor woodland-code confusion.
- Change recording (9.x)
  - Introduction of change coding (Real change, Error Change, No change) with the ability to flag and correct previous data.
  - Generally strong agreement between CS and QA on change coding across broad habitats and linear/point features; some challenges remained for habitat-change interpretation due to complexity of definitions and mosaics.
  - The digital workflow enabled in-field validation and updating of changes, albeit with a learning curve for surveyors.

## Notable Issues and Explanations

- Habitat definition challenges
  - Blanket Bog and its relation to Dwarf Shrub Heath caused notable mismatches, particularly in upland squares; evolving field handbook definitions were implemented for 2007, with ongoing work to refine definitions.
  - Woodland classification (Broadleaf vs Coniferous) sometimes blurred by legacy guidelines; most mismatches occurred in mosaics or where classification relied on indirect allocation.
- Upland mosaics
  - Large mosaics in upland squares (e.g., 261, 765, 1113) increased mismatches due to disaggregation of mosaics into Broad Habitats, illustrating difficulties mapping continuous habitat gradients.
- Localized or rare habitats
  - Anomalies like machair on Scottish dunes could affect recordings; often such habitats mapped within adjacent Broad Habitats (Neutral/Improved Grassland) rather than as their own BH, highlighting context-sensitive interpretation issues.
- Species-level concordance
  - Although many polygons had shared species, broad concordance of listed species was around 40%, reflecting differences in observed dominance, cover estimates, and the larger species set captured by QA.

## Conclusions and Implications for Practice

- The shift to digital mapping, real-time QA, and a structured QA framework substantially improved data quality and comparability with previous datasets.
- Most habitat allocations between CS and QA were consistent, with minor discrepancies explainable by habitat definitions, mosaics, and very localized landscape variation.
- The exercise highlights the need for ongoing refinement of habitat definitions, especially for Blanket Bog and woodland types, and continued training to reduce misclassification in complex mosaics.
- The methodology demonstrates robust, multi-scale QA capabilities (area, raster, point, and polygon analyses) that can be used to validate national-scale environmental monitoring datasets and support policy-relevant environmental health assessments.
- Data management implications:
  - QA data were stored in geodatabases and integrated with survey data; ongoing data integration and accessibility through portals/wiki support transparent scrutiny and broader reuse.
  - The 100-point, raster, and full-square comparison frameworks provide transparent benchmarks for monitoring data quality over time and for integrating with other national spatial datasets.