# Supporting Information for data deposit EIDCHELP-29310

- Dataset title: Population count data from a resource degradation and temperature variation population dynamics experiment in the Plodia -Venturia host-parasitoid interaction

## Overview
- Describes a long-term microcosm experiment investigating how daily stochastic temperature fluctuations and resource (diet) degradation affect the population dynamics of Plodia interpunctella (host) and Venturia canescens (parasitoid).
- Data include both temperature time-series and detailed population counts across multiple microcosms and treatments over 262 days.

## Experimental design and treatments
- Multi-generation microcosm study (~6 host generations) using laboratory strains of both species.
- Temperature treatments:
  - Constant (Cst): mean 26°C
  - Variable (Var): daily temperature fluctuates around 26°C (22.3–30.2°C; AR(1) = 0.02)
- Resource degradation (diet) treatments:
  - 0, 25, 50, 75% of wheat germ replaced with methyl cellulose (indigestible bulking agent)
- Full factorial design: 2 temperature treatments × 4 diet levels
- Experiment duration: 262 days

## Microcosm setup and monitoring
- Replicates: 3 replicates per microcosm type per treatment, totaling 48 microcosms (3 × 2 × 2 × 4)
- Start conditions: each microcosm with 15 male and 15 female fifth instar host larvae
- Containers: 175 × 116 × 60 mm, with 83 g of assigned resource
- Protocol:
  - All microcosms start at 26°C until host pupation
  - After week 1, microcosms maintained under assigned temperature treatment
  - Weekly partial replenishment of resource (one sixth replaced)
  - PiVc (host-parasitoid) microcosms: parasitoids added at week 13 after host cohorts reach appropriate instars
- Data collection (weeks 9–37): weekly counts of dead adults, host instars (early L1-L3 and late L4-L5), host pupae, and parasitoid pupae

## Datasets included
- VariableTemperatureTimeSeries_DQE.csv
  - DAY: day in the temperature time series
  - Date: date of temperature measurement
  - Week: experimental week since start
  - Temp: temperature in °C
- Pop-counts-data_DQE.csv
  - Date: date of population monitoring
  - Population_code: microcosm ID encoding species, temperature treatment, diet level, and replicate
  - Population_observation: unique observation ID for each population and week
  - Treatment: combined microcosm type, temperature, and diet
  - Population_Replicate: replicate ID (3 per microcosm treatment)
  - Temperature: Cst or Var
  - Diet: 0, 25, 50, 75 (percent degradation)
  - Species: Pi (host alone) or PiVc (host-parasitoid)
  - Experimental_week: week from experiment start
  - Experimental_day: day from experiment start
  - Monitoring_week: week from start of population monitoring (week 9 onward)
  - Section_replaced: diet section replaced weekly (diet split into halves a/b for counting)
  - Number_dead_Pi: dead host counts
  - Number_dead_Vc: dead parasitoid counts
  - Number_Pi_L1-L3_instars: early host instars
  - Number_Pi_L4-L5_instars: late host instars
  - Number_Pi_pupae: host pupae counts
  - Number_Vc_pupae: parasitoid pupae counts
  - Observer_Diet-AdultsCounts: person performing diet replacement and adult counts
  - Observer_LarvalCounts: person counting larvae and pupae
  - Comments: additional notes

## Key variables and data structure
- Microcosm-centric design: Population_code aggregates species, temperature, diet, and replicate
- Treatments are explicit within the data: Pi vs PiVc, CST vs VAR, and diet degradation level
- Temporal resolution: daily temperature data and weekly population monitoring data
- Rich counts by life stage (larvae instars, pupae) and mortality for both host and parasitoid

## Temporal coverage and data collection
- Temperature time series spans Day 1 onward; 262-day experiment duration
- Population monitoring from week 9 to week 37; weekly observations
- Data quality control: entries checked for errors; outliers rechecked in initial analysis

## Quality control and provenance
- Data entry checks performed; outliers re-examined during early analysis
- References informing experimental design and diet formulation included

## How this data can be used in GIS contexts
- Spatially explicit units: microcosms serve as discrete spatial polygons/points for mapping population dynamics across treatments
- Temporal dynamics: combine Pop-counts-data_DQE.csv with VariableTemperatureTimeSeries_DQE.csv to create spatiotemporal visualizations of host and parasitoid populations under different temperature and diet regimes
- Attribute-rich mapping: use Population_code, Treatment, Diet, and life-stage counts to create thematic maps (e.g., abundance by microcosm, survival rates, stage distributions)
- Data integration: align with external GIS layers or metadata (treatment gradients, experimental layout) for broader ecological or policy-relevant visualizations

## References
- Begon, M., Sait, S.M. & Thompson, D.J. (1995) Persistence of a parasitoid-host system Refuges and generation cycles. Proceedings of the Royal Society B-Biological Sciences, 260, 131-137.
- Boots, M. (2011) The evolution of resistance to a parasite is determined by resources. American Naturalist, 178, 214-220.
- Cameron, T.C., Wearing, H.J., Rohani, P. & Sait, S.M. (2007) Two-species asymmetric competition: effects of age structure on intra- and interspecific interactions. Journal of Animal Ecology, 76, 83-93.