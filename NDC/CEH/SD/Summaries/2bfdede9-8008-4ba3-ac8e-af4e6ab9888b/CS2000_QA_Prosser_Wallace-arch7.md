# COUNTRYSIDE SURVEY 2000 QUALITY ASSURANCE EXERCISE

- A QA study evaluating the CS2000 field work across 38 squares to measure consistency and reliability of recording, mapping, and change assessment.
- Focus areas: plot relocation, species concordance, vegetation cover estimates, landcover and boundary mapping, and recording of change.
- Method: resurvey of one quarter of each selected square (234 species plots across 9 plot types); comparison with original CS2000 data; analysis of plotting, coding, and mapping processes.

## Aims and Scope

- Quantify field recording accuracy for CS2000 and comment on change statistics.
- Examine plot relocation efficiency and errors.
- Explain differences in recording due to observer error, plot location, management, or season.
- Relate QA findings to CS1990 outcomes and assess mapping accuracy.

## Key Findings

- Plot relocation
  - 210 plots fully searched; 86.7% relocation success.
  - CS2000 surveyors: about 60% accurately relocated plots; ~25% relocated but not precisely; ~15% inadequately relocated.
  - Small 4 m Habitat (Y-plots) most difficult to relocate (23% failure).
  - Plate recovery by assessors: 69.3% (compared with 65.2% in 1991 QA for CS1990); total effective recovery estimated around 40–45%.
  - Overall implication: eight years on, relocation was feasible but less precise than the original year; next survey cohorts face increased plate/search challenges.

- Species concordance and recording
  - ~71% of CS2000 records were confirmed as present; ~2% attributed to real management/seasonal changes.
  - Initial field recording efficiency estimated ~73%, similar to the CS1990 QA when adjusted for different conditions.
  - QA identified various mis-matches (identification, locate/orientation, and overlooked species) with detailed categorization (types 1–9, 20–24) to explain discrepancies.

- Vegetation cover
  - Comparison of cover for the 30 most frequent species showed generally good agreement, but with notable differences for several grasses (e.g., Holcus lanatus, Dactylis glomerata, Anthoxanthum odoratum, Elymus repens, Arrhenatherum elatius) likely influenced by season and plot overlap.
  - Statistical tests (Wilcoxon) indicated significant differences for several species in some plots, while others showed no significant difference.
  - Overall: substantial overlap in cover estimates, but some species-specific discrepancies exist.

- Change in vegetation and axis analysis
  - DECORANA ordination showed no significant directional bias between CS2000 and QA axis scores when pooled across plot types.
  - Changes in axis scores varied by plot type, reflecting differences in location/orientation and cover assignments; however, no uniform directional shift was detected.

- Landcover mapping and codes
  - Codes categorized into primary landcover, secondary descriptive, and cover codes.
  - Concordance (agreement) for primary landcover codes: ~88%; BAP (broad habitat) codes: ~77%; primary boundary codes: ~85%; principal qualifying landcover codes: ~73%; boundary qualifiers: ~83%; species-awarded cover codes: ~63–74%.
  - Excluding BAP codes, total concordance for primary land cover: 91.6%; with BAP included: 87.5%.
  - Overall, mapping at the primary landcover level was broadly reliable; some discrepancies occurred in BAP classifications and boundary-related coding.
  - New/modified codes (Annex discussions) had limited success; most boundaries could be captured with existing codes, but some boundary/right-of-way changes were not fully captured.

- Change recording in land use
  - Change concordance between CS2000 and QA: ~51.4%.
  - Change not noted by CS2000: ~33.9%.
  - Change recorded but not substantiated by assessors: ~14.7%.
  - Conclusion: substantial proportion of changes since 1990 may have been missed or not properly documented; changes documented in plot data are more reliable for evaluating long-term change.

- Hedge diversity plots
  - 124 total species recorded; 74.2% overall agreement; 77.4% surveyor efficiency.
  - Mean species per plot: CS2000 5.16 vs QA 5.89 (QA often recorded more species).
  - Hedge-specific data showed many overlooked woody species and boundary-related codes.

- Arable plots
  - Only five plots; concordance very poor (around 30.6%).
  - Seasonality and familiarity with ruderal species likely contributed to differences; recommendation for multiple visits if arable margins are included in future surveys.

## Implications for GIS Data and Map-based Products

- Data quality and reliability
  - QA demonstrates strong general reproducibility for mapping outputs, but notable uncertainties remain in plot relocation, plant identifications, and seasonal changes.
  - Boundaries, hedge shapes, and landuse transitions require robust coding schemes and, where possible, field verification to maintain GIS integrity over time.

- Coding and standardization
  - High concordance in primary codes suggests stability, but BAP codes and certain hedge/ boundary qualifiers need careful handling to avoid misclassification in GIS layers.
  - Consistency between surveyors and QA assessors is crucial for reliable change detection layers and lineage tracking.

- Change analysis
  - Partial under-recording of changes indicates caution when using CS2000 data to infer dynamic landscape changes without QA-backed corroboration.
  - For GIS applications, use validated change strings where available and treat unsubstantiated changes as uncertain.

- Data integration and longitudinal studies
  - Long-term datasets benefit from detailed QA metrics to quantify uncertainty due to relocation, misidentification, and seasonal variation.
  - When combining CS1990/CS2000 time slices, account for observed biases in species frequency and cover reporting.

## Conclusions

- CS2000 QA confirms substantial reliability in landcover mapping and boundary coding, with high concordance for primary codes and reasonable agreement for land classes and boundaries.
- Plot relocation and species recording show room for improvement, particularly regarding precise plot positioning, seasonal effects, and certain species identifications.
- Change detection between CS2000 and QA (and by extension historic CS1990) is moderate to low in concordance, highlighting potential under-recording of landscape change and the need for careful interpretation in GIS analyses.
- Arable and hedge-related data, while generally usable, require extra caution and, in some cases, additional sampling to ensure GIS products reflect true conditions.

## Methodology Highlights (For GIS Practitioners)

- Sampling: 38 of 519 squares; 1/4 of each square resurveyed; 234 plots across 9 plot types.
- Relocation: plate and plot relocation tracked; multiple categorization of relocation success used for quality metrics.
- Mapping and coding: primary land cover, BAP codes, boundary and hedge codes, and landuse qualifiers were audited against QA assessments.
- Analysis: concordance metrics, DECORANA ordination, and cross-tabulations used to quantify reliability; annexes describe coding schemes and change assessments.

## Recommendations for GIS Data Practices

- Maintain rigorous plate/plot relocation documentation and consider GPS-backed relocation methods to improve spatial precision in future surveys.
- Strengthen species identification training and provide field references to reduce mis-identifications and improve cross-survey consistency.
- Continue using structured coding hierarchies for landcover and boundary features, but review BAP and hedge coding practices to minimize misclassifications.
- Integrate QA-derived uncertainty metrics into GIS datasets to support uncertainty-aware analyses and inform users about data reliability across years and plot types.
- When planning future sampling, consider more visits to arable margins and hedgerows to improve reliability in those more variable habitats.