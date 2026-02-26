# NERC project NE/R000875/1, Objective 1, Experiment 1: ReadMe document for data files

## Purpose and experimental question
- Document describes data collected to test whether experimentally increased reproduction in Bombus terrestris queens incurs a longevity cost.
- Experimental design divides colonies into two treatments:
  - Removal (R): eggs removed and counted to induce higher fertility and higher potential costs of reproduction.
  - Control (C): eggs removed, counted, and replaced to control for disturbance from egg removal.
- Additional measurements:
  - Worker aggression toward the queen and queen activity are recorded and workers displaying aggression are removed to avoid confounding effects on colony fertility and queen longevity.
  - Locomotory activity and disturbance response are tracked as indicators of ageing.
  - RNA sequencing (mRNA) sampling at two timepoints corresponding to mortality phases: TP1 at 10% mortality and TP2 at 60% mortality within each treatment.
- References for protocol and related manuscript provided.

## Experimental setup and key concepts
- Treatments:
  - R: egg removal (increases worker egg-laying and aggression toward the queen).
  - C: egg removal with replacement (control for disturbance).
- Sub-groups:
  - G1 and G2 designate sampling points for RNA at 10% and 60% mortality, respectively, within each treatment.
  - Some colonies are designated as Extra (E) colonies.
- Source colonies: 17, 51, 54, 62 used as source and not experimentally manipulated.
- Data scope includes behavioural observations, colony initial sizes, survival/longevity data, dissection/mRNA sampling details, egg counts, worker turnover, and queen morphology measurements.

## Data files included (CSV format) and what they contain
- NER0008751_Obj1_Exp1_aggression_data.csv
  - Records worker aggression and egg-laying behavior during 10-minute observation periods every four days, plus queen movement and disturbance response.
  - Key columns: Date, Count, Col_no, ID, Treatment, Q.Active, Q.Response, and counts of buzzing, charging, butting, grappling, stinging; Aggression total; Worker_egg.
- NER0008751_Obj1_Exp1_arrival_sorting.csv
  - Initial colony sizes, queen status on arrival, and sub-group/treatment assignments.
  - Key columns: Arrival_Workers, Queenright?, Sub-group, Treatment, ID.
- NER0008751_Obj1_Exp1_death_sheet.csv
  - Queen longevity data (natural death, censoring, or harvest for RNA). 
  - Key columns: Day_of_Death, Cause, Number_left, Date_of_death, First_day, Cumulative_deaths, Alive_18_5, Alive_8_7.
- NER0008751_Obj1_Exp1_dissections.csv
  - Details of queens removed for dissection and RNA extraction; includes tissue-specific RNA sample IDs and virus detection status.
  - Key columns: Brain_label, Ovary_label, Fat_body_label, date_killed, Extraction_date, Dissection_date, Virus_detected.
- NER0008751_Obj1_Exp1_egg_counts.csv
  - Colony-level egg counts over time; records old/new eggs and cells, totals, and derived metrics.
  - Key columns: Old_cells, Old_cells_eggs, New_cells, New_cells_eggs, Total_cells, Total_eggs, Eggs_per_cell; plus date, Col_no, Treatment, ID.
  - Note: Eggs_per_cell computed as Total_eggs / Total_cells; '*' denotes null values due to zero Total_cells.
- NER0008751_Obj1_Exp1_numbers_sheet_data.csv
  - Worker turnover data: additions and removals throughout the experiment.
  - Key columns: Date, Count, Col_no, ID, W_add, Removed_aggression, Removed_egglaying, Removed_other, W_removed, W0_dead, 20?.
- NER0008751_Obj1_Exp1_queen_stats_print.csv
  - Size measurements for queens: thorax width and marginal cell width from two measurements each; averages calculated.
  - Key columns: Thorax_1, Thorax_2, Wing_1, Wing_2, Av_thorax, Av_wing; Col_no.

## Data structure and identifiers
- Row definitions: Each row typically represents a colony within a behavioural monitoring event, a dissection, an egg-count event, or a timepoint in longevity tracking, depending on file context.
- IDs and subgroups:
  - IDs encode treatment (T for removal, C for control) and subgroups (R1, R2; G1, G2 for RNA sampling points).
  - Extra colonies prefixed with E.
- Subtle distinctions:
  - G1/G2 specify mortality-phase-based sampling for RNA (TP1 at 10% mortality, TP2 at 60% mortality).
  - Life-history vs. TP1G/TP2G annotations appear in death-related data to denote whether longevity data or RNA sampling occurred.

## Data provenance and references
- Protocol and details available in:
  - Protocol_NER0008751_Objective 1_Experiment 1_v4_2019-03-26.docx
  - Collins DH, Prince DC, Donelan JL, Chapman T, Bourke AFG. Queen eusocial insects show costs of reproduction and transcriptomic signatures of reduced longevity. Manuscript.
- Data files described with column-by-column detail; each table begins on a new page in the ReadMe.

## How these data can be used (analytical ideas)
- Assess whether egg-removal treatment (R) correlates with reduced queen longevity or higher mortality, compared with control (C).
- Examine whether increased reproductive effort (egg removal) associates with higher worker aggression toward the queen and changes in queen activity.
- Link behavioural metrics (Aggression, Q.Active, Q.Response) to longevity outcomes and mortality timing.
- Explore how egg-laying dynamics (Eggs_per_cell, Total_eggs) relate to queen lifespan and colony stability.
- Use RNA sampling timepoints (TP1, TP2) to compare gene expression signatures between mortality phases and treatments; integrate with virus detection (SBPV) status from dissections.
- Analyze colony-level dynamics: initial colony size, queenright status on arrival, and subsequent changes in worker turnover and survival.

## Notes and cautions for analysts
- Data are split across multiple files with consistent colony identifiers (Col_no, ID) but ensure proper joins on treatment, sub-group, and mortality phase.
- Some fields contain NA values; interpret cautiously and consider data imputation or sensitivity analyses where appropriate.
- Source colonies (17, 51, 54, 62) are not experimentally manipulated, so they may serve as controls for baseline characteristics but are not part of the experimental treatment effect estimation.
- Data are linked to specific protocol and manuscript; cross-reference for definitions of life-history categories and RNA sampling timing.