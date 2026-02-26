# Supporting Documentation Ecologically relevant radiation exposure triggers elevated metabolic rate and nectar consumption in bumblebees

- Overview
  - Purpose: Document environmental health monitoring data to understand how ionising radiation affects bumblebee energy budgets, feeding, and activity.
  - Focus: Provide datasets that capture dose-rate–response relationships across multiple physiological and behavioural measures to inform policy decisions and future monitoring.

- Experimental design and scope
  - Settings: Controlled radiation facility at the University of Stirling.
  - Subjects: Bumblebees (two cohorts in Experiment 1; one cohort in Experiment 2 subsets).
  - Dose rates: 0, 40, 100, and 200 μGy h-1 (Experiment 1); gradient up to 192 μGy h-1 across 19 dose-rate treatments (Experiment 2).
  - Phases (Experiment 1 and related datasets): Three 10-day phases per cohort — no radiation, radiation, and recovery (no radiation).
  - Measurements: Nectar consumption (daily or every two days), CO2 production (metabolic rate), movement and activity (video/observational data), thorax temperature, body mass, age, and cohort information.
  - Data collection cadence: Approximately every 2 days for most measurements; CO2 and movement data collected during specific days within radiation/recovery phases.

- Datasets and key measures
  - metabandsuc.csv
    - Purpose: Track nectar consumption, metabolic rate, and activity across bees exposed to different dose rates.
    - Size/structure: 25 columns; individual bee records; three 10-day phases; includes dose rate, colony, days, phase, environmental context (temperature and humidity), nectar volume from two feeders (5% and 40%), and CO2 output.
    - Outcomes: Nectar intake, metabolic rate (CO2), and activity-related metrics (buzzing, walking, etc.), plus total active/inactive time and movement.
  - appetiteexp2metabfin.csv
    - Purpose: Same experimental aim as metabandsuc but with repeated measurements per bee (longitudinal entries for the same individuals).
    - Size/structure: 20 columns; multiple entries per bee across time; includes dose rate, bee ID, mass, age, nectar access, colony, nectar volumes, thorax temperature, facility temperature/humidity, phase and timing details, CO2 metrics.
    - Outcomes: Time-series data linking dose rate to feeding and metabolic responses.
  - movementdatafin.csv
    - Purpose: Characterise movement-related behaviours in a subset of bees during metabolic assessments.
    - Size/structure: 11 columns; bee ID, dose rate, video file ID, observation period, movement category (walking, waving, sitting, buzzing), duration, distance travelled, active/inactive duration, and phase.
    - Outcomes: Movement type and extent as a behavioural proxy for energy expenditure under radiation exposure.
  - apet ite.csv (apetite.csv)
    - Purpose: Investigate dose-rate thresholds for radiation effects on nectar consumption and related traits.
    - Size/structure: 19 columns; includes dose rate, bee ID, weight, nectar concentration, thorax temperature, start weight, days within experiment, daily nectar consumption, colony, ambient facility temperature/humidity, and dry cadaver weights.
    - Outcomes: Nectar intake across a gradient of dose rates; body and tissue measurements at termination to assess effects on survival and health.
  - appetiteexp2metabfin.csv (duplicate context)
    - Purpose/structure: Reinforces longitudinal measurements of nectar consumption, body metrics, and environmental conditions across dose-rate treatments; details align with appetite dataset above.
    - Size/structure: 20 columns (as described), including phase, days within phase, cohort information, and CO2/metabolic indicators.

- Metadata, data handling, and governance
  - Metadata and data quality
    - Datasets include extensive metadata fields (dosage, phase, cohort, age, temperature, humidity, colony, etc.) to support data verification and reuse.
    - Recognizes barriers noted by monitoring-framework professionals: metadata gaps, data silos, and the need for clear data governance and shared standards.
  - Data sharing and openness
    - Data are described for public sharing and reuse, highlighting potential barriers related to sharing raw data and ensuring proper documentation.
  - Data provenance and stewardship
    - Collected and interpreted by Jessica Burrows, within the University of Stirling, under an IAPETUS DTP PhD studentship, with data processing and analysis described.
  - Data structure and consistency
    - Multiple datasets share related variables (dose rate, bee ID, age, phase, environmental context) to enable cross-dataset synthesis, though each dataset has its own schema and column set.

- Implications for monitoring frameworks
  - Indicators of interest for environmental health monitoring
    - Nectar consumption as a proxy for foraging and energy budget under radiation exposure.
    - Metabolic rate via CO2 output as a direct physiological stress indicator.
    - Movement and activity patterns as behavioral energy expenditure metrics.
    - Body mass, thorax temperature, and cadaver weight to assess individual health and potential dose-threshold effects.
  - Experimental design insights for policy monitoring
    - Dose-rate gradient enables identification of thresholds where energy budgets shift significantly.
    - Three-phase design (no radiation, exposure, recovery) supports evaluation of reversibility and resilience.
  - Data governance considerations
    - Emphasizes the need for robust metadata, open data practices, and standardized data structures to facilitate cross-study comparability and policy-relevant analyses.
  - Practical guidance for future monitoring
    - Encourage standardized data collection templates around key indicators (feeding, metabolism, movement, environmental context).
    - Promote transparent data sharing with clear documentation to reduce barriers identified by monitoring framework authors.

- Takeaways for policy and decision-making
  - A rich, multi-dimensional data collection approach provides actionable indicators of how environmental radiative stressors impact pollinator energy budgets and health.
  - The combination of feeding, metabolic, and behavioural data across dose-rate gradients supports nuanced risk assessments and the development of precautionary monitoring thresholds.
  - Addressing metadata quality, data-sharing barriers, and governance will enhance the utility of these datasets for informing future environmental health decisions.