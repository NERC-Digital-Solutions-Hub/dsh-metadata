# Supporting Documentation Ecologically relevant radiation exposure triggers elevated metabolic rate and nectar consumption in bumblebees

## Overview
- Reports on experiments investigating how ionising radiation affects bumblebee energy budgets, nectar consumption, and activity.
- Uses controlled exposure with dose rates from 0 to 200 μGy hr-1 across three 10-day phases: pre-radiation, radiation, and recovery.
- Two experiments conducted with two cohorts of bees (leading to 288 individuals in Experiment 1) and a separate dose-rate threshold study (Experiment 2) with 141 bees.
- Data collected include feeding (nectar consumption), metabolic rate (CO2 production), thorax temperature, movement/behavior, and related environmental conditions.

## Experimental design

### Experiment 1: Effect of radiation on bumblebee feeding, metabolic rate and activity
- Dose rates: 0, 40, 100, 200 μGy hr-1.
- Phases: 10-day no-radiation, 10-day radiation, 10-day recovery.
- Subjects: Two cohorts of bees (n=148 and n=140) comprising a total of 288 individuals.
- Measurements:
  - Nectar consumption (weighed nectar tubes every 2 days; high and low concentration feeders used from radiation phase onward).
  - Metabolic rate: CO2 production measured over 5 minutes for a subset of 30 bees from control and 200 μGy hr-1 groups.
  - Activity: video-recorded movement during CO2 measurements; buzzing, walking, etc.
- Setup: Individual housing in containers with access to pollen, nectar (40% w/v), nesting materials; IRGA for CO2 measurement; environmental data logged (temperature and humidity).

### Experiment 2: The dose-rate threshold of the effect of radiation on bumblebee nectar consumption
- Dose rates: Gradient across 0–192 μGy hr-1 using a 137Cs source.
- Subjects: 141 known-age worker bumblebees; nectar feeder concentrations of 20–50% sucrose.
- Measurements:
  - Nectar consumption and weight (collected every 2 days; dry weight measured at termination).
  - Thorax temperature and bee mass tracked over 30 days.
  - Cadaver dry weight and percent dry weight relative to start weight.
  - Additional metrics: age, days within experiment, cohort status, and phase context.
- Objective: Identify lower dose-rate thresholds where radiation begins to affect feeding.

## Datasets

- metabandsuc.csv
  - Size: 31 KB
  - Description: Data for Experiment 1, recording nectar consumed, metabolic rate, and activity for 288 bees across 30 days and three phases. Variables include bee ID, dose rate, colony, day within phase, overall day, phase, environmental conditions (temperature, humidity), bee attributes (weight, age), nectar intake from both feeders, CO2 output, movement metrics, and activity status.
  - Data structure: 25 columns covering identifiers, dose, cohort/colony, timing, environmental measurements, feeding, metabolism, and activity metrics.

- appetiteexp2metabfin.csv
  - Size: 2.4 MB
  - Description: Experiment 1 data variant where each bee appears multiple times (repeated measures). Contains nectar intake, metabolic rate, and activity data across the same three-phase design and dose-rate treatments as metabandsuc.csv. Variables include dose rate, bee ID, mass at start, age, nectar concentration access, thorax temperature, facility temperature/humidity, phase, days within phase, cohort status, CO2 metrics, and metabolic/feeding measures.
  - Data structure: 20 columns detailing dose, identity, mass/age, nectar access, environmental conditions, timing, cohort, CO2, and metabolism/activity.

- movementdatafin.csv
  - Size: 92 KB
  - Description: Movement/activity data for a subset of 60 bees used for metabolic rate analysis, focusing on motion categories (walking, waving appendages, sitting, buzzing) and associated CO2/phase measurements.
  - Data structure: 11 columns including bee ID, dose rate, video/file identifier, observation period, movement category, duration, distance traveled, active/inactive times, and phase.

- apetite.csv
  - Size: 86 KB
  - Description: Experiment 2 data detailing nectar consumption and related metrics for 141 bees across a gradient of dose rates (0–192 μGy hr-1). Variables include dose rate, bee ID, starting weight, age, nectar concentration, thorax temperature, dry weight at termination, days within experiment, and nectar/CO2-related measurements.
  - Data structure: 19 columns covering dose, identity, age/weight, nectar intake, thorax temperature, dry weight, days, cohort information, and environmental context.

## Data collection and quality considerations
- Standardised housing and feeding conditions; random assignment to dose-rate positions.
- Multiple measurement modalities: nectar weighing, CO2 production via infrared gas analyser, thorax temperature, and video-recorded activity.
- Phased design ensures capture of baseline, exposure, and recovery responses.
- Data are organized with explicit identifiers (bee ID, dose rate, colony), timing (days, phase), and environmental context (temperature, humidity).

## Implications for environmental monitoring and analysis
- Provides standardized, openly structured datasets to assess how ionising radiation at environmentally relevant dose rates can alter pollinator energy budgets and foraging behavior.
- Enables cross-dataset analyses to:
  - Model relationships between dose rate and nectar consumption or metabolic rate.
  - Identify dose-rate thresholds where behavioral or physiological changes emerge (Experiment 2 focus).
  - Correlate environmental conditions with radiation-mediated effects.
- Highlights opportunities to combine these datasets with broader environmental monitoring data (e.g., pollinator health indicators, ecosystem service metrics) to evaluate policy and ecological health performance over time.

## Key considerations for analysts
- Ensure careful handling of repeated-measures data (apetiteexp2metabfin.csv) to avoid pseudoreplication.
- Consider phase context (pre-radiation, radiation, recovery) when modeling dose-response relationships.
- Use the environmental covariates (temperature, humidity) to adjust for confounding in energy-budget analyses.
- Leverage the documented column definitions to harmonize these datasets with other environmental monitoring data portals and metadata standards.