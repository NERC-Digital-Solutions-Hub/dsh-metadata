# Mapping Quality Assurance Exercise

- Purpose: Assess the quality and consistency of digital habitat mapping in Countryside Survey 2007 by comparing surveyor data with a dedicated QA dataset using standardized methods.
- Scope: Field mapping in 2007 using a bespoke Surveyor software and a wiki-enabled QA workflow to ensure timely checks and uniform data capture.
- Team and setting: CEH Lancaster and partner institutions; QA teams conducted independent assessments across multiple 1km squares.

## Key Aims and Approaches

- Ensure data compatibility with previous approaches and enable rapid analysis within a geodatabase.
- Use digital mapping to reduce subjectivity, improve clarity of mapping and attributes, and enable early QC feedback.
- QA approaches employed:
  - 4.1 Direct comparison of aggregate areas/lengths/points for whole squares.
  - 4.2 Raster data comparisons (10 x 10 m sub-units per 1 km square; dominant Broad Habitat per unit).
  - 4.3 100-point grid analysis to assess concordance of Broad Habitats at a fixed resolution.
  - 4.4 Attribute comparison for areas, lines, and points via reference IDs.

## Extent and Field Coverage

- QA mapping covered 23 1-km squares; target exceeded previous QA efforts but some areas were inaccessible (refusals).
- QA squares intentionally represented diverse land classes to test surveyor performance and mapping consistency.

## Data and Analysis Foundations

- Data collected with standard Countryside Survey tablets; data uploaded to a geodatabase and cross-checked against QA data.
- Analyses spanned aggregate habitat extents, raster-level correspondence, point and linear feature congruence, and species attribute comparisons.

## Surveyor Efficiency and Data Capture

- Digital controls (mandatory fields, visit status, and wiki checks) improved data completeness and species reporting.
- Very small area not visited due to access issues (average around 0.4% in most squares); ownership/refusal factors accounted for.
- Species recording per area increased in 2007 (2.03 avg) compared with earlier years, reflecting enhanced data capture.

## 6. Results in Key Comparisons

- 6.1 Direct aggregate area comparisons
  - In 81% of squares, Broad Habitats (BH) were recorded by both CS and QA teams.
  - Mean differences for many BH categories were typically under 1–3.5%, with some habitats showing larger deviations and potential coding issues (e.g., Improved/Neutral Grassland, Dwarf Shrub Heath vs Blanket Bog, Urban vs grassland).
  - Notable issues discussed: Blanket Bog classification, upland habitat mosaics, and machair-related notes; training and key definition updates highlighted as avenues to reduce discrepancies.

- 6.2 Raster data comparisons
  - Overall raster agreement across squares averaged about 76%, with some squares much higher (e.g., 364, 488) and others lower (e.g., 261, 773).
  - Agreement by Broad Habitat varied by square; some BHs showed high concordance while others (e.g., Neutral vs Improved Grassland; urban vs grassland) exhibited more inconsistencies.
  - The 1,000-cell raster grid facilitated spatial and attribute-level cross-checks between CS and QA data.

- 6.3 100-point grid analysis
  - Concordance across squares generally strong, but some notable exceptions (e.g., square 773 only 19% concordance; 261 around 41%).
  - Overall concordance for Broad/Priority Habitats typically around 70–80% in many squares; some squares revealed mis-matches tied to habitat definitions and mosaics.

- 6.4 Polygon analysis of species attributes
  - Matching species between QA and CS polygons occurred in about 45% of matched polygons.
  - For polygons with matching species, 77% also had a matched Broad Habitat.
  - Species concordance overall around 40% for commonly recorded species (Lolium perenne, Calluna, Molinia, etc.), reflecting identification challenges and habitat-driven species selection differences.
  - Notable species-level patterns: dominant grasses in Improved Grassland more consistently matched; woody species and upland indicators showed greater divergence due to habitat complexity and mosaic mapping.

## 7. Linear Features Analysis

- 7.1 Direct comparison of aggregate linear features
  - Overall close agreement in total linear lengths per square across land-use themes (Banks, Fences, Forestry, etc.).
  - Some minor mismatches between related feature types (e.g., belts of trees vs woody features) but generally consistent-language usage between CS and QA.
- 7.2 Land-use theme consistency
  - High consistency in the major themes (with only small numbers of features being recorded by one party and not the other).
  - Slight potential confusion between forestry-related codes (FO, WNS, WUS), but no systematic problems observed.

## 8. Points Analysis

- 8.1 Point feature habitat codes
  - Point-level habitat codes showed high consistency between QA and CS point features.
  - Minor confusions occurred around woody/woodland coding in some cases, but overall alignment was strong.

## 9. Change Recording Assessment

- Change coding in 2007 benefited from digital inputs:
  - Change categories included Real Change, Error Change, and No Change.
  - An “error change” field helped flag and correct misclassifications against the previous dataset.
- Agreement on change coding between CS and QA was high for most broad habitats and linear/point features (with some complexity for habitat-level changes).
- The digital approach improved ability to record and verify new changes while also checking prior maps, though some surveyors required guidance to apply change coding consistently.

## Overall Conclusions and Implications for Analysts

- Digital mapping and QA processes substantially improved data quality, with high overall agreement between CS surveyors and QA assessments across multiple dimensions (area, raster, and linear/point features; with some habitat-specific challenges).
- Most discrepancies were tractable and often tied to:
  - Definition nuances in certain habitats (notably Blanket Bog, Neutral/Improved Grassland, and urban vs grassland allocations).
  - Mosaic or continuum mapping in upland areas, complicating precise cross-comparisons.
  - Habitat definitions and legacy coding for woodlands (Broadleaf vs Coniferous) and machair-related variability.
  - Species-level concordance being more variable due to dominance and identification issues.
- Recommendations for analysts:
  - Consider refining habitat definitions and allocation rules where consistent mismatches occur (e.g., Blanket Bog vs Dwarf Shrub Heath).
  - Use training and calibration exercises to reduce misclassification in mosaicked upland terrains.
  - Continue leveraging digital change recording and QA feedback loops to further enhance data integrity.
  - Explore targeted deep-dives on species-habitat relationships to improve concordance in polygonal species listings.
- Overall, the exercise demonstrates strong data governance and provides a framework for ongoing data quality improvement in environmental monitoring programs.