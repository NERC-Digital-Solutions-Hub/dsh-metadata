# Countryside Survey 2007: Quality Assurance Exercise. Appendix

- Overview
  - The appendix evaluates whether variation in CS2007 surveyors introduces bias into the species records, using two data sets: Full QA2007 (532 samples from 266 plots) and Matched Triplicate (108 plots common to 1990, 1998, and 2007 surveys).
  - Modifications for comparability: cryptogams (mosses, liverworts, lichens) are removed; data are converted to presence/absence before multivariate analyses.

- Data Sets and Modifications
  - Full QA2007 data set: 532 samples (CS2007 vs QA2007) with cryptogams eliminated; presence/absence used.
  - Matched Triplicate data set: 108 plots common to all three QA exercises (1990, 1998, 2007); same data modifications applied.
  - Analyses focus on species richness, multivariate ordination (Decorana/DCAs), and Ellenberg indicator values (L, N, F).

- Analyses Conducted
  - Diversity: comparisons of mean species per plot; paired t-tests and ANOVA with Tukey post-hoc tests; repeat-measures ANOVA for matched triplicate data.
  - Multivariate: DCA ordinations (full and matched triplicate) with presence/absence data; exploration of axis scores and their relationship to Ellenberg values.
  - Ecological indicators: Ellenberg L (light), N (fertility), F (moisture) calculated per quadrat and related to ordination axes.
  - Data quality/context: outlier removal (three extreme plots), cross-time comparisons across 1990, 1998, 2007.

- Key Findings on Data Quality and Bias
  - Cryptogams removal reduces but does not eliminate discrepancies between CS2007 and QA2007; overall difference in mean species per plot remains modest but statistically significant in many plot categories.
  - Across the Full QA2007 data, CS2007 generally records fewer species than QA2007, with an approximate overall shortfall around 13% when cryptogams are excluded.
  - Matched Triplicate results show persistent declines in CS-recorded species numbers over time (1990 → 2007) and larger gaps between CS and QA as time progresses; QA records remain comparatively higher.
  - For several plot types, CS2007 under-recording appears substantial (e.g., X, Y, S, hedges, streams, verges), while QA tends to show smaller declines over time.
  - Sphagnum-based cryptogams are particularly poorly recorded by CS2007 (about 50% of what QA would distinguish); however, when recorded, Sphagna are usually allocated to the correct group (93% accuracy).
  - A general pattern of time-related declines in species richness exists in both CS and QA data, but the CS declines are often exaggerated in 2007 CS results.

- Group/Plot Type and Landscape Findings
  - Grasses: notable CS under-recording relative to QA, with ~10% fewer grasses recorded by CS2007 than would be expected from 1998 levels.
  - Cyperaceae and Juncaceae: declines in CS data over time; QA shows smaller or different patterns; overall, CS performance worsens in later surveys.
  - Woody species (trees/shrubs): increases in recorded frequency from 1990 to 2007 in both CS and QA; CS/QA trends are parallel, suggesting comparable performance for this group.
  - Subshrubs and ferns: limited data but trends suggest stable or modest changes; no clear CS vs QA bias dominating these groups.
  - Forbs: recording declines since 1998, with CS showing a larger shortfall than QA.
  - Cryptogams: overall poor identification; CS2007 records substantially fewer cryptogams than QA1998 would expect.
  - Boundaries and hedge plots: declines in CS data not always matched by QA; hedge plots show time-related declines but with less clear surveyor effects.
  - Streams and verges: consistent declines in species richness, with CS2007 results showing larger declines than QA; CS under-recording amplifies perceived losses.
  - Landscape classes: both lowland and upland show declines over time, but the magnitude and theCS vs QA differences vary by landscape; uplands show stronger CS under-recording in later years.

- Ordination and Ecological Indicators
  - DCA shows axis 1 strongly related to fertility (Ellenberg N); both CS and QA show declines over time, but CS1990→2007 changes appear exaggerated relative to QA.
  - Axis 2 relates to shading/exposure; minor changes observed in both datasets with significant differences in both surveyors.
  - Ellenberg indicator trends: L (light) and N (fertility) show measurable shifts over time; however, the CS declines in Axis 1 and Ellenberg N are exaggerated in the CS data, while QA trends are more stable.
  - Overall, there is no consistent directional bias favoring CS or QA across axes, but time-based changes tend to be more pronounced in the CS records.

- Epilogue: Par Scores and Adjustment Implications
  - To bridge CS2007 to CS1998 levels (excluding cryptogams), crude “par” adjustments are proposed by plot type:
    - Hedge: 0 change
    - Boundary: +0.3 species/plot
    - Stream: +0.8
    - Verge: +1.9
    - X/U plots: +2.1
  - These par scores are crude, derived from matched-triplicate trends, and intended to aid interpretation of long-term changes and to guide data harmonization efforts.

- Data Stewardship Implications and Recommendations
  - Documentation and metadata
    - Clearly document data transformations: cryptogams removal, presence/absence conversion, outlier exclusions, and any reclassification of Sphagnum records.
    - Include detailed metadata on surveyor differences, QA procedures, and time-series harmonization steps.
  - Data quality and governance
    - Maintain QA metrics as part of data quality profiles; flag plots or plot types with known surveyor-related biases.
    - Consider providing QA-adjusted layers or indicators for time-series analyses to prevent misinterpretation of genuine ecological trends.
  - Data discovery, sharing, and reuse
    - Ensure dataset descriptions emphasize potential biases in taxa groups and plot-types, especially when integrating across years.
    - Provide guidance or companion datasets that reflect adjusted or harmonized values (e.g., par-adjusted counts per plot type) for users focusing on long-term trends.
  - Standards and interoperability
    - Assess and standardize handling of cryptogams across surveys to improve comparability and reduce interpretive risk.
    - Capture and expose the transformation history in data catalogs to support reproducibility and transparent lineage tracing.
  - Actionable next steps
    - Consider publishing harmonized time-series datasets that include both raw and QA-adjusted values, with clear caveats.
    - Integrate QA findings into ongoing data governance processes to improve future survey design, data capture, and cross-year comparability.

- Takeaway for Data Stewards
  - The QA exercise confirms no overarching directional bias between CS surveyors and QA assessors, but substantial time-related declines in species richness reported by CS data are partially exaggerated in the 2007 CS results, especially for several plot types.
  - Transparent documentation of data processing, careful metadata practices, and harmonization strategies are essential to ensure that long-term analyses are reliable and discoverable by data users.