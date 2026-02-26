# Supporting Documentation Ecologically relevant radiation exposure triggers elevated metabolic rate and nectar consumption in bumblebees

## Overview
- Documents a set of datasets from controlled radiation exposure experiments assessing how ionising radiation affects bumblebee energy budgets, feeding, metabolism, and activity.
- Two main experiments (including a secondary dataset focus) conducted at the University of Stirling, with multiple dose-rate treatments and longitudinal measurements over 30 days.
- Data are organized into four datasets, each capturing different aspects: nectar/metabolic data, repeated-measures metabolic data, movement/behavior data, and broader nectar consumption with body/physiological measures.

## Datasets and what they contain
- metabandsuc.csv (31 KB)
  - Single-measure per bee across 30 days; three 10-day phases: no radiation, radiation, recovery.
  - Dose rates: 0, 40, 100, 200 μGy hr-1.
  - Measurements include: nectar volume (from 40% and 5% feeders), CO2 production, activity, body weight at entry, age, temperature/humidity, phase, and derived movement/metabolic metrics.
  - Structure includes 25 columns with identifiers, environmental conditions, and performance metrics.

- appetiteexp2metabfin.csv (2.4 MB)
  - Repeated (longitudinal) measurements for the same bees; complements metabandsuc.csv by providing repeated entries per data point.
  - Dose rates and similar design as Experiment 1; includes mass at start, age, nectar volumes, thorax temperature, colony, phase/days within phase, cohort indicator, days within experiment, ambient CO2, and mean CO2 output.
  - Structure includes 20 columns detailing individual bee trajectories and physiological readings.

- movementdatafin.csv (92 KB)
  - Movement activity data for a subset of 60 bees used in metabolic rate analysis; focuses on movement type and duration.
  - Measurements include: bee ID, dose rate, video/file identifier, observation period (phase), movement category (sitting/waving/walking/buzzing), duration, distance traveled, active/inactive times, and phase label.
  - Structure includes 11 columns.

- appetite.csv (86 KB)
  - Nectar consumption data across a broader dose-rate gradient; 141 bees over 30 days.
  - Dose rates ranged across 19 treatments using a 137Cs source (0 to 192 μGy hr-1).
  - Measured: nectar concentration, thorax temperature, start weight, mass during study, weight change, death age, days to death, cadaver dry weight, percent dry weight, daily nectar volumes (40% feeder), and colony information; plus thorax temperature and facility temperature/humidity near measurements.
  - Structure includes 19 columns.

## Experimental design and data collection
- Experiment 1
  - Three 10-day phases: no radiation, radiation, recovery.
  - Dose-rate treatments: 0, 40, 100, 200 μGy hr-1.
  - Bee cohorts: two groups entering at day 1 (n=148) and day 10 (n=140) for radiation phase.
  - Data collected: nectar weighed every two days; a subset of 30 bees from control and 200 μGy hr-1 groups had CO2 production measured over 5 minutes with movement filming.
  - Additional measurements: environmental conditions (temperature, humidity); CO2 output; movement, buzzing, and activity metrics.

- Experiment 2
  - Dose-rate threshold assessment for nectar consumption.
  - 141 bees exposed to 19 dose-rate treatments (0–192 μGy hr-1) over 30 days.
  - Nectar feeders with varying sucrose concentrations (20–50% w/v); nectar weighed to derive consumption.
  - Measurements: live mass, thorax temperature, cadaver dry weight at termination, dry weight percent, and other body/physiological metrics.
  - Objective: identify lower dose rates at which radiation effects on feeding begin.

## Key variables and data relations
- Dose rate of radiation (μGy hr-1) as a central driver across datasets.
- Bee identifiers and cohort/entry details to align longitudinal records.
- Phase and days within phase and total days in the experiment to synchronize measurements.
- Nectar consumption (ml) from different feeders, feeding status, and moves between feeders.
- Metabolic indicators: CO2 output (μmol/min) and metabolic rate proxies.
- Movement and activity metrics: duration, distance traveled, and categories (sitting, waving, walking, buzzing).
- Physiological measures: body mass, thorax temperature, humidity/temperature in facility, dry weight (cadaver), weight change over time.
- Environmental context: colony origin, data logger proximity, ambient CO2, and environmental conditions.

## Data structure and integration considerations
- Multiple datasets with overlapping bee identifiers and experimental phases allow cross-dataset analyses (e.g., linking nectar intake to CO2 output or movement metrics).
- Datasets have differing column sets; careful merging is required (e.g., by bee ID, dose rate, phase, and day).
- Longitudinal design (Experiment 1 and appetite exp2) supports dose-response and time-course analyses but requires alignment of phase definitions and cohort flags.

## How to use and potential research questions
- Assess dose-response: how nectar consumption, metabolic rate (CO2 output), and movement respond to increasing radiation dose rates.
- Explore temporal dynamics: how feeding and metabolism change across the no-radiation, radiation, and recovery phases.
- Identify thresholds: use appetite.csv to determine lower dose rates where feeding begins to be affected.
- Compare cohorts: examine whether entry timing (cohort) influences observed effects or recovery patterns.
- Integrate physiology with behavior: correlate thorax temperature, body weight changes, and movement patterns with metabolic indicators.

## Data quality and reuse notes
- Datasets vary in size and scope; metabandsuc.csv and appetiteexp2metabfin.csv provide complementary single-event and repeated-measures perspectives, respectively.
- Experimental design includes two cohorts and multiple dose-rate treatments, enabling robust dose-response inferences but requiring careful alignment of records across datasets.
- Data provenance: collected and interpreted by Jessica Burrows; University of Stirling; part of an IAPETUS DTP PhD program.

## Practical considerations for data support
- Ensure consistent key linking fields (bee ID, dose rate, phase, and day) when merging datasets.
- Account for phase-specific measurements and potential missing values across datasets.
- Normalize or harmonize units where necessary (e.g., μGy hr-1, ml, μmol/min, cm, s, °C, %).
- Document any cohort-specific nuances (e.g., differences in entry days or measurement windows) in any dissemination or tooling built on the data.