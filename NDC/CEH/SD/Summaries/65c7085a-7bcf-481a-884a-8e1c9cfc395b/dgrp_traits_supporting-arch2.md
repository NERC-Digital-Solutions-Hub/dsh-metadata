# Overview

- Objective: Provide experimental data to quantify phenotypic variance in locomotor activity, mortality, and pathogen shedding in a panel of Drosophila melanogaster lines after infection with Pseudomonas aeruginosa, aiming to estimate broad-sense heritability for each trait and the genetic covariances between trait pairs.
- Data source: Experimental work conducted Jan–Oct 2023 at the Institute of Ecology and Evolution, University of Edinburgh; data collection led by Megan Kutzer (PDRA in Pedro Vale's lab).

## Aim and scope

- Measure variance components for three traits (locomotor activity, mortality, pathogen shedding) across genetic lines and sexes.
- Estimate broad-sense heritability and genetic covariances among trait pairs.
- Produce standardized outputs suitable for downstream analyses and cross-study comparisons.

## Organisms and sampling framework

- System: Drosophila melanogaster from the Drosophila Genetic Reference Panel (DGRP).
- Design: 60 DGRP lines × two sexes; 6–10 replicate flies per line/sex; 5–10 treatment replicates; total ~707 samples.
- Experimental structure: Conducted across 5 blocks with variable replication per block.

## Collection, generation, and transformation methods

- Pathogen shedding: After overnight infection, individual flies placed in sterile tubes; 24-hour CFU counts on Pseudomonas-selective media (PIM) to quantify shed bacteria.
  - CFU_5ul: CFUs counted in diluted sample.
  - CFUshed: Estimated CFUs shed per fly, accounting for dilution and sampled volume.
- Locomotor activity: Each fly placed in a Drosophila Activity Monitor (DAM); track total activity events at 1-minute resolution until death or end of experiment.
  - Recorded metrics include Movements, Activity_bouts, and Lifespan_mins.
- Mortality: Determined by last detected movement in DAM data.
- Data processing: All data curated and transformed using simple arithmetic in R.

## Laboratory instrumentation and environment

- Activity data: DAM5 monitors (Trikinetics).
- Environmental conditions: Climate-controlled incubator at 25°C with a 12h:12h light:dark cycle (7 AM–7 PM).
- Calibration: Control tubes (empty) to establish zero-activity baseline.

## Nature and units of recorded values

- Data file: DGRP_traits.csv with 18 columns:
  - Genotype, Sex, Block, Replicate
  - Well, Plate, Dilution, CFU_5ul
  - CFUshed, Monitor, Channel
  - Movements, Activity_bouts, Lifespan_mins
  - Alive, Proportion_active, Censor, Movements_per_min
- Derived measures:
  - Proportion_active = Activity_bouts / Lifespan_mins
  - CFUshed derived from CFU_5ul and dilution parameters

## Data file structure and access

- Primary dataset: DGRP_traits.csv
- Columns capture genotype, sex, experimental design factors, pathogen shedding, locomotor activity, lifespan, and censoring information.
- Data collection and processing occurred June–October 2023.

## Analytical methods and quality control

- Analytical approach: All reported values either raw measurements or simple arithmetic calculations performed in R.
- Quality control: Visual inspection for obvious outliers; validation that zero-activity readings occur only in tubes without flies; overall data within expected ranges.
- Purpose of analyses: Enable estimation of heritability and genetic correlations across the measured traits.

## Context and references

- Key references related to the data and methods include:
  - Mackay et al. 2012 on the DGRP resource
  - Siva-Jothy et al. 2018 on oral infection and shedding in Drosophila
  - Pfeiffenberger et al. 2010 on DAM system methodology
  - Anderson et al. 2022 on mitochondrial DNA effects on activity and sleep
  - Kutzer et al. 2024 on mitochondrial background and immune costs
- Data generated in the context of established DGRP usage and DAM-based activity measurement techniques.