# COUNTRYSIDE SURVEY 2000 QUALITY ASSURANCE EXERCISE

## Overview
- This report evaluates quality assurance (QA) for the Countryside Survey 2000 field programme, focusing on consistency and reliability across major components: plot relocation, species records, vegetation cover, landcover mapping, and change assessment.
- A QA sub-sample examined 38 squares (from 519 total) with one quarter of each resurveyed, covering 234 species plots across nine CS2000 plot types.

## Key QA Findings

- Plot relocation and plate recovery
  - Relocation success: CS2000 surveyors accurately relocated about 60% of plots; ~25% relocated to a close position; ~15% poorly relocated.
  - Plate recovery: Assessors located 69.3% of plates (roughly similar to the 1991 QA for CS1990). Overall, relocation of older plates eight years on is feasible but challenging.
  - A substantial portion of discrepancies arose from mis-location or mis-orientation of plots rather than absence of species, with some cases of incorrect side of streams or hedge boundaries being used.

- Species concordance and records
  - Across ~6000 records in 210 plots, about 71% of original records were confirmed as present; ~2% non-concordances due to real management/seasonal changes.
  - The QA indicated an initial recording accuracy of about 73%, with differences largely attributable to plot location errors.
  - QA repeatedly found that same surveyors and assessors produced broadly consistent rankings of plot richness, though the exact species lists varied due to location/orientation errors and mis-identifications.

- Vegetation cover estimates
  - For the 30 most frequent species, there was general agreement between CS2000 surveyors and QA assessors on cover levels, though several grasses showed significant discrepancies (e.g., Holcus lanatus, Dactylis glomerata, Anthoxanthum odoratum).
  - Some species showed systematic over- or under-estimation, but overall no consistent directional bias was detected across the dataset.

- Landcover and boundary coding
  - Primary land cover codes: Overall concordance 87.5% (excluding BAP codes); primary-BAP concordance 77.4%; when including BAP codes, overall primary land cover concordance remained high (about 87.5%).
  - Boundary features: Primary boundary coding concordance around 85%; boundary code concordance about 92%. Hedge and wall condition codes showed moderate concordance (~67.5%), with some mis-match between wall condition codes and hedge shapes.
  - Land-use change between 1990 and 2000: Change concordance was relatively low at 51.4%, with a substantial portion of changes not noted by CS2000 (33.9%) or recorded but not substantiated by assessors (14.7%). This indicates many changes since 1990 were missed or inconsistently captured.

- Change detection and coding
  - The level of concordance in recording change was disappointingly low; many changes identified by surveyors were not confirmed by QA assessors, suggesting cautious interpretation of change data and a need for robust field verification protocols.

- Arable plots
  - Five arable margin plots showed very tentative concordance; seasonality and familiarization with ruderal species influenced accuracy. Recommendation: plan multiple visits for future arable margin plots.

- DECORANA ordination and axis changes
  - No evidence of directional bias between CS2000 and QA across plot types; mean Axis 1 scores were statistically similar, indicating no systematic shift between time 1 and time 2 records.
  - Some axis-score shifts were attributable to location/orientation issues or cover-value disagreements, but large-scale directional bias was not detected.

## Implications for GIS data products

- Data reliability
  - High concordance in primary land cover and boundary coding supports robust GIS mapping products, but lower change-detection concordance highlights uncertainties in temporal analyses.
- Spatial accuracy
  - Plot relocation and plate recovery limitations affect spatial precision; eight-year plate relocation success is mixed, suggesting caution when using historical plot locations for precise GIS analyses.
- Coding systems
  - Strong performance for primary landcover codes; hedge/wall boundary coding and new hedge-type codes require careful handling and documentation.
- Change over time
  - Change data between 1990 and 2000 should be used with caution in GIS applications; substantial mis-match potential exists, underscoring the need for explicit QA metadata on change assertions.
- Seasonal effects
  - Seasonal variation influenced species records and some cover estimates; GIS analyses should consider seasonality metadata when integrating multi-temporal data layers.

## Recommendations for practice

- QA procedures
  - Maintain and document robust plot relocation protocols, including permanent markers and precise sketch maps to improve future relocations.
  - Continue using a QA sub-sample approach (like the 38-square QA) to monitor data reliability across years and plot types.
  - For arable margins, implement multiple visits across different seasons to reduce misclassification and improve species detection.
- Data management and metadata
  - Attach QA metrics to GIS datasets (e.g., concordance rates, efficiency, and axis-score changes) to inform users about data quality and uncertainty.
  - Record change metadata explicitly, distinguishing real ecological change from mis-codings or mis-location consequences.
  - Provide detailed documentation on boundary and hedge coding decisions, including rationale for selecting or adjusting hedge/ boundary codes and any new hedge codes (374–380) that may be underutilized.
- GIS integration
  - Treat landcover and boundary coding as high-confidence layers for mapping, but flag areas with potential mis-location or mis-orientation issues for review.
  - Integrate hedge/wall condition codes and stockproof status with boundary attributes to enhance landscape modeling.
  - Use the QA findings to calibrate automated GIS workflows (e.g., change detection routines) and to inform uncertainty buffers around relocated plots.
- Long-term data strategy
  - Consider permanent, clearly marked plots and standardized data-entry protocols to reduce mis-location errors in future cycles.
  - Plan for repeat visits and seasonally aware surveys for arable margins and hedgerows to improve reliability of temporal comparisons.

## Summary of end-to-end takeaways
- The CS2000 QA demonstrates generally strong spatial coding reliability (landcover and boundaries) but highlights notable uncertainties in plot relocation, temporal change detection, and some species-cover estimates.
- For GIS users, the data provide solid primary land cover and boundary information with measurable QA context, but temporal change data should be used with explicit uncertainty flags and robust metadata describing QA outcomes and potential biases.