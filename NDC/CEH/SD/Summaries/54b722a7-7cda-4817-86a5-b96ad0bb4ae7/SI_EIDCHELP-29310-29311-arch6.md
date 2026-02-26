# Supporting Information for data deposit EIDCHELP-29310

## Overview
- Experimental study of how daily stochastic temperature fluctuations and resource degradation affect a host-parasitoid system: Plodia interpunctella (host) and Venturia canescens (parasitoid).
- Multi-generation microcosm experiment spanning ~ six host generations, about 262 days.
- Factorial design with two temperature treatments and four levels of host-resource degradation.

## Experimental Design and Setup
- Species and origin:
  - Plodia interpunctella (Pi) as host; Venturia canescens (Vc) as parasitoid (parthenogenetic strain).
  - Hosts from laboratory stock; parasitoids from a laboratory parthenogenetic strain.
- Microcosms:
  - 48 total microcosms: 3 replicates for each combination of microcosm type (host alone Pi vs host-parasitoid PiVc), temperature treatment, and resource degradation level.
  - Each microcosm started with 15 male and 15 female fifth instar Pi larvae in 83 g of resource.
  - Containers: 175 × 116 × 60 mm.
  - Initial conditions: constant 26°C for all microcosms until the first cohort of 30 host larvae pupated; then assigned to their designated temperature treatment.
  - Monitoring period: weekly counts from week 9 to 37 of the experiment.
- Diet and resource degradation:
  - Diet degraded by replacing 0, 25, 50, or 75% of wheat germ with methyl cellulose (indigestible bulking agent).
  - Diet percentages expressed as 0, 25, 50, 75.
- Parasitoid introduction:
  - In PiVc microcosms, two newly emerged adult parasitoids added after the initial host development (week 13) when fourth and fifth instars were present across treatments.
- Maintenance schedule:
  - Each week from week 9 to 37, the oldest diet section replaced; one sixth of resource replenished with fresh diet of the same treatment.
  - Monitoring included removal and counting of dead adults; counting of hosts (early L1-L3 and late L4-L5 instars), host pupae, and parasitoid pupae in half-diet sections.

## Treatments and Conditions
- Temperature:
  - Constant (Cst): mean 26°C with no fluctuation.
  - Variable (Var): daily temperature fluctuates around 26°C with a range from 22.3°C to 30.2°C (26°C ± 1.5°C SD; AR(1) = 0.02; 95% CI [-0.10, 0.14]).
- Resource degradation (Diet):
  - 0, 25, 50, 75% of the host diet replaced by methyl cellulose.
- Design layout:
  - Fully factorial across: microcosm type (Pi vs PiVc), temperature (Cst vs Var), and diet level (0, 25, 50, 75), with 3 replicates each.

## Data Collected and Files
- VariableTemperatureTimeSeries_DQE.csv:
  - Variables: DAY (day in temperature time series), Date, Week (experimental week), Temp (temperature in °C).
- Pop-counts-data_DQE.csv:
  - Population_code: combines species (Pi or PiVc), temperature treatment (Cst or Var), diet level, and replicate.
  - Other fields: Date, Population_observation (unique per Population_code and week), Treatment (Pi vs PiVc, temperature, and diet), Population_Replicate, Temperature, Diet, Species, Experimental_week, Experimental_day, Monitoring_week, Section_replaced, Number_dead_Pi, Number_dead_Vc, Number_Pi_L1-L3_instars, Number_Pi_L4-L5_instars, Number_Pi_pupae, Number_Vc_pupae, Observer_Diet-AdultsCounts, Observer_LarvalCounts, Comments.
  - Notes: Monitoring occurred weekly from week 9; the dataset captures counts from half-diet sections where old diet was replaced.
- Population_code encoding:
  - Indicates temperature: 'Cst' or 'Var'.
  - Indicates diet level: 0 to 75 (percent replacement).
  - Replicate: 1–3.

## Data Quality and Documentation
- Quality control:
  - Data entry checks performed; outliers rechecked during initial analysis.
- References informing methods:
  - Begon, Sait & Thompson (1995) on parasitoid-host refuges and generation cycles.
  - Boots (2011) on resource effects on parasite resistance evolution.
  - Cameron, Wearing, Rohani & Sait (2007) on resource effects in interspecific interactions.

## Key Considerations for Data Use
- Temporal structure:
  - Experimental_week and Monitoring_week provide alignment between the experimental timeline and population monitoring.
- Hierarchical tracking:
  - Population_code and Population_Replicate enable separation of replicates within each treatment combination.
- Data integration:
  - VariableTemperatureTimeSeries_DQE.csv provides the precise temperature regime per microcosm, needed to link temperature exposure with population dynamics in Pop-counts-data_DQE.csv.
- Biological context:
  - Pi alone vs PiVc dynamics allow inference on how parasitism interacts with temperature stress and resource degradation.
- Potential analyses:
  - Assess impacts of temperature regime and diet on host survival, development stages, and parasitoid success across generations.
  - Explore interaction effects between temperature variability and resource degradation on host-parasitoid dynamics.