# Guillemot_Isle_of_May_1982-2019_metadata

## Overview
- A metadata description for the Guillemot Isle of May dataset spanning 1982–2019.
- Captures annual breeding and demographic metrics, environmental context, chick development, parental effort, diet, prey characteristics, and adult survival and condition.

## Temporal and Spatial Scope
- Years included: 1982–2019
- Spatial context: area bounded by 56°-57°N and 1°-3°W
- Key environmental variable: Sea Surface Temperature (SST) in February–March of the defined area (SST) and lagged SST (SSTt-1)

## Key Variables

- Breeding and population
  - Year
  - Pairs: number of breeding pairs in year t
  - Pairst-1: number of breeding pairs in year t−1
  - PopGR: rate of change in breeding numbers between years

- Environmental context
  - SST: February–March SST for the specified area in year t
  - SSTt-1: February–March SST for year t−1

- Productivity and chick outcomes
  - N_hatched: number of chicks hatched
  - N_fledged: number of chicks fledged
  - Fled_success: proportion of hatched chicks that fledged
  - Fled_Age: mean age of chick at fledging (days)

- Chick mass, growth, and morphology
  - Chick_Mass_N: number of chicks weighed
  - Chick_Mass_x: mean mass (g) of chicks with wings ≥ 60 mm
  - Chick_M_SEM: standard error of mean chick mass
  - Chick_growth_index: mean mass at fledging divided by mean age at fledging (g per day)
  - Chick_lineargrowth: growth rate (g/mm) for chicks with wing lengths 25–59 mm

- Parental presence and effort
  - 2_adults_present: proportion of chicks with two adults present mid-day
  - 2_adults_SE: standard error of proportion with two adults present
  - NoAdult_present: proportion of chicks with no adult present mid-day
  - Parental_effort: index of parental effort
  - PESE: standard error of the parental effort index
  - Time_togther: time adults spent together after a chick was fed (minutes)

- Foraging and diet
  - FeedsD_1: number of fish fed to a chick in a day
  - Fish_samples: number of fish identified
  - PropDiet_SE: proportion of chick diet by mass contributed by sandeels
  - PropDiet_Clup: proportion of chick diet by mass contributed by Clupeidae
  - PropDiet_others: proportion of chick diet by mass from other species
  - SE_length: mean length of a sandeel (cm)
  - Clup_length: mean length of a Clupeidae (cm)
  - SE_energy: calculated mean energy value of a sandeel (kJ)
  - Clup_energy: calculated mean energy value of a Clupeidae (kJ)

- Adult survival and body condition
  - AdSurvival: mean adult survival from year t to year t+1
  - AdS_LowCI: lower bound of 95% CI for adult survival
  - AdS_UpCI: upper bound of 95% CI for adult survival
  - Ad_M_N: number of breeding adults weighed
  - Ad_Mass_x: mean mass (g) of weighed breeding adults
  - Ad_M_SEM: standard error of the mean mass of breeding adults

## Derived Metrics and Data Characteristics
- Many variables have associated standard errors or confidence intervals, indicating measurement uncertainty.
- A mix of counts, proportions, means, and indices (with units such as grams, days, minutes, cm, kJ) is present.
- Data enable analysis of relationships among environment (SST), breeding success, chick development, parental behavior, diet, and adult survival.

## Potential Analytical Opportunities
- Examine the impact of February–March SST (and lagged SST) on breeding success and population growth (Pears, N_hatched, N_fledged, PopGR).
- Link chick growth and mass metrics (Chick_Mass_x, Chick_growth_index, Fled_Age) to fledging success and parental effort.
- Assess how diet composition (PropDiet_SE, PropDiet_Clup, PropDiet_others) relates to chick growth, survival, and energy intake (SE_energy, Clup_energy).
- Investigate the relationship between parental presence/effort (2_adults_present, Parental_effort) and chick outcomes (N_fledged, Fled_success, Fled_Age).
- Model adult survival (AdSurvival) in relation to adult mass (Ad_Mass_x) and environmental variables (SST).

## Data Quality and Considerations for Analysts
- Units and measurement scales are explicit (mass in g, energy in kJ, lengths in cm, time in minutes, etc.).
- Presence of standard errors and CIs supports uncertainty quantification in analyses.
- Spatial and temporal alignment is defined (specific SST region and February–March timing); ensure consistent matching when merging with other datasets.
- Be mindful of potential missing values and varying sample sizes across years for derived metrics.