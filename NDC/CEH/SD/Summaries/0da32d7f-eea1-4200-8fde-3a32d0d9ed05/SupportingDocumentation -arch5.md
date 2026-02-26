# Supporting Documentation Ecologically relevant radiation exposure triggers elevated metabolic rate and nectar consumption in bumblebees

## Overview
- A set of ecologically focused radiation-behavior experiments on bumblebees conducted at the University of Stirling.
- Four CSV datasets capturing feeding, metabolic rate, activity, movement, temperature, and mass data across 30 days with three phases: no radiation, radiation, and recovery.
- Dose rates ranged from 0 to 200 μGy hr-1 (and up to 192 μGy hr-1 in one dataset); two cohorts participated in the experiment.
- Primary aim: understand how ionising radiation affects bumblebee energy budgets, feeding, and activity; datasets are collected under an IAPETUS DTP PhD project.

## Datasets at a glance

- metabandsuc.csv
  - Size: 31 KB
  - What it contains: nectar consumption, metabolic rate, and activity for 288 bumblebees; each bee measured once per row across the 30-day period.
  - Experimental design: three 10-day phases (no radiation, radiation, recovery); dose rates 0, 40, 100, 200 μGy hr-1; subset measurements of CO2 production and activity for a sample of bees.
  - Data structure: 25 columns including bee ID, dose rate, colony, day, phase, temperature/humidity, initial weight/age, nectar volume (5% and 40%), CO2 output, movement and activity metrics.
  - Data collectors: Jessica Burrows; analysis by Burrows and Matthew Tinsley.

- appetiteexp2metabfin.csv
  - Size: 2.4 MB
  - What it contains: similar measurements to metabandsuc but with repeated entries per bee (longitudinal per-bee records).
  - Experimental design: same phased exposure and dose-rate scheme; two cohorts noted (n=148 and n=140 at different phases).
  - Data structure: 20 columns (dose rate, bee ID, mass/age, nectar concentration access, colony, nectar intake, environmental conditions, activity/metabolic measures, CO2).
  - Data collectors: Jessica Burrows; analysis by Burrows and Tinsley.

- movementdatafin.csv
  - Size: 92 KB
  - What it contains: activity/movement data for a subset of 60 bees focused on CO2 measurements and movement categories.
  - Experimental design: same three-phase radiation experiment; movement categories include sitting, waving, walking, buzzing.
  - Data structure: 11 columns (bee ID, dose rate, video/file ID, observation period, movement category, duration, distance, active/inactive, activity flag, phase).
  - Data collectors: Jessica Burrows; analysis by Burrows and Tinsley.

- apetite.csv
  - Size: 86 KB
  - What it contains: nectar consumption and associated phenotypes for 141 bees across 30 days, across 19 dose-rate treatments (0–192 μGy hr-1).
  - Experimental design: continuous exposure for 30 days; measurements every 2 days; end-of-study dry weight, cadaver weight, thorax temperature, feed concentrations (20, 30, 40, 50%).
  - Data structure: 19 columns including dose rate, bee ID, age/weight, nectar intake, thorax temperature, cadaver dry weight and percent dry weight, colony, environmental conditions.
  - Special data handling: cadaver weights processed to ensure changes were below 1 mg; dataset designed to detect lower dose-rate effects on feeding.
  - Data collectors: Jessica Burrows; analysis by Burrows and Tinsley.

## Data collection and structure details

- Common design elements
  - Bee housing: individual plastic containers with pollen, nectar solution, and nesting materials.
  - Feeding: nectar weighed every two days; some bees exposed to high/low sugar feeders (range 5%–40% or 20%–50% depending on dataset).
  - Metabolic rate: CO2 production measured with infrared gas analyser (IRGA) during selected 5-minute windows (days 7 and 9 in radiation/recovery phases).
  - Movement: video/recordings used to classify movement in a subset of bees.
  - Environment: temperature and humidity recorded around the bees and facility during measurement windows.

- Experimental phases and cohorts
  - Three 10-day phases per bee: pre-radiation, radiation, post-radiation recovery.
  - Dose-rate treatments include multiple levels (0, 40, 100, 200 μGy hr-1, plus additional gradients in appetite-specific dataset).
  - Two cohorts in metabandsuc/appetite datasets; coordinated data collection within University of Stirling facility.

- Instrumentation and measurements
  - IRGA for CO2 measurements; weight measurements of nectar tubes and bees; thorax temperature readings; cadaver dry weight after termination.
  - Data entries include longitudinal day counts, phase labels, colony identifiers, and environmental context (temperature/humidity).

## Provenance and responsibility

- Primary investigator/collector: Jessica Burrows.
- Co-analyst: Matthew Tinsley.
- Institutional context: University of Stirling; IAPETUS DTP PhD studentship support.
- Data are described as generated and analyzed within controlled radiation facility and lab settings.

## Metadata and governance considerations for Data Stewards

- Metadata richness:
  - Each dataset documents: dataset name, size, purpose, data collection methods, responsible personnel, experimental design (phases, dose rates, cohorts), data structure (column definitions), and measurement details.
  - Some datasets provide more granular notes (e.g., duplicates removal in apetite, specific measurement windows for CO2, and feeder concentrations).

- Standards and interoperability:
  - Datasets use consistent units (μGy hr-1 for dose; days for time; ml for nectar; g for weight; °C for temperature), but column names differ across datasets.
  - Cross-dataset mapping will require harmonization of variable names (e.g., dose rate, bee ID, cohort, phase, days) to enable integration.

- Data quality considerations:
  - Deduplication note in apetite.csv; explicit statements about how measurements were conducted and validated.
  - Clear phase delineations and cohort descriptions aid reproducibility but require careful alignment when merging datasets.

- Access, sharing, and preservation:
  - The document does not specify external access restrictions or licensing; stewardship should define data use licenses, access controls, and hosting/repository strategy.
  - Given the longitudinal nature and multiple datasets, implement dataset-level and file-level versioning, along with a data dictionary and provenance records.

- Documentation needs for stewardship:
  - Create unified data dictionaries and a canonical metadata schema covering all datasets.
  - Establish consistent variable naming, units, and categorical encodings.
  - Provide data lineage: experimental protocols, data processing steps (e.g., how CO2 was subtracted from ambient), and any transformations applied.
  - Assign persistent identifiers to bees (where feasible) and maintain cohort and phase mappings across datasets.

## Practical guidance for Data Stewards

- Normalize metadata:
  - Develop a master data dictionary capturing all columns across datasets, including definitions, units, allowed values, and data types.
  - Align phase labels and cohort identifiers to enable cross-dataset joins.

- Ensure reproducibility and discoverability:
  - Archive raw and processed forms with clear provenance, and document any data cleaning steps (e.g., removal of duplicate weight entries, calculation methods for derived metrics like mean CO2).
  - Provide example queries or schemas to facilitate reuse by data users.

- Access and licensing:
  - Clearly state data license, usage permissions, and any embargo or consent considerations.
  - If sharing externally, consider a data portal with dataset previews and a data dictionary.

- Versioning and preservation:
  - Implement version control for datasets and associated metadata; track changes to column definitions or data cleaning rules.
  - Plan long-term preservation, including format stability (CSV) and metadata sustainability.

## Summary of key points for action

- The document outlines four interrelated datasets from radiation impact experiments on bumblebees, including feeding, metabolism, movement, and body condition measures, collected over 30 days with defined radiation phases.
- Data governance needs include harmonizing metadata across datasets, documenting data collection methods and processing steps, and establishing clear licensing and repository strategies.
- Data stewards should focus on metadata standardization, data dictionaries, cross-dataset linkage keys (bee ID, cohort, phase), and robust provenance to support reuse and reproducibility.