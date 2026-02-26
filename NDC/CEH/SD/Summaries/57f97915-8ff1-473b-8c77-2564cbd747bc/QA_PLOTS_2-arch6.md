# Countryside Survey 2007: Quality Assurance Exercise. Appendix

- Purpose: Assess whether variation in CS2007 surveyors’ species records introduced bias into the data by comparing CS2007 surveyors with QA assessors using two data sets and multiple analytical approaches.

## Data sets analyzed

- Full QA2007 data set
  - 532 samples (266 plots recorded by both CS2007 surveyors and QA2007 assessors)
  - Cryptogams removed for comparability; data converted to presence/absence
- Matched Triplicate data set
  - 108 plots common to three QA exercises (1990, 1998, 2007), offering six species lists per plot
  - Cryptogams removed; presence/absence data used
  - Analyses include time sequence (1990, 1998, 2007) and surveyor type (CS vs QA)

## Methods and modifications

- Modifications to data
  - Cryptogams (mosses, liverworts, lichens) eliminated to improve comparability
  - Data converted to presence/absence to reduce cover-variation issues
- Analyses performed
  - Species richness: mean species per plot; paired t-tests and ANOVA with Tukey post-hoc
  - Matched Triplicate: repeat measures ANOVA; Wilcoxon paired tests for pairwise year comparisons
  - Multivariate analyses: Decorana (DCA) on presence/absence data; outlier removal followed by re-analysis
  - Ellenberg indicator values (Light, Fertility, Moisture) calculated per quadrat; correlations with DCA axes analyzed
  - Ordination: assessment of axis scores and their relation to environmental gradients (Ellenberg L, N, F)
- Outputs compared
  - CS2007 vs QA2007 across plot types and landscape classes
  - Temporal trends (1990, 1998, 2007) within CS and QA
  - Grouped species analyses (grasses, Cyperaceae, Juncaceae, woody species, subshrubs, ferns, forbs, cryptogams)

## Key findings

- Overall recording differences without cryptogams
 - Even after removing cryptogams, CS2007 tended to record fewer species per plot than QA2007, with a modest overall shortfall (~13%), varying by plot type.
- Plot-type and landscape effects
 - Hedge and arable plots showed larger disparities; upland squares often recorded less efficiently than lowland plots, even after cryptogams removal.
 - Land class analyses generally confirmed CSunder-recording, with upland plots showing stronger differences over time than lowland plots.
- Matched Triplicate (1990–2007) trends
 - Across six matched surveys, CS2007 records show a decline in species numbers relative to QA, particularly for grasses and sedges; forbs contribute about half of total records and show declines consistent with broader patterns.
 - Sphagnum cryptogams: recording of Sphagna by CS was poor (about 48% of presence detected by QA in the matched set); when present, correctly allocated to the right group about 93% of the time.
 - Woody species and subshrubs: CS and QA trends largely parallel since 1998, indicating some recovery/consistency in woody taxa recording, but other groups lag.
- Group-specific recording patterns
 - Grasses: CS1998-to-CS2007 decline more pronounced than QA; CS2007 recorded roughly 10% fewer grasses than would be expected at the 1998 CSA efficiency level.
 - Cyperaceae and Juncaceae: smaller declines; CS showed greater drop in 2007 for some groups.
 - Forbs: about 5% fewer records in CS2007 relative to CS1998, reflecting broader declines in forbs recording.
 - Cryptogams: sustained under-recording of allowable cryptogams by CS2007 relative to 1998; Sphagnum under-recording remains a particular issue.
- Ordination and environmental gradients
 - DCA axis 1 (fertility) showed a negative Ellenberg N relationship; CS1990–CS2007 changes exaggerated in CS data, with QA data indicating more modest changes.
 - Axis 2 (shade vs exposure) and Ellenberg L also showed changes; both CS and QA detected increases in shade-tolerant assemblages over time, though CS results tended to exaggerate changes in axis scores.
 - Axis 3 was less clearly related to the measured gradients.
- Epilogue: potential adjustments (par scores)
 - Estimated additional species per plot needed for CS2007 to match CS1998 levels (excluding cryptogams) varied by plot type:
    - Hedge: 0 or 1
    - Boundary: ~0.3
    - Stream: ~0.8
    - Y plots: ~1.9
    - X and U plots: ~2.1
  - These are crude extrapolations based on matched triplicate data and QA1998–QA2007 comparisons.

## Implications for data support and practice

- Data quality and comparability
 - Cryptogams removal and presence/absence transformation improved comparability but revealed persistent under-recording by CS2007 for several plot types and taxa.
- Bias assessment
 - Across both data sets, there is no strong, uniform directional bias detected across all axes and environmental indicators; some analyses show small CS-vs-QA differences in specific axes or Ellenberg N, but overall the QA data align with previous QA exercises and reveal nuanced, group- and plot-type–dependent differences.
- Data use and communication
 - The results highlight the importance of clear, standardized data collection practices, training, and documentation to minimize surveyor-related variability and improve data reuse.
- Data products and accessibility
 - Findings support developing self-serve data products (e.g., presence/absence matrices, plot-level richness summaries, and ordination layouts) with transparent documentation of potential biases and data cleaning steps (cryptogams removal, presence/absence conversion).

## Takeaways for Data Support perspective

- When integrating data from heterogeneous surveyors, consider targeted data cleaning (cryptogam exclusion, presence/absence reformats) to enable robust cross-time and cross-surveyor comparisons.
- Use multi-faceted analyses (univariate richness, group-level assessments, and multivariate ordination with environmental proxies) to detect subtle biases and understand their sources (plot types, landscapes, taxonomic groups).
- Provide explicit bias-adjustment guidance (as in the epilogue par scores) to inform users about how to align legacy survey data with newer collection standards.
- Communicate findings clearly to stakeholders to promote wider data reuse and to justify methodological choices in future surveys.