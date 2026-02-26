# NERC project NE/R000875/1, Objective 1, Experiment 1: ReadMe document for data files

- Purpose of the data
  - Data were collected to test whether experimentally increasing reproduction in Bombus terrestris queens imposes a longevity cost.
  - Experimental design: two treatments—Removal (R) where eggs are removed to induce higher fertility costs, and Control (C) where eggs are removed, counted, and replaced to control for disturbance.
  - Across colonies, the study tracked queen longevity, worker aggression towards the queen, colony dynamics, and insect aging effects on locomotion.
  - RNA sampling was performed at two mortality-related timepoints (10% mortality, TP1; 60% mortality, TP2) for transcriptomic analysis; mRNA was collected from brain, ovaries, and fat body.
  - Data files document behavioural, demographic, physiological, and molecular measurements, plus dissection and RNA-seq related metadata and virus screening.

- Experimental design and sampling overview
  - Treatments and subgroups
    - R (egg removal) vs C (egg removal and replacement/control).
    - Subgroups within treatments (G1 and G2) determined RNA sampling timepoints (TP1 at ~10% mortality; TP2 at ~60% mortality); some colonies designated as Extra (E) with unique IDs.
  - Key measurements collected
    - Behavioural data: aggression towards the queen (buzzing, charging, butting, grappling, stinging), overall Aggression, queen activity (Q.Active), and response to disturbance (Q.Response) during 10-minute observation periods every four days while the queen remained alive.
    - Colony dynamics: colony arrival size, queenright status, and ongoing egg-laying (colony egg counts, egg-cell dynamics).
    - Longevity data: days to death, cause of death (natural, harvest for RNA, or censoring), and survival status over time.
    - RNA sampling and dissection: 24 queens dissected for RNA (brain, ovary, fat body); virus screening for SBPV in collected tissues.
    - Morphometrics: queen thorax width and wing marginal cell width, with multiple measurements per queen and calculated averages.
  - Data collection cadence
    - Behavioral monitoring every four days; mortality milestones guide RNA sampling timing; dissection and RNA extraction dates recorded.

- Data files and what they contain
  - NER0008751_Obj1_Exp1_aggression_data.csv
    - Records aggression and activity per colony during observation days.
    - Columns include: Date, Count, Col_no, ID, Treatment, Q.Active, Q.Response, aggression counts (buzzing, charging, butting, grappling, stinging), Aggression, Worker_egg.
  - NER0008751_Obj1_Exp1_arrival_sorting.csv
    - Initial colony size, queenstatus on arrival, treatment/sub-group assignment, ID, and related fields.
  - NER0008751_Obj1_Exp1_death_sheet.csv
    - Queen longevity data: Day_of_Death, Cause (death, harvest, censor), Number_left, Date_of_death, First_day, Cumulative_deaths, Alive_18_5, Alive_8_7.
    - Includes life-history vs RNA-sampling subgroups (G1/G2) annotations.
  - NER0008751_Obj1_Exp1_dissections.csv
    - Details of queens removed for dissection and RNA extraction: brain_label, ovary_label, fat_body_label, date_killed, Extraction_date, Dissection_date, Virus_detected.
  - NER0008751_Obj1_Exp1_egg_counts.csv
    - Egg-laying data by colony per counting event: Old_cells, Old_cells_eggs, New_cells, New_cells_eggs, Total_cells, Total_eggs, Eggs_per_cell, along with Date, count, Col_no, ID, Treatment, etc.
  - NER0008751_Obj1_Exp1_numbers_sheet_data.csv
    - Worker counts and removals over time: W_add, Removed_aggression, Removed_egglaying, Removed_other, W_removed, W0_dead, 20?.
  - NER0008751_Obj1_Exp1_queen_stats_print.csv
    - Queen morphometrics: Thorax_1/2, Wing_1/2, Av_thorax, Av_wing, along with Col_no.
    - Notes missing values where applicable.

- Data provenance, documentation, and references
  - Protocol source: Protocol_NER0008751_Objective 1_Experiment 1_v4_2019-03-26.docx.
  - Publication reference: Collins DH, Prince DC, Donelan JL, Chapman T, Bourke AFG. Queen eusocial insects show costs of reproduction and transcriptomic signatures of reduced longevity.
  - Data capture context: This ReadMe documents the contents and column-by-column definitions for the CSV data files associated with Objective 1, Experiment 1 of NERC project NE/R000875/1.

- Data management and potential reuse
  - Data are organized in clearly described CSV tables with explicit column definitions, enabling standardised data cleaning, verification, and transformation.
  - The files are designed to be integrated with standard environmental health indicators (e.g., colony health, longevity, and molecular signatures) and could be combined with external datasets to assess how environmental stressors influence pollinator reproductive costs and longevity.
  - Observed challenges or opportunities highlighted include increasing dataset value through cross-dataset linkage (e.g., coupling behavioural and longevity data with RNA-seq results) and enabling broader access to underlying data for reuse.