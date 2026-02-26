# Invertebrate activity data from an experiment in Malaysian Borneo, 2014-16 [HMTF] (2017) Griffiths, H.M., Ashton, L.A., Walker, A.E., Hasan, R., Evans, T., Eggleton, P., Parr, C.L.

## Overview of the data
- Three CSV data files are provided:
  - AntMonitoringData.csv: time-series of ant abundance at bait-monitoring cards, every two weeks from December 2014 to March 2017.
  - NonAntInvertebrate.csv: time-series of non-ant invertebrate abundance at bait-monitoring cards, every two weeks from December 2014 to December 2016.
  - PercentageBaitRemovedData.csv: amount of bait removed when access was manipulated (ants/vertebrates) during September–October 2016.
- Study site: lowland, old-growth dipterocarp rainforest in Maliau Basin Conservation Area, Sabah, Malaysia.
- Experimental design: 8 plots (50 x 50 m) within a 42-ha area, central 50 x 50 m, with a 15 m buffer. 4 control plots and 4 ant-suppression plots, at least 100 m apart.
- Treatments and baits:
  - Ant suppression used two bait types: Synergy Pro® (hydramethylnon and pyriproxyfen) and a Whiskas cat-food sugar solution bait with Imidacloprid.
  - Integrated pest management approach to limit insecticide use.
- Objective: quantify contributions of ants, other invertebrates, and vertebrates to ecosystem function and assess potential functional redundancy.

## Experimental design and sampling regime
- Timeframe and location details:
  - Oct 2014 establishment of plots; sampling from Dec 2014 to Oct 2016 (and additional data through Mar 2017 for ants).
- Ant and non-ant invertebrate monitoring (AntMonitoringData.csv, NonAntInvertebrate.csv):
  - Sampling method: two 50 m transects per plot; on each of 20 cards (0.3 g Whiskas cat food per card), left for 1 hour.
  - Counting approach:
    - Ants: counted using a rank scale (0 = 0 ants; 6 = >50 ants) due to field counting difficulty.
    - Non-ant invertebrates: identified to major group (wasp, cricket, fly, springtail, beetle, cockroach, spider, harvestman) and recorded by abundance.
- Bait removal experiment (PercentageBaitRemovedData.csv):
  - September–October 2016: 30 stations per plot (15 open, 15 caged) with three bait types (carbohydrate biscuit, sunflower seed, dried fish protein).
  - Experimental setup:
    - Baits placed on the forest floor (open) or inside cages (vertebrate-exclusion) with 1 x 1 cm mesh to allow invertebrate access.
    - Baits dried to constant mass prior to deployment; weight measured before and after 24 hours.
  - Replication: 5 baits per treatment per plot per transect across three 50 m transects; repeated on two days (total n = 480 across plots).
- Data interpretation notes:
  - Aimed to quantify the relative roles of ants, other invertebrates, and vertebrates in ecosystem function.
  - Data authorship: A.L. Walker and F. Hasan collected data; Griffiths et al. contributed interpretation.
  - Bearded pigs (Sus barbatus) destroyed 103 bait stations and these data were removed from the dataset.

## Details of data structure

- AntMonitoringData.csv
  - Date: date of monitoring
  - Plot: experimental plot identifier
  - Treatment: A = ant suppression; C = Control
  - Score: ordinal index for ant counts (0–6)

- NonAntInvertebrateData.csv
  - Date: date of monitoring
  - Plot: experimental plot identifier
  - Treatment: A = ant suppression; C = Control
  - Wasp, Cricket, Fly, Springtail, Beetle, Cockroach, Spider, Harvestman: counts per group
  - Sum: total non-ant invertebrates observed

- PercentagebaitRemoved.csv
  - Date_put_out: date bait was placed
  - Date_collected: date bait was collected
  - rep: replicate number
  - plot: experimental plot identifier
  - plot_treat: A = ant suppression; C = Control
  - bait: type of bait used
  - cage_treat: open (forest floor) or caged (vertebrate-exclusion)
  - start_weight: initial dry weight of bait
  - end_weight: final dry weight after 24 hours
  - perc_gone: percentage of bait removed

## Data quality, limitations, and notes for data leadership
- Potential data limitations:
  - Ant counts are semi-quantitative (ranked scores) due to field counting constraints.
  - Bearded pigs caused dataset gaps (103 bait stations removed).
  - Data collection spans multiple years with potential environmental variability (seasonality, rainfall).
- Metadata and discoverability considerations:
  - Clear per-file column definitions and treatment codes are provided.
  - Data cover central plots within a defined rainforest reserve; spatial scope limited to experimental plots in Maliau Basin.
- Governance and reuse considerations:
  - Data are structured to compare contributions across trophic groups (ants, other invertebrates, vertebrates) to ecosystem function.
  - To maximise reuse, ensure alignment of treatment labels and consistent time-series interpretation across files; account for any missing data due to pig disturbance.

## Potential uses for data leaders
- Evaluate the roles of different taxa (ants, other invertebrates, vertebrates) in resource removal and ecosystem processes.
- Assess functional redundancy and cross-taxon interactions in a tropical forest food web.
- Inform data stewardship practices by illustrating structured, multi-taxa field datasets with clear metadata, sampling regimes, and processing steps.
- Support cross-site or cross-network comparisons by providing a well-documented case study with explicit measurement methods and data-capture protocols.