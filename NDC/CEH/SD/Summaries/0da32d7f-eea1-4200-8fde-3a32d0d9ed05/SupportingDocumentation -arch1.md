# Ecologically relevant radiation exposure triggers elevated metabolic rate and nectar consumption in bumblebees

## Overview
- Study investigates how ionising radiation affects bumblebee energy budgets, focusing on nectar consumption, metabolic rate, and activity.
- Conducted at the University of Stirling using a controlled radiation facility with Cs-137 sources.
- Key goal: characterise dose-rate effects and potential dose–response relationships on feeding and physiology.

## Experimental design and datasets
- Experimental framework
  - Three 10-day phases per bee: no radiation (baseline), radiation exposure, and recovery (radiation shielded).
  - Dose rates: 0, 40, 100, and 200 μGy h⁻¹.
  - Two cohorts in Experiment 1: cohort 1 (n=148) starts at day 1; cohort 2 (n=140) starts at day 10.
  - Experiment 2 expands dose-rate exploration with a broader dose-rate gradient.
  - Measurements include nectar intake, metabolic rate via CO2 production, and movement/activity; environmental conditions recorded.

- Datasets and their focus
  - metabandsuc.csv
  - appetiteexp2metabfin.csv
  - movementdatafin.csv
  - apetite.csv

## Dataset details and key variables

- metabandsuc.csv
  - Focus: volume of nectar consumed, metabolic rate, and activity for individual bees during a 30-day experiment.
  - Size and design: 288 bees; two cohorts (no-radiation start and radiation start); three phases (no radiation, radiation, recovery).
  - Data structure: 25 columns including
    - Bee ID, dose rate (μGy h⁻¹), colony, days within phase, overall day, phase, environmental conditions (temperature, humidity), initial weight and age, nectar access (high/low feeders), CO2 output (μmol/min), daily nectar volumes (two feeders), activity metrics (buzzing, walking, etc.), total active/inactive times, distance walked, and a flag for activity.
  - Key measurements: nectar intake every two days; for a CO2 subset (n of 30 per control and 200 μGy h⁻¹) CO2 during 5-minute recordings.

- appetiteexp2metabfin.csv
  - Focus: similar metrics to metabandsuc.csv but with repeated measurements per bee (longitudinal data).
  - Size and design: 288 bees; repeated measures across days within phases.
  - Data structure: 20 columns including
    - Dose rate, bee ID, body mass at entry, age at entry and during experiment, nectar feeder access, colony, nectar intake per day (40% and 5% feeders), thorax temperature and facility conditions (temperature, humidity), phase and day within phase, cohort indicator, ambient CO2, and CO2 output during metabolism.
  - Key measurements: repeated nectar consumption, metabolic rate (CO2), and body/age metrics across the experiment.

- movementdatafin.csv
  - Focus: activity/movement patterns of a subset of bees (60 bees) in relation to radiation exposure.
  - Size and design: 60 bees; three phases; dose rates of 0 and 200 μGy h⁻¹.
  - Data structure: 11 columns including
    - Bee ID, dose rate, video file identifier, observation period (pre-radiation, radiation, recovery), movement category (sitting, waving, walking, buzzing), duration and distance of movement, active/inactive status, and phase.
  - Key measurements: categorized movement and associated timing/duration during metabolic recording periods.

- apetite.csv
  - Focus: dose-rate threshold for radiation effects on nectar consumption.
  - Size and design: 141 bees across 19 dose-rate treatments (0–192 μGy h⁻¹) over 30 days.
  - Data structure: 19 columns including
    - Dose rate, bee ID, bee age, nectar concentration in feeder, thorax size, start weight, daily nectar consumption, cadaver dry weight at end, days in the experiment, death timing, thorax temperature, and other growth/condition metrics.
  - Key measurements: daily nectar consumption, weight dynamics, and end-point dry weight to assess dose-dependent effects.

## Measurements and variables of interest
- Nectar-related: volume consumed per day, total nectar intake, concentration feeder effects (5% vs 40%), and combined nectar intake across feeders.
- Metabolic indicators: CO2 production (μmol/min), thorax temperature, ambient facility temperature, and humidity.
- Activity and movement: duration and type of movement (buzzing, walking, waving, sitting), and total active/inactive times.
- Morphometrics and demographics: bee age, initial mass, thorax size, colony, and cohort.
- Environmental context: phase timing, facility conditions, and day within experiment.

## Experimental scope and participants
- Bees: 288 in Experiment 1 (two cohorts); 60 used for movement/metabolic analyses; 141 in Experiment 2 focusing on dose-rate thresholds for nectar consumption.
- Dose-rate range: 0–192 μGy h⁻¹ across experiments; multiple replicates per condition.
- Phases: no radiation (baseline), radiation exposure, recovery (post-exposure).
- Purpose across datasets: establish how radiation dose-rate influences feeding, metabolism, and activity, enabling dose–response analyses and potential predictive modelling of energy budgets under radiation.

## Implications for analysis
- Data allow dose–response modelling of nectar consumption, metabolic rate, and activity across multiple bees and cohorts.
- Potential to integrate datasets to link nectar intake with CO2-based metabolic rate, environmental conditions, and movement patterns.
- Longitudinal design supports temporal trend analyses within and across phases.
- Variability in measurements and data structures (different column sets and repeated measures) requires careful data harmonisation and appropriate handling of cohort and phase effects.

## provenance and collection notes
- Data generated and interpreted by Jessica Burrows and colleagues under an IAPETUS DTP PhD studentship.
- All experiments conducted in the University of Stirling radiation facility with controlled environmental conditions and standardized feeding protocols.

## Summary takeaway
- The collection comprises a richly structured, multi-dataset platform linking radiation dose-rate to bumblebee feeding, metabolism, and activity over time, enabling robust analysis of dose-dependent effects on energy budgets and behaviour.