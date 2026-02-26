# Sampling regime and collection methods

## Overview
- Study of a wild banded mongoose population on the Mweya Peninsula, Queen Elizabeth National Park, Uganda, ongoing since 1995.
- Population typically comprises 10–12 social groups with ~20 adults per group plus offspring.
- Individual identification via fur marks and dye marks; radio collars used for location; groups routinely observed by researchers.
- Data collected across multiple breeding attempts to assess effects of provisioning on social and offspring outcomes.

## Study setting and data collection context
- Groups visited every 1–3 days for at least 20 minutes; pups observed and tracked from birth through early life.
- Reproductive events highly synchronized; pregnancy detected by abdominal swelling and ultrasound.
- Pups marked and sampled for genetics to assign parentage; escorting behavior recorded post-den emergence.
- Spatial context inferred via radio telemetry locations and regular group visits, enabling potential GIS-based mapping of territories and movements.

## Experimental design
- Split-plot provisioning experiment to test effects of early-life resource provisioning:
  - Fed (provisioned) vs. non-fed (control) pregnant females within breeding attempts.
  - Randomized assignment within age-matched pairs; cross-pairing rules applied to maintain balance.
  - Each manipulated breeding attempt followed by an unmanipulated (control) attempt to dissipate provisioning effects before next manipulation.
- Provisioning details:
  - Fed females received an average of 50 g of egg/day (randomized 0, 50, or 100 g and time of day to prevent anticipation).
  - Across the study: 34 breeding attempts in 7 mongoose groups (2013–2016) resulting in 101 fed pregnancies and 97 non-fed pregnancies.
- Offspring outcomes:
  - Pups emerged around 30 days after birth; a communal escorting period lasts ~60 days.
  - Pups marked and genetically parented; maternity assignments with ~90% probability.

## Fieldwork instrumentation and workflow
- Data collected with a bespoke app (Mongoose 2000) on Samsung tablets; data stored in MS Access database.
- Measurements:
  - Weights obtained via portable electronic scales (Sartorius TE6100).
  - Radio collars (~30 g) with whips for location tracking.
  - Pregnancy confirmed via ultrasound (pre-2017 SIUI CTS-900V or Sonoscape S6BW).
- Calibration:
  - Field instruments calibrated to factory settings.

## Analytical focus (key variables and computations)
- Female condition:
  - Pre-pregnancy weight baseline (67–74 days before birth) and percent weight change during pregnancy, post-pregnancy, and escorting period.
- Escorting behavior:
  - Female and male escorting effort: proportion of group visits in which the individual escorted.
  - Age at escorting period; ratio of adults to pups in the group.
- Allocation of escorting:
  - For manipulated litters, amount of escorting by fed vs non-fed females (and by males) toward each pup.
  - Age and helper ratio context for adults and pups.
- Pup outcomes:
  - Pup weights (30–90 days old) with age-at-weighing; within-litter variance relative to total variance.
  - Amount of escorting received by each pup (escorts’ group visits, likelihood of escort-neighbor proximity, feeding rate by escorts).
  - Survival to 90 days, 180 days, and 365 days, with end ages and helper ratios context.
- Dyadic relationships:
  - Pairwise relatedness between pup-adult dyads.

## Quality control
- Internal checks in Mongoose 2000 to ensure data integrity (e.g., presence requirements for data collection on individuals).
- Data quality checks performed via MS Access queries and bespoke R code to detect inconsistencies (e.g., multiple death records).

## Data structure and contents
- Data stored in 15 CSV files, detailing multiple aspects of the study:
  - Female weight changes from pre-pregnancy baseline to birth.
  - Female weight changes from pre-pregnancy baseline to post-pregnancy.
  - Female weight changes from pre-pregnancy baseline to the escorting period.
  - Female escorting effort across the escorting period (by age, esc.index, esc.freq, category).
  - Male escorting effort across the escorting period (by age, esc.index, esc.freq, exp, helper.ratio).
  - Amount of escorting effort that fed and non-fed females directed toward each pup (pup.id; age; pup.sex; esc.index; esc.freq; pup.category; ad.category; helper.ratio).
  - Pairwise relatedness between pup-adult pairs and escort-pup dyads (r-dyadic; dyadic relatedness; escort indicator).
  - Amount of escorting effort that males directed toward each pup (pup.id; age; pup.sex; esc.index; esc.freq; pup.category; helper.ratio).
  - Pup weights (indiv; pup ID; group; weight; litter; age; sex; category; helper.ratio).
  - Relative within-litter variance in pup weight (relative.variance; age.cat; litter.cat).
  - Amount of escorting received by pups (pack; group; litter; esc.index; esc.freq; helper.ratio; category; sex).
  - Rate of escort feeding (focal.id; category; group; litter; feeds.rate; nn.str; obs).
  - Pup survival to 90 days (surv.90days; end.age.90day; helper.ratio; sex).
  - Pup survival to 180 days (surv.6mo; end.age.6mo; helper.ratio; sex).
  - Pup survival to 365 days (surv.year; end.age.year; helper.ratio; sex).
- Each dataset is linked by identifiers such as indiv (individual ID), breeding attempt ID, litter, pack, group, and category (fed, non-fed, or unmanipulated).

## GIS relevance and potential map-based data products
- Spatially anchored observations:
  - Group locations and movements via radio telemetry can be mapped to visualize territory boundaries, overlap, and movement corridors.
  - Locations of births, den emergence, and pup escorting events can be linked to group territories for spatial pattern analysis.
- Temporal-spatial analyses:
  - Map pup survival and growth outcomes by group and over time to explore spatial variation in provisioning effects.
  - Visualize provisioning treatments across groups and breeding attempts to assess spatially driven experimental effects.
- Data integration opportunities:
  - Combine with spatial layers of terrain, vegetation, and human disturbance to assess habitat factors influencing escorting, pup survival, and weight changes.
  - Network-style maps: illustrate dyadic escort relationships and relatedness networks among adults and pups, potentially overlaid with spatial proximity data.
- Visualization-ready datasets:
  - A repository of CSVs with consistent keys enables construction of GIS-ready layers (points for observations, polygons for territories, choropleth layers for survival rates, and network graphs for escort interactions).

## Summary for GIS specialists
- The document details a long-term, location-based study of banded mongooses employing a randomized provisioning experiment to assess effects on maternal condition, social behavior, and offspring outcomes.
- Data are collected via a dedicated mobile app, integrated into an MS Access database, with extensive quality control and calibration steps.
- The study yields rich, 15-file CSV datasets capturing physiological, behavioral, genetic, and survival metrics at the individual, litter, and group levels, suitable for GIS-enabled analyses of spatial patterns, movement, social networks, and habitat associations.
- Key GIS-centric opportunities include mapping territory use, escorting and dispersal pathways, pup survival spatial gradients, and integrating spatial context with the provisioning experiment to explore how space and habitat influence social and reproductive dynamics.