# NERC project NE/R000875/1, Objective 3, Experiment 3: ReadMe document for data files

## Overview
- Purpose: Data from Objective 3, Experiment 3 of the NERC project to study how larval diet (three regimes) affects the fecundity-longevity relationship in Drosophila melanogaster.
- Experimental setup: Three diet treatments (1 = 20% SYA, 2 = 100% SYA, 3 = 120% SYA) with data collected from adult flies on death date, daily/bi-daily egg counts, and offspring counts.
- Documentation relationship: Protocol and manuscript references provided for full details.

## Data files included
- NER0008751_Obj3_Exp3_eclosion.csv — eclosion counts by vial/date, with hours-to-eclosion metrics and per-event counts.
- NER0008751_Obj3_Exp3_egg_counts_data.csv — daily egg counts per life-history fly, with totals and 7-day totals.
- NER0008751_Obj3_Exp3_female_sizes.csv — thorax and wing measurements (two measurements each) and their means.
- NER0008751_Obj3_Exp3_individual_females.csv — per-fly details: diet, source population, eclosion date, sub-group, life-history linkage.
- NER0008751_Obj3_Exp3_LH_data.csv — life-history data: age, eggs, offspring, viability, mean rates, mating-event summaries, thorax/wing means.
- NER0008751_Obj3_Exp3_mating_events.csv — per-mating-event data: eggs and offspring after each mating, totals, and derived means (up to 10 events).
- NER0008751_Obj3_Exp3_offspring_counts_data.csv — daily counts of adult offspring produced as eggs; totals and 7-day totals.
- NER0008751_Obj3_Exp3_pupation.csv — pupation counts by event, total pupation time, mean pupation times, and mean pupation duration.
- NER0008751_Obj3_Exp3_replacements.csv — records of replacements between sub-groups (R1, R2, L replaced by C) and replacement details.
- NER0008751_Obj3_Exp3_samples_for_RNA.csv — RNA sampling plan: counts, censors, death rates needed to reach RNA thresholds, collection dates and ages.
- NER0008751_Obj3_Exp3_tissue_samples.csv — tissue RNA pool metadata: sample IDs, treatment, sub-group, replicate, dissection and RNA extraction dates, and pooling details.

## Data schema and key variables
- Treatments and identifiers:
  - Diet: 1 = 20% SYA, 2 = 100% SYA, 3 = 120% SYA
  - Source_population: four Dahomey populations (1–4)
  - Treatment_date / Treatment_time / Treatment_time_rounded
  - Researcher_name and Larvae_number
- Eclosion data (eclosion.csv):
  - ecl.m.n / ecl.f.n / ecl.n.n: counts by sex and total
  - true_hoursN: hours from plating to each counting event
  - total_hours_to_eclosion, total_number_of_eclosions, Mean_eclosion_time
- Egg counts (egg_counts_data.csv):
  - day_counted, Count, date_counted
  - day_produced, date_produced
  - Total_eggs, 7D_eggs
  - Rows L1-L168 correspond to individual life-history flies
- Size data (female_sizes.csv):
  - Thorax1/Thorax2, Wing1/Wing2 measurements
  - Mean_Thorax, Mean_Wing
- Individual females (individual_females.csv):
  - Life_history_number, L_history_numeric, eclosion_date, sub_group, source_pop, etc.
- Life-history data (LH_data.csv):
  - age, exp_age, tot_eggs, tot_offspring, viability
  - mean_eggs, mean_offspring, mating-event summaries (m.off.tot, m.age, m.off.mean, m.egg.tot, m.egg.mean)
  - eggs_7d, off_7d
  - Thorax2/Mean_Thorax, Wing2/Mean_Wing
- Mating events (mating_events.csv):
  - m.off.1 to m.off.10, m.off.tot, m.age, m.off.mean
  - m.egg.1 to m.egg.10, m.egg.tot, m.egg.mean
- Offspring counts (offspring_counts_data.csv):
  - day_produced, date_produced
  - Total_offspring, 7D_off
- Pupation (pupation.csv):
  - pup.n.1 to pup.n.16, true_hours1 to true_hours16
  - total_hours_to_pupation, total_number_of_pupae
  - Mean_pupation_time, Mean_pupation_duration
- Replacements (replacements.csv):
  - Day, Treatment, Sub-group, Sub-group_numeric
  - Replacement_sub-group, Replacement_sub-group_numeric
- RNA sampling (samples_for_RNA.csv):
  - Treatment, Sub-group (L, R1, R2), Total_at_start, Total_after_die-off_day4
  - Censors, Total_minus_censors, Death_%_needed, Death_number, Number_for_RNA
  - Date_collected, Age_at_collection
- Tissue samples (tissue_samples.csv):
  - Sample_name, Fly_sample, Treatment, Sub-group, Replicate, Number_of_flies
  - Dissection_date, RNA_extraction_date, RNA_sample

## Data quality, handling, and conventions
- Missing data markers:
  - NA = missing values
  - . (dot) = not observed due to death or not applicable
  - * = null or due to missing values in a specific field
- Consistency considerations:
  - Diet encoding standardized to 1–3 across files
  - Temporal fields (dates, hours) require consistent units (hours, dates)
  - Per-fly and per-vial linking via Life_history_number and Treatment metadata
- RNA-related data are subject to planned sampling windows and replacement rules (R1/R2/L vs C sub-groups) and include censoring notes.

## Documentation and provenance
- Primary protocol: Protocol_NER0008751_Objective 3_Experiment 3_v1_2018-05-05.docx
- Associated manuscript: Collins DH, Prince DC, Donelan JL, et al. The effect of larval diet on the fecundity-longevity relationship and age-related gene expression in Drosophila melanogaster
- ReadMe-style description: Each data file contains column-by-column definitions; data are organized to support traceability from treatments to outcomes.

## Access, sharing, and maintenance considerations
- Data are provided as CSV files with explicit field definitions to facilitate discovery and reuse.
- To support data stewardship:
  - Maintain a data dictionary mapping column names to definitions, units, and allowable values
  - Capture data provenance, including protocol version and manuscript reference
  - Use controlled vocabularies for treatments and populations
  - Version datasets and record last update dates
- Potential use and reuse considerations:
  - Rich life-history, fecundity, longevity, and RNA data enable cross-file linkage but require careful attention to linkage keys (e.g., Life_history_number, Treatment, Sub-group)
  - RNA-related datasets may be subject to access controls until publication; follow repository policies.