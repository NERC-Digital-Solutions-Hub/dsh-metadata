# Guillemot_Isle_of_May_1982-2019_metadata

## Overview
- Longitudinal metadata for Guillemots on the Isle of May covering 1982–2019.
- Describes variables spanning population metrics, environmental conditions, chick biology, parental behavior, diet, and adult survival/mass.
- Each item links to specific measurements or counts used to explore breeding success, growth, and foraging dynamics.

## Data elements by theme

- Population and reproduction
  - Year
  - Pairs
  - Pairst-1 (breeding pairs in year t-1)
  - PopGR (rate of change in breeding numbers between years)

- Environment
  - SST (Sea Surface Temperature in February–March for area 56°-57°N, 1°-3°W, year t)
  - SSTt-1 (SST for year t-1)

- Chick outcomes and growth
  - N_hatched (number of chicks hatched)
  - N_fledged (number of chicks fledged)
  - Fled_success (proportion of hatched chicks that fledged)
  - Fled_Age (mean age at fledging in days)
  - Chick_Mass_N (number of chicks weighed)
  - Chick_Mass_x (mean mass of chicks with wings ≥ 60 mm)
  - Chick_M_SEM (standard error of mean chick mass)
  - Chick_growth_index (mean mass at fledging divided by mean age in days)
  - Chick_lineargrowth (growth rate in g/mm for chicks with wing 25–59 mm)

- Parental behavior and care
  - 2_adults_present (proportion of chicks with two adults present at midday)
  - 2_adults_SE (standard error for 2_adults_present)
  - NoAdult_present (proportion of chicks with no adult present at midday)
  - Parental_effort (index of parental effort)
  - PESE (standard error of parental effort)
  - Time_togther (time adults spent together after a chick was fed)

- Foraging and diet
  - FeedsD_1 (number of fish fed to a chick per day)
  - Fish_samples (number of fish identified)
  - PropDiet_SE (seasonally estimated diet proportion by mass)
  - PropDiet_Clup (proportion by mass of Clupeidae)
  - PropDiet_others (proportion by mass of other species)
  - SE_length (mean length of a sandeel in cm)
  - Clup_length (mean length of a Clupeidae in cm)
  - SE_energy (mean energy value of a sandeel in kJ)
  - Clup_energy (mean energy value of a Clupeidae in kJ)

- Adult survival and mass
  - AdSurvival (mean adult survival from year t to t+1)
  - AdS_LowCI (Lower 95% CI of adult survival)
  - AdS_UpCI (Upper 95% CI of adult survival)
  - Ad_M_N (number of breeding adults weighed)
  - Ad_Mass_x (mean mass of breeding adults)
  - Ad_M_SEM (standard error of the mean mass for breeding adults)

## Data use considerations

- Variables include year-specific measures and some lagged terms (e.g., year t-1) for comparative analyses.
- The dataset enables exploration of links between environment (SST), breeding output (pairs, fledging), chick growth and survival, parental investment, diet composition, and adult condition. 
- Suitable for creating dashboards, time-series analyses, and self-serve data products to inspect trends and relationships over the 1982–2019 period.