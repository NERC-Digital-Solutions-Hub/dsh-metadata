# Population count data from a resource degradation and temperature variation population dynamics experiment in the Plodia -Venturia host-parasitoid interaction

## Overview
- Supporting information for dataset EIDCHELP-29310; investigates the combined effects of daily stochastic temperature fluctuations and resource degradation on host-parasitoid population dynamics (Plodia interpunctella and Venturia canescens) across multiple generations in microcosms.
- Experimental scope: approximately six host generations in controlled lab conditions, with host-alone and host-parasitoid setups, across a full factorial design of temperature and diet treatments.

## Experimental design and treatments
- Full factorial design:
  - Temperature: Constant (CST) at 26°C vs Variable (VAR) with daily fluctuations around 26°C (26°C ± 1.5°C; AR(1) = 0.02).
  - Resource degradation (Diet): 0, 25, 50, 75% of wheat germ replaced by methyl cellulose.
- Microcosm setup:
  - 3 replicates per combination for both host-alone (Pi) and host-parasitoid (PiVc) microcosms.
  - Total: 48 microcosms (3 replicates × 2 temperature treatments × 2 host treatments × 4 diet levels).
  - Start with 15 male and 15 female fifth instar host larvae per microcosm.
  - PiVc microcosms receive two newly emerged adult parasitoids around weeks 9–13; experiments run for 262 days.
- Monitoring and resource management:
  - Weekly monitoring with replacement of one sixth of the diet; oldest diet section replaced with fresh diet of the same treatment.
  - Data collected from week 9 to week 37, with counts of hosts and parasitoids, as well as developmental stages.

## Data collection and variables
- Population monitoring:
  - Weekly counts of dead adults (Pi and/or Vc) and counts of live hosts and parasitoids from the previous week.
  - Developmental stage counts: Pi instars (L1-L3 and L4-L5) and Pi pupae; Vc pupae counted in PiVc microcosms.
- Diet and observations:
  - Diet section replacement, with counts taken from the replaced section (half-section a or b).
  - Observers recorded who performed diet replacement and counts.
- Time indexing:
  - Experimental_week and Experimental_day (from the start of the experiment).
  - Monitoring_week (week from the start of population monitoring).
- Data structure:
  - Population_code encodes species (Pi or PiVc), temperature treatment (Cst or Var), and diet level (0–75).
  - Population_Replicate identifies the replicate within each treatment combination.
- Quality control:
  - Data entry checks with rechecking of outliers during initial analysis.

## Datasets and schema
- VariableTemperatureTimeSeries_DQE.csv
  - Key fields: DAY, Date, Week, Temp.
- Pop-counts-data_DQE.csv
  - Key fields include:
    - Date, Population_code, Population_observation, Treatment, Population_Replicate
    - Temperature, Diet, Species
    - Experimental_week, Experimental_day, Monitoring_week
    - Section_replaced
    - Number_dead_Pi, Number_dead_Vc
    - Number_Pi_L1-L3_instars, Number_Pi_L4-L5_instars
    - Number_Pi_pupae, Number_Vc_pupae
    - Observer_Diet-AdultsCounts, Observer_LarvalCounts
    - Comments
- Notes:
  - Population_code consolidates species, temperature, and diet treatment; three replicates per microcosm type × temperature × diet combination.

## Data quality and governance
- Quality assurance:
  - Errors checked during data entry; outliers rechecked in early analyses.
- Methodological provenance:
  - References linked to experimental design and data interpretation: Begon, Sait & Thompson (1995); Boots (2011); Cameron, Wearing, Rohani & Sait (2007).
- Metadata and discoverability:
  - Dataset includes detailed variable definitions, units, and coding schemes to facilitate reuse and replication.

## Usage considerations and potential analyses
- Suitable for examining how thermal variability and resource quality influence population dynamics, developmental stage distribution, and host–parasitoid interactions under controlled conditions.
- Enables time-series analyses across multi-generational scales and comparative analyses between Pi and PiVc dynamics.
- Limitations:
  - Laboratory microcosm context may limit generalizability to natural systems.
  - Some granularity is tied to diet section counts; consider potential missing data or section-level nuances when modeling.