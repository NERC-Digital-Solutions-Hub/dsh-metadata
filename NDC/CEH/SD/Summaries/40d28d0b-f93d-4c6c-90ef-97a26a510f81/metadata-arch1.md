# Ecol-Evol_Bennett_CommonGuillemot_occupancy-data.csv

## Overview
- Dataset containing occupancy-related observations for Common Guillemots across sub-colonies and breeding/non-breeding seasons.
- Null values are represented as 'NA'.
- Focus on occupancy, timing (lay date), bird presence, and derived standardized metrics to support analyses of correlations and predictive relationships with breeding success.

## Key variables (high-level categories)
- Identifiers
  - season: non-breeding season (e.g., '2017_18')
  - sub_colony: sub-colony ID
  - site_ID: site identifier within each sub-colony
- Breeding timing and success
  - ordinal_laid: ordinal day of lay within the breeding season
  - standard_lay: mean-centered and scaled lay date relative to sub-colony and season
  - success: breeding success in the following season (1 = yes, 0 = no)
- Bird presence and occupancy counts
  - no_images_1, no_images_2, no_images_any, no_images_not_present: counts of images with 1 bird, 2 birds, any birds, or no birds
  - no_days_1, no_days_2, no_days_any, no_days_not_present: days with occupancy by 1 bird, 2 birds, any birds, or no birds
- First occupancy return timing
  - ordinal_return_1, ordinal_return_2, ordinal_return_any: first ordinal day of the season with occupancy by 1 bird, by 2 birds, or by any bird
- Standardized site metrics (relative to sub-colony and season)
  - standard_quality: mean-centered and scaled site quality
  - standard_ordinal_return: mean-centered and scaled first occupancy day relative to sub-colony/season
  - standard_time: mean-centered and scaled relative time investment (images per day with occupancy divided by total images that day with occupancy)
  - standard_days: mean-centered and scaled proportion of survey days with occupancy
  - prop_days: proportion of survey days with occupancy
- Sub-category standardized metrics (per 1-bird and 2-bird occupancy)
  - standard_time_1, standard_days_1, standard_ordinal_return_1, prop_days_1
  - standard_time_2, standard_days_2, standard_ordinal_return_2, prop_days_2

## Temporal and spatial structure
- Temporal
  - Data organized by season names (e.g., '2017_18'), representing the non-breeding period (1 Oct to 31 Mar) and associated breeding-season context
  - Standardized variables are computed within each sub-colony and study season to enable comparability
- Spatial
  - Observations span multiple sub-colonies and sites within those sub-colonies (site_ID is unique within a sub-colony)

## Data preparation and use considerations
- Data are numerical with many derived, standardized metrics designed to facilitate cross-site and cross-season comparisons.
- Missing values are indicated as NA; handling of NA is required for analyses.
- The dataset supports analyses of correlations between occupancy metrics and breeding success, as well as predictive modelling of success or occupancy dynamics.
- Because standard_ variables are mean-centered and scaled per sub-colony and season, models should account for this grouping (e.g., include sub-colony/season as random effects or fix the standardization in validation splits).

## Potential analyses for analysts
- Investigate relationships between lay timing (standard_lay) and occupancy intensity (no_images_any, no_days_any).
- Examine whether occupancy patterns (ordinal_return_* and standard_time_*) predict breeding success (success).
- Explore differences in occupancy dynamics between 1-bird and 2-bird scenarios (standard_time_1 vs standard_time_2; standard_days_1 vs standard_days_2).
- Model site quality and occupancy timing as predictors of occupancy duration and return timing.
- Compare across sub-colonies and seasons to identify consistent patterns or local variation.
- Ensure reproducibility by tracking data sources and maintaining metadata for derived standardized variables.