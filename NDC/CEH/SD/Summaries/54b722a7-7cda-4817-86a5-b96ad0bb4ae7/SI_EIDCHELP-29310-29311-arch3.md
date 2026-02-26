# Supporting Information for data deposit EIDCHELP-29310

## Overview
- Presents data from a multi-generation microcosm experiment on population dynamics in a host–parasitoid system: Plodia interpunctella (host) and Venturia canescens (parasitoid).
- Aims to quantify how daily stochastic temperature fluctuations and resource degradation affect population responses over ~6 host generations.
- Experimental system uses laboratory stock cultures with a parthenogenetic parasitoid strain; initial conditions held at constant 28°C before experimental treatments.

## Experimental design
- Full factorial design combining:
  - Temperature: constant (Cst) vs daily variable (Var) around a mean of 26°C.
  - Resource degradation (diet): 0, 25, 50, 75% of wheat germ replaced with methyl cellulose.
- Temperature treatment specifics:
  - Constant: fixed 26°C.
  - Variable: 26°C ± 1.5°C daily, with random daily fluctuations (range 22.3–30.2°C; AR(1) = 0.02; 95% CI [-0.10, 0.14]).
- Experiment duration: 262 days starting from day 1 of the temperature time series.

## Microcosm experiment
- 48 microcosms in total: 3 replicates for each combination of microcosm type, temperature, and diet (Pi, PiVc × Cst/Var × 0/25/50/75).
  - Microcosm types: Pi (host alone) and PiVc (host–parasitoid).
- Setup details:
  - Each microcosm begins with 15 male and 15 female fifth-instar host larvae from stock cultures.
  - Resource amount: 83 g of the assigned diet in each container.
  - Phase 1: kept at 26°C constant until 30 host larvae pupate; then maintained under the assigned temperature treatment.
  - Phase 2: from week 9 onward, 1/6 of resource is replenished weekly by replacing the oldest section with fresh resource of the same treatment.
  - PiVc microcosms: second host cohort allowed to develop to fourth/fifth instars; two newly emerged adult parasitoids added (to each PiVc microcosm) after week 13.
- Monitoring and data collection:
  - Weeks 9–37: weekly removal and counting of dead adults (hosts and parasitoids).
  - Counts performed for host instars (L1-L3 and L4-L5) and host pupae; parasitoid pupae counted in half of each diet section during weekly monitoring.
  - Diet is divided into six sections; counts are taken from half sections (a or b) corresponding to the replaced old diet.

## Datasets and key variables

### dataset VariableTemperatureTimeSeries_DQE.csv
- KEY FIELDS:
  - DAY: day in the temperature time series
  - Date: date of temperature measurement
  - Week: experimental week (0 = seeding as pupae; 1 = adults emerged)
  - Temp: temperature in degrees Celsius

### dataset Pop-counts-data_DQE.csv
- KEY FIELDS:
  - Date: date of population monitoring
  - Population_code: microcosm identifier combining species present ('Pi' or 'PiVc'), temperature treatment ('Cst' vs 'Var'), diet/degradation level (0–75), and replicate
  - Population_observation: unique ID per Population_code and Monitoring_week
  - Treatment: combination of microcosm type, temperature treatment, and diet
  - Population_Replicate: 3 replicates per microcosm combination
  - Temperature: 'Cst' or 'Var'
  - Diet: degradation level (0, 25, 50, 75)
  - Species: 'Pi' (host alone) or 'PiVc' (host–parasitoid)
  - Experimental_week / Experimental_day: timing from experiment start
  - Monitoring_week: week from start of population monitoring (begins week 9)
  - Section_replaced: diet section replaced weekly (6 sections total; oldest section replaced; counts taken from half sections a or b)
  - Number_dead_Pi, Number_dead_Vc: weekly dead counts for host and parasitoids
  - Number_Pi_L1-L3_instars, Number_Pi_L4-L5_instars: counts of early and late host instars
  - Number_Pi_pupae, Number_Vc_pupae: counts of host and parasitoid pupae
  - Observer_Diet-AdultsCounts, Observer_LarvalCounts: staff identifiers for counts
  - Comments: additional field notes

## Data quality and governance
- Quality control: data entry checks and rechecking of outliers during initial analysis.
- Metadata and structure:
  - Explicit, field-level descriptions of dataset contents and variable meanings.
  - Use of coded fields (e.g., Population_code, Treatment) to enable dataset linking and integration.
- Data sharing readiness:
  - Datasets are accompanied by detailed descriptions of experimental design, treatments, and monitoring protocols, enabling reproducibility and transparency.
  - Observational provenance (who performed counts) is recorded to support data governance and accountability.
- Data provenance references:
  - Begon, Sait & Thompson (1995)
  - Boots (2011)
  - Cameron, Wearing, Rohani & Sait (2007)

## Relevance for monitoring frameworks
- Demonstrates a robust approach to environmental health monitoring data:
  - Full factorial experimental design to isolate effects of multiple stressors (temperature variability and resource degradation).
  - Time-series and end-point population metrics enabling trend analysis and model validation.
  - Clear data schema with replicates, treatment codes, and monitoring schedules to support data integration and comparability across studies.
  - Emphasis on data quality control, metadata clarity, and accountability (observer fields) to meet governance standards.
- Practical guidance for monitoring framework authors:
  - Importance of defining explicit dataset codes and comprehensive field dictionaries.
  - Structuring long-term monitoring data with consistent time indexing (week, day) and clear treatment labeling.
  - Balancing data richness (detailed counts) with tractable data management through modular datasets.

## References
- Begon, M., Sait, S.M. & Thompson, D.J. (1995) Persistence of a parasitoid-host system: Refuges and generation cycles. Proceedings of the Royal Society B-Biological Sciences, 260, 131-137.
- Boots, M. (2011) The evolution of resistance to a parasite is determined by resources. American Naturalist, 178, 214-220.
- Cameron, T.C., Wearing, H.J., Rohani, P. & Sait, S.M. (2007) Two-species asymmetric competition: effects of age structure on intra- and interspecific interactions. Journal of Animal Ecology, 76, 83-93.