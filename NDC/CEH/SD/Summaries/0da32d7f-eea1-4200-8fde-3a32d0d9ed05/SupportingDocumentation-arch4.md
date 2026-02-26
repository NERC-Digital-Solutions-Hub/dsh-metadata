# Supporting Documentation Ecologically relevant radiation exposure triggers elevated metabolic rate and nectar consumption in bumblebees

## Overview
- Reports a set of datasets from a study on how ionising radiation exposure affects bumblebee energy budgets, focusing on nectar consumption, metabolic rate, and activity.
- Conducted at the University of Stirling using a Cs-137 gamma radiation setup with dose rates from 0 to 192 μGy hr-1.
- Experimental design spans 30 days with three 10-day phases: no radiation, radiation, and recovery.
- Data collected include feeding (nectar volume), metabolic rate (CO2 output), movement/behaviour, body metrics, thorax temperature, and environmental conditions.

## Datasets included
- metabandsuc.csv (31 KB)
  - Single-measurement per bee across 30 days; 25 columns.
  - Dose rates: 0, 40, 100, 200 μGy hr-1.
  - Measures: nectar consumption (two feeders), CO2 production, activity, temperature, humidity, bee weight, age, phase, colony, and movement metrics.

- appetiteexp2metabfin.csv (2.4 MB)
  - Repeated measurements per bee across entries; 20 columns.
  - Same experimental structure and dose rates as metabandsuc.csv.
  - Includes dose rate, bee ID, mass, age, nectar consumption, thorax temperature, dry weight at end, and survival/phase data.

- movementdatafin.csv (92 KB)
  - Subset of 60 bees used for metabolic rate analysis; 11 columns.
  - Movement categories: sitting, waving, walking, buzzing; includes duration, distance, activity state, and phase.

- apet ite.csv (19 columns)
  - Experiment 2: dose-rate threshold of radiation effect on nectar consumption; 141 bees.
  - Dose rates 0–192 μGy hr-1; measurements over 30 days.
  - Variables: dose rate, bee ID, age, body mass, nectar concentration, thorax temperature, live weight, cadaver dry weight, days in experiment, cohort, and ambient/environmental measurements (temperature, humidity).

## Experimental design and data collection
- Two cohorts: cohort 1 (n=148) begins at day 1; cohort 2 (n=140) joins at day 10.
- Three 10-day phases per bee: no radiation, radiation, recovery.
- Data collected every 2 days for feeding and mass; CO2 production measured in a subset during days 7 and 9 of radiation and recovery phases.
- Movement data collected for a subset during metabolic rate assessments.
- Bee housing: individual containers with ad libitum pollen and 40% sucrose nectar; environmental conditions recorded.

## Data structure and variables (highlights)
- Datasets provide extensive metadata per bee, including:
  - Identification: bee ID, colony, cohort (where applicable)
  - Treatment: dose rate (μGy hr-1)
  - Time: phase, day within phase, overall day
  - Phenotypic: mass/weight, age, thorax temperature, dry weight
  - Behavior: nectar consumption (ml), CO2 output (μmol/min), movement metrics (duration, distance), activity status
  - Environment: temperature and humidity (facility and recorded periods)
  - Outcomes: phase-specific metrics, survival/death data

## Relevance for Data Leaders
- Demonstrates integration of multi-modal data (feeding, physiology, behavior, environment) to study a system-wide question.
- Rich longitudinal design with multiple cohorts enables temporal and dose-response analyses.
- Clear documentation of data collection protocols, variable definitions, units, and structure supports data discoverability and reuse.
- Potential for cross-dataset analyses (e.g., linking nectar intake with metabolic rate and movement) and meta-analyses across similar radiobiology studies.

## Data quality, standards, and governance considerations
- Consistency of units and terminology across datasets (e.g., μGy hr-1, ml, g, °C, % humidity) is essential for integration.
- Metadata completeness: ensure data dictionaries, column definitions, and measurement protocols are centralized and versioned.
- Data provenance: document collection dates, equipment (IRGA model), and facility settings to support reproducibility.
- Data quality checks: address repeated measures per bee, cohort differences, and phase transitions to avoid misalignment in analyses.
- Access and licensing: establish clear data licenses, usage rights, and stable identifiers to enable sharing within the wider bee-ecology research community.

## Practical next steps for leveraging these assets
- Create a centralized data catalog entry for each dataset with a machine-readable data dictionary, units, and provenance.
- Harmonize column names and units across metabandsuc.csv, appetiteexp2metabfin.csv, movementdatafin.csv, and apet ite.csv for seamless integration.
- Document cohort and phase metadata explicitly to support stratified analyses (e.g., phase-specific dose-response).
- Develop reproducible analysis pipelines (scripts/notebooks) that handle multi-dataset joins, time alignment, and covariate adjustments (temperature, humidity).
- Assess data quality gaps and plan supplemental collection or imputation strategies if re-use across studies is anticipated.
- Engage with the data community to establish best practices for radiation-ecology datasets and potential cross-study meta-analyses.