# NERC project NE/R000875/1, Objective 1, Experiment 1: ReadMe document for data files

## Overview
- Describes data collected in Objective 1, Experiment 1 of the NERC project NE/R000875/1.
- Experimental question: does increased reproduction in Bombus terrestris queens influence longevity?
- Design involves two treatments (Removal vs Control) with subsequent RNA sampling and behavioral monitoring, plus longitudinal longevity and RNA data.
- Data cover behavioral observations, colony demographics, queen longevity, dissections for RNA (brain, ovaries, fat body), RNA sequencing timepoints, and virus detection.

## Experimental design and data scope
- Subjects: young Bombus terrestris colonies; two treatments:
  - Removal (R): eggs removed and counted to induce higher fertility costs.
  - Control (C): eggs removed, counted, and replaced to control for disturbance.
- Subgroups: G1 and G2 determine when RNA samples are taken (10% mortality for G1; 60% mortality for G2).
- Timeline and measurements:
  - Behavioral and locomotion monitoring, with workers removed if displaying aggression toward the queen.
  - Longevity of queens tracked; colony fertility defined by egg counts every two days.
  - mRNA sequencing at TP1 (10% mortality) and TP2 (60% mortality) during the experiment.
  - RNA dissections from queen brain, ovaries, and fat body; SBPV virus detection in samples.
- Sample tagging: multiple colony IDs, with some “source” colonies not experimentally manipulated; explicit treatment and subgroup labeling.

## Data files and key contents
- NER0008751_Obj1_Exp1_aggression_data.csv
  - Behavioral monitoring data (every four days) and queen activity; aggression metrics (buzzing, charging, butting, grappling, stinging) and total aggression; queen movement/response; colony ID and treatment grouping.
- NER0008751_Obj1_Exp1_arrival_sorting.csv
  - Initial colony sizes, queen presence at arrival, subgroup assignment (G1/G2/neither), treatment, and colony IDs.
- NER0008751_Obj1_Exp1_death_sheet.csv
  - Queen longevity data: death date, cause (natural, harvest for RNA, censor), days alive, and survival-related counts.
  - Subgroup annotations include life-history, TP1G, TP2G strands.
  - Alive status on filming dates and cumulative deaths.
- NER0008751_Obj1_Exp1_dissections.csv
  - RNA sampling details: brain/ovary/fat body sample IDs, dissection dates, extraction dates, and virus detection (SBPV present/absent).
- NER0008751_Obj1_Exp1_egg_counts.csv
  - Colony egg counts over time; egg cell dynamics (old/new cells and eggs), eggs per cell, and related counts.
  - Includes old_cells, old_cells_eggs, new_cells, new_cells_eggs, totals, and NA handling.
- NER0008751_Obj1_Exp1_numbers_sheet_data.csv
  - Worker population changes: additions, removals due to aggression/egg-laying/other reasons; remaining workers; dead workers; end-of-period counts.
- NER0008751_Obj1_Exp1_queen_stats_print.csv
  - Queen morphometrics: thorax width and wing width measurements (two readings per metric), with averages computed (Av_thorax, Av_wing).
- All data files use a consistent colony-level ID system (Col_no, ID) and treatment/subgroup coding; Source colonies (17, 51, 54, 62) are designated as non-manipulated.

## Metadata, data quality, and governance
- Data are stored as CSV files with detailed per-column descriptions provided in the ReadMe.
- Key identifiers:
  - Col_no (colony number) and ID (treatment, subgroup, unique colony identifier).
  - Treatment codes: R (egg removal) and C (egg removal with replacement).
  - Subgroup codes: G1, G2, or neither;Extra colonies (E-prefixed IDs).
- Data quality notes:
  - Some NA values present; certain colonies are non-manipulated source colonies.
  - Date fields and life-stage labels enable longitudinal linkage across datasets.
  - "Virus_detected" field indicates SBPV presence in RNA samples.
- Documentation references:
  - Protocol_NER0008751_Objective 1_Experiment 1_v4_2019-03-26.docx for experimental protocol and details.
  - Related manuscript: Collins et al. “Queen eusocial insects show costs of reproduction and transcriptomic signatures of reduced longevity.”

## How this data supports data leadership and strategy
- Data integration and discoverability:
  - Rich, multi-modal dataset linking behavior, demographics, transcriptomics, and morphology through consistent IDs and timepoints.
  - Clear linkage points across files via Col_no and ID to enable cross-dataset joins (behavior, longevity, RNA sampling, dissections, egg counts, and worker dynamics).
- Data governance and metadata quality:
  - Comprehensive column-level definitions facilitate data accuracy, reuse, and validation.
  - Explicit treatment and subgroup labeling supports stratified analyses and reproducibility.
  - Inclusion of raw counts, derived metrics (e.g., eggs per cell, averages of morphometrics), and sampling timepoints aids transparency.
- Data strategy implications:
  - Demonstrates the value of maintaining protocol-linked datasets with integrated metadata to support cross-functional analyses (biology, computational biology, statistics, policy implications in ecology).
  - Highlights potential data access considerations (source colonies, NA values, and laboratory-derived metadata) relevant to building data catalogs and governance practices.
  - Provides a model for documenting complex experimental data with multiple data domains (behavioral, demographic, molecular, and morphological) for future reuse and collaboration.

## Access, references, and provenance
- Primary ReadMe accompanies the data to explain file contents, column definitions, and experimental context.
- For full experimental details, consult:
  - Protocol_NER0008751_Objective 1_Experiment 1_v4_2019-03-26.docx
  - Collins DH, Prince DC, Donelan JL, Chapman T, Bourke AFG. Queen eusocial insects show costs of reproduction and transcriptomic signatures of reduced longevity. Manuscript.