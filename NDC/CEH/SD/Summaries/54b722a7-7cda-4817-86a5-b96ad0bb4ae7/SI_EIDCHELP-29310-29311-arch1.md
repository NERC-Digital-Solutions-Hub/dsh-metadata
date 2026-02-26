# Population count data from a resource degradation and temperature variation population dynamics experiment in the Plodia -Venturia host-parasitoid interaction

## Overview
- Investigates combined effects of daily stochastic temperature fluctuations and resource degradation on host (Plodia interpunctella) and parasitoid (Venturia canescens) population dynamics.
- System comprises a host-parasitoid interaction studied in multi-generation microcosms.
- Parasitoids are from a parthenogenetic thelytokous strain.
- Experiment spans approximately six host generations and 262 days.

## Experimental design and conditions
- Full factorial design with two temperature treatments and four diet/resource degradation levels.
  - Temperature treatments: constant (Cst) and variable (Var) with mean 26°C; Var fluctuates daily between 22.3°C and 30.2°C (26°C ± 1.5°C SD; AR(1) = 0.02; 95% CI [-0.10, 0.14]).
  - Diet/resource degradation: 0, 25, 50, 75% replacement of wheat germ with methyl cellulose (MC), an indigestible bulking agent.
- Experimental timeframe: starts at day 1, monitoring through week 37, with total duration 262 days.
- Microcosms include host-alone (Pi) and host-parasitoid (PiVc) types.

## Microcosm setup and replication
- Replication: 3 microcosms per treatment combination for each microcosm type, yielding 48 microcosms total (3 replicates × 2 temperature × 2 population types × 4 diet treatments).
- Initialization: each microcosm started with 15 male and 15 female fifth-instar host larvae from stock cultures.
- Conditions: all microcosms initially kept at 26°C until all hosts pupated, then maintained under their assigned temperature treatment.
- Resource management: weekly monitoring involved replacing one sixth of the diet; oldest section replaced with fresh diet of the same treatment.
- Parasitoid introduction: in PiVc microcosms, two newly emerged adult parasitoids added after week 13 when fourth and fifth instars were present in all treatments.
- Data collection: weekly counts of dead adults, host larvae, host and parasitoid pupae; counts of instars (L1-L3 and L4-L5) and host pupae; parasitoid pupae; diet section counts; and observer records.

## Datasets and key variables
- VariableTemperatureTimeSeries_DQE.csv
  - Key fields: DAY (day in temperature series), Date, Week, Temp (temperature in °C).
- Pop-counts-data_DQE.csv
  - Population_code: microcosm ID encoding species (Pi or PiVc), temperature treatment (Cst/Var), degradation level, replicate.
  - Population_observation: unique ID per population observation (based on Population_code and Monitoring_week).
  - Treatment: combined microcosm type, temperature, and diet degradation.
  - Population_Replicate: replicates per microcosm type × temperature × degradation.
  - Temperature, Diet (0, 25, 50, 75), Species (Pi or PiVc).
  - Experimental_week, Experimental_day, Monitoring_week.
  - Section_replaced: diet section replaced weekly (six sections per microcosm; counted in half sections).
  - Counts: Number_dead_Pi, Number_dead_Vc, Number_Pi_L1-L3_instars, Number_Pi_L4-L5_instars, Number_Pi_pupae, Number_Vc_pupae.
  - Observer_Diet-AdultsCounts, Observer_LarvalCounts.
  - Comments: additional notes from monitoring.
- Quality control: data checked for entry errors; outliers rechecked during initial analysis.

## Data collection timeline and procedures
- Microcosms seeded with host larvae; constant 26°C during initial phase (week 1).
- After week 1, assigned temperature treatment implemented; weekly resource replenishment begins after week 8.
- PiVc microcosms receive parasitoids after week 13.
- Weekly counts span weeks 9 to 37 for population metrics.

## Quality and provenance
- Data entry quality checks performed; outliers reexamined during early analyses.
- Data linked to established methodological references for host–parasitoid systems and resource effects.

## References
- Begon, Sait & Thompson (1995) Persistence of a parasitoid-host system: Refuges and generation cycles.
- Boots (2011) The evolution of resistance to a parasite is determined by resources.
- Cameron, Wearing, Rohani & Sait (2007) Two-species asymmetric competition: effects of age structure on intra- and interspecific interactions.

## Potential analytical applications for researchers
- Assess how temperature variability interacts with resource degradation to influence host survival, development stages, and parasitoid success.
- Develop and test population dynamics or stage-structured models under contrasting environmental conditions.
- Explore correlations between environmental time series (temperature) and population outcomes across microcosm treatments.
- Compare host-alone versus host–parasitoid dynamics under identical environmental stressors to quantify parasitism effects under resource and thermal stress.