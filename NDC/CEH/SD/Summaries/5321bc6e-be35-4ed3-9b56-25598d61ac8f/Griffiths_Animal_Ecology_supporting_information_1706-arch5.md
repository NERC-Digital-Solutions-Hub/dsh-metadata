# Invertebrate activity data from an experiment in Malaysian Borneo, 2014-16 [HMTF] (2017) Griffiths, H.M., Ashton, L.A., Walker, A.E., Hasan, R., Evans, T., Eggleton, P., Parr, C.L.

## Overview of the dataset
- Three CSV data files are provided:
  - AntMonitoringData.csv: time-series of ant abundance on bait monitoring cards, biweekly from December 2014 to March 2017.
  - NonAntInvertebrate.csv: time-series of non-ant invertebrate abundance at bait cards, biweekly from December 2014 to December 2016.
  - PercentageBaitRemovedData.csv: amount of bait removed when ants or vertebrates were prevented from accessing resources, collected in September–October 2016.
- Study site: lowland, old-growth dipterocarp rainforest in Maliau Basin Conservation Area, Sabah, Malaysia.
- Experimental design: 8 plots (50 x 50 m) within a 42-ha area; 4 control and 4 ant-suppressed plots; two ant-suppressing baits (Synergy Pro® and a Whiskas®-based bait with Imidacloprid) used; integrated pest management to maintain suppression.
- Purpose: quantify contributions of ants, other invertebrates, and vertebrates to ecosystem function and assess functional redundancy.

## Experimental design and sampling regime
- Setup date: October 2014; central sampling restricted to the 50 x 50 m area of each treatment plot; 15 m buffer around plots.
- Plot layout: eight plots, separated by at least 100 m; 4 control (no suppression) and 4 ant-suppressed.
- Bait monitoring regime: two 50 m transects per plot; 0.3 g Whiskas® cat food on 20 cards (5 x 5 cm) spaced 5 m apart; left for 1 hour; counted.
- Treatments: ant suppression via two bait types; integrated pest management approach to minimize excess insecticide use.
- Bait removal assays: September–October 2016; 30 stations per plot (15 open, 15 caged); three bait types (carbohydrate biscuit, sunflower seed, dried fish protein); 24-hour exposure; data collected in replicated transects with randomization across plots.

## Data collection methods
- Ants and non-ant invertebrates:
  - Ants: abundance estimated using a ranked scale (0 to 6) due to counting difficulty in the field.
  - Non-ant invertebrates: identified to major group (wasp, cricket, fly, springtail, beetle, cockroach, spider, harvestman) with abundance recorded.
- Bait removal data:
  - Stations placed open or inside cages to exclude vertebrates; bait types dried and weighed before exposure (start_weight) and after 24 hours (end_weight); percent removed calculated (perc_gone).
  - Replication: multiple transects and days; total across plots: substantial replication (n = 480 across plots).
  - Bearded pigs (Sus barbatus) destroyed 103 bait stations and were removed from the dataset.

## Data structure and fields
- AntMonitoringData.csv
  - Date: date of monitoring
  - Plot: experimental plot identifier
  - Treatment: A = ant suppression; C = control
  - Score: 0–6 scale for ant numbers
- NonAntInvertebrateData.csv
  - Date: date of monitoring
  - Plot: plot identifier
  - Treatment: A or C
  - Wasp, Cricket, Fly, Springtail, Beetle, Cockroach, Spider, Harvestman: counts per group
  - Sum: total non-ant invertebrates observed
- PercentagebaitRemoved.csv
  - Date_out: date bait was placed
  - Date_collected: date bait was collected
  - rep: replicate number
  - plot: plot identifier
  - plot_treat: treatment (A or C)
  - bait: bait type
  - cage_treat: open or caged
  - start_weight: initial dry weight of bait
  - end_weight: final dry weight after 24 hours
  - perc_gone: percent of bait removed

## Provenance, quality, and governance
- Data collection and interpretation
  - Collected by A L Walker and F Hasan; interpretation by H M Griffiths, L A Ashton, P Eggleton, C L Parr.
- Data quality and curation
  - Pig interference led to removal of 103 bait stations; dataset reflects this exclusion.
  - Units and measurement precision documented (e.g., weights to 0.01 g; mass-based bait removal).
- Documentation and metadata
  - Clear column definitions and measurement scales provided; time-series design enables cross-taxa ecosystem-function analyses.

## Practical considerations for data stewardship
- Metadata and standardization
  - Ensure consistent date formats and plot/treatment labeling across files; document any exclusions (e.g., pig-destructed stations).
- Data lineage and processing
  - Record rationale for excluding destroyed stations; note any adjustments to counts (ant-score scaling) and aggregation rules.
- Reuse and accessibility
  - Dataset supports cross-taxa analyses and tests of functional redundancy; suitable for meta-analyses on trophic interactions and ecosystem functioning.
- Licensing and versioning
  - Maintain versioned releases and provide citation info to link to the associated publication and data descriptions.