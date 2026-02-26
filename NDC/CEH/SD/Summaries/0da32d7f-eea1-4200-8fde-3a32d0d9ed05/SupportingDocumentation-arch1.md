# Ecologically relevant radiation exposure triggers elevated metabolic rate and nectar consumption in bumblebees

## Overview
- Studies how ionising radiation affects bumblebee energy budgets, focusing on nectar consumption, metabolic rate, and activity.
- Two experiments conducted at the University of Stirling with multiple dose-rate treatments and a recovery phase.
- Data collected include feeding, CO2 production, movement, body mass, thorax temperature, and environmental conditions over 30 days.

## Experimental design

- Experiment 1
  - Phases: three 10-day periods – no radiation, radiation exposure, and recovery (radiation shielded again).
  - Dose rates: 0, 40, 100, 200 μGy hr−1.
  - Cohorts: cohort 1 (n=148) starts at day 1; cohort 2 (n=140) starts at day 10.
  - Measurements: nectar consumption weighed every 2 days; a subset of 30 bees from control and 200 μGy hr−1 group measured for CO2 production and activity during days 7 and 9.
  - Feeding: half the bees received two nectar concentrations (5% and 40% w/v) during radiation and repeated weighings.
  - Outcomes: energy budget-related metrics including nectar intake, metabolic rate, CO2 output, and movement.
- Experiment 2
  - Objective: determine dose-rate threshold for radiation effects on nectar consumption.
  - Dose rates: gradient across 0 to 192 μGy hr−1 (19 treatment levels).
  - Subjects: 141 bees observed for 30 days; measured nectar intake, thorax temperature, and dry weight at termination.
  - Additional measures: cadaver dry weight and percent of dry weight, along with age, weight, and colony origin.

## Datasets overview

- metabandsuc.csv (31 KB)
  - Per-bee data across 30 days; columns include bee ID, dose rate, colony, phase, day, environmental conditions, initial weight and age, nectar volumes from 40% and 5% feeders, CO2 output, buzzing/walking/activity metrics, total active/inactive time, and other movement-related measures.

- appetiteexp2metabfin.csv (2.4 MB)
  - Repeated-measures per bee; 20 columns including dose rate, bee ID, mass at entry, age, feeder access, colony, nectar volumes (40% and 5%), thorax temperature, facility temperature/humidity, phase, days within phase, cohort flag, and CO2-related measures.

- movementdatafin.csv (92 KB)
  - Focused on activity/movement for a subset (60 bees) used in metabolic-rate analysis; 11 columns covering bee ID, dose rate, video file, observation period (phase), movement category, duration, distance, active/inactive times, and phase.

- apetite.csv (86 KB)
  - Experiment 2 nectar consumption dataset; 19 columns including dose rate, bee ID, entry age, nectar concentration, thorax size, start weight, weight changes, age at death, days to death, thorax temperature, cadaver dry weight, dry-weight percent, daily nectar volume from 40% feeder, nectar mass, colony, and facility temperature/humidity.

## Data collection and structure

- Data collection context
  - All data gathered at the University of Stirling; led by Jessica Burrows, with interpretation by Burrows and Matthew Tinsley; part of an IAPETUS DTP PhD project.
  - Data generated and analysed within the radiation facility and associated laboratories.
- Data structure and formats
  - Datasets are CSVs with structured columns detailing per-bee measurements, phase/day indexing, dose rates, environmental variables, and outcome measures.
  - Experiment 1 datasets emphasize single-measure snapshots per bee across days; Experiment 2 includes longitudinal tracking for threshold analysis.
  - Some datasets provide multiple entries per bee (repeat measurements) to enable within-bee analyses.

## Key variables and measurements

- Radiation exposure
  - Dose rate values (μGy hr−1) across low to high ranges; distinct regimes in different datasets (0–200 μGy hr−1 for Experiment 1; up to ~192 μGy hr−1 across 19 treatments in Experiment 2).
- Nectar and feeding
  - Nectar volume consumed per day from 40% and 5% feeders; in some datasets total nectar consumption per day.
- Metabolic and physiological measures
  - Mean CO2 output (μmol/min) during metabolic-rate assessments.
  - Thorax temperature; body mass at entry and changes over time; dry weight measurements in termination.
- Activity and movement
  - Movement categories (walking, buzzing, waving appendages, sitting); duration and distance metrics; active/inactive state during metabolic assessments.
- Temporal/experimental context
  - Phase indicators (pre-radiation, radiation, recovery), day within phase, cohort membership, colony origin.
  - Environmental conditions recorded alongside bee measurements (temperature and humidity in the facility or data logger vicinity).

## Analytical opportunities and considerations

- Dose-response analyses
  - Relate dose rate to nectar consumption, metabolic rate, CO2 output, and activity to identify dose-dependent effects.
- Threshold and phase effects
  - Use Experiment 2 to pinpoint dose-rate thresholds for nectar consumption changes; assess whether effects persist or reverse during recovery.
- Within-bee vs. between-bee comparisons
  - Exploit repeat measurements (apetite.csv) for within-bee analyses; compare across phases and dose rates; cross-validate with metabandsuc and movement datasets.
- Multivariate modeling
  - Combine variables (mass, thorax temp, colony, age) with dose rate to model energy budgets and resource intake under radiation exposure.
- Data quality considerations
  - Different datasets have varying column structures; ensure proper alignment when merging (bee ID, phase, cohort, day indices).
  - Some measurements are subset-based (e.g., CO2 for selected bees), which should be accounted for in analyses.

## Provenance and accessibility

- Data origin
  - Ecologically focused irradiation experiments conducted at the University of Stirling; datasets associated with a PhD project funded through IAPETUS DTP.
- Documentation and metadata
  - Datasets include comprehensive column descriptions and experimental context (phases, dose rates, sampling intervals) to support reproducibility and re-use.