# Invertebrate activity data from an experiment in Malaysian Borneo, 2014-16 [HMTF] (2017) Griffiths, H.M., Ashton, L.A., Walker, A.E., Hasan, R., Evans, T., Eggleton, P., Parr, C.L.

## Overview
- Three CSV data files: AntMonitoringData.csv, NonAntInvertebrate.csv, PercentageBaitRemovedData.csv
- Time-series data collected biweekly from December 2014 to March 2017 (ants) and December 2014 to December 2016 (non-ant invertebrates); bait removal data from September–October 2016
- Location: lowland old-growth dipterocarp rainforest in Maliau Basin Conservation Area, Sabah, Malaysia
- Experimental setup: eight 50 x 50 m plots (4 control, 4 ant-suppressed) within a 42-ha area; ligand 2-Factor design with vertebrate exclusion
- Purpose: quantify contributions of ants, other invertebrates, and vertebrates to ecosystem function and assess functional redundancy
- Disturbance note: bearded pigs destroyed 103 bait stations and were excluded from the dataset

## Experimental design
- Plot layout: central 50 x 50 m sampling area within eight plots; buffer zones of 15 m; plots separated by at least 100 m
- Treatments: ant suppression plots vs control plots
- Ant suppression: two bait types applied (Synergy Pro® with hydramethylnon and pyriproxyfen; custom bait with Whiskas® cat food in sugar solution containing Imidacloprid) implemented in an integrated pest management framework
- Data collection window: 2014–2017 for ant data; 2014–2016 for non-ant invertebrates; multi-day bait removal study in Sep–Oct 2016

## Data collection methods
- Ant and non-ant invertebrate monitoring
  - Two 50 m transects per plot with 0.3 g Whiskas cat food on 20 laminated cards (5 x 5 cm each)
  - Exposure: 1 hour; counting protocol:
    - Ants: estimated using a ranked scale 0–6 (0 = none; 6 = >50 ants)
    - Non-ant invertebrates: identified to major group (wasp, cricket, fly, springtail, beetle, cockroach, spider, harvestman)
- Bait removal study
  - 30 bait stations per plot (15 open, 15 caged) within the core sampling area
  - Bait types: carbohydrate biscuit, sunflower seed (seed), dried fish protein
  - Preparation: baits dried to constant mass; mass measured before and after 24 hours
  - Experimental design: baits placed randomly across three 50 m transects per plot; each bait type x treatment replicated five times per plot; data collected on two different days
  - Outcome: quantifies removal by ants, other invertebrates, and vertebrates to assess their relative contributions to ecosystem function

## Data structure and columns
- AntMonitoringData.csv
  - Date: date of monitoring
  - Plot: plot identifier
  - Treatment: A = ant suppression; C = Control
  - Score: ordinal abundance estimate (0 = 0 ants to 6 = >50 ants)
- NonAntInvertebrateData.csv
  - Date: date of monitoring
  - Plot: plot identifier
  - Treatment: A or C
  - Wasp, Cricket, Fly, Springtail, Beetle, Cockroach, Spider, Harvestman: counts per group
  - Sum: total non-ant invertebrates observed
- PercentagebaitRemoved.csv
  - Date_put_out: date bait was placed
  - Date_collected: date bait was collected
  - rep: replicate number
  - plot: plot identifier
  - plot_treat: treatment (A or C)
  - bait: bait type
  - cage_treat: open or caged (vertebrate exclusion)
  - start_weight: initial dry weight of bait
  - end_weight: final dry weight after 24 hours
  - perc_gone: percentage of bait removed

## Data quality, limitations, and governance
- Data quality notes
  - Bearded pig disturbances led to exclusion of affected bait stations
  - Ant counts rely on a rank-based estimation rather than exact counts
  - Data collected at biweekly intervals; capture of dynamics at sampling frequency
- Metadata and governance
  - clear documentation of plot layout, treatments, sampling regime, and bait types
  - Data collectors: A L Walker and F Hasan; interpretation by Griffiths, Ashton, Eggleton, Parr
  - Data sharing and openness considerations highlighted by the broader monitoring-framework context (transparent methods and metadata facilitate reuse)

## Relevance for monitoring frameworks
- Provides standardized, repeatable measures of invertebrate activity and resource uptake under manipulated trophic conditions
- Distinguishes vertebrate influence via open vs. caged bait treatments, enabling assessment of functional roles and redundancy across trophic groups
- Includes explicit metadata: sampling frequency, plot layout, treatment codes, and measurement scales
- Demonstrates data cleaning steps and caveats (e.g., pig disturbance) that inform robust data governance and quality assurance
- Combines abundance proxies (ordinal ant scores) with resource-removal metrics to evaluate ecosystem function and redundancy across trophic levels

## Practical considerations for applying in policy-relevant monitoring
- Ensure complete metadata and consistent units for cross-study comparability
- Plan for potential disturbances and data gaps; document exclusions transparently
- Align sampling frequency and plot arrangement with decision-making timescales
- Consider ethical and ecological implications when deploying bait-based monitoring in sensitive habitats