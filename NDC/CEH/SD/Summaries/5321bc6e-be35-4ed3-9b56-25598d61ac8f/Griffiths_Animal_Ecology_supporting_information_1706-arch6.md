# Invertebrate activity data from an experiment in Malaysian Borneo, 2014-16 [HMTF] (2017) Griffiths, H.M., Ashton, L.A., Walker, A.E., Hasan, R., Evans, T., Eggleton, P., Parr, C.L.

## Overview of data
- Three CSV datasets provided:
  - AntMonitoringData.csv: time series of ant abundance at bait monitoring cards, biweekly from Dec 2014 to Mar 2017.
  - NonAntInvertebrate.csv: time series of non-ant invertebrate abundance at bait cards, biweekly from Dec 2014 to Dec 2016.
  - PercentageBaitRemovedData.csv: amount of bait removed from experimental plots when access by ants/vertebrates was manipulated, Sept–Oct 2016.
- Study location: lowland, old-growth dipterocarp rainforest in Maliau Basin Conservation Area, Sabah, Malaysia.
- Experimental design: eight 50x50 m plots within a 42-ha area; four plots as controls and four as ant suppression; two poison baits used for suppression (Synergy Pro® and a Whiskas®-based bait with Imidacloprid); integrated pest management approach employed.
- Purpose: quantify contributions of ants, other invertebrates, and vertebrates to ecosystem function and assess functional redundancy.

## Experimental design / sampling regime
- Plot setup: eight 50x50 m plots with a 15 m buffer; central 50x50 m used; plots divided into control (C) and ant suppression (A) treatments, separated by ≥100 m.
- Baiting for ant suppression:
  - Synergy Pro® (hydramethylnon and pyriproxyfen) and Whiskas-based bait with Imidacloprid.
- Data scope: aims to understand how different groups contribute to ecosystem processes under suppression conditions.

## Data collection methods
- AntMonitoringData.csv and NonAntInvertebrate.csv:
  - Biweekly sampling using bait cards along two 50 m transects in the plot center.
  - Bait setup: 0.3 g Whiskas cat food on twenty 5x5 cm cards, spaced 5 m apart.
  - Protocol: baits left for 1 hour; counts recorded.
  - Ant counts: field-estimated using a rank scale due to counting difficulties (0 to >50 ants; 0–6 scale).
  - Non-ant invertebrates: major taxa identified (wasp, cricket, fly, springtail, beetle, cockroach, spider, harvestman) with abundance categorized.
- PercentageBaitRemovedData.csv:
  - 30 bait removal stations per plot (15 open, 15 caged) within the core 50x50 m area.
  - Baits: three types—carbohydrate biscuit, sunflower seed, fish protein.
  - Treatments: open (verTEbrate access) vs cage (vertebrate exclusion).
  - Replication: each bait type x treatment replicated along three 50 m transects; five placements per plot per transect; two sampling days.
  - Procedure: baits dried to constant mass before placement; 24-hour exposure; post-exposure drying and weighing to determine mass removed.
  - Timing: conducted in September–October 2016; Bait types designed to reflect natural resources (sugars, seeds, protein).
  - Note: Bearded pigs (Sus barbatus) destroyed 103 bait stations; those data omitted from the dataset.

## Data structure (columns)
- AntMonitoringData.csv
  - Date: date of monitoring
  - Plot: experimental plot identifier
  - Treatment: A (ant suppression) or C (control)
  - Score: estimated ants observed on bait cards (0, 1, 2, 3, 4, 5, 6)
- NonAntInvertebrateData.csv
  - Date: date of monitoring
  - Plot: experimental plot
  - Treatment: A or C
  - Wasp, Cricket, Fly, Springtail, Beetle, Cockroach, Spider, Harvestman: counts observed
  - Sum: total non-ant invertebrates observed
- PercentagebaitRemoved.csv
  - Date_put_out: date bait was placed in field
  - Date_collected: date bait was collected
  - rep: replicate number
  - plot: plot identifier
  - plot_treat: A or C
  - bait: bait type
  - cage_treat: open or cage
  - start_weight: initial bait mass (dry)
  - end_weight: final bait mass (dry)
  - perc_gone: percentage removed after 24 hours

## Data quality and provenance notes
- Bearded pigs caused substantial data loss (103 bait stations removed) and those data excluded from the PercentageBaitRemoved dataset.
- Ant counts are estimated using a standardized 0–6 rank scale due to field counting limitations.
- Bait removal measurements rely on precise drying to constant mass and controlled exposure times, with multiple replications to capture variability.

## Potential data products and analyses
- Time-series assessment of ant vs. non-ant invertebrate activity under ant suppression vs. control.
- Evaluation of vertebrate exclusion effects on bait removal across resources (carbohydrate, seed, protein).
- Cross-taxa comparisons to assess functional roles and redundancy among ants, other invertebrates, and vertebrates.
- Spatial/temporal patterns of foraging activity and resource use in tropical rainforest ecosystems.

## Authors and data collection credits
- Data collection: A L Walker and F Hasan
- Interpretation: H M Griffiths, L A Ashton, P Eggleton, C L Parr