# NERC project NE/R000875/1, Objective 3, Experiment 3: ReadMe document for data files

- The document describes data collected in Objective 3, Experiment 3 of a NERC project, aimed at manipulating the fecundity-longevity relationship in Drosophila melanogaster by varying larval diet (three regimes: 20% SYA, 100% SYA, 120% SYA).
- Data comprise per-fly and per-vial life-history and reproductive measures, with detailed metadata and timing for each observation.
- Protocols referenced: the experiment protocol document and a manuscript on the effect of larval diet on fecundity-longevity and age-related gene expression.

## Data files and key contents

- NER0008751_Obj3_Exp3_eclosion.csv
  - Eclosion data by vial and diet; includes counts of adult males/females, total adults, and timing metrics (true_hours, total_hours_to_eclosion, mean_eclosion_time) across up to 15 counting events.
  - Columns include vial ID, diet (1=20% SYA, 2=100% SYA, 3=120% SYA), source_population, treatment date/time, researcher, larval count, and per-event eclosion counts.

- NER0008751_Obj3_Exp3_egg_counts_data.csv
  - Egg counts for life-history sub-group females on each experimental day; includes day_counted, count, date_counted, day_produced, date_produced.
  - Rows L1-L168 correspond to individual flies; includes Total_eggs and 7D_eggs.

- NER0008751_Obj3_Exp3_female_sizes.csv
  - Morphometrics for life-history females: thorax and wing lengths (Thorax1/2, Wing1/2), with Means (Mean_Thorax, Mean_Wing).

- NER0008751_Obj3_Exp3_individual_females.csv
  - Individual female metadata: diet, Life_history_number, source_population, eclosion_date, sub-group (R1, R2, N, C), sub_group_numeric, life_history_number, L_history_numeric.

- NER0008751_Obj3_Exp3_LH_data.csv
  - Life-history data per female: death date, age, exp_age, eggs/offspring totals, viability, mean eggs/offspring, mating-event related metrics (m.off.tot, m.age, m.off.mean, m.egg.tot, m.egg.mean), early-life metrics (eggs_7d, off_7d), thorax/wing measurements (Mean_Thorax, Mean_Wing).

- NER0008751_Obj3_Exp3_mating_events.csv
  - Reproductive output by mating event: m.off.1 to m.off.10, m.off.tot, m.age, m.off.mean, m.egg.1 to m.egg.10, m.egg.tot, m.egg.mean; includes diet, Life_history_number, and mating-event timing.

- NER0008751_Obj3_Exp3_offspring_counts_data.csv
  - Offspring counts by day produced as eggs; includes day_produced, date_produced, and Total_offspring and 7D_off.

- NER0008751_Obj3_Exp3_pupation.csv
  - Pupation data by vial and diet; includes pup.n.1...pup.n.16, true_hours1...true_hours16, total_hours_to_pupation, total_number_of_pupae, Mean_pupation_time, and Mean_pupation_duration.

- NER0008751_Obj3_Exp3_replacements.csv
  - Replacement records for flies in R1, R2, and L sub-groups replaced by C-subgroup flies; details Day, Treatment, Sub-group, Sub-group_numeric, Replacement_sub-group, Replacement_sub-group_numeric.

- NER0008751_Obj3_Exp3_samples_for_RNA.csv
  - RNA sampling plan: Treatment, Sub-group (L, R1, R2), totals at start and after die-off, censors, deaths needed for RNA, date_collected, and Age_at_collection.

- NER0008751_Obj3_Exp3_tissue_samples.csv
  - Tissue sample metadata for RNA1/RNA2 subgroups (treatments 2 and 3): Sample_name, Fly_sample, Treatment, Sub-group, Replicate, Number_of_flies, Dissection_date, RNA_extraction_date, RNA_sample.

## Experimental design and data collection

- Diet treatments: three larval dietary regimes (1=20% SYA, 2=100% SYA, 3=120% SYA).
- Populations: four Dahomey source populations (numbered 1–4).
- Timeline and observations:
  - Eclosion data collected across up to 15 counting events; timing recorded as hours after larval plating.
  - Egg counts tracked for life-history females across days; total eggs and 7-day sums computed.
  - Morphometrics measured for life-history females (thorax and wing lengths) with means computed.
  - Life-history data include longevity, fecundity, offspring viability, and mating-event metrics.
  - Pupation data include counts and timing; mean pupation time and duration computed.
  - Replacements policy documented for early days (RNA and life-history subgroups replaced by contingency group).
  - RNA sampling planned at specific death-rate milestones (10% and 60% for RNA1/RNA2) with tissue pools described.

## Data quality, metadata and governance notes

- Data use requires careful interpretation due to:
  - Missing values represented as NA or '.', with some fields as '*' indicating null means due to missing inputs.
  - Replacement and curation procedures (R1/R2 replaced by C) may affect continuity and lineage tracing.
  - Censoring in life-history data (e.g., death by injury/escape) influences calculations (e.g., m.age, m.off.mean, etc.).
  - Metadata density varies across files; some columns rely on consistent coding (e.g., diet, source_population, dates/times).
- Data governance implications:
  - The dataset emphasizes data provenance (protocol references) and openness (understanding of data lineage is crucial for policy-relevant monitoring).
  - Sharing underlying data is beneficial for transparency but may pose barriers if metadata are incomplete or inconsistent across components.
  - The ReadMe provides a structured mapping of variables to phenotypic and temporal measures, which is essential for integration into broader environmental health indicators.

## Relevance for Monitoring Frameworks

- Demonstrates how environmental conditions (dietary environment during larval stage) influence life-history outcomes (fecundity, longevity, development timing) in a model organism.
- Illustrates the creation of a multi-layered set of indicators:
  - Survival and timing metrics (eclosion, pupation timing).
  - Reproductive output (eggs produced, offspring produced, offspring viability).
  - Growth and morphology indicators (thorax and wing sizes).
  - RNA-based molecular sampling aligned with life-history milestones.
- Highlights key monitoring framework challenges:
  - Ensuring data quality and rich metadata to enable cross-study comparability.
  - Breaking down data silos by providing table-level descriptions and cross-references to protocols.
  - Managing data transformations and standardizing formats for integration into policy-relevant dashboards or reports.
  - Balancing openness with consistent data governance and provenance, especially for complex, multi-subgroup experiments.