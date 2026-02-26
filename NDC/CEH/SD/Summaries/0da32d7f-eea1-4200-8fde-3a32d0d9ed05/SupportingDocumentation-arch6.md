# Ecologically relevant radiation exposure triggers elevated metabolic rate and nectar consumption in bumblebees

- Overview
  - Describes a set of datasets from experiments examining how ionising radiation affects bumblebee energy budgets, focusing on nectar consumption, metabolic rate, and activity.
  - Two experiments:
    - Experiment 1: Effects of radiation on feeding, metabolism, and activity across three 10-day phases (no radiation, radiation, recovery) with dose rates 0, 40, 100, 200 μGy/hr.
    - Experiment 2: Dose-rate threshold effects on nectar consumption across a gradient of dose rates (19 treatments, 0–192 μGy/hr).
  - Setting and researchers: University of Stirling radiation facility; Jessica Burrows and Matthew Tinsley; data generated under an IAPETUS DTP PhD studentship.
  - Data scope: 30-day experiments with repeated measurements every 2 days for nectar intake, plus additional CO2/Metabolic-rate assessments and movement observations for subsets.

- Datasets (names, size, and purpose)
  - metabandsuc.csv (31 KB)
    - Purpose: Metabolic rate and nectar consumption data for bumblebees exposed to radiation; a subset (n=30 control and n=30 highest-dose bees) had CO2 measurements during days 7 and 9.
    - Key structure: 25 columns including bee ID, dose rate, colony, day, phase, temperature/humidity, bee weight and age, nectar volumes from 40% and 5% feeders, CO2 output, movement/behavior metrics, and activity flags.
    - Experimental details: 288 bees total; two cohorts (cohort 1 starting day 1 with no radiation; cohort 2 starting day 10 with radiation); three 10-day phases.
  - appetiteexp2metabfin.csv (2.4 MB)
    - Purpose: Repeated-measures dataset tracking nectar consumption, metabolic rate, and activity for each bee across the experiment.
    - Key structure: 20 columns including dose rate, bee ID, mass/age, nectar volumes, environmental conditions, phase details, days within the phase, cohort, CO2 measurements.
    - Experimental details: Similar three-phase design; two cohorts; 288 bees; subset CO2 data similar to metabandsuc.csv.
  - movementdatafin.csv (92 KB)
    - Purpose: Movement/activity data for a subset of bees (60 bees) focusing on CO2 measurements and movement categories.
    - Key structure: 11 columns including bee ID, dose rate, video/file ID, observation period, movement category (sitting, waving, walking, buzzing), duration, distance, active/inactive status, and phase.
  - appetite.csv (86 KB)
    - Purpose: Dose-rate threshold investigation for nectar consumption across 141 bees under 19 dose-rate treatments (0–192 μGy/hr).
    - Key structure: 19 columns including dose rate, bee ID, age, feeder nectar concentration, thorax temperature, start and in-experiment weight, days, cadaver dry weight, percent dry weight at death, nectar volume consumed per day, colony, and environmental conditions.
    - Experimental details: Each bee monitored for 30 days; cadaver/dry weight measurements at termination; multiple dose-rate treatments to identify thresholds for feeding effects.

- Experimental design and data structure
  - Subjects: Bumblebees housed individually; two cohorts in Experiment 1; Experiment 2 expands dose-rate treatments.
  - Phases and timeline: Three 10-day phases per bee (no radiation → radiation → recovery) over a 30-day period.
  - Measurements and variables:
    - Nectar consumption: volume per day from 40% and 5% feeders.
    - Metabolic rate: CO2 production via infrared gas analyser; combined with movement/behavior data.
    - Activity: categorized into walking, buzzing, waving appendages, sitting; active vs inactive times; movement durations and distances.
    - Environmental conditions: ambient/ facility temperature and humidity around measurement periods.
    - Bee characteristics: weight at entry, age, thorax temperature (in Experiment 2), and dry weight at death or end of experiment.
    - Dose-rate exposure: precise μGy/hr values; multiple dose-rate treatments in Appetite dataset.
  - Data collection details: Conducted at University of Stirling; CO2 measurements taken with IRGA (PP Systems EGM-4); phase-defined sampling windows; samples analysed in radiation facility and laboratory.
  - Data integration: Datasets include bee identifiers, cohort information, phase and day indicators, facilitating cross-dataset linking for integrated analyses (e.g., linking nectar intake, metabolic rate, and movement to dose rate and phase).

- How this supports data-enabled work
  - Data assets enable self-serve exploration and dashboard-style analyses of how radiation dose affects feeding, energy budgets, and activity patterns in bumblebees.
  - Potential data products:
    - Dose-response dashboards comparing nectar consumption and metabolic rate across dose rates and phases.
    - Survival/weight-change timelines correlated with dose-rate and nectar intake.
    - Cross-dataset models linking thorax temperature, CO2 output, and movement with dose-rate exposure.
  - Data preparation considerations:
    - Harmonize bee IDs, cohorts, and phase labels across datasets for integrated analyses.
    - Handle repeated measures (appetiteexp2metabfin.csv) versus single measurements per bee in metabandsuc.csv.
    - Align time scales (days within the experiment vs days within phases) when combining datasets.

- Notable challenges and considerations for use
  - Patchy or inconsistent timing across measures; ensure alignment of phase/day fields when merging.
  - Multiple data formats and columns across datasets; careful mapping of variables (e.g., nectar volume, CO2, movement) is needed for integrative analyses.
  - Data quality checks around cadaver weight and death timing in appetite.csv to ensure correct interpretation of weight changes.

- Practical takeaway for data support
  - The collection provides a rich, multi-dimensional view of radiation effects on bumblebee energy budgets, with clearly defined phases, dose-rate treatments, and repeated measures.
  - By linking bee-level identifiers, cohorts, phase, and day, analysts can build comprehensive models of how dose rate influences nectar intake, metabolism, and activity, supporting evidence-based data products and further data creation advocacy.