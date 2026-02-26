# Supporting Documentation Ecologically relevant radiation exposure triggers elevated metabolic rate and nectar consumption in bumblebees

## Study goals and context
- Investigates how ionising radiation affects bumblebee energy budgets, nectar consumption, metabolic rate, and activity.
- Uses controlled radiation facility experiments at the University of Stirling with three 10-day phases: no radiation, radiation, and recovery.
- Bees exposed to dose rates of 0, 40, 100, and 200 μGy hr-1; measurements include nectar intake every two days, CO2 production, and movement/behavior during specified periods.

## Datasets and contents

- metabandsuc.csv
  - Dataset Size: 31 KB
  - Description: Nectar consumption, metabolic rate, and activity for individual bees over 30 days; each bee appears once; data collected across three 10-day phases and four dose-rate groups.
  - Key Structure: 25 columns including bee ID, dose rate, colony, phase, day, temperature, humidity, body mass, age, nectar volumes (from 40% and 5% feeders), CO2 output, and activity metrics (buzzing, walking, etc.), total active/inactive times, and movement metrics.
  - Data Collection Context: 288 bees total; two cohorts (one entering at day 1, another at day 10); subset of 30 bees per group for CO2 measurements.
  - Purpose: Understand how radiation exposure influences energy budgets.

- appetiteexp2metabfin.csv
  - Dataset Size: 2.4 MB
  - Description: Similar to metabbandsuc but with repeated measurements for each bee entry; covers nectar consumption, metabolic rate, and activity.
  - Key Structure: 20 columns (including dose rate, bee ID, mass, age, nectar volumes, temperature, humidity, phase, cohort flag, CO2 data, etc.).
  - Data Collection Context: Same experimental design and cohorts as metabbandsuc.csv.
  - Purpose: Examine radiation effects on energy budgets with repeated measures per bee.

- movementdatafin.csv
  - Dataset Size: 92 KB
  - Description: Movement activity for a subset of 60 bees used for metabolic rate analysis; categories include walking, waving appendages, sitting, buzzing.
  - Key Structure: 11 columns (bee ID, dose rate, video file ID, observation period/phase, movement category, duration, distance, active/inactive timing, activity flag, phase).
  - Data Collection Context: Focused on movement during CO2 measurements across the radiation and recovery phases.
  - Purpose: Characterize behavioral responses to radiation exposure.

- apetite.csv
  - Dataset Size: 86 KB
  - Description: Nectar consumption data for a broader dose-rate range; 141 bees exposed to a gradient of dose rates over 30 days.
  - Key Structure: 19 columns (dose rate, bee ID, age at entry, feeder nectar concentration, thorax temperature, start weight, daily weight, weight change, life/death status, days to death, thorax temperature, dry cadaver weight, dry weight percent, daily nectar volume from 40% feeder, daily nectar mass, colony, facility temperature/humidity measures around nectar measurements).
  - Data Collection Context: Continuous measurement over 30 days with varied sucrose concentrations (20–50% w/v).
  - Purpose: Identify dose-rate threshold(s) where radiation begins to affect nectar consumption.

## Data collection and provenance

- Location and host institution: University of Stirling radiation facility; data generated under an IAPETUS DTP PhD studentship (Jessica Burrows; data interpretation by Jessica Burrows and Matthew Tinsley).
- Experimental design details common across datasets:
  - Three 10-day phases (no radiation, radiation, recovery).
  - Dose-rate treatments: 0, 40, 100, 200 μGy hr-1 (with earlier experiment including a gradient up to 192 μGy hr-1 in appetite.csv).
  - Bees housed individually; nectar feeding and environmental conditions recorded; CO2 production measured with infrared gas analyser for subsets.
  - Two cohorts in metabandsuc/appetite-related datasets: first cohort entering day 1, second cohort entering day 10.
- Data governance and discovery notes:
  - Data are described with dataset-specific column definitions, units, and sampling details to enable reuse and cross-dataset linking (bee ID, colony, phase, day, dose rate, environmental conditions, and physiological/behavioral measurements).

## Data structure, variables, and standards

- Common variables across datasets:
  - Bee identifiers, dose-rate (μGy hr-1), colony, age/entering age, day/phase indexing, phase labels, temperature (°C), humidity (%), weight (g), nectar volume/mass (ml/g) from various feeders, CO2 output (μmol/min), and activity metrics (time-based and categorical movement).
- Dataset-specific structure highlights:
  - metabandsuc.csv: 25 columns; comprehensive set including multiple time-based metrics for metabolic rate and activity.
  - appetiteexp2metabfin.csv: 20 columns; similar variables with repeated measures per bee.
  - movementdatafin.csv: 11 columns; movement category, duration, distance, active/inactive flags, phase.
  - apetite.csv: 19 columns; dose-rate gradient with thorax temperature, weight changes, dry weight, nectar consumption metrics, and colony/location metadata.
- Units and measurement details:
  - Dose rate: μGy hr-1
  - Nectar: ml (volume) and g (mass)
  - Temperature: °C
  - Humidity: %
  - Time-based metrics: minutes or seconds for movement and CO2 measurements
- Data quality considerations for stewardship:
  - Align bee IDs and cohort identifiers across datasets to enable cross-dataset linkage.
  - Maintain consistent units and definitions for temperature, humidity, nectar measures, and CO2 outputs.
  - Be aware of dataset-specific nuances (e.g., metabandsuc vs appetiteexp2metabfin with repeated measures; movement data subset; cadaver weight calculations in apetite.csv).

## Governance, sharing, and reuse considerations

- Documentation and metadata:
  - Rich data dictionaries are embedded in dataset descriptions (column names and meanings).
  - Clear provenance: contributor names, institution, funding context, and experimental setup.
- Access and reuse guidance for Data Stewards:
  - Ensure datasets are discoverable via standardized metadata (title, dataset size, purpose, variables, units, and collection context).
  - Provide cross-references among datasets for joined analyses (e.g., linking bee IDs, cohorts, phases, and dose rates).
  - Include data quality notes and any data cleaning steps (e.g., cadaver dry weight handling, repeated measurements, or cohort distinctions).
- Potential stewardship challenges to anticipate:
  - Incomplete alignment between datasets with different column structures and measurement schedules.
  - Reconciling differing levels of aggregation (per-bee single entry vs repeated measures).
  - Managing multiple cohorts and phase flags to support longitudinal analyses.
  - Handling varying dataset sizes and file formats when integrating into data portals or catalogs.

## Practical takeaways for reuse and data stewardship

- Use the detailed metadata to link datasets at the bee level across phases and dose-rate treatments.
- Standardize and preserve units across all datasets; maintain the explicit column definitions and data dictionaries.
- Maintain cohort and phase identifiers to enable accurate longitudinal analysis of radiation effects.
- Ensure data provenance is preserved for reproducibility (author, institution, funding, and data collection context).
- Plan for data discovery by cataloguing dataset names, sizes, purposes, and key variables so researchers can assess fit for secondary analyses (e.g., threshold effects, dose-response relationships, and behavioral/metabolic correlations).