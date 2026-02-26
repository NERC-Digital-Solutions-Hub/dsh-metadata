# NERC project NE/R000875/1, Objective 1, Experiment 1: ReadMe document for data files

## Overview
- Data from Objective 1, Experiment 1 of the NERC project testing whether increased reproduction costs affect longevity in Bombus terrestris queens.
- Experimental design: two treatments
  - Removal (R): eggs removed and counted to induce higher fertility costs.
  - Control (C): eggs removed, counted, and replaced to control for disturbance.
- Monitoring focus: queen longevity, worker aggression toward the queen, queen locomotion and disturbance response.
- Handling: aggressive workers removed to prevent confounding effects on colony fertility.
- Sampling: RNA sequencing at two timepoints representing mortality phases (TP1 at ~10% mortality and TP2 at ~60% mortality) for each treatment.
- Data format: multiple CSV data files with column-by-column metadata and per-row colony-level observations. Protocol and additional details are provided in linked documents and a manuscript.

## Experimental Design and Procedures
- Subjects: young Bombus terrestris colonies allocated to R or C treatments; subgroups within treatments (G1, G2) determine RNA sampling timepoints; some colonies designated as Extra (E) and several source colonies were not manipulated.
- Measurements and events
  - Behavioral monitoring: 10-minute observation periods every four days, recording queen activity, disturbance responses, and worker aggression (buzzing, charging, butting, grappling, stinging).
  - Colony management: removal of workers displaying aggression or egg-laying, and ongoing monitoring of colony size and egg-laying dynamics.
  - Reproduction and longevity: tracking queen longevity and colony fertility (eggs counted bi-daily).
  - Molecular sampling: tissue dissection and RNA extraction for transcriptomic analyses at TP1 (10%) and TP2 (60%) mortality phases.
  - Pathogen screening: virus detection (SBPV) in dissected tissues.
- Data organization: each colony’s data are tracked through multiple stages, including behavior, egg counts, worker dynamics, and RNA sampling.

## Data Files and Contents
- NER0008751_Obj1_Exp1_aggression_data.csv
  - Behavioral data during 10-minute monitoring events (every four days); columns include Date, Count, Col_no, ID, Treatment, Q.Active, Q.Response, and various aggression metrics (buzzing, charging, butting, grappling, stinging) plus Aggression and Worker_egg.
- NER0008751_Obj1_Exp1_arrival_sorting.csv
  - Initial colony state after arrival: Arrival_Workers, Queenright?, Sub-group (G1, G2, or NA), Treatment (R or C), ID. Indicates which colonies were assigned to which subgroups.
- NER0008751_Obj1_Exp1_death_sheet.csv
  - Queen longevity data: Day_of_Death, Cause (death, harvest, censor), Number_left, Date_of_death, First_day, Cumulative_deaths, Alive_18_5, Alive_8_7. Includes sub-group and life-history annotations (e.g., TP1G, TP2G).
- NER0008751_Obj1_Exp1_dissections.csv
  - Dissection metadata for 24 queens (12 per treatment, 6 per subgroup): Tissue sample IDs (Brain_label, Ovary_label, Fat_body_label), date fields (date_killed, Extraction_date, Dissection_date), Virus_detected (SBPV present/absent).
- NER0008751_Obj1_Exp1_egg_counts.csv
  - Colony egg counts: Date, Count, Col_no, ID, Treatment, Old_cells, Old_cells_eggs, New_cells, New_cells_eggs, Total_cells, Total_eggs, Eggs_per_cell. Includes NA where not applicable.
- NER0008751_Obj1_Exp1_numbers_sheet_data.csv
  - Worker numbers and removals: Date, Count, Col_no, ID, W_add, Removed_aggression, Removed_egglaying, Removed_other, W_removed, W0_dead, 20? (remaining workers at period end).
- NER0008751_Obj1_Exp1_queen_stats_print.csv
  - Queen morphometrics: Thorax_1, Thorax_2, Wing_1, Wing_2, Av_thorax, Av_wing, with NA for missing data. Col_no may be NA for some rows.

## Data Semantics and Meta-Data
- Row-level granularity: most datasets describe a colony within a behavioural monitoring event or life-history stage; source colonies (17, 51, 54, 62) were not manipulated.
- ID encoding: prefixes T/C denote Treatment; R1/R2 denote subgroups; E denotes Extra colonies.
- Timepoints and sampling: TP1 and TP2 correspond to 10% and 60% mortality, guiding RNA sampling decisions.
- Key derived metrics: colony fertility (eggs per cell), aggression totals, worming through age-related measurements (e.g., locomotion, activity).
- Data quality notes: NA values indicate missing data; some fields reflect specific life-history categorizations (life-history vs TP1G/TP2G).

## Data Access, Protocols and References
- Primary protocol and context: Protocol_NER0008751_Objective 1_Experiment 1_v4_2019-03-26 (protocol and details supporting methods and data interpretation).
- Related manuscript: Collins DH, Prince DC, Donelan JL, Chapman T, Bourke AFG. Queen eusocial insects show costs of reproduction and transcriptomic signatures of reduced longevity.
- This ReadMe provides schema, column definitions, and guidance for data reuse and verification.