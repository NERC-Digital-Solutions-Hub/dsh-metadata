# Invertebrate activity data from an experiment in Malaysian Borneo, 2014-16 [HMTF] (2017) Griffiths, H.M., Ashton, L.A., Walker, A.E., Hasan, R., Evans, T., Eggleton, P., Parr, C.L.

## Overview
- Time-series datasets from a rainforest experiment in Maliau Basin, Sabah, Malaysia (lowland old-growth dipterocarp rainforest).
- Study period: December 2014 to March 2017 for ants; December 2014 to December 2016 for non-ant invertebrates.
- Aimed to quantify contributions of ants, other invertebrates, and vertebrates to ecosystem function and assess functional redundancy.
- Data gathered via standardized bait-monitoring and bait-removal assays; focuses on environmental monitoring and ecological health indicators.

## Experimental design and sampling regime
- Location and setup: Eight 50 x 50 m experimental plots within a 42-ha area; four plots as controls and four as ant suppression plots, with at least 100 m between plots; central 50 x 50 m area used for sampling.
- Treatments: Ant suppression using two bait types—Synergy Pro® (hydramethylnon and pyriproxyfen) and a custom bait (Whiskas® cat food in sugar solution with Imidacloprid); integrated pest management approach.
- Plot structure: Buffer zone of 15 m around treatment plots.
- Sampling period: Biweekly monitoring; timeframe captured in AntMonitoringData.csv and NonAntInvertebrate.csv.

## Data collection methods
- Ant and non-ant invertebrate monitoring (AntMonitoringData.csv and NonAntInvertebrateData.csv):
  - Two 50 m transects per plot; two monitoring cards per transect.
  - Bait: 0.3 g Whiskas® cat food on 20 cards placed 5 m apart; left for 1 hour; ants and non-ant invertebrates counted/recorded.
  - Ant counts: estimated on a 1–6 rank scale (0 = 0 ants; 6 = >50 ants) due to counting limitations.
  - Non-ant invertebrates: visually assigned to major groups (wasp, cricket, fly, springtail, beetle, cockroach, spider, harvestman).
- Bait removal assay (PercentageBaitRemovedData.csv):
  - 30 stations per plot (15 open, 15 in cages) within the core 50 x 50 m area.
  - Three bait types representing natural resources: carbohydrate (biscuit), seed (sunflower seed), protein (fish).
  - Bait types x treatment (open vs. caged) replicated on three 50 m transects; five replicates per treatment per plot; repeated on two days.
  - Procedure: baits dried to constant mass before placement; re-collected after 24 hours; end weight used to calculate percentage removed.
  - Open cages allowed invertebrates to access baits; cages prevented vertebrate access.
  - Baits measured for mass loss (start_weight, end_weight) and perc_gone.

## Data structure and file contents
- AntMonitoringData.csv
  - Date: sampling date.
  - Plot: experimental plot identifier.
  - Treatment: A = ant suppression; C = control.
  - Score: rank-based estimate of ant numbers (0–6).
- NonAntInvertebrateData.csv
  - Date: sampling date.
  - Plot: experimental plot identifier.
  - Treatment: A = ant suppression; C = control.
  - Wasp, Cricket, Fly, Springtail, Beetle, Cockroach, Spider, Harvestman: observed counts by group.
  - Sum: total non-ant invertebrates observed.
- PercentagebaitRemoved.csv
  - Date_put_out: bait placement date.
  - Date_collected: bait collection date.
  - rep: replicate number.
  - plot: plot identifier.
  - plot_treat: treatment (A or C).
  - bait: bait type (carbohydrate, seed, biscuit, etc.).
  - cage_treat: open or caged.
  - start_weight: initial dry weight of bait.
  - end_weight: remaining dry weight after 24 hours.
  - perc_gone: percentage of bait removed.

## Data quality, limitations, and notes
- Bearded pigs (Sus barbatus) destroyed 103 bait stations and were excluded from the dataset.
- Data collected and interpreted by the listed authors; methods reflect standard ant ecology approaches (e.g., bait assays) and allow cross-plot and temporal comparisons.
- Data storage and accessibility aligned with broader monitoring practices; designed to enable data sharing and integration with other environmental datasets.

## Relevance for environmental monitoring and analysis
- Provides standardized, time-resolved indicators of trophic interactions and resource use in a tropical rainforest.
- Enables assessment of the relative roles of ants, other invertebrates, and vertebrates in ecosystem functioning and redundancy.
- Suitable for integrating with other environmental datasets to evaluate policy outcomes, habitat health, and biodiversity responses over time.