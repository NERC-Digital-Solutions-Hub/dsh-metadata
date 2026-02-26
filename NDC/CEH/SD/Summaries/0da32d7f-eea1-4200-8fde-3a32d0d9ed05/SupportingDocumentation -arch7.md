# Ecologically relevant radiation exposure triggers elevated metabolic rate and nectar consumption in bumblebees

## Overview
- Describes experiments investigating how ionising radiation affects bumblebee energy budgets, focusing on nectar consumption, metabolic rate, and activity.
- Conducted at the University of Stirling in a controlled radiation facility using a 137 Cs source.
- Two experiments with multiple dose-rate treatments (0–200 μGy hr^-1; up to 192 μGy hr^-1 in one dataset) and 30-day timeframes.
- Data designed for analysis of dose-response relationships and energy expenditure under different radiation exposure conditions.

## Datasets and key variables
- metabandsuc.csv (metabolic rate, nectar consumption, activity)
  - 25 columns per bee: ID, dose rate, colony, day, phase, temperature, humidity, initial weight and age, nectar volumes (40% and 5%), CO2 output, movement and activity metrics, and derived totals (e.g., total active/inactive time, distance walked).
  - Structure: 30 days across three 10-day phases; two cohorts (entering at day 1 or day 10); subset for CO2 measurements (n=30 control, n=30 at 200 μGy hr^-1).

- appetiteexp2metabfin.csv (alternative metabolic/nectar view)
  - 20 columns per bee: dose rate, bee ID, mass and age at entry, nectar concentrations, cohort indicator, nectar volumes, temperature/humidity proxies, phase/day tracking, CO2 metrics.
  - Repeats measurements across the experiment for 288 bees (two cohorts across similar phases).

- movementdatafin.csv (bee activity categories)
  - 11 columns: bee ID, video/file reference, observation period, movement category (sitting, waving, walking, buzzing), movement duration, distance traveled, active/inactive time, activity flag, and phase.
  - Focused on a subset of 60 bees for metabolic-rate analysis at 0 and 200 μGy hr^-1.

- appetite.csv (nectar consumption and body metrics)
  - 19 columns: dose rate, bee ID, entry age, nectar concentration, thorax temperature, start weight, days within experiment, weight changes, death/exit timing, thorax temperature, cadaver dry weight, dry-weight percent, daily nectar volumes (40% feeder), colony, and facility context (two-day temp/humidity logs).
  - 141 bees across 30 days with repeated mass and nectar measurements; final cadaver dry weights measured post-mortem.

## Experimental design and timelines
- Experiment 1: Dose-rate exposure during three 10-day phases
  - Dose rates: 0, 40, 100, 200 μGy hr^-1
  - Two cohorts: starting at day 1 (no radiation) and day 10 (radiation phase)
  - Measurements: nectar consumption every 2 days; CO2 production and movement during days 7 and 9 for a subset
- Experiment 2: Dose-rate threshold assessment
  - 141 known-age workers across 19 dose-rate treatments (0–192 μGy hr^-1)
  - 30-day exposure with nectar concentration treatments (20–50% sucrose)
  - Variables measured: nectar volume, bee weight, thorax temperature; cadaver dry weight upon termination

## Data collection and provenance
- Location: University of Stirling radiation facility
- Methods:
  - Individual bees housed in containers with ad libitum pollen and nectar; weight measurements taken regularly
  - Radiation exposure via ^137Cs source; phases include pre-radiation, radiation, and recovery
  - CO2 output measured with infrared gas analyzer (IRGA) during metabolic-rate assessments
  - Movement recorded via video and categorized; environmental conditions (temperature, humidity) logged nearby
- Personnel and governance:
  - Data collection led by Jessica Burrows; interpretation by Burrows and Matthew Tinsley
  - Part of an IAPETUS DTP PhD project; samples processed in Stirling facilities

## Data structure and accessibility
- Datasets come in CSV format with explicit column definitions per dataset
- Key recurring themes across datasets:
  - Bee identifiers, dose rates, cohort/phase information
  - Temporal markers: days within phase, days since experiment start
  - Physiological metrics: weight, thorax temperature, dry weight
  - Behavioral metrics: nectar intake, CO2 output, movement categories and timing
- Dataset sizes vary from ~92 KB to ~2.4 MB, spanning hundreds of bees and multiple measurement types

## GIS relevance and potential data products
- While the study is lab-based and non-spatial, the data offer GIS-enabled opportunities:
  - Integrate time-series energy-budget data with spatial metadata if location or enclosure coordinates are available (e.g., map dose-rate zones within the facility or colonies tied to origin locations).
  - Create spatially informed visualizations of exposure gradients and resultant metabolic/nectar-consumption responses across a facility map.
  - Develop interactive dashboards showing dose-rate heatmaps, per-bee trajectories (from movement data), and phase-based changes over time.
  - Link to external environmental layers (facility zones, sensor locations) to contextualize temperature/humidity influences.
- Data preparation needs for GIS use:
  - Standardize variable naming across datasets; align time references (days, phases) for cross-dataset joins.
  - If possible, attach geographic or zone identifiers to each bee or cohort to enable spatial analyses.
  - Ensure consistent handling of repeated measures and cohort splits to support longitudinal mapping.

## Notes, limitations, and considerations
- The data originate from controlled lab experiments, limiting natural variability and geospatial heterogeneity.
- Some datasets have naming inconsistencies (e.g., appet ite vs appetite) that require harmonization before integration.
- Two cohorts and multi-phase design require careful alignment during analyses to avoid confounding phase effects with dose-rate effects.
- Potential for richer GIS applications if spatial metadata (locations, enclosure mapping, or colony origins) is incorporated or linked.