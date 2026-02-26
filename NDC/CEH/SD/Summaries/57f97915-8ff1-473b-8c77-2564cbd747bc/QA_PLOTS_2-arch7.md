# Countryside Survey 2007: Quality Assurance Exercise. Appendix

## Overview
- This appendix assesses whether variation in CS2007 surveyors' species records introduced bias into the dataset, using two datasets:
  - Full QA2007: 532 samples (266 plots recorded by both CS2007 surveyors and QA2007 assessors).
  - Matched Triplicate: 108 plots common to three QA exercises (1990, 1998, 2007) across both surveyors and assessors, providing six species lists per plot.
- Modifications to data for comparability:
  - Cryptogams (mosses, liverworts, lichens) removed from analyses.
  - Data converted to presence/absence prior to multivariate analyses to mitigate cover misclassification.

## Datasets and Methods
- Analyses performed on:
  - Full QA2007 dataset (532 samples) and the Matched Triplicate dataset (648 samples, 108 plots with three surveys each).
- Key techniques:
  - Univariate: paired t-tests for 2007 CS vs QA; ANOVA with Tukey post-hoc for matched triplicate data; repeated-measures ANOVA for time effects.
  - Multivariate: Detrended Correspondence Analysis (DCA) on presence/absence data; Ellenberg indicator values (Light, Nitrogen, Moisture) calculated and related to DCA axes.
  - Ordination robustness checked after removing outliers.
  - Subgroup analyses by plot type and landscape class (lowland vs upland).

## Data Processing and Modifications
- Cryptogams removed from all analyses to improve comparability with prior QA exercises.
- Presence/absence data used to reduce variability in cover estimates.
- Ellenberg indicators computed for each quadrat and correlated with ordination axes.

## Key Findings: Full QA2007 Data Set
- Changes in species number:
  - CS2007 generally recorded fewer species per plot than QA2007 across most plot types, even after cryptogams were removed (approximate average shortfall around 13% overall).
  - Hedge and arable plots showed particular weaknesses in CS recording.
- DCA and ordination:
  - Axis 1: strongly related to nitrogen fertility (Ellenberg N) with a negative correlation; Axis 2 related to shade vs exposure; Axis 3 less clear.
  - No strong directional bias detected between CS2007 and QA2007 in mean axis scores or Ellenberg values overall; differences were small (comparable to patterns seen in 1998 QA analysis).
- Ellenberg indicators:
  - Axis 1 declines over time indicate a shift toward species benefiting from higher fertility, a trend that CS1998/CS2007 exaggerates relative to QA results.
  - Axis 2 shows a decline in L (light) indicating increased shade tolerance over time; supported by Ellenberg L trends.
- Plot-type and landscape effects:
  - Upland plots remained affected by under-recording even after cryptogams removal; lowland plots showed improvements but CS2007 still lagged behind QA in several categories.
- Sphagnum cryptogams:
  - Recording of Sphagna remained substantially lower by CS2007 (~48% of presence records recorded by QA), though when recorded, they were usually assigned to the correct group (93% accuracy for Sphagnum when present).

## Key Findings: Matched Triplicate Data Set
- Species-number trends (including cryptogams):
  - Across 1990, 1998, 2007, QA records generally higher than CS, with CS showing a consistent decline by 2007; however, declines in QA were less pronounced.
- Group-specific trends:
  - Grasses: both CS and QA show declines from 1990 to 2007; CS2007 under-recorded relative to 1998 level by about 10% for grasses.
  - Cyperaceae and Juncaceae: small declines in CS but less pronounced in QA; overall recording efficiency differs between CS and QA over time.
  - Woody species (excluding subshrubs): increased in both CS and QA since 1990, with parallel increases suggesting comparable recording efficiency.
  - Subshrubs and ferns: changes small; recording efficiency relatively stable.
  - Forbs (about 50% of records): decline in CS since 1998, with QA showing smaller declines; overall CS under-recording persists.
  - Allowable cryptogams: CS1990–1998–2007 shows poorer performance by CS2007; recorded cryptogams remain substantially undercounted relative to QA1998/1990.
- Plot-type and landscape effects:
  - X/Y plots and stream/verge plots show strong time effects and notable CS vs QA discrepancies; hedge/boundary plots show mixed results with QA declines being less dramatic than CS in some cases.
- Ordination (matched triplicate data):
  - Axis 1 (fertility) declines over time for both CS and QA, but CS decline is exaggerated; Axis 2 (shade/ exposure) declines indicating increased shade tolerance, with both CS and QA showing changes.
  - The overall structure of the ordination with six survey records is consistent with the larger dataset, though some axis loadings differ slightly.

## Landscape and Plot-Type Differences
- Lowland vs upland:
  - Upland squares show greater sensitivity to surveyor differences and time effects; declines in CS appear more pronounced here, while QA shows more moderate changes.
  - Lowland plots show declines over time but with smaller CS-QA disparities than upland.
- Plot-type summaries:
  - X/Y plots: strong time and surveyor effects; CS2007 shows notably lower species counts.
  - Stream plots: clear declines over time with consistent CS vs QA disparities.
  - Verge and hedge plots: time trends present; QA trends sometimes align with CS but often with smaller magnitudes.
  - Boundaries: less clear but notable time and surveyor effects in QA data.

## Epilogue: par scores and adjustment guidance
- The appendix proposes approximate “par scores” to adjust CS2007 species counts to align with a 1998 baseline (cryptogams excluded):
  - Hedge plots: no change
  - Boundary plots: +0.3 species
  - Stream and Verge plots: +0.8 species
  - Y plots: +1.9 species
  - X and U plots: +2.1 species
- These adjustments are crude, based on matched-triplicate comparisons, and intended to aid reconciliation of CS2007 with earlier baselines for data interpretation and GIS mapping.

## Practical Implications for GIS Specialists
- Data bias awareness:
  - CS2007 data show consistent under-recording of species richness compared with QA2007, particularly in upland, hedge, arable, and certain plot types.
  - Cryptogams, especially Sphagna, are under-recorded in CS2007, affecting habitat and biodiversity mapping if cryptogams are used.
- Data preparation recommendations:
  - Use presence/absence data to stabilize analyses and map products when dealing with cover variability.
  - Consider applying QA-based par scores to harmonize CS2007 data with earlier baselines for time-series vegetation change mapping.
  - Treat CS2007-derived richness maps with caution, particularly for upland and stream/hedge landscapes where discrepancies are larger.
- Multivariate interpretation:
  - Ordination results indicate ecological gradients (fertility, shade) align with Ellenberg indicators, but apparent time-related shifts can reflect surveyor differences as well as ecological changes.
  - When aggregating across years, be mindful of potential exaggeration of declines in CS data relative to QA data.
- Data quality controls:
  - Incorporate routine QA-like validations in GIS workflows to detect and adjust for surveyor-induced biases.
  - Maintain separate QA-adjusted layers or confidence metrics for map products derived from CS2007 data.
- Data integration:
  - When combining CS data with other datasets, account for differences in taxonomic resolution (cryptogams removed) and presence/absence transformation to ensure compatibility.