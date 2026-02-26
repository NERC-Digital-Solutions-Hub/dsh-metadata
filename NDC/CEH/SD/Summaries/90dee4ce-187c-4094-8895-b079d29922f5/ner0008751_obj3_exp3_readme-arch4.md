# NERC project NE/R000875/1, Objective 3, Experiment 3: ReadMe document for data files

- A ReadMe detailing data collected in Objective 3, Experiment 3 of the NERC project NE/R000875/1, which manipulated the fecundity-longevity relationship in Drosophila melanogaster via larval diet.
- Experimental setup: three larval diets (1 = 20% SYA, 2 = 100% SYA, 3 = 120% SYA); data collected from adult flies across multiple life-history measures.
- Data sources: protocol document and a manuscript; data files are provided as CSV with column-by-column definitions.

## Data files included (high-level)
- NER0008751_Obj3_Exp3_eclosion.csv: eclosion counts by vial and sex, plus timing metrics.
- NER0008751_Obj3_Exp3_egg_counts_data.csv: daily egg counts for life-history sub-group females; total and 7-day sums.
- NER0008751_Obj3_Exp3_female_sizes.csv: thorax and wing measurements for life-history females (with means).
- NER0008751_Obj3_Exp3_individual_females.csv: treatment, source population, eclosion date, and sub-group assignment per female.
- NER0008751_Obj3_Exp3_LH_data.csv: life-history data per female (age, eggs, offspring, viability, mean rates, mating metrics, thorax/wing morphology).
- NER0008751_Obj3_Exp3_mating_events.csv: offspring and egg counts after each mating event (up to 10 events), plus derived mating metrics.
- NER0008751_Obj3_Exp3_offspring_counts_data.csv: daily counts of adult offspring produced (as eggs) per life-history female.
- NER0008751_Obj3_Exp3_pupation.csv: pupation counts and timing; mean pupation time and duration.
- NER0008751_Obj3_Exp3_replacements.csv: replacement events for R1/R2/L sub-groups with C sub-group replacements.
- NER0008751_Obj3_Exp3_samples_for_RNA.csv: RNA sampling plan and outcomes (start numbers, censors, death thresholds, collection dates, ages).
- NER0008751_Obj3_Exp3_tissue_samples.csv: summary tissue-sample data from RNA1/RNA2 subgroups, including pooling into replicates and dates of dissection and RNA extraction.

## Key design and metadata aspects
- Experimental design details
  - Diet treatments: 1 (20% SYA), 2 (100% SYA), 3 (120% SYA).
  - Source populations: four Dahomey populations (coded 1–4).
  - Sub-groups: L (life-history), R1 (RNA1), R2 (RNA2), C (contingency). Replacements can occur from C to other sub-groups (days 1–3 primarily; later replacements limited).
  - Sampling for RNA: 10% death threshold (RNA1) and 60% death threshold (RNA2); samples collected and stored for sequencing.
  - Data files include both raw counts and derived metrics (means, totals, proportions, rates).
- Data granularity and structure
  - Each file is a CSV with detailed, column-level definitions provided.
  - Columns include event-level timings (hours since plating), counts by day/event, and per-fly or per-vial identifiers (e.g., Life_history_number, Diet, Source_population, Treatment_date, eclosion counts, etc.).
  - Derived metrics available: total_hours_to_eclosion, Mean_eclosion_time, total_number_of_eclosions, mean_eggs/mean_offspring, viability, m.off.mean, m.egg.mean, pupation means, etc.
- Missing data and data quality markers
  - Missing values indicated by '.' or 'NA'.
  - '*' used to denote null means caused by missing values in certain measurements (e.g., thorax/wing means).
  - Censoring and replacements documented (e.g., censored deaths, replacement events).
- Data provenance and references
  - Protocol document: Protocol_NER0008751_Objective 3_Experiment 3_v1_2018-05-05.docx.
  - Manuscript: Collins et al., The effect of larval diet on the fecundity-longevity relationship and age-related gene expression in Drosophila melanogaster.
- Relevance and use for analyses
  - Enables integrated analyses of how larval diet affects fecundity, longevity, development timing (eclosion, pupation), morphology, and RNA-level signals.
  - Supports cross-file linkage via identifiers (e.g., Diet, Source_population, Life_history_number, Treatment, Sub_group) for holistic data analyses and reproducibility.

## Data handling and integration notes for Data Leaders
- Ensure consistent mapping of diets, sub-groups, and replacement events across all files to enable accurate longitudinal analyses.
- Leverage the per-individual life-history data (LH_data.csv) in combination with mating events and offspring data to study lifetime performance by diet.
- Use RNA sampling metadata (samples_for_RNA.csv, tissue_samples.csv) to align molecular data with life-history phenotypes.
- Be mindful of censored data and replacements when computing survival, fecundity, and aging-related metrics.
- Validate that derived fields (e.g., mean eggs, m.off.mean, mean_pupation_time) are computed consistently across datasets.

## Practical considerations and caveats
- Some measurements are dated and context-dependent (e.g., eclosion times, pupation timing) and may be affected by replacements and censoring.
- Data include both raw counts and derived statistics; ensure clear documentation of how derived metrics are calculated when sharing analyses.
- RNA-based samples are collected at defined death-rate thresholds, which should be considered when interpreting gene-expression results relative to life-history trajectories.

## References for protocol and context
- Protocol_NER0008751_Objective 3_Experiment 3_v1_2018-05-05.docx
- Collins DH, Prince DC, Donelan JL, Chapman T, Bourke AFG. The effect of larval diet on the fecundity-longevity relationship and age-related gene expression in Drosophila melanogaster. Manuscript.