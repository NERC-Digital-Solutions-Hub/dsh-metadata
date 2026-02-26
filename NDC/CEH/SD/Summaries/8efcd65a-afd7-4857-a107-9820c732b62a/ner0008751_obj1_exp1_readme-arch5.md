# NERC project NE/R000875/1, Objective 1, Experiment 1: ReadMe document for data files

## Overview
- Describes data collected in Objective 1, Experiment 1 of the NERC project NE/R000875/1.
- Experimental design: Bombus terrestris queens with two treatments—Removal (R) of eggs to induce higher fertility and costs of reproduction, and Control (C) with egg removal, counting, and replacement to control for disturbance.
- Objectives include assessing queen longevity, worker aggression toward the queen, queen activity, and transcriptomic signatures during mortality phases.
- Data were collected across multiple data streams: behavioural observations, colony demographics, longevity, tissue dissection for RNA, and RNA sequencing at two mortality timepoints (TP1: 10% mortality; TP2: 60% mortality).
- References for protocol and broader context are provided (Protocol_NER0008751_Objective 1_Experiment 1_v4_2019-03-26.docx; Collins et al. Manuscript).

## Data Files Included
- NER0008751_Obj1_Exp1_aggression_data.csv
  - Behavioural data on worker aggression and egg-laying during 10-minute observation periods, collected every four days; includes queen activity and response to disturbance.
  - Key fields: Date, Count, Col_no, ID, Treatment, Q.Active, Q.Response, buzzing, charging, butting, grappling, stinging, Aggression, Worker_egg.
- NER0008751_Obj1_Exp1_arrival_sorting.csv
  - Initial colony sizes, queen status on arrival, and subgroup/treatment assignments.
  - Key fields: Arrival_Workers, Queenright?, Sub-group, Treatment, ID.
- NER0008751_Obj1_Exp1_death_sheet.csv
  - Queen longevity data: natural death, censoring, or harvest for RNA; includes death day, cause, and survival status.
  - Key fields: Day_of_Death, Cause, Number_left, Date_of_death, First_day, Cumulative_deaths, Alive_18_5, Alive_8_7.
- NER0008751_Obj1_Exp1_dissections.csv
  - Data on 24 queens removed for dissection and RNA extraction; tissue- and sample-level labels and collection dates; virus detection status.
  - Key fields: Brain_label, Ovary_label, Fat_body_label, date_killed, Extraction_date, Dissection_date, Virus_detected.
- NER0008751_Obj1_Exp1_egg_counts.csv
  - Colony egg-count events; includes counts, old/new egg-cell data, and derived metrics.
  - Key fields: Date, count, Col_no, ID, Old_cells, Old_cells_eggs, New_cells, New_cells_eggs, Total_cells, Total_eggs, Eggs_per_cell.
- NER0008751_Obj1_Exp1_numbers_sheet_data.csv
  - Workers added/removed during the experiment; daily tallies of additions and removals due to aggression, egg-laying, or other causes.
  - Key fields: Date, Count, Col_no, ID, W_add, Removed_aggression, Removed_egglaying, Removed_other, W_removed, W0_dead, 20?.
- NER0008751_Obj1_Exp1_queen_stats_print.csv
  - Morphometrics for queens: thorax width and marginal cell width measurements; includes averages.
  - Key fields: Thorax_1, Thorax_2, Wing_1, Wing_2, Av_thorax, Av_wing.

## Data Structure, Standards, and Metadata
- All datasets use consistent identifiers to link records across files:
  - Col_no and ID tie data to specific colonies and treatment groups (R1, R2, or C with subgroups).
  - Treatment (R or C) and Sub-group (G1, G2, or neither) encode sampling and experimental conditions.
- Subgroups indicate sampling for RNA at 10% mortality (G1) or 60% mortality (G2) and life-history subsets.
- Data include NA values where information is not applicable or missing (e.g., some colonies designated as source colonies or not sampled for RNA).
- Data provenance is explicit:
  - References to the protocol document and a manuscript outline provide methodological context and enable reproducibility.
  - RNA samples are labeled by tissue type (brain, ovary, fat body) with respective sample IDs, and dates of RNA extraction and dissection are recorded.
- Some colonies (e.g., 17, 51, 54, 62) are designated as source colonies and were not experimentally manipulated, which is important for dataset filtering and analysis.
- Virus screening is included for RNA samples (Virus_detected flag in dissections), enabling contamination checks and metadata completeness.

## Governance, Data Quality, and Stewardship Considerations
- The ReadMe furnishes detailed column-level descriptions for each dataset, supporting data accuracy, consistency, and reuse.
- The presence of protocol and manuscript references supports traceability of methods and data lineage.
- Data are stored with explicit experimental context (treatment, subgroup, colony IDs) to facilitate data discovery, discovery, and governance in data catalogs.
- File-level documentation aligns with good data management practices by providing metadata about sampling times, observational events, and measurement techniques.
- Limitations and caveats to consider during stewardship:
  - Some fields contain NA values; researchers should account for incomplete data in analyses.
  - Large, multi-file datasets require careful cross-file linkage (e.g., via Col_no and ID) to reconstruct per-colony trajectories.

## Practical Guidance for Reuse
- To analyze colony-level trajectories, link across files using Col_no and ID, factoring in Treatment and Sub-group to interpret sampling and experimental conditions.
- Use death_sheet and arrival_sorting to contextualize longevity with initial colony status and queen presence.
- Behavioral and egg-count data (aggression_data and egg_counts) can be aligned with mortality and RNA sampling (TP1/TP2) to explore associations between social dynamics, reproduction costs, and transcriptomic changes.
- Transcriptomic insights should be interpreted with tissue-specific labels (Brain_label, Ovary_label, Fat_body_label) and virus screening results (Virus_detected).
- Ensure filtering out source colonies (not experimentally manipulated) when conducting treatment-focused analyses.