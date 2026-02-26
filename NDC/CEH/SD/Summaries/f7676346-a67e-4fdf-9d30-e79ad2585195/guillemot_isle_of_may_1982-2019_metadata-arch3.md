# Guillemot_Isle_of_May_1982-2019_metadata

## Overview
- Metadata for a Guillemot monitoring dataset covering Isle of May from 1982 to 2019.
- Defines a comprehensive suite of measured variables used to monitor population dynamics, breeding success, chick condition, parental behavior, diet, and environmental context.
- Each variable includes a clear description and, where applicable, uncertainty estimates or sample characteristics.

## Key variables and their meaning
- Population and growth
  - Year
  - Pairs: The number of breeding pairs in year t
  - Pairst-1: The number of breeding pairs in year t-1
  - PopGR: The rate of change in breeding numbers between years

- Environmental context
  - SST: Sea Surface Temperature (°C) in February–March for area 56°-57°N, 1°-3°W in year t
  - SSTt-1: Sea Surface Temperature (°C) in February–March for year t-1 in the same area

- Breeding outcomes
  - N_hatched: The number of chicks hatched
  - N_fledged: The number of chicks fledged
  - Fled_success: The proportion of hatched chicks that fledged
  - Fled_Age: The mean age of chick at fledging (days)

- Chick condition and growth
  - Chick_Mass_N: The number of chicks weighed
  - Chick_Mass_x: The mean mass (g) of chicks with wings ≥ 60 mm
  - Chick_M_SEM: The standard error of mean chick mass
  - Chick_growth_index: Mean mass at age adjusted for fledging age
  - Chick_lineargrowth: Growth rate (g/mm) for chicks with wing lengths 25–59 mm

- Adult and parental factors
  - 2_adults_present: Proportion of chicks with two adults present mid-day
  - 2_adults_SE: Standard error of the proportion above
  - NoAdult_present: Proportion of chicks with no adult present mid-day
  - Parental_effort: Index of parental effort
  - PESE: Standard error of the parental effort index
  - Time_togther: Time adults spent together after a chick was fed (mins)
  - AdSurvival: Mean adult survival from year t to year t+1
  - AdS_LowCI / Ad_UpCI: 95% confidence interval bounds for adult survival
  - Ad_M_N: Number of breeding adults weighed
  - Ad_Mass_x: Mean mass (g) of breeding adults
  - Ad_M_SEM: Standard error of the mean mass of breeding adults

- Feeding, diet, and prey characteristics
  - FeedsD_1: Number of fish fed to a chick in a day
  - Fish_samples: Number of fish identified
  - PropDiet_SE: Standard error of the diet composition by mass
  - PropDiet_Clup: Proportion of chick diet by mass from Clupeidae
  - PropDiet_others: Proportion of chick diet by mass from other species
  - SE_length: Mean length of a sandeel (cm)
  - Clup_length: Mean length of a Clupeidae (cm)
  - SE_energy: Calculated mean energy value of a sandeel (kJ)
  - Clup_energy: Calculated mean energy value of a Clupeidae (kJ)

- Additional outcomes
  - AdSurvival and associated confidence limits capture survival uncertainty
  - Ad_M_N, Ad_Mass_x, Ad_M_SEM provide sampling details and variability for adult weights

## Temporal scope and data structure
- Time frame: 1982–2019
- Includes year-to-year change metrics (PopGR) and lagged environmental context (SST, SSTt-1)
- Combines demographic, reproductive, physiological, behavioral, dietary, and environmental data in a single metadata framework

## Data quality and governance considerations
- Measurements include uncertainty indicators (SEM, CI bounds) for several variables, supporting transparent interpretation.
- Metadata provides explicit definitions, units, and sampling details (e.g., counts, means, and sample sizes) to enable consistent use and comparison.
- The dataset embodies a broad range of data types (counts, proportions, means, indices) that require careful data management and quality assurance when used for monitoring and decision-making.

## Relevance to environmental health monitoring and policy
- Enables assessment of population viability, breeding success, and factors driving changes in Guillemot populations.
- Links demographic and reproductive outcomes with environmental variables (SST), providing insight into climate impacts on breeding ecology.
- Captures trophic ecology and energy intake through diet composition and prey energy metrics, informing ecosystem-based management.
- Supports evaluation of management interventions and policy decisions by providing standardized, quality-assured indicators with uncertainty estimates.
- Facilitates communication of complex findings through clearly defined metrics and accompanying metadata, aiding stakeholders and decision-makers.