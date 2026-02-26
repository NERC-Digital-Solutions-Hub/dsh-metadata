# Supporting Information for data deposit EIDCHELP-29310

## Overview
- Dataset documents a multi-generation microcosm experiment assessing how daily stochastic temperature fluctuations and host-resource degradation affect population dynamics in a host-parasitoid system (Plodia interpunctella and Venturia canescens).
- Approximately six host generations followed across 262 days, using laboratory stock cultures for hosts and a parthenogenetic parasitoid strain.

## Experimental design and treatments
- Factorial design with:
  - Temperature: Constant (Cst) at 26°C vs Variable (Var) with daily fluctuations around 26°C (22.3–30.2°C; mean 26°C; AR(1)=0.02).
  - Resource degradation (Diet): 0, 25, 50, 75% of wheat germ replaced by methyl cellulose.
- Microcosms: 48 total (3 replicates per combination of microcosm type, temperature, and diet), comprising:
  - Pi: host-alone microcosms
  - PiVc: host-parasitoid microcosms
- Start conditions: Each microcosm initialized with 15 male and 15 female fifth instar larvae on 83 g of designated resource.
- Experimental timeline:
  - Initially held at 26°C constant until host pupation; then maintained under assigned temperature treatment.
  - Weekly monitoring from week 9 to week 37, with a gradual refresh of diet over time.
  - In PiVc microcosms, parasitoids were added after the host cohort reached fourth to fifth instars (around week 13).

## Data collection and monitoring
- Measurements:
  - Weekly counts of dead adults (hosts and parasitoids) after their emergence.
  - Counts of host instars (early L1-L3 and late L4-L5) and host/pparasitoid pupae from half-sections of old diet replaced weekly.
- Diet management: Each microcosm divided into six diet sections; one sixth replaced weekly, with counts taken from half of the replaced section.
- Replication: Three microcosms per treatment combination and per microcosm type (Pi or PiVc).

## Datasets and data structure
- VariableTemperatureTimeSeries_DQE.csv
  - Variables: DAY (day in the temperature time series), Date, Week, Temp (temperature in °C).
- Pop-counts-data_DQE.csv
  - Key fields include:
    - Date, Population_code (encodes species, temperature, diet, replicate)
    - Population_observation (unique ID per population observation per week)
    - Treatment (Pi vs PiVc; temperature; diet)
    - Population_Replicate (3 replicates per treatment)
    - Temperature (Cst vs Var)
    - Diet (0, 25, 50, 75)
    - Species (Pi or PiVc)
    - Experimental_week, Experimental_day
    - Monitoring_week (week from monitoring start, week 9)
    - Section_replaced (diet section counted)
    - Number_dead_Pi, Number_dead_Vc (weekly dead counts)
    - Number_Pi_L1-L3_instars, Number_Pi_L4-L5_instars
    - Number_Pi_pupae, Number_Vc_pupae
    - Observer_Diet-AdultsCounts, Observer_LarvalCounts
    - Comments (additional notes)
- Population_code encoding
  - Combines species (Pi or PiVc), temperature treatment (Cst or Var), diet level (0–75), and replicate (1–3).

## Data quality and provenance
- Data entry checks performed; outliers rechecked during early analysis.
- Linked to established methodological references for parasite-host systems and experimental design (Begon et al. 1995; Boots 2011; Cameron et al. 2007).

## Relevance for environmental monitoring and analysis
- Provides a standardized, long-term dataset linking environmental stressors (temperature variability and resource quality) to population dynamics in a controlled setting.
- Enables cross-study synthesis with other monitoring datasets and supports analyses of how environmental fluctuations influence ecological interactions and policy-relevant indicators.
- Metadata-rich design (treatment codes, weekly monitoring, life-stage counts) supports temporal trend analyses and scenario modeling.

## References
- Begon, M., Sait, S.M. & Thompson, D.J. (1995) Persistence of a parasitoid-host system: Refuges and generation cycles. Proceedings of the Royal Society B-Biological Sciences, 260, 131-137.
- Boots, M. (2011) The evolution of resistance to a parasite is determined by resources. American Naturalist, 178, 214-220.
- Cameron, T.C., Wearing, H.J., Rohani, P. & Sait, S.M. (2007) Two-species asymmetric competition: effects of age structure on intra- and interspecific interactions. Journal of Animal Ecology, 76, 83-93.