# COUNTRYSIDE SURVEY 2000 QUALITY ASSURANCE EXERCISE

- This report documents quality assurance (QA) of the Countryside Survey 2000 (CS2000), focusing on consistency, reliability, and mapping accuracy across field recording, plot relocation, species data, vegetation cover, land-cover coding, and change detection. A subsample of squares and plots was re-surveyed eight years after prior surveys to assess robustness of methods and data products.

## Aims and Scope

- Quantify field recording accuracy in CS2000 and comment on change statistics.
- Examine plot relocation efficiency and exactness.
- Explain recording differences in terms of observer error, plot location/relocation, plot type, management, and season.
- Relate CS2000 findings to CS1990 levels of agreement.
- Assess land-cover mapping accuracy and the recording of land-use changes.

## Methods and Design

- Sample: 38 of 519 squares; in each, one quarter resurveyed; 234 species plots across nine plot types, including quadrats, road verges, streamsides, boundaries, and arable margins.
- Plate/plot relocation: location of buried plates (corner markers) re-evaluated after eight years; comparison with 1990/1991 QA exercises.
- Mapping and coding: land-cover and boundary features coded with primary, secondary, and cover codes; comparison with CS2000 codes to assess concordance.

## Key Findings

- Plot relocation
  - 86.7% of full searches could relocate plots; eight-year relocation comparable to 12-month results from earlier QA.
  - CS2000 surveyors precisely relocated 60% of 1990 plots; ~25% relocated approximately; ~15% inadequately relocated.
  - Small 4 m Habitat (Y-plots) most difficult to relocate (23% failure).
- Species concordance and recording accuracy
  - About 71% of records were confirmed present by QA assessors; ~2% non-concordances due to management/seasonal changes.
  - Initial recording accuracy around 73%, slightly lower than CS1990 (c.78%), largely due to plot-location errors in CS2000.
  - QA found that same assessors’ evaluations revealed similar levels of efficiency as in 1990/1991 QA exercises.
- Vegetation cover estimates
  - Among the 30 most frequent species with appreciable cover, six species had significantly different cover levels between CS2000 and QA; some differences likely seasonal.
  - Overall cover-level agreement improved to ~74% across land-use points; species-specific discrepancies common for grasses and some forbs.
  - Certain species (e.g., Dactylis glomerata, Anthoxanthum odoratum, Arrhenatherum elatius, Eriophorum vaginatum) showed notable cover differences likely due to season.
- Direction of vegetation change
  - DECORANA ordination axis shift between time one and QA was insignificant; no directional bias detected across plot types or land classes.
- Land-cover mapping accuracy
  - Codes grouped into primary land-cover, secondary descriptive codes, and cover codes.
  - Agreement levels: Primary land-cover 88%; BAP (broad habitat) 77%; Primary boundary codes 85%; Principal qualifying land-cover codes 73%; Boundary qualifying codes 83%; Species awarded cover 63%; Species cover codes 74%.
  - Compared with CS1990 QA, concordance levels were broadly similar.
- Recording of change
  - 177 instances of change were examined; 16.4% attributed to errors/omissions in the 1990 survey.
  - Overall change concurrence: 51.4%; 33.9% changes not noted by CS2000; 14.7% changes recorded but not substantiated by assessors.
  - Substantial proportion of post-1990 changes may have been missed; plot data deemed more reliable for change assessment.
- Frequency and occurrence of species
  - About 35% of mismatches occurred between plots; overall, common species showed broadly similar ranking but with notable mis-identifications (e.g., Poa vs. Elymus; Ranunculus/Rumex; etc.) and overlooked species.
  - Mosses were frequently overlooked; under-recording of some grasses (e.g., Agrostis capillaris, Elymus repens) noted.
- Hedge diversity plots
  - Total hedge-species data: 124 total species, 92 common; agreement 74.2%; surveyor efficiency 77.4%; mean species per hedge plot 5.16 (CS2000) vs 5.89 (QA).
  - Hedge data treated inconsistently at times, leading to higher apparent discrepancy.
- Arable plots
  - Only five arable plots; concordance very low (30.6%), largely due to seasonal variation and less familiarity with ruderal species.
  - Suggests planning two well-spaced visits for future arable-margin plots.
- Change and axis analysis by plot type and landclass
  - Ordination by landclass (LC, LG, MA, UP) shows no directional bias; mean axis scores for CS2000 and QA are very close across land classes.
  - No single dominant cause of axis-score discrepancy; location/orientation, cover mis-matches, and overlooked species contribute.
- Boundary and land-use coding
  - Primary boundary features: overall concordance 85%; boundary height 89%; stockproofing 83.8%; most boundary discrepancies involved hedges and fences.
  - Hedge shapes (codes 374–380) had limited success; many hedges omitted or mis-coded.
  - Land-use primary concordance (without BAP) around 87.5% overall; BAP codes improved or remained consistent with QA.
  - Change in land-use coding and boundary changes showed notable discordance between CS2000 and QA, with some changes recorded by CS2000 later found not to be real by assessors.
- Change in land use and boundary features
  - Change concordance in land-use and hedge-type was moderate; some changes were misinterpreted or mis-coded between survey and QA.
  - Where changes existed, some were not captured in the CS2000 data, indicating potential under-recording of landscape dynamics.

## Implications for GIS Data Products

- Location precision and uncertainty
  - Relocation accuracy varies by plot type; eight-year relocation introduces non-trivial location uncertainty that should be captured as metadata in GIS layers (e.g., location quality, confidence, and possible mis-location).
- Coding and schema consistency
  - Land-cover and boundary coding show substantial agreement but notable mis-codings (especially for hedges, boundary types, and some grass species). GIS datasets should include code provenance and confidence scores, plus documented common mis-matches.
- Change detection and time-series
  - Change data show substantial non-recording and misrecording risk; time-series analyses should incorporate uncertainty flags and cross-checks to avoid misinterpreting landscape change.
- Data integration and provenance
  - Since CS2000 and CS1990 data show differences in records and coding, GIS products should maintain versioning, lineage logs, and crosswalks between coding schemes (e.g., primary vs. qualifying codes, BAP vs. non-BAP).
- Data quality metadata
  - Include QA-derived metrics (concordance, efficiency, axis-score shifts, percent agreement, etc.) as metadata to inform end-users about data reliability by plot type, landclass, and code group.

## Recommendations for GIS Data Products and Workflows

- Capture and communicate uncertainty
  - Attach location confidence (origin plate status, relocation success category) to each plot and polygon; flag plots with high relocation uncertainty.
- Improve data capture standards
  - Standardize coding conventions for hedges, boundaries, and land-use changes; adopt a robust crosswalk between CS2000 and prior survey codes.
- Enhance arable-margin data collection
  - Plan multiple, well-spaced field visits for arable plots to reduce season-related mis-matches; document sampling dates to support time-sensitive analyses.
- Integrate QA indicators into data pipelines
  - Store QA metrics (e.g., % concordance by code group, mean axis shifts, engagement of mis-match types) alongside primary data for GIS analysis and quality control dashboards.
- Provide guidance for change interpretation
  - Include explicit rules for distinguishing genuine landscape change from survey/code changes; highlight cases with high risk of misinterpretation in GIS-ready reports.
- Documentation and user guidance
  - Deliver detailed metadata explaining plot relocation categories, code groups, and common mis-matches; supply examples of typical QA discrepancies to assist GIS analysts in interpretation.

## Summary Takeaways for GIS Specialists

- CS2000 QA confirms overall data reliability but reveals notable location precision issues, coding discrepancies (especially for hedge/boundary features), and moderate change-detection concordance.
- Relocation accuracy and species-concordance metrics vary by plot type; hedges and arable margins require particular attention in data capture and interpretation.
- Land-cover and boundary codes show high concordance, enabling robust GIS mapping, but still benefit from explicit QA metadata and crosswalks for long-term time-series analyses.
- For GIS workflows, embed QA-derived confidence, maintain code provenance, and implement clear handling of uncertainty and change detection to ensure reliable map-based data products.