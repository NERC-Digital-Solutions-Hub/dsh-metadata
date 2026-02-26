# Overview

- Purpose: The resource is experimental data from Jan–Oct 2023 at the Institute of Ecology and Evolution, University of Edinburgh, aimed at measuring phenotypic variance in locomotor activity, mortality, and pathogen shedding in a panel of Drosophila melanogaster lines infected with Pseudomonas aeruginosa. The goal is to estimate broad-sense heritability for each trait and genetic covariances between trait pairs.
- Data provenance: Collected by Megan Kutzer (PDRA in Pedro Vale's lab, UoE).
- Experimental scope: 60 DGRP lines exposed to oral infection; 6–10 replicates per line and sex; 5 experimental blocks; a total of 707 samples.

## Dataset Description

- Primary file: DGRP_traits.csv with 18 columns.
- Key variables:
  - Genotype: DGRP line name (RAL-nnn)
  - Sex: M or F
  - Block: 1–5
  - Replicate: 1–6
  - Well, Plate, Dilution: plate-well metadata for CFU processing
  - CFU_5ul: CFU count in the diluted sample
  - CFUshed: estimate of CFUs shed per fly after dilution and sampling
  - Monitor, Channel: DAM device and channel for each fly
  - Movements: total movements during the experiment
  - Activity_bouts: total 1-min intervals with activity
  - Lifespan_mins: minutes until last movement
  - Alive: alive or dead at end
  - Proportion_active: Activity_bouts / Lifespan_mins
  - Censor: survival-analysis indicator (0 alive, 1 dead)
  - Movements_per_min: average movements per minute
- Units: CFU counts, minutes, counts of events, proportions, and binary alive/dead status; activity data recorded at 1-minute resolution; lifespan spans 2,500–20,000 minutes depending on fly fate.

## Experimental Design

- Population: 60 lines from the DGRP panel.
- Infection: Oral infection with Pseudomonas aeruginosa.
- Replication: 6–10 replicates per genotype and sex.
- Scheduling: Data collected across 5 experimental blocks.
- Outcome measures: Pathogen shedding (CFU), locomotor activity (DAM-based), and mortality timing.

## Data Collection and Laboratory Methods

- Pathogen shedding: Fly placed in sterile Eppendorf; CFUs quantified from Pseudomonas-selective media (PIM) after 24 hours.
- Activity monitoring: Flies placed in Drosophila Activity Monitors (DAM5); activity counted at 1-minute resolution until death or end of observation.
- Mortality: Recorded as the last detected movement in DAM.
- Environmental conditions: Flies kept at 25°C, 12h light:12h dark cycle (7 AM–7 PM) in climate-controlled incubator.
- Calibration: Empty tubes used to calibrate zero-activity readings.

## Analytical Methods and Quality Control

- Data processing: All values recorded or calculated in R.
- Quality control: Raw data checked for obvious outliers and equipment malfunctions; no activity detected in blank DAM tubes.
- Data handling: Measurements include direct counts (CFU) and derived metrics (e.g., CFUshed, Proportion_active, Censor).

## Variables and Measurements (Details)

- Genotype, Sex, Block, Replicate, Well, Plate, Dilution
- CFU_5ul, CFUshed
- Monitor, Channel
- Movements, Activity_bouts
- Lifespan_mins, Alive
- Proportion_active, Censor
- Movements_per_min

## GIS and Data Product Opportunities (Perspective for GIS Specialists)

- Conceptual spatialize the dataset within a map-like structure:
  - Plate/Well level as a spatial grid: visualize CFU shedding, Movements, and Activity_bouts across the 96-well plate layout for a given block, sex, and genotype.
  - Block and monitor localization: treat experimental blocks and DAM monitors as spatial layers to compare phenotypes by location (e.g., block-level heatmaps of activity or survival indicators).
  - Genotype-by-location views: create choropleth-like maps showing trait means or distributions by genotype across blocks/plates, enabling quick cross-genotype comparisons.
  - Time-series mapping: incorporate Lifespan_mins and Activity_bouts as temporal attributes for individual flies, enabling temporal heatmaps or animated visuals to illustrate how activity evolves until death.
  - Multivariate spatial visuals: combine CFUshed, Proportion_active, and Lifespan_mins in layered maps to highlight trade-offs or genetic covariances across spatially organized experimental units.
- Data product concepts:
  - Plate- and block-level dashboards showing per-genotype summaries and confidence intervals.
  - Interactive filters by genotype, sex, block, plate, and monitor to explore distributions of shedding, activity, and survival.
  - Spatially-aware QC maps highlighting any plate-related anomalies or calibration issues.
- Data compatibility considerations:
  - Although the dataset is not geographical, its structured grid (plates, wells, monitors) lends itself to spatial visualization techniques common in GIS, enabling map-based exploration and communication of complex genetic-phenotypic relationships.

## References

- Mackay TFC et al. 2012. The Drosophila melanogaster Genetic Reference Panel. Nature 482, 173-178.
- Siva-Jothy JA et al. 2018. Oral Bacterial Infection and Shedding in Drosophila melanogaster. JoVE, e57676-e57676.
- Pfeiffenberger C et al. 2010. Locomotor Activity Level Monitoring Using the Drosophila Activity Monitoring (DAM) System. Cold Spring Harb Protoc.
- Anderson L et al. 2022. Variation in mitochondrial DNA affects locomotor activity and sleep in Drosophila melanogaster. Heredity.
- Kutzer MAM et al. 2024. Mitochondrial background can explain variable costs of immune deployment. Journal of Evolutionary Biology.