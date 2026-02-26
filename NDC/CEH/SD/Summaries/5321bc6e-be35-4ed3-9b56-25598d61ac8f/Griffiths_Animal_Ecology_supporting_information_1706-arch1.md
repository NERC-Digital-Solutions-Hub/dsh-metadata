# Invertebrate activity data from an experiment in Malaysian Borneo, 2014-16 [HMTF] (2017) Griffiths, H.M., Ashton, L.A., Walker, A.E., Hasan, R., Evans, T., Eggleton, P., Parr, C.L.

## Overview of data
- Three CSV data files:
  - AntMonitoringData.csv: time series of ant abundance at bait monitoring cards, biweekly, Dec 2014–Mar 2017
  - NonAntInvertebrate.csv: time series of non-ant invertebrate abundance at bait cards, biweekly, Dec 2014–Dec 2016
  - PercentageBaitRemovedData.csv: amount of food resource removed when ants/vertebrates were prevented from accessing bait, Sept–Oct 2016
- Experimental context: lowland old-growth dipterocarp rainforest in Maliau Basin Conservation Area, Sabah, Malaysia
- Experimental design: eight 50 x 50 m plots within a 42-hectare area; four control (no ant suppression) and four ant-suppression plots; central plots analyzed
- Ant suppression: two poison baits applied (Synergy Pro® with hydramethylnon and pyriproxyfen; and Whiskas cat food with sugar solution containing Imidacloprid) under an integrated pest management approach
- Data use: quantify roles of ants, other invertebrates, and vertebrates in ecosystem function and assess functional redundancy

## Study area and experimental design
- Location: Maliau Basin Conservation Area, Sabah, Malaysia (tropical lowland rainforest)
- Plot layout: eight plots (50 x 50 m) within a 42-ha area; buffer zone of 15 m; two transects per plot
- Treatments: A = ant suppression, C = control; minimum 100 m between plots
- Ant suppression details: dual bait strategy to maintain suppression while minimizing insecticide use
- Notable field event: bearded pigs (Sus barbatus) destroyed 103 bait stations and were removed from the dataset

## Data collection methods
- Ants and non-ant invertebrates
  - Monitoring every two weeks using bait cards: two 50 m transects per plot; 0.3 g Whiskas cat food on twenty 5 x 5 cm cards spaced 5 m apart
  - Exposure: 1 hour; counts recorded
  - Ant counts: estimated on a 0–6 ordinal scale (0 = 0 ants; 6 = >50 ants) due to counting difficulty
  - Non-ant invertebrates: major groups identified (wasp, cricket, fly, springtail, beetle, cockroach, spider, harvestman) with abundance per card recorded; sum calculated per card
- Bait removal study (vertebrate and invertebrate exploration of resources)
  - 30 bait stations per plot (15 open, 15 caged) within the central 50 x 50 m area
  - Bait types: carbohydrate biscuit, sunflower seed, and dried fish protein
  - Setup: open or cage treatments; cages allowed invertebrates but excluded vertebrates
  - Mass and measurement: baits dried to constant mass, weighed before and after 24 hours to calculate percent removed
  - Replication and timing: three bait types x two treatments x three transects per plot; repeated on two different days
  - Timing: field setup between 09:00 and 11:00; observations in September–October 2016
  - Data handling: 30 stations per plot, 60 per plot across two days, 480 total across all plots; all baits dried and weighed in lab
- Data collection responsibilities: A.L. Walker and F. Hasan collected the data; H.M. Griffiths, L.A. Ashton, P. Eggleton, and C.L. Parr interpreted results

## Data structure and column definitions
- AntMonitoringData.csv
  - Date: date of monitoring
  - Plot: experimental plot identifier
  - Treatment: A = ant suppression, C = control
  - Score: ordinal ants count (0–6)
- NonAntInvertebrateData.csv
  - Date: date of monitoring
  - Plot: plot identifier
  - Treatment: A = ant suppression, C = control
  - Wasp, Cricket, Fly, Springtail, Beetle, Cockroach, Spider, Harvestman: counts per major invertebrate group
  - Sum: total non-ant invertebrates observed
- PercentagebaitRemoved.csv
  - Date_put_out: bait placement date
  - Date_collected: bait collection date
  - rep: replicate number
  - plot: plot identifier
  - plot_treat: A or C treatment
  - bait: bait type
  - cage_treat: open or cage (vertebrate exclusion)
  - start_weight: dry weight at placement
  - end_weight: dry weight after 24 hours
  - perc_gone: percent bait removed after 24 hours

## Considerations for analysis
- Time-series and treatment effects: potential to model how ant suppression influences both ant and non-ant invertebrate activity, plus vertebrate-foraging pressure
- Data types and modeling: ants captured as an ordinal score; non-ant invertebrates as counts by group; bait removal as percent change
- Spatial scale: central 50 x 50 m area; potential local variability between plots
- Data quality considerations: bearded pig disturbance leading to data exclusion; effects of Integrated Pest Management on results
- Metadata and provenance: clear attribution of data collection and interpretation, enabling reproducibility and cross-study synthesis

## Potential analyses and questions
- Do ant suppression plots show reduced ant activity and corresponding changes in non-ant invertebrate abundance or composition?
- How do vertebrates and other invertebrates contribute to resource removal under different treatments, and what is the extent of functional redundancy?
- What temporal patterns emerge in ant and non-ant invertebrate activity, and how do bait removal rates relate to these patterns?
- Can observed data inform predictive models of ecosystem function under ant suppression or similar interventions in tropical forests?