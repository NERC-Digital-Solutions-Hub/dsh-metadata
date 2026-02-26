# Ecologically relevant radiation exposure triggers elevated metabolic rate and nectar consumption in bumblebees

## Overview
- Describes laboratory studies on how ionising radiation affects bumblebee energy budgets, feeding, metabolism, and activity.
- Two experiments conducted at the University of Stirling radiation facility with controlled dose-rate treatments and 30-day timelines.
- Aims to support data-driven insights that could be represented as map-based data products (GIS-style) by organizing temporal, treatment, and environmental variables.

## Datasets included
- metabandsuc.csv
  - Size: 31 KB
  - Focus: Effect of radiation on feeding (nectar consumption), metabolic rate, and activity
  - Design: Three 10-day phases (no radiation, radiation, recovery); dose rates 0, 40, 100, 200 μGy hr-1; 288 bees across two cohorts (day 1 and day 10); nectar weighed every two days; subset (30 bees per group) with CO2 production measurements over 5 minutes
  - Key variables: bee ID, dose rate, colony, day in phase, phase, temperature/humidity around measurements, initial weight/age, nectar volumes (5% and 40% feeders), mean CO2 output, activity metrics (buzzing, walking, etc.)
- appetiteexp2metabfin.csv
  - Size: 2.4 MB
  - Focus: Repeated-measures nectar consumption, metabolic rate, and activity per bee
  - Design: Same phase structure and dose-rate range; two cohorts totaling 288 bees; measurements repeated across days
  - Key variables: dose rate, bee ID, initial weight/age, cohort indicator, nectar volumes per feeder, CO2 metrics, temperature/humidity around measurements, phase/day, activity indicators
- movementdatafin.csv
  - Size: 92 KB
  - Focus: Bee movement and activity with metabolism data
  - Design: Subset of 60 bees (0 and 200 μGy hr-1); three 10-day phases; movement categories recorded (sitting, waving appendages, walking, buzzing)
  - Key variables: bee ID, dose rate, video/file ID, observation period (phase), movement category, duration, distance, active/inactive indicators
- appetite.csv
  - Size: 86 KB
  - Focus: Dose-rate threshold effects on nectar consumption
  - Design: 141 bees exposed to a gradient of dose rates over 30 days; measured nectar consumption, weight, thorax temperature, and dry weight
  - Key variables: dose rate, bee ID, age at entry, feeder concentration, thorax temperature, start weight, daily/periodic measurements, cadaver dry weight, percentage of dry weight, nectar volume per day, colony, environmental readings (facility temperature/humidity)
  
## Common data schema and variables (GIS-oriented perspective)
- Temporal scope: 30 days with 10-day phases and multiple measurement points (every 2 days; CO2 measurements on select days; 5-minute metabolic-rate windows)
- Treatment dimension: dose-rate as the primary spatially-relevant exposure factor (0, 40, 100, 200 μGy hr-1)
- Spatial/locations within the facility: colonies and individual bee containers serve as discrete locations for aggregation (potential to create micro-environment maps within the radiation facility)
- Key environmental/contextual variables: temperature and humidity (facility and data-logger proximity), phase information (no radiation, radiation, recovery)
- Biological identifiers: bee ID, colony, age/weight at entry, cohort membership
- Response variables suitable for GIS-style visualization: nectar consumption (ml per day), nectar per feeder (5% vs 40%), body metrics (weight, thorax temperature, dry weight), metabolic rate metrics (CO2 output), movement/behavior categories and durations, activity vs inactivity totals

## How these data products can be mapped or visualized (GIS use)
- Time-enabled maps or dashboards showing nectar consumption versus dose rate across colonies and days (per-bee or per-cohort aggregation)
- Choropleth-like visuals of metabolic rate or CO2 output across the facility, by bee-container locations (where container coordinates are defined)
- Visualization of phase transitions (no radiation → radiation → recovery) as animated time layers illustrating changes in feeding or activity
- Layered views combining nectar intake, weight changes, and environmental conditions (temperature/humidity) to identify microclimate effects linked to radiation exposure
- For Experiment 2, dose-rate threshold visualization: mapping nectar consumption and thorax temperature across the dose-rate gradient

## Data quality, provenance, and notes
- Primary data collector and analyst: Jessica Burrows; analysis supported by Matthew Tinsley
- Generated under an IAPETUS DTP PhD studentship; all samples analyzed at the University of Stirling facility
- Datasets vary in structure (different column counts and ordering) but share core concepts: dose rate, bee identifiers, phase/day, environmental context, and response measures
- Spans two experiments with overlapping timelines and measurements; integration requires careful alignment of cohorts, days, and phase labels
- No explicit GIS metadata (geospatial coordinates) provided; opportunities exist to treat facility locations or containers as regional units for micro-mapping within a controlled environment

## Practical considerations for using the data as GIS specialists
- Harmonize columns across datasets to enable cross-dataset joins (bee ID, dose rate, phase, day)
- Create time-enabled layers to visualize changes over the 30-day period
- Define spatial proxies (e.g., container positions within the facility or colony-based groupings) if geographic coordinates are available or can be inferred
- Derive additional variables for mapping (e.g., nectar consumption rate per day, CO2 output per bee per phase)
- Ensure consistent handling of repeated measures and cohort distinctions when aggregating for map visuals