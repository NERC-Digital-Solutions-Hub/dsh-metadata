# Supporting Documentation Ecologically relevant radiation exposure triggers elevated metabolic rate and nectar consumption in bumblebees

## Overview
- Studies how ionising radiation affects bumblebee energy budgets, focusing on nectar consumption, metabolic rate (CO2 production), and activity.
- Two main experimental frameworks:
  - Experiment 1: three 10-day phases (no radiation, radiation, recovery) across dose rates of 0, 40, 100, and 200 μGy hr⁻¹; cohorts of bees observed over 30 days; primary datasets include metabolic/nectar data and movement data.
  - Experiment 2: dose-rate threshold exploration across 19 dose-rate treatments (0–192 μGy hr⁻¹) over 30 days; measures nectar consumption, bee mass, thorax temperature, and dry weight.
- Datasets are designed for linking radiation exposure to feeding, metabolism, and movement, with repeated measures and cohort replication.

## Experiments and Data Collections
- Experiment 1 focuses on energy budgets under radiation with three datasets:
  - metabandsuc.csv: nectar consumption, metabolic rate, and activity measures for individual bees; 30 days; three 10-day phases; dose rates 0–200 μGy hr⁻¹; two cohorts (entering at day 1 and day 10).
  - appetiteexp2metabfin.csv: similar measurements with repeated entries per bee; broader dataset structure to capture repeated observations across the 30-day period.
  - movementdatafin.csv: activity classifications (walking, buzzing, waving appendages, sitting) with CO2/metabolic context; subset of bees (0 and 200 μGy hr⁻¹) across phases.
- Experiment 2 provides appetite-focused data:
  - apetite.csv (note spelling in file): nectar consumption and associated metrics for 141 bees across a gradient of dose rates; includes bee weight, thorax temperature, and dry weight at termination; 30 days with multiple measurements and death/termination tracking.

## Datasets at a Glance (names, sizes, purposes)
- metabandsuc.csv
  - Size: 31 KB
  - Purpose: detailed per-bee records of nectar consumed, metabolic rate, and activity across 30 days and three phases.
  - Key content: dose rate, bee ID, colony, phase, environmental conditions (temperature, humidity), initial weight and age, nectar volumes (40% and 5%), CO2 output, movement-related metrics.
- appetiteexp2metabfin.csv
  - Size: 2.4 MB
  - Purpose: energy-budget related measurements with repeated entries per bee; 30-day period with radiation exposure.
  - Key content: dose rate, bee ID, mass, age, phase and days within phase, nectar consumption, CO2/metabolic context, colony, environmental conditions.
- movementdatafin.csv
  - Size: 92 KB
  - Purpose: movement/activity data for a subset of bees used in metabolic rate analyses.
  - Key content: bee ID, dose rate, video/file identifiers, observation period, movement category, duration, distance, active/inactive timing, and phase.
- apetite.csv
  - Size: 86 KB
  - Purpose: dose-rate threshold exploration for nectar consumption and related metrics.
  - Key content: dose rate, bee ID, age and weight, nectar concentration, thorax temperature, days within experiment, death/termination data, dry weight, and related measurements.

## Data Structure and Common Variables
- Across datasets, common fields include:
  - Dose rate (μGy hr⁻¹)
  - Bee identifiers and cohort information
  - Phase or period within the experiment
  - Time-related measures (days, days within phase)
  - Nectar-related metrics (volume consumed, feeder concentration)
  - Physiological/contextual measures (mass/weight, thorax temperature, ambient temperature and humidity)
  - Metabolic indicators (CO2 output)
  - Movement/activity classifications and timing

## Data Collection Context and Provenance
- Collected and curated by Jessica Burrows; data interpretation by Jessica Burrows and Matthew Tinsley.
- Generated under an IAPETUS DTP PhD studentship; analyses conducted in the University of Stirling radiation facility and laboratory.
- Datasets are designed to support analysis of dose-response relationships and the coupling between radiation exposure and bee energy budgets.

## Practical Guidance for Data Leaders
- Opportunities for cross-dataset integration:
  - Link individual bee data across metabandsuc.csv, appetiteexp2metabfin.csv, movementdatafin.csv, and apetite.csv via bee ID, cohort, and phase to perform integrated dose-response analyses.
  - Assess thresholds of radiative impact on nectar consumption, metabolic rate, and activity patterns.
- Data governance and stewardship considerations:
  - Maintain consistent unit usage and documentation for variables (e.g., dose rate, nectar volumes, temperature/Humidity).
  - Ensure alignment of bee IDs and phase definitions across datasets to enable accurate longitudinal analyses.
  - Leverage cohort and phase metadata to control for potential confounders and to replicate findings.
- Analytical avenues:
  - Dose-response modeling to identify thresholds where radiation begins to affect feeding or metabolism.
  - Energy budget modeling by linking nectar intake to CO2-based metabolic rate across radiation levels.
  - Movement pattern analysis in relation to dose rate and metabolic state.

## Access and Attribution
- Data originate from the University of Stirling radiation facility; provided as supporting documentation with specified file names and descriptions.
- Proper citation of the datasets and acknowledgement of the investigators (Jessica Burrows, Matthew Tinsley) is recommended for reuse.