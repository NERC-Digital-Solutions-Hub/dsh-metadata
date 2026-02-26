# Invertebrate activity data from an experiment in Malaysian Borneo, 2014-16 [HMTF] (2017) Griffiths, H.M., Ashton, L.A., Walker, A.E., Hasan, R., Evans, T., Eggleton, P., Parr, C.L.

## Overview
- Time-series datasets documenting ant and non-ant invertebrate abundance at bait monitoring cards across eight 50×50 m plots within a 42-hectare area in degraded lowland rainforest, Maliau Basin Conservation Area, Sabah, Malaysia.
- Three CSV data products:
  - AntMonitoringData.csv: biweekly ant abundance (via a 1–6 ranked scale) from Dec 2014–Mar 2017.
  - NonAntInvertebrate.csv: biweekly counts of major non-ant invertebrate groups from Dec 2014–Dec 2016.
  - PercentageBaitRemovedData.csv: 24-hour bait removal assays (Sept–Oct 2016) assessing resource uptake by different taxa, with open vs vertebrate-excluded cages.
- Spatial context: experimental plots and transects positioned within a rainforest landscape; data suitable for GIS-powered visualization of spatial and temporal trends.

## Experimental design and sampling regime
- Location and setup
  - Area: 42-ha lowland, old-growth dipterocarp rainforest in Maliau Basin Conservation Area, Sabah, Malaysia.
  - Plots: eight 50×50 m experimental plots with a 15 m surrounding buffer; four treated as ant-suppressed, four as controls; minimum 100 m separation between plots.
- Treatments
  - Ant suppression plots received two poison bait types: Synergy Pro® (hydramethylnon and pyriproxyfen) and a custom bait (Whiskas cat food in sugar solution with Imidacloprid).
  - Integrated pest management approach used to minimize insecticide use.
- Bait resources
  - Parallel baiting setup for biomass and resource-flow assessments conducted via ant suppression and control plots.

## Data collection methods
- AntMonitoringData.csv and NonAntInvertebrate.csv
  - Sampling: every two weeks; two 50 m transects per plot.
  - Bait: 0.3 g Whiskas cat food on twenty 5×5 cm laminated cards spaced 5 m apart; left for one hour.
  - Recording: ants scored on a 0–6 scale (0 = 0 ants; 6 = >50 ants); non-ant invertebrates categorized by major group (wasp, cricket, fly, springtail, beetle, cockroach, spider, harvestman) with abundance.
- PercentageBaitRemovedData.csv
  - Setup: 30 bait stations per plot (15 open, 15 caged) within core 50×50 m area; 3 bait types (carbohydrate biscuit, seed (sunflower), protein (fish)).
  - Access: cages (1×1 cm mesh) excluded vertebrates but allowed most invertebrates.
  - Replication: each bait type×treatment on three 50 m transects; five replicates per plot per treatment; repeated on two days.
  - Procedure: baits dried to constant mass, placed 09:00–11:00, collected after 24 hours; end weights used to compute percentage removed.
  - Notes: bearded pigs (Sus barbatus) destroyed 103 bait stations; such data removed from the dataset.
- Responsible parties
  - Data collection: A L Walker, F Hasan.
  - Data interpretation: H M Griffiths, L A Ashton, P Eggleton, C L Parr.

## Data structure and file descriptions
- AntMonitoringData.csv
  - Date: sampling date.
  - Plot: experimental plot.
  - Treatment: A = ant suppression; C = Control.
  - Score: ant abundance estimate on a 0–6 scale.
- NonAntInvertebrateData.csv
  - Date: sampling date.
  - Plot: experimental plot.
  - Treatment: A = ant suppression; C = Control.
  - Wasp, Cricket, Fly, Springtail, Beetle, Cockroach, Spider, Harvestman: counts per group.
  - Sum: total non-ant invertebrates observed.
- PercentagebaitRemoved.csv
  - Date_put_out, Date_collected: when bait was placed and collected.
  - rep: replicate number.
  - plot, plot_treat: plot and treatment (A or C).
  - bait: bait type (carbohydrate, seed, or fish/protein).
  - cage_treat: open vs cage (vertebrate exclusion).
  - start_weight, end_weight: dry mass at placement and after 24 hours.
  - perc_gone: percentage of bait removed in field.

## GIS and data suitability
- Spatial granularity
  - Plot-level spatial units (eight 50×50 m plots) with internal transect-level sampling, enabling spatial mapping of activity patterns across treatments.
  - Transect coordinates and exact plot locations not provided in the summary, but the study design supports joining to GIS layers for boundary and distance analyses.
- Temporal coverage
  - Longitudinal biweekly time series for ants and non-ant invertebrates (2014–2017), plus a discrete 24-hour bait removal assay (2016).
- Data integration potential
  - Combine with plot boundaries, habitat layers, and environmental data (e.g., rainfall) for enriched GIS analyses.
  - Possible visualizations: time-series charts per plot/treatment, spatial heatmaps of ant activity, vertebrate exclusion effects, and resource removal contrasts by bait type.
- Data quality and caveats
  - Ant counts are ordinal estimates (0–6) rather than exact counts, which may limit some quantitative analyses but supports robust comparative mapping.
  - Vertebrate exclusion effect observed via cage/open treatments; bearded pig disturbance noted and data filtered.
  - Some data gaps or uncertainties inherent to field-based biweekly sampling and seasonal variability.

## Potential GIS products and analyses
- Interactive dashboards
  - Time-series plots of ant and non-ant invertebrate activity by plot and treatment.
  - Bait removal efficiency by bait type, treatment, and cage/open condition.
- Spatial analyses
  - Mapping of activity indices across plots to identify spatial patterns of ant suppression efficacy.
  - Proximity analyses relative to habitat features or transects.
- Comparative analyses
  - Evaluate functional roles of ants vs other invertebrates and vertebrate-mediated effects on resource removal.
  - Assess redundancy and complementarities in ecosystem functioning across taxa.
- Data layering
  - Integrate with environmental rasters (rainfall, elevation) and disturbance layers for broader ecological inferences.