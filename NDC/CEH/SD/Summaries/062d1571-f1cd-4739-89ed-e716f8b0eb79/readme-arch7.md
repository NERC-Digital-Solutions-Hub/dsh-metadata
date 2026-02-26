# Movement metrics of singing and silent Hawaiian field crickets (Teleogryllus oceanicus) in a semi-natural arena.

## Overview
- Study tracking movement metrics of eight crickets per trial (4 females, 4 males) over 3 hours.
- Two treatments: Silent (flatwing males) and Singing (normal-wing males).
- Trials conducted from 20 March to 5 April 2017; 16 trials total, alternating treatments.
- Crickets released into a semi-natural arena with overhead camera array; post-trial offspring data collected from females.

## Data collection and experimental design
- Tracking method: cricket locations extracted from image series; movement metrics calculated in MATLAB.
- Experimental flow: 5-minute habituation, 5 minutes before triggering, then 3-hour trial.
- After each trial: females laid eggs; hatchlings counted.

## Recorded values and units
- Identifiers and basic attributes:
  - ID: individual cricket tag ID.
  - Trial: trial number.
  - Sex: M or F.
  - Age: days old.
- Experimental factors:
  - Treatment: fw (flatwing) or n (normal wing).
  - Weight: in milligrams.
- Reproductive outcomes:
  - Offspring: number of hatchlings (females only).
  - Mated: binary indicator if the female produced any offspring.
- Movement and social metrics:
  - TotalDistance: cumulative distance traveled (pixels). Convert to meters by dividing by 4000.
  - MinsStill: minutes spent stationary.
  - MinsSocial: minutes spent within 15 cm of other crickets.
  - OtherSexPropVar: proportional variation in time spent with crickets of the opposite sex.
- Dataset structure:
  - Each row corresponds to metrics for an individual cricket within a trial; includes trial ID and treatment.

## Quality control
- Trials with tag loss or camera malfunction omitted.
- Result: 3 trials removed, leaving 7 Silent and 6 Singing trials.

## Data structure and accessibility
- Data organized per individual per row, with trial ID and treatment captured alongside behavioral and demographic metrics.
- Source publication: Behavioural plasticity compensates for adaptive loss of cricket song (DOI: https://doi.org/10.1111/ele.14404).

## GIS-oriented considerations and potential data products
- Spatial visualization:
  - Trajectories and heatmaps of movement per trial and per treatment.
  - Comparative maps of total distance across fw vs n treatments.
- Data preparation for GIS:
  - Convert TotalDistance from pixels to meters; align with a spatial grid if georeferencing is possible.
  - Consider adding time stamps per position to enable true space-time trajectories (current data Summary per row; temporal granularity not specified).
- Network and proximity analyses:
  - MinsSocial and OtherSexPropVar enable proximity-based interaction maps or social network visuals.
- Integrated analyses:
  - Link movement patterns to reproductive outcomes (Offspring, Mated) for females.
  - Explore sex- and treatment-specific movement differences (Sex, Treatment, Age, Weight).
- Data quality and provenance:
  - Track which trials were omitted due to data loss; document any gaps when building GIS products.