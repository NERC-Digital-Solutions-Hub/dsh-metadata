# NERC project NE/R000875/1, Objective 1, Experiment 1: ReadMe document for data files

## Overview
- Describes data collected in Objective 1, Experiment 1 of the NERC project NE/R000875/1.
- Aimed to test whether experimentally increased reproduction in Bombus terrestris queens affects longevity.
- Experimental design includes two treatments:
  - Removal (R): eggs removed to increase queen fertility and purported costs to longevity.
  - Control (C): eggs removed, counted, and replaced to control for disturbance.
- Data cover queen longevity, colony behavior (worker aggression, queen movement), RNA sampling for transcriptomics (10% mortality TP1 and 60% mortality TP2), and related measurements.
- All data are in CSV files with per-colony observations and are linked by colony identifiers and treatment groupings.
- Timepoints and groupings:
  - Mortality-based sampling at 10% (TP1, G1) and 60% (TP2, G2).
  - Multiple data collection events include behavioral observations every four days, egg counts, worker additions/removals, and dissection/RNA extraction.

## Data files and contents
- NER0008751_Obj1_Exp1_aggression_data.csv
  - Per colony in behavioural monitoring events (every 4 days; 10-minute observations).
  - Records aggression and queen activity/movement (Q.Active, Q.Response) plus counts of worker aggression (buzzing, charging, butting, grappling, stinging) and overall aggression.
  - Contains: Date, Count, Col_no, ID, Treatment, Q.Active, Q.Response, aggression metrics.

- NER0008751_Obj1_Exp1_arrival_sorting.csv
  - Initial colony size data after arrival, queen status, and sub-group/treatment assignment.
  - Contains: Arrival_Workers, Queenright?, Sub-group (G1/G2 or neither), Treatment (R or C), ID, Col_no.

- NER0008751_Obj1_Exp1_death_sheet.csv
  - Queen longevity data (died naturally, censored, or harvested for RNA).
  - Contains: Day_of_Death, Cause, Number_left, Date_of_death, First_day, Cumulative_deaths, Alive_18_5, Alive_8_7.

- NER0008751_Obj1_Exp1_dissections.csv
  - Details on queens removed for dissection and RNA extraction (24 queens; 12 per treatment; 6 per subgroup).
  - Contains: Brain_label, Ovary_label, Fat_body_label, date_killed, Extraction_date, Dissection_date, Virus_detected.

- NER0008751_Obj1_Exp1_egg_counts.csv
  - Colony egg counts (per count event).
  - Contains: Old_cells, Old_cells_eggs, New_cells, New_cells_eggs, Total_cells, Total_eggs, Eggs_per_cell; includes NA when not applicable.

- NER0008751_Obj1_Exp1_numbers_sheet_data.csv
  - Workers added/removed per colony across events.
  - Contains: W_add, Removed_aggression, Removed_egglaying, Removed_other, W_removed, W0_dead, 20? (final workers).

- NER0008751_Obj1_Exp1_queen_stats_print.csv
  - Queen size measurements (thorax width and wing width) with two measurements each, plus means.
  - Contains: Thorax_1, Thorax_2, Wing_1, Wing_2, Av_thorax, Av_wing.

## Key variables and data structure
- Colony identifiers:
  - Col_no: unique colony number; source colonies (17, 51, 54, 62) not experimentally manipulated.
  - ID: composite ID encoding Treatment (T or C), Sub-group (R1/R2 or G1/G2), and unique colony number.
- Treatments and groupings:
  - Treatment: R (egg removal) or C (egg removal and replacement).
  - Sub-group: G1/G2 for targeted sampling at TP1 (10%) and TP2 (60%), plus potential life-history or NA designations.
- Measurements span:
  - Behavioral observations (aggression metrics, queen activity).
  - Egg-laying and egg-count metrics (colony-level).
  - Worker population dynamics (additions/removals, mortality).
  - Queen longevity (death and censoring details).
  - Morphometrics for queens (thorax and wing sizes).
  - RNA sampling and dissection notes (brain/ovary/fat body tissue labels, dates, and virus detection status).
- Timepoints and events:
  - Observations every four days for behavior.
  - TP1 and TP2 correspond to mortality milestones (10% and 60% mortality phases) for RNA sampling.
  - Date fields and first-day as baseline for age tracking.

## Linking data for GIS-like per-colony analyses
- Core linkage keys:
  - Col_no and ID are the primary keys to join across files for per-colony analyses.
  - Treatment and Sub-group fields contextualize the comparisons across groups.
- Data fusion possibilities:
  - Combine longevity, behavior, egg counts, worker dynamics, and morphometrics to create composite colony profiles.
  - Align behavioral events with dates to analyze spatially-referenced time series if location data is available externally.
  - Integrate RNA/dissection data with corresponding colony IDs to map biological responses to reproductive costs.

## Temporal structure and sampling design
- Observations are time-structured:
  - Behavioral data: every four days during the experiment.
  - TP1 and TP2 RNA sampling correspond to early and late mortality phases.
- Experimental design notes:
  - Source colonies not manipulated; main comparisons among R vs C and within subgroups G1/G2.
  - Data include many NA values indicating missing measurements or non-applicability under certain groupings.

## Data quality and considerations
- Missing data indicated by NA across several fields.
- Some fields reflect event-specific conditions (e.g., only R colonies remove eggs; other fields may be NA for those rows).
- The dataset includes censoring and harvest events affecting queen longevity.
- Virus detection status captured in dissections, enabling potential correlations with physiological data.

## GIS visualization and data product opportunities
- Create colony-level maps if geographic coordinates are available externally by joining on Col_no/ID.
- Generate time-series map layers showing colony outcomes (longevity, queen activity, aggression) across treatment groups.
- Visualize multi-layer per-colony profiles (behavioral activity, egg-laying dynamics, worker population changes, and RNA sampling points).
- Use TP1/TP2 sampling points to annotate temporal layers indicating sampling for molecular analyses and mortality phases.

## References and related documentation
- Protocol_NER0008751_Objective 1_Experiment 1_v4_2019-03-26.docx (protocol details).
- Collins DH, Prince DC, Donelan JL, Chapman T, Bourke AFG. Queen eusocial insects show costs of reproduction and transcriptomic signatures of reduced longevity. Manuscript (context for transcriptomic analyses).