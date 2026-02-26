# NERC project NE/R000875/1, Objective 1, Experiment 1: ReadMe document for data files

## Overview
- This ReadMe documents data collected in Objective 1, Experiment 1 of the NERC project NE/R000875/1.
- Experimental design: Bombus terrestris queen colonies assigned to two treatments
  - Removal (R): eggs removed and counted to induce higher fertility costs
  - Control (C): eggs removed, counted, and replaced to control for disturbance
- Measured outcomes include queen longevity, worker aggression toward the queen, queen locomotion, and mortality phases.
- Data collection spans behavioral observation, colony size dynamics, egg counts, and molecular data
  - RNA sequencing samples collected at 10% mortality (TP1) and 60% mortality (TP2)
- Data are organized into multiple CSV files, each describing columns in detail; source colonies 17, 51, 54, 62 are non-manipulated references, and extra colonies (E-series) exist

## Experimental design and data collection
- Treatments and sampling
  - R = egg-removal treatment (increased fertility costs)
  - C = egg removal with replacement (control)
  - Subgroups G1 and G2 denote RNA sampling at 10% mortality (TP1) or 60% mortality (TP2)
  - Some colonies have NA in subgroup or treatment fields if not assigned to a specific group
- Behavior and movement
  - Queen activity, response to disturbance, and various worker aggression metrics recorded during 10-minute observations every four days
  - Aggression metrics include buzzing, charging, butting, grappling, and stinging; Aggression is the sum of these
- Colony dynamics
  - Data include initial colony size, queenright status, and subsequent worker additions/removals
  - Egg-laying dynamics tracked via Old/New cells and eggs per cell
- Longevity and sampling
  - Queen longevity tracked with Day_of_Death, Cause (natural death, harvest for RNA, or censoring), and related timing
  - RNA sampling at TP1 (10% mortality) and TP2 (60% mortality); dissections include brain, ovary, and fat body tissues
  - Virus detection (SBPV) reported for each tissue sample
- Data collection timepoints
  - First day of experiment (as birth proxy) and dates of key events (death, dissection, RNA extraction)

## Data files and key variables
- NER0008751_Obj1_Exp1_aggression_data.csv
  - Rows represent colonies within a behavioural monitoring event
  - Key fields: Date, Count, Col_no, ID, Treatment, Q.Active, Q.Response, buzzing, charging, butting, grappling, stinging, Aggression, Worker_egg
- NER0008751_Obj1_Exp1_arrival_sorting.csv
  - Initial colony info: Arrival_Workers, Queenright?, Sub-group (G1/G2), Treatment, ID
- NER0008751_Obj1_Exp1_death_sheet.csv
  - Longevity data: Day_of_Death, Cause, Number_left, Date_of_death, First_day, Cumulative_deaths, Alive_18_5, Alive_8_7
  - Sub-group details indicate life-history vs TP1G/TP2G sampling
- NER0008751_Obj1_Exp1_dissections.csv
  - Dissection and RNA-sample metadata: Brain_label, Ovary_label, Fat_body_label, date_killed, Extraction_date, Dissection_date, Virus_detected
- NER0008751_Obj1_Exp1_egg_counts.csv
  - Colony egg-laying data: Date, count, Col_no, Treatment, ID, Old_cells, Old_cells_eggs, New_cells, New_cells_eggs, Total_cells, Total_eggs, Eggs_per_cell
- NER0008751_Obj1_Exp1_numbers_sheet_data.csv
  - Workforce dynamics: Date, Count, Col_no, ID, W_add, Removed_aggression, Removed_egglaying, Removed_other, W_removed, W0_dead, 20?
- NER0008751_Obj1_Exp1_queen_stats_print.csv
  - Queen size metrics: Col_no, Thorax_1, Thorax_2, Wing_1, Wing_2, Av_thorax, Av_wing

## Linking and data usage
- Core identifiers for cross-file linkage
  - Col_no: colony identifier (note: source colonies 17, 51, 54, 62 are non-manipulated)
  - ID: composite colony/experimental unit ID encoding Treatment (R/C), Sub-group (R1/R2 or G1/G2), and a unique within-group number
  - Treatment and Sub-group fields enable partitioning by R vs C and TP sampling points (G1/G2)
- Timepoints and sampling alignment
  - TP1 and TP2 designate RNA sampling points aligned with 10% and 60% mortality phases, respectively
  - Life-history data vs TP sampling are distinguished in death_sheet and other related fields
- Potential analyses enabled
  - Longevity and mortality risk by treatment and subgroup
  - Behavioral responses and aggression as a function of treatment and colony dynamics
  - Relationship between colony growth/egg-laying dynamics and longevity
  - Association between RNA-seq tissue data labels (Brain, Ovary, Fat_body) and phenotypic outcomes
  - Validation of SBPV presence across tissues and its potential link to stress or longevity

## Data quality and caveats
- Missing values (NA) present in several fields (e.g., subgroup assignments, some measurement fields)
- Some colonies are designated as source colonies and not experimentally manipulated
- Alive_18_5 and Alive_8_7 indicate survival at specific date checkpoints; careful handling required for censoring in analyses
- Unit and format consistency across CSV files; cross-file integration relies on Col_no and ID

## References and related materials
- Protocol_NER0008751_Objective 1_Experiment 1_v4_2019-03-26.docx (protocol details)
- Collins DH, Prince DC, Donelan JL, Chapman T, Bourke AFG. Queen eusocial insects show costs of reproduction and transcriptomic signatures of reduced longevity. Manuscript (RNA-seq context)

## Practical notes for users
- Start with NER0008751_Obj1_Exp1_death_sheet.csv to assess longevity outcomes and censoring
- Use Col_no and ID to link longevity, behavior, egg counts, and RNA sample metadata across files
- Examine NER0008751_Obj1_Exp1_aggression_data.csv for behavioral patterns relative to treatment and mortality stage
- Integrate RNA-seq related files via Brain_label/Ovary_label/Fat_body_label with TP1/TP2 sampling context from dissections
- Review queen size metrics in NER0008751_Obj1_Exp1_queen_stats_print.csv as potential covariates in longevity analyses