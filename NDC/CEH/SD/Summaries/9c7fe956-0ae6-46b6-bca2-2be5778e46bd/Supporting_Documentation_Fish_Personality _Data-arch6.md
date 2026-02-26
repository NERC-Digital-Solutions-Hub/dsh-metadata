# Sex-differences and temporal consistency in stickleback fish boldness

## Overview
- Investigates sex differences and temporal consistency in exploratory boldness in 48 three-spined sticklebacks.
- Measures exploratory behaviour as proportion of time spent out of cover during 1-hour trials across two consecutive test days (Day 3 and Day 4) within four-day cycles.
- Includes data on catch order across two occasions (Catch#1 and Catch#2, nine months apart) to assess short-term sex effects and long-term consistency.

## Subjects and Housing (Data context)
- Subjects: 48 sticklebacks (30 females, 18 males), derived from a non-endangered population; individually identifiable via VIE tags.
- Ethical approvals: Approved as nonregulatory by the Royal Veterinary College Ethics and Welfare Committee.
- Housing: Initially group-housed, then placed in individual 2.8 L tanks within a rack system to standardise feeding and reduce inter-individual motivation differences; temperature 16°C, light regime 8L:16D to minimise breeding-related behaviours.
- Sex determination: Sex revealed post-experiment by temp-induced breeding coloration (increase to 20°C for 3 days).

## Experimental Design and Data Collection (Data collection)
- Catch order (Catch#1 and Catch#2): Net-caught sequentially from holding tanks; Catch#2 recorded nine months after Catch#1 to assess long-term consistency in catching order.
- Exploratory behaviour protocol: Tests conducted in opaque tanks with 15 cm wide lanes, a cover-providing plant, and a feeding tile behind a screen containing bloodworms. Video recorded each test.
- Test cycles: Four days per cycle.
  - Days 1–2: Two bloodworms placed behind the screen; a fish of known identity tested; if eaten, food replaced.
  - Days 3–4: No bloodworms; measure transitions into/out of cover to calculate Proportion of Time Out of Cover (PTOC) as an index of exploration.
- Data handling: Some fish (n=15; 8 females, 7 males) failed to locate food on days 1–2; main analyses exclude these individuals as their exploratory status is uncertain; full-sample analyses also conducted.

## Datasets and Variables (Data structure)
- Data files (8 total) largely in two-column, row-based tabular form:
  - PropTimeOut_DAY3: Proportion of time out of cover on Day 3.
  - PropTimeOut_DAY4: Proportion of time out of cover on Day 4.
  - Ave_PropTimeOut with Catch#1: Mean PTOC across Days 3–4 (two days) with Catch#1 identifier.
  - Data for full sample with Catch#1.
  - Sex differences in Ave_PropTimeOut (n = 10 males, 23 females) across full sample.
  - Data for full sample: Sex differences in Ave_PropTimeOut.
  - Sex differences for catch number (i.e., catch order) (n = 18 males, 30 females).
  - Catch#1 vs Catch#2 data: Order of net-capture nine months apart, enabling longitudinal assessment.
- Each dataset described as 34 rows (including header) with 2 columns; overall, 8 files covering day-by-day, mean aggregates, sex comparisons, and longitudinal catch data.

## Data quality and analysis considerations (Data support perspective)
- Data quality: Standardised housing and procedures to reduce confounding variables; explicit handling of missing data by excluding non-locators from main analyses.
- Measures: PTOC on Days 3–4 as a robust exploration index; repeated measures across days and months to enable temporal and sex-difference analyses.
- Potential outputs: Data products such as dashboards or reports enabling exploration of:
  - Sex differences in PTOC (Day 3, Day 4, and average).
  - Interaction of sex with catch order and longitudinal consistency (Catch#1 vs Catch#2).
  - Subset analyses including and excluding non-solvers (those who failed to locate food).

## Ethical and provenance considerations (Data governance)
- Ethics: Procedures approved by the Royal Veterinary College; non-regulatory status for these procedures.
- Animal welfare: Clear protocols for housing, feeding, and tagging; generation of reproducible data through controlled environmental conditions.
- Provenance: Detailed description of variables and data collection methods enabling re-use and re-analysis.