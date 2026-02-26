# Metadata for physiology data

- This document describes three linked datasets derived from threespine stickleback experiments examining metabolism, sociability, and temperature preference across geothermal and ambient populations.

## Overview of datasets

- Data are generated from respirometry and behavioral experiments on wild-caught sticklebacks, with populations from geothermal (warm) and ambient (cold) habitats.
- Primary sources: Pilakouta et al. 2020 (metabolic rate under multigenerational warming) and Pilakouta et al. 2023 (sociability and temperature preference under warmer conditions).
- Data include standardized measurements and descriptive metadata to support cross-study analyses and replication.

## Data set 1: Metabolism.csv

- Purpose: Measure whole-body metabolism (standard metabolic rate, SMR) via oxygen consumption (mg O2/hr) in a flow-through chamber over weeks.
- Key variables (six columns):
  - AcclimTemp: acclimation temperature (Celsius)
  - PopTemp: thermal habitat type of origin (Cold or Warm; ambient vs geothermal)
  - Pop: population site code (e.g., Ashn, GTS, CSWY, Myv) with W/C suffix for warm/cold
  - PopPair: sympatric or allopatric designation relative to geographic context
  - Mass: weight of individual (grams)
  - SMR: standard metabolic rate (mg O2/hr)
- Experimental context: threespine sticklebacks from multiple populations; measurements taken over several weeks.
- References: Pilakouta 2020.

## Data set 2: Sociability.csv

- Purpose: Assess sociability by tracking distance to a stimulus shoal in social trials.
- Experimental design: wild-caught fish from geothermal and ambient populations; video-tracked to compute mean distance to shoal over a 30-minute trial.
- Key variables:
  - populationpair: allopatric or sympatric
  - population: population name
  - HabitatTemp: origin habitat (Warm or Cold)
  - Temp: acclimation temperature and testing temperature
  - ID: individual fish identifier
  - trial: trial number (1 or 2)
  - sociability: mean distance to stimulus shoal (cm)
- Standardization: densities across treatment groups were controlled.
- Reference: Pilakouta 2023 (A warmer environment can reduce sociability in an ectotherm).

## Data set 3: temperature preference.csv

- Purpose: Measure temperature preferences in a lab chamber allowing fish to choose between temperatures, over 24 hours.
- Experimental design: wild-caught sticklebacks from geothermal and ambient populations; same observer collected all data to minimize observer bias.
- Key variables:
  - Test date: date of data collection
  - Population: sympatric or allopatric designation
  - Popn: population and habitat combination as in Data set 1
  - TempPref: time spent in a preferred temperature (minutes)
  - LogTempPref: natural log of time spent in the preferred temperature
  - Mass: weight in grams
  - LogMass: natural log of weight
- Data processing: outliers checked; log transformations applied for analysis.
- Reference: Pilakouta 2023 (Geothermal stickleback populations prefer cool water despite multigenerational exposure to a warm environment).

## Common metadata, provenance, and notes for analysts

- Population context: comparisons between geothermal (warm) and ambient (cold) habitats, with sympatric vs allopatric population designations.
- Measurements and units:
  - SMR in mg O2/hr; Mass in grams
  - Sociability in centimeters
  - TempPref in minutes; LogTempPref, LogMass as transformed metrics
- Data quality and collection:
  - Outliers checked in temperature preference data
  - All data collected by the same person in the temperature preference study to control for observer effects
- Integration considerations:
  - Align population codes (Pop, Popn, PopPair) across datasets for cross-variable analyses
  - Consider scaling and transformations (e.g., log) when modeling relationships between physiology, behavior, and temperature preference
  - Potential to combine datasets to examine links among metabolism, sociability, and temperature preference under warming conditions
- Suggested analyses for decision-making:
  - Correlations between acclimation temperature and SMR across populations
  - Effects of habitat type and population pairing on sociability
  - Relationship between temperature preference behavior and metabolic rate or body mass
  - Predictive modeling of how multigenerational exposure to warm environments may influence metabolic, social, and thermal-preference traits
- References for context and replication:
  - Pilakouta et al. 2020 Functional Ecology
  - Pilakouta et al. 2023 Ecology and Evolution
  - Pilakouta et al. 2023 Global Change Biology