# NERC project NE/R000875/1, Objective 3, Experiment 3: ReadMe document for data files

- Overview
  - Aim: Manipulate the fecundity-longevity relationship in Drosophila melanogaster by altering larval diet.
  - Diet regimes: 1) 20% SYA, 2) 100% SYA, 3) 120% SYA.
  - Data collected per adult fly include: date of death, daily egg counts, daily offspring counts, and a rich set of life-history and morphometric measurements. Several sub-groups and sampling schemes were used, including RNA sub-groups for gene expression work.

- Data organization and files
  - Each data file is a .csv; contents are described column-by-column in dedicated tables.
  - Files and their focus:
    - NER0008751_Obj3_Exp3_eclosion.csv
      - Eclosion data by vial and counting event (up to 15 events after the first).
      - Key columns include Diet, Source_population, Treatment_date/time, ecl.m./ecl.f./ecl.n. counts, true_hours, and total_eclosions.
    - NER0008751_Obj3_Exp3_egg_counts_data.csv
      - Daily egg counts for the life-history (L) female sub-group.
      - Includes day_counted, date_counted, day_produced/date_produced, per-fly counts, Total_eggs, 7D_eggs.
    - NER0008751_Obj3_Exp3_female_sizes.csv
      - Size measurements for life-history females: Thorax and Wing lengths (two measurements each), with Means.
    - NER0008751_Obj3_Exp3_individual_females.csv
      - Per-fly metadata: Diet, Life_history_number, Source_population, Eclosion_date, Sub_group, and Life_history identifiers.
    - NER0008751_Obj3_Exp3_LH_data.csv
      - Life-history data for females: age at death, total eggs/offspring, viability, mean eggs/offspring, mating event summaries (m.off.tot, m.age, m.off.mean, m.egg.tot, m.egg.mean), first-7-day summaries, and morphometrics (Mean_Thorax, Mean_Wing).
    - NER0008751_Obj3_Exp3_mating_events.csv
      - Offspring and egg counts following each mating event (up to 10 events per female), plus totals and averages (m.off.tot, m.age, m.off.mean, m.egg.tot, m.egg.mean).
    - NER0008751_Obj3_Exp3_offspring_counts_data.csv
      - Daily counts of adult offspring produced as eggs, plus Total_offspring and 7D_off.
    - NER0008751_Obj3_Exp3_pupation.csv
      - Pupation data by vial and counting events (pup.n.1 to pup.n.16) with true_hours, total_hours_to_pupation, total_number_of_pupae, Mean_pupation_time, Mean_pupation_duration.
    - NER0008751_Obj3_Exp3_replacements.csv
      - Replacement events: Day, Treatment, Sub-group, Sub-group_numeric, Replacement_sub-group, Replacement_sub-group_numeric.
    - NER0008751_Obj3_Exp3_samples_for_RNA.csv
      -RNA sampling plan and results by sub-group and treatment: totals at start and after die-off, censors, death percentage/number, date and age at collection.
    - NER0008751_Obj3_Exp3_tissue_samples.csv
      - Summary of tissue/RNA samples: sample_name, Fly_sample, Treatment, Sub-group, Replicate, Number_of_flies, Dissection_date, RNA_extraction_date, RNA_sample.

- Key concepts and data structure
  - Diet encoding: 1 = 20% SYA, 2 = 100% SYA, 3 = 120% SYA.
  - Sub-groups and sampling: 
    - R1 = RNA1 sub-group (collected after ~10% mortality),
    - R2 = RNA2 sub-group (collected after ~60% mortality),
    - L = life-history sub-group (no RNA sampling),
    - C = contingency sub-group used to replace losses.
    Replacement scheme: early days use C to replace deaths in R1, R2, and L; later replacements limited to accidents.
  - Data conventions:
    - Missing values: NA; non-detects in counts shown as '.'; '*' indicates null means due to missing data.
    - Censoring: death due to injury/escape recorded as censoring in life-history data.
  - Multilevel data structure:
    - Vial- and larval-stage information (diet, source population, treatment date/time, researcher) linked to adult outcomes.
    - Individual fly-level records across eclosion, egg counts, offspring counts, pupation, and life-history outcomes.
    - RNA sampling provides gene-expression context for subsets of individuals.

- Potential uses for analysis
  - Examine how larval diet modulates the fecundity-longevity relationship.
  - Link morphometrics (thorax/wing size) to fecundity, longevity, and viability across diets.
  - Assess how mating history influences offspring/egg production, and how this interacts with diet and life-history strategy.
  - Integrate reproductive data with RNA/ Tissue samples to explore molecular correlates of life-history traits.
  - Leverage replacement and curation metadata to ensure correct interpretation of treatment groups and sampling time points.

- Important considerations for analysts
  - Expect multiple data layers per individual: eclosion timing, egg/offspring counts, life-history metrics, morphometrics, mating events, pupation, and RNA sampling.
  - Carefully map subgroup designations (R1, R2, L, C) and diet codes when merging datasets.
  - Handle missing data thoughtfully (NA, ., and *) and consider censoring in longevity analyses.
  - Maintain provenance by tracking treatment, vial, and counting-event timestamps when modeling time-to-event or longitudinal outcomes.