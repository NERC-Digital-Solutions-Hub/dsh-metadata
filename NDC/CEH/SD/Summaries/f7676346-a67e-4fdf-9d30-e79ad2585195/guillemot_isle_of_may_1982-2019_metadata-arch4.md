# Guillemot_Isle_of_May_1982-2019_metadata

## Overview
- Metadata dictionary describing a longitudinal dataset on Guillemot population and biology at the Isle of May from 1982 to 2019.
- Captures annual breeding counts, climate covariates, chick development, parental behaviour, diet, energetics, and adult survival.
- Provides both raw counts/observations and derived metrics, with associated uncertainty measures.

## Data structure and scope
- Year-based time series with annual observations.
- Key temporal lags include year t-1 (e.g., Pairst-1) and year-to-year changes (PopGR).
- Variables cover multiple domains: population dynamics, climate, chick development, parental effort, diet, and adult survival.

## Key variable groups

- Population and climate
  - Year
  - Pairs
  - Pairst-1
  - PopGR
  - SST (Sea Surface Temperature in Feb–Mar for a defined lat/long box)
  - SSTt-1

- Chick biology and growth
  - N_hatched
  - N_fledged
  - Fled_success
  - Fled_Age
  - Chick_Mass_N
  - Chick_Mass_x
  - Chick_M_SEM
  - Chick_growth_index
  - Chick_lineargrowth

- Parental behaviour and provisioning
  - 2_adults_present
  - 2_adults_SE
  - NoAdult_present
  - Parental_effort
  - PESE
  - Time_togther

- Diet and prey metrics
  - FeedsD_1
  - Fish_samples
  - PropDiet_SE
  - PropDiet_Clup
  - PropDiet_others
  - SE_length
  - Clup_length
  - SE_energy
  - Clup_energy

- Adult survival and mass
  - AdSurvival
  - AdS_LowCI
  - AdS_UpCI
  - Ad_M_N
  - Ad_Mass_x
  - Ad_M_SEM

## Data quality and measurement details
- Provides uncertainty indicators:
  - Standard errors (e.g., Chick_M_SEM, 2_adults_SE, PESE, Ad_M_SEM)
  - Confidence intervals for survival (AdS_LowCI, AdS_UpCI)
- Units and scales specified:
  - SST: degrees Celsius
  - Mass measures: grams
  - Energy: kilojoules
  - Time: minutes or days as specified in variable descriptions
- Some metrics are derived (e.g., Chick_growth_index, Chick_lineargrowth) from primary measurements (mass, age, wing length).

## Temporal and spatial scope
- Temporal: 1982 through 2019 (annual data points).
- Spatial: Sea Surface Temperature defined for a specific area (56°-57°N, 1°-3°W) relevant to the Guillemot population study.

## Governance, reuse, and reproducibility considerations
- Metadata provides clear names and descriptions for discoverability and reuse.
- Clear documentation of units, measures, and derivations supports reproducibility and cross-study integration.
- Presence of lagged variables and derived indices enables time-series analyses and modeling of drivers (climate, prey, parental effort) on chick outcomes and adult survival.

## How data leaders can use this metadata
- Assess data coverage across population, climate, chick development, diet, and survival domains to plan analyses and data collection.
- Link climate (SST) to chick performance and survival through lagged relationships (t vs. t-1).
- Evaluate data quality by examining uncertainty measures and confidence intervals to inform weighting in analyses.
- Develop governance for data provenance and updates by aligning raw counts with derived metrics (e.g., growth indexes, survival estimates).
- Support cross-domain insights (e.g., how diet composition (PropDiet_Clup, PropDiet_SE) relates to chick growth and fledging success).