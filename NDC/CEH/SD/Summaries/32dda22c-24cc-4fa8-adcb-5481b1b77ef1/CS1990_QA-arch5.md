# 1990 Countryside Survey: Quality Assurance Exercise

- A comprehensive evaluation of the quality assurance processes used in the 1990 Countryside Survey, reporting scope, results, and recommendations to improve future surveys and data quality.

## Purpose, Scope and Context
- Aim: quantify accuracy of field recording, explain differences in recording, relate findings to previous work, and recommend methodological modifications to improve accuracy and confidence of statistics.
- Context: field work involved many recorders; QA sought to measure consistency, reliability, and potential biases across major components (plots, cover estimates, boundaries, landuse, etc.).

## QA Design and Methods
- Two main QA series:
  - Autumn 1990: 21 original survey squares assessed using sketch maps for plot relocation; two independent assessors.
  - 1991: expanded to include photographs of plots; included 1 km squares from original terrain classes; some assessors re-surveyed same plots; additional self-assessment squares.
- Plot types and relocation:
  - Quadrats: 200 m2 (X plots) and 4 m2 (Y plots).
  - Linear plots including road verges, hedges, streamsides, boundaries.
  - Plate relocation: attempted to locate buried corner of quadrats; evaluation of recovery rate with time limits.
- Data collected and evaluated:
  - Landcover and boundary features recorded at 9 pre-determined points per square quarter.
  - Photo and sketch-based relocation; use of metal plates to mark change plots.
  - Several concordance metrics used to compare T1 (original) and T2 (QA) records.
- Additional QA aspects:
  - Mapping of land use and vegetation with primary/secondary codes; coding consistency checked across different assessors and time periods.
  - Evaluation of vegetation cover estimates for selected species.

## Key Findings: Data Quality and Observations
- Species recording and concordance:
  - Autumn 1990: mean species per plot around 22; overall agreement between T1 and QA was modest (approx. 45% using initial metrics).
  - 1991 full QA: significant increase in species counts per plot (1990: ~20.7; 1991: ~23.4); suggests both real ecological differences and improved recording efficiency; seasonal and drought effects contribute to observed differences.
  - Across all plots, a substantial portion of variation arises from misidentifications, species overlooked, plot relocation errors, and seasonal/management changes.
- Plot relocation and plate-based locating:
  - Autumn 1990: plate recovery rate about 71% within five minutes.
  - 1991: higher success in locating plates and plots; overall improvement attributed to familiarity and the inclusion of photographs aiding relocation.
- Accuracy and efficiency:
  - Initial efficiency of recording (excluding T2 variations) averaged around 74%; upper bounds approach previously reported maxima for standardized field searches.
  - Across plot types, X plots tended to have better relocation/search efficiency; Y plots (4 m2) were notably more difficult to relocate accurately.
- Landuse mapping and coding:
  - Primary landuse code concordance between original and QA generally high (around 88–89% overall).
  - Boundary codes and related descriptors showed substantial agreement but with notable ambiguities, especially for hedges and boundary compositions.
  - Some codes (e.g., marsh 114) used inconsistently; upland vs. lowland classifications required refinement.
- Vegetation cover measurements:
  - Broad patterns showed reasonable consistency for dominant species; however, co-dominant and minor species exhibited lower concordance.
  - Bryophyte recording, and some grass identifications, were sources of error, indicating a need for targeted training and clearer field protocols.
- Landclass and ecological gradients:
  - DECORANA (first axis) analysis indicated shifts consistent with broader land-use change trends, with upland vs lowland differentiation largely preserved.
  - In aggregate, there was an observed axis shift between 1990 and 1991 that was directionally consistent with earlier ECOLUC findings, though year-to-year variation could produce perturbations.
- Overall implications for data quality:
  - While there is notable variation at the plot level, aggregated land-use coding and major vegetation descriptors show robust agreement, indicating reliability for broad-scale analyses with appropriate caveats about plot-level changes.

## Data Quality Metrics and Tables (Highlights)
- Species agreement and accuracy: 60.9% overall concordance when considering total matches and mismatches across T1 vs T2; higher when seasonal and location variations are accounted for.
- Initial efficiency of recording (1990 QA): around 58–74% depending on the specific metric; after adjustments, reached up to ~79% maximum efficiency observed in comparable studies.
- 1991 QA results: significant increase in detected species per plot, with robust statistical support; essential factoring in real ecological change versus observer efficiency.
- Landuse code concordance: primary landuse codes ~88–89% across assessments; boundary primary codes ~80–83% with some assessor-pair effects.
- Mapping and cover concordance: mapping of vegetation cover to dominant species showed reasonable agreement for primary species, but lower concordance for co-dominants; use of only the two most prevalent species recommended to improve reproducibility.

## Sources of Variation and Error (Categories)
- A: Apparent mis-identifications or mis-codings.
- B: Species overlooked at T1 or T2; seasonal/annual changes implicated.
- C: Over-zealous recording and mis-placements into plots.
- D, E, F: Management changes, seasonal effects, and crop-related changes.
- G, H, I, J: Plot relocation failures, mis-location, mis-orientation, and “mysteries” (unexplained discrepancies).
- Emphasis: many B-type and I-type errors reflect genuine seasonal/management changes; location-based errors (G/H) significantly influence accuracy.

## Recommendations for Future Surveys and Data Governance
- QA timing and seasonality:
  - Conduct QA as close as practical to the initial survey; avoid cross-season comparisons when possible.
  - QA should be restricted to the same season and year as the original survey to minimize climatic and phenological differences.
- Plot relocation and documentation:
  - Use metal marker plates for X plots wherever possible; enhance relocation efficiency with improved ground-truthing methods.
  - For Y plots, enhance positioning with survey tapes and fixed orientation; ensure SE corner and NS orientation are standardized.
  - Annotate photographs with ground-truth features; include distances and compass bearings on sketches.
  - Photographs should be annotated by surveyors and tied to the relevant plot metadata.
- Mapping codes and vegetation data:
  - Expand primary landuse codes (e.g., subdivide upland grassland types; add lowland rush pasture; recognize wet heath as distinct vegetation type).
  - Limit vegetation mapping to the two most prevalent species to improve reproducibility; reduce emphasis on minor species and fine-grained cover percentages.
  - Provide explicit guidelines for recording tree/shrub cover and for coding boundary features; clarify qualifying codes to reduce ambiguity.
  - Consider adopting simplified, dichotomous coding schemes to enhance inter-operator reliability.
- Bryophyte and grass identification:
  - Target bryophytes and grasses in training and QA sampling; provide reference specimens and habitat-specific lists to improve accuracy.
- Data governance and metadata:
  - Document QA procedures, data lineage, and versioning; clearly separate original survey data from QA-adjusted datasets.
  - Capture and store detailed metadata on plot relocation success, use of photographs, and any seasonal adjustments.
  - Ensure that QA findings (sources of error, efficiency metrics, and recommended code changes) are incorporated into data dictionaries and analyst guidance for future surveys.

## Implications for Data Stewards (Governance, Storage, Sharing)
- Data quality documentation:
  - Maintain separate QA datasets from the main survey data, with clear provenance and version history.
  - Store detailed error classifications (A–J) and their quantified impact on plots and aggregated results.
- Metadata standards:
  - Include fields for photographic aids used, plate markers, plot relocation success, and season/year of QA relative to the original survey.
  - Record landuse coding decisions, code expansions, and rationale for any changes to the coding schema.
- Data interoperability:
  - Align landuse and vegetation codes with updated, expanded code lists to support reproducible cross-survey comparisons.
  - Adopt consistent, machine-friendly representations for plot types, coordinates, and boundary features.
- Accessibility and discoverability:
  - Provide clear documentation linking QA results to the specific survey squares and plot types, enabling researchers to assess data reliability for site-level versus landscape-level analyses.
- Data quality improvements:
  - Use QA insights to refine data collection protocols, training materials, and data validation rules in future surveys.
  - Ensure that any public data releases include summaries of QA findings and their implications for interpretation of change statistics.

## Conclusion for Data Stewards
- The 1990 Countryside Survey QA exercise demonstrates meaningful improvements in data reliability when photography, standardized relocation, and clearer plotting protocols are employed.
- While plot-level concordance remains imperfect due to seasonal, management, and relocation factors, major data products (landuse codes and primary vegetation descriptors) show robust consistency suitable for broad-scale analyses with careful interpretation at finer scales.
- Implementing the prioritized recommendations will enhance future data governance, metadata richness, coding consistency, and overall data quality for countryside vegetation and landuse datasets.