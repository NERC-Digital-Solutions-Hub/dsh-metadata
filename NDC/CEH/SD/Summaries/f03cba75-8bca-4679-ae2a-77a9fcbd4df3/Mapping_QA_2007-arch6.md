# Mapping Quality Assurance Exercise

## Aim and scope
- Assess quality of 2007 Countryside Survey habitat mapping using digital field mapping (Surveyor software) and early QA workflows.
- Produce a geodatabase enabling integration with national spatial datasets; reduce post-survey interpretation errors.
- Compare surveyor outputs with QA assessments to evaluate accuracy, consistency, and data product usability.

## Data, tools and workflow
- Digital field mapping via Surveyor with mandatory fields and visit-status layers; hand-written/digitisation errors eliminated.
- Early data checks via an interactive wiki used by surveyors and QA staff; QA teams visited survey teams to ensure protocol compliance.
- QA approaches involved:
  - 4. Direct comparison of aggregate areas/lengths/points per 1km square.
  - 4.2 Raster comparisons: transform polygons to 10x10 m raster cells, compare Broad Habitats across squares.
  - 4.3 100-point grid analyses: evaluate geographic concordance of Broad Habitats at ~100 locations per square.
  - 4.4 Attribute-level comparisons for areas, lines, and points (reference ID matching and species attributes).
- Coverage: QA exercised 23 1km squares; common survey areas masked to allow comparability.
- Outputs included SAS analyses, raster layers, and 100-point comparisons to quantify agreement and differences.

## Key methodological highlights
- Direct aggregate comparisons: proportions of Broad Habitats (BH) per square; assessment of primary attributes across features (areas, lines, points).
- Raster-based comparisons: measure absolute and spatial agreement of BH occupancy at 10x10 m resolution; quantify geographic concordance.
- 100-point analysis: per-square concordance scores for BH, highlighting where matching occurred or failed.
- Attribute comparisons: reference-ID-based matching to compare species attributes between CS and QA datasets.
- Linears and points: separate treatment due to scale and mapping differences; linear features buffered for comparison; point features buffered similarly for habitat codes.

## Main findings

### Overall data quality and consistency
- High overall agreement between CS surveyors and QA assessments for many habitat types and attributes.
- The digital workflow enabled more complete attribute recording (dominant species per area) and reduced missing data.

### Habitat-level agreement
- Direct square-level comparisons: in many habitats, differences in BH extent between CS and QA were small (often under 1–3%), but variability existed across habitat types.
- 100-point analysis: generally high concordance across squares, with a few notable exceptions (e.g., square 773 showed very low concordance; square 261 also relatively low).
- Raster-based BH concordance across squares varied widely by square:
  - High concordance (e.g., around 90–98% in several squares such as 364, 488, 355, 359, 1260).
  - Moderate to low concordance in others (e.g., squares 773, 261, 935, 1039, 434).
- Notable habitat-specific challenges:
  - Neutral vs Improved Grassland: overlap in species and classification led to contested allocations in some squares.
  - Broadleaf vs Coniferous Woodland: occasional misclassification; historic use of woodland codes contributed to some confusion.
  - Upland mosaics: mapping mosaics of multiple BHs caused mismatches when disaggregated to component BHs.
  - Blanket Bog vs Dwarf Shrub Heath: definitional debates and evolving field handbook revisions affected consistency, especially in certain Scottish squares (e.g., square 773) and upland squares (991, 1034).

### Species and vegetation attributes
- Polygon-level species concordance: about 45% of QA polygons had at least one listed species matching within the location-matched CS polygon; higher concordance for woodlands and Improved Grassland.
- Species-level concordance varied by taxa; Lolium perenne showed higher agreement, reflecting ease of identification and dominance in swards.
- Overall, species concordance lower than habitat concordance, reflecting broader biodiversity variation and the influence of habitat classification on dominant species choice.

### Change recording
- Change coding (Real change, Error change, No change) generally aligned between CS and QA for most habitat types and features.
- Change assessment was complex, particularly for habitat-based changes; error-change fields and field guidance helped, but some surveyors struggled early in the process.
- Change coding was most consistent for linear and point features, with greater complexity and variability in habitat-based changes.

### Linear and point features
- Linear features: high consistency in land-use theme choices between QA and CS for linears; minimal mismatches (e.g., fences vs walls generally not confounded); some confusion between forestry belts and woody linears (FO vs WNS/WUS) but overall low impact.
- Point features: habitat codes for points largely consistent between QA and CS; minor confusion around woodland/forest code usage.

## Practical implications for data users and data products
- Digital workflow and QA processes yield a robust geodatabase suitable for integration with national datasets and rapid analysis.
- Quantified agreement metrics (per square, per habitat, per point/line) provide transparent indicators of data reliability and highlight areas needing refinement.
- Identified definitional gaps (e.g., Blanket Bog, Neutral vs Improved Grassland, woodland classifications) point to needs for clearer keys and targeted training.

## Recommendations and improvements
- Refine habitat definitions and decision rules in key problem areas:
  - Blanket Bog and Dwarf Shrub Heath in upland contexts; update field handbook guidance accordingly.
  - Neutral vs Improved Grassland overlap; establish clearer allocation criteria.
  - Woodland classification rules to reduce cross-type misclassifications (Broadleaf vs Coniferous).
- Enhance training, especially for upland mosaics and complex habitat mosaics, to reduce mis-matches in future surveys.
- Clarify urban vs grassland boundaries and improve guidance on “Amenity grass > 1 ha” rule to reduce misclassifications.
- Maintain and strengthen the digital change-recording workflow to maximize accurate historical comparisons and data updating.
- Continue leveraging 100-point and raster-based QA alongside direct aggregate comparisons to monitor data quality across scales.

## Conclusion
- The 2007 Mapping Quality Assurance Exercise demonstrates that digital field mapping, combined with structured QA workflows, yields high overall data quality and substantial agreement between surveyors and QA assessments.
- While most habitat allocations and derived metrics show strong concordance, certain habitat definitions, upland mosaics, and landscape-specific contexts require ongoing refinement and targeted training.
- The digital, geodatabase-centered approach significantly enhances data reliability, transparency, and the potential for self-serve data products and analyses, aligning with the Data Support archetype’s aims.