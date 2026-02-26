# Ecologically relevant radiation exposure triggers elevated metabolic rate and nectar consumption in bumblebees

## Purpose and Context
- Investigates how ionising radiation affects bumblebee energy budgets, specifically nectar consumption, metabolic rate, and activity.
- Conducted at the University of Stirling radiation facility to understand ecological relevance of radiation exposure on pollinators.

## Experimental Design
- Setup: 30-day experiment with three 10-day phases per bee (no radiation, radiation, recovery).
- Dose rates: 0, 40, 100, and 200 μGy h-1.
- Cohorts: Two cohorts (first cohort started day 1 with 148 bees; second cohort started day 10 with 140 bees), total approaching 288 bees across datasets.
- Measurements:
  - Nectar consumption weighed every 2 days (two feeders: high and low concentration).
  - Metabolic rate assessed via CO2 production during 5-minute periods (days 7 and 9) for a subset of bees.
  - Movement and activity recorded via video to derive activity metrics (buzzing, walking, etc.).
- Environment: Monitoring of temperature and humidity in the housing and radiation facility; CO2 ambient levels recorded during measurements.
- Data collection and interpretation: Led by Jessica Burrows; analysis by Burrows and Matthew Tinsley; funded under IAPETUS DTP.

## Datasets Summary

- metabandsuc.csv
  - Size: 31 KB
  - Description: Nectar consumed, metabolic rate, and activity for 288 bumblebees across three phases and multiple dose rates.
  - Key structure: 25 columns including bee ID, dose rate (μGy h-1), colony, phase, day, nectar volume (40% and 5% feeders), CO2 output, and movement/active metrics.
  - Purpose: Understand how radiation affects energy budgets and feeding behavior at the individual bee level.

- appetiteexp2metabfin.csv
  - Size: 2.4 MB
  - Description: Repeated measurements of nectar consumption, metabolic rate, and activity for the same experimental setup (two cohorts).
  - Key structure: 20 columns capturing dose rate, bee ID, mass, age, nectar feeder access, colony, nectar volumes, temperature/humidity, phase, cohort, days, CO2 metrics.
  - Purpose: Provide repeated-measures perspective on energy budget responses to radiation.

- movementdatafin.csv
  - Size: 92 KB
  - Description: Movement/activity data for a subset of 60 bees used in metabolic rate analysis.
  - Key structure: 11 columns including bee ID, dose rate, video file ID, observation period, movement category (walking, waving, sitting, buzzing), movement duration, distance traveled, active/inactive status, and phase.
  - Purpose: Characterize behavioral responses and activity patterns under radiation and recovery.

- apet ite.csv (apetite.csv)
  - Size: 86 KB
  - Description: Dose-rate threshold study on bumblebee nectar consumption (Experiment 2) across 141 bees.
  - Key structure: 19 columns covering dose rate, bee ID, weight at entry, age, nectar concentration, thorax temperature, days in experiment, cadaver dry weight, and nectar consumption metrics.
  - Purpose: Identify lower dose-rate thresholds where radiation begins to affect feeding behavior.

- apet ite exp2/metabfin variation (apetiteexp2metabfin.csv)
  - Note: Document references an appetite-related dataset with similar aims to metabent analyses. Primary focus remains on threshold-related feeding and metabolic measures across dose rates.

## Data Collection, Quality, and Access
- Data were generated and curated in a controlled laboratory setting; measurements standardized across cohorts and phases.
- Environmental variables (temperature, humidity) and CO2 levels were recorded to accompany metabolic and feeding data.
- Data provenance emphasizes traceability: experimental work by Jessica Burrows; interpretation by Burrows and Tinsley; broader analyses within the University of Stirling facility.
- Although not explicit in this summary, the documentation emphasizes storing and uploading datasets to appropriate portals, aligning with standard monitoring practices to support data reuse and policy evaluation.

## Relevance for Environmental Monitoring and Policy
- Provides a multi-dimensional, dose-responsive data framework linking radiation exposure to pollinator energy budgets, feeding, and behavior.
- The standardized phase-based design and rich metadata enable:
  - Cross-dataset integration (needing to combine feeding, metabolism, and movement data).
  - Comparative analyses with other environmental stressors affecting pollinators.
  - Transparent data sharing to support scrutiny of environmental health over time and inform policy decisions affecting radiation safety and pollinator conservation.
- Core challenge alignment: enhances value by enabling data integration with other environmental datasets and facilitating broader access to underlying data for scrutiny and reuse.