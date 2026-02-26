# NERC project NE/R000875/1, Objective 3, Experiment 3: ReadMe document for data files

## Overview
- Purpose: Document data collected in Objective 3, Experiment 3 of the NERC project NE/R000875/1.
- Experimental aim: Manipulate the fecundity-longevity relationship in Drosophila melanogaster by altering larval diet.
- Diet regimes: 1) 20% SYA, 2) 100% SYA, 3) 120% SYA.
- Data collected on adult flies include death date, daily/bi-daily egg counts, and daily/bi-daily offspring counts.
- Data are organized into multiple CSV files with extensive, column-level metadata.

## Data files included (and purposes)
- NER0008751_Obj3_Exp3_eclosion.csv: Eclosion counts by vial and counting event; includes timing metrics and per-vial totals.
- NER0008751_Obj3_Exp3_egg_counts_data.csv: Daily egg counts for life-history sub-group females; totals and 7-day sums.
- NER0008751_Obj3_Exp3_female_sizes.csv: Thorax and wing measurements for life-history females; includes means.
- NER0008751_Obj3_Exp3_individual_females.csv: Individual female metadata (treatment, source population, eclosion date, sub-group, etc.).
- NER0008751_Obj3_Exp3_LH_data.csv: Life-history female metrics (age, eggs, offspring, viability, mating metrics, morphology means, etc.).
- NER0008751_Obj3_Exp3_mating_events.csv: Offspring and egg counts following each mating event (up to 10 events); includes mating-age and derived stats.
- NER0008751_Obj3_Exp3_offspring_counts_data.csv: Daily adult offspring counts for life-history females; totals and 7-day sums.
- NER0008751_Obj3_Exp3_pupation.csv: Pupation counts and timings across counting events.
- NER0008751_Obj3_Exp3_replacements.csv: Replacement details for flies in R1, R2, L sub-groups with C replacements; replacement rules by day.
- NER0008751_Obj3_Exp3_samples_for_RNA.csv: RNA sampling plan and counts by treatment and sub-group; collection dates and ages.
- NER0008751_Obj3_Exp3_tissue_samples.csv: Summary tissue-sample metadata for RNA pools (6 flies per pool, pooling details, dissection and extraction dates).

## Data structure and key variables
- Each file is CSV with column-by-column definitions included in the accompanying documentation.
- Common themes across files:
  - Dietary treatment applied during larval stage.
  - Source population (Dahomey) and vial/larval setup details.
  - Time metrics: treatment times, eclosion/pupation counting times, and hours from plating to events.
  - Life-history sub-group (L) and RNA sub-groups (R1, R2) with contingency (C) and replacement rules.
  - Handling of missing data: '.' indicates data not recorded due to death; 'NA' indicates missing values; '*' indicates null means caused by missing data.
  - Derived metrics: total and mean counts (eggs, offspring, eclosion times, pupation times), mating-event statistics, and morphological means (thorax/wing).

## Experimental design and data collection details
- Population and diet:
  - Four Dahomey source populations; larvae assigned to three diet treatments (20%, 100%, 120% SYA).
- Observations and timing:
  - Eclosion data collected across up to 15 counting events per vial.
  - Egg and offspring data collected for life-history sub-group females; mating event data captured every ~8 days (up to 10 events while alive).
  - Pupation data collected across multiple counting events; timing metrics include total hours to pupation and mean pupation time.
- Sub-groups and replication:
  - Life-history sub-group (L) used for longevity/fecundity data.
  - RNA sub-groups (R1, R2) for gene expression sampling; contingency (C) used for replacements.
  - Replacements occurred via designated sub-groups on early days (with day-by-day replacement rules).
- RNA sampling and tissue pooling:
  - Sampling planned at predefined death-rate milestones (e.g., 10% and 60% mortality) with dates and ages recorded.
  - Tissue samples pooled (groups of 12 flies) for RNA extraction; metadata includes replicate and dissection/extraction dates.

## Data handling and quality notes
- Data quality considerations:
  - Missing data represented with NA or '.'; some derived values depend on censoring (e.g., RNA sampling for censored individuals).
  - Some measures include '*' to denote null means due to missing inputs.
  - Replacements and contingencies introduce complexity; documentation provides full lineage and replacement rules.
- Data provenance:
  - Protocol referenced: Protocol_NER0008751_Objective 3_Experiment 3_v1_2018-05-05.docx.
  - Related manuscript: Collins et al., on larval diet effects on fecundity, longevity, and age-related gene expression (manuscript in preparation).

## Data provenance, usage, and objectives
- Source: NERC project NE/R000875/1, Objective 3, Experiment 3.
- ReadMe authors: David Collins, Andrew Bourke (15 November 2021).
- Use-case alignment:
  - While primarily an experimental biology dataset, it demonstrates rigorous, multi-parameter data collection, documentation, and data management suitable for environmental-health related analyses, including integration with other datasets for monitoring and policy-relevant insights.

## Access, storage, and recommended usage
- Files are supplied as CSV with extensive metadata; ensure cross-file linkage via consistent identifiers (e.g., treatment, source_population, Life_history_number).
- For monitoring-style analysis, integrate with environmental exposure datasets, time-series summaries, and standardized quality checks to compare across treatments or replicate populations.
- Consider handling of censoring, replacements, and RNA-sampling biases when aggregating across sub-groups.