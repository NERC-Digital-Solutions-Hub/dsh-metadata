# Ecologically relevant radiation exposure triggers elevated metabolic rate and nectar consumption in bumblebees

## Overview
- Investigates how ionising radiation affects bumblebee energy budgets, including nectar consumption, metabolic rate, and activity.
- Conducted at the University of Stirling with 30-day experiments that include three 10-day phases: no radiation, radiation, and recovery.
- Bees exposed to dose rates of 0, 40, 100, and 200 μGy h⁻¹; two cohorts (initial 148 bees and a second cohort of 140 bees added during the radiation phase).
- Data collected across multiple facets: nectar intake, metabolic rate via CO2 production, and movement/activity.

## Experimental design and scope
- Three 10-day phases:
  - Phase 1: no radiation
  - Phase 2: radiation exposure
  - Phase 3: recovery (radiation shielded)
- Each bee housed individually with pollen and nectar solution; nectar provided at high (40%) and/or low (5%) concentrations.
- Measurements:
  - Nectar consumption weighed every two days
  - Subset of 30 bees per group used for CO2 production and movement filming during days 7 and 9
  - Infrared gas analyser (IRGA) used for CO2 measurement
- Two cohorts:
  - Cohort 1: entered at day 1 (n=148)
  - Cohort 2: entered at day 10 (n=140)
- Movement and activity categorized alongside CO2 data for a subset of bees

## Datasets included
- metabandsuc.csv
  - 25 columns detailing bee ID, dose rate, colony, phase, day, temperature and humidity (air, facility), bee weight and age, nectar consumption (40% and 5% feeders), CO2 output, movement metrics (buzzing, stationary, walking), activity timing, and derived totals (active/inactive time, distance walked).
- appetiteexp2metabfin.csv
  - 20 columns covering dose rate, bee ID, bee mass at entry, age, nectar concentration, thorax size, initial weight, weight changes, death timing, phase and day within phase, cohort indicator, days within the experiment, ambient CO2, CO2 output, and related observations.
- movementdatafin.csv
  - 11 columns focused on movement behavior: bee ID, dose rate, video file identifier, observation period (phases), movement category (sitting, waving, walking, buzzing), duration, distance, active/inactive time, active flag, and phase.
- apetite.csv
  - 19 columns describing dose rate, bee ID, age at entry and during the experiment, nectar concentration, thorax temperature, bee mass and changes, cadaver dry weight, dry weight as a percent of start weight, nectar consumption volumes, colony, and two-day facility temperature/humidity measures.

## Data collection and provenance
- Lead data collection: Jessica Burrows; interpretation by Jessica Burrows and Matthew Tinsley.
- Funding and setting: IAPETUS DTP PhD studentship; experiments conducted at the University of Stirling.
- Methods and instruments:
  - Bees housed individually with pollen and nectar (40% w/v) or alternatives
  - Nectar weights measured every two days
  - CO2 production measured with IRGA during designated days
  - Movement data captured and classified (walking, buzzing, etc.)
- Purpose: to understand the dose-rate threshold at which radiation affects bumblebee feeding and energy budgets.

## Data structure and variables (key points)
- Each dataset provides a detailed, structured set of variables to enable dose-response and temporal analyses:
  - Dose rate (μGy h⁻¹), bee identifiers, colony/source, phase and days within phases, and overall days in the experiment
  - Physiological and environmental context: temperature and humidity (air and facility), bee age and weight at entry, thorax size, and environmental conditions during measurements
  - Behavioral and metabolic measures: nectar consumption from various feeders, CO2 production, movement category and metrics (duration, distance, active/inactive times)
  - Outcome indicators: cadaver dry weight and dry weight percentage in appetitive dataset; death timing in appetite-focused dataset
- Data capture spans three phases with repeated measures, enabling robust monitoring and assessment of sublethal effects under varying radiation exposure.

## Relevance for monitoring and policy frameworks
- Provides a multi-dimensional view of how an environmental stressor (radiation) influences pollinator energy budgets through feeding, metabolism, and behavior.
- The gradient of dose rates supports dose-response modelling and threshold identification, informing environmental risk assessments and monitoring programs.
- Rich, well-structured datasets with explicit variable definitions and phase-based timing support reproducibility, cross-study comparisons, and integration into broader environmental health dashboards or reports.
- Emphasizes the importance of coordinated data collection across phenotypic (feeding, metabolism, movement) and contextual (phase, environmental conditions) dimensions for transparent, evidence-based monitoring.