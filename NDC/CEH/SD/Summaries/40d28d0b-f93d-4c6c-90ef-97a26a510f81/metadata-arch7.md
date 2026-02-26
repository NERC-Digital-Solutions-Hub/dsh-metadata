# Ecol-Evol_Bennett_CommonGuillemot_occupancy-data.csv

## Overview
- A data file describing occupancy of Common Guillemots across sub-colonies and sites during the non-breeding season, using time-lapse imagery.
- Null values are indicated by NA.
- Season format exemplified as '2017_18', representing the non-breeding period from 1 Oct to 31 Mar.
- Includes raw counts (e.g., no_images_1, no_images_2, no_days_any) and derived metrics (e.g., standard_quality, standard_time) that are mean-centred and scaled relative to each sub-colony and study season.
- Variables cover occupancy presence, number of birds observed, timing of first presence, and proportion of survey effort, enabling spatial and temporal analysis of occupancy patterns.

## Key fields

- Temporal and seasonal context
  - season: non-breeding season of study (e.g., '2017_18').
  - ordinal_laid: day of year when an egg was laid during the breeding season following the non-breeding period.
  - standard_lay: mean-centred and scaled lay date relative to sub-colony and season.
  - ordinal_return_1 / ordinal_return_2 / ordinal_return_any: first ordinal day of the season that one bird, two birds, or any bird was present.
  - standard_ordinal_return: mean-centred and scaled first presence date relative to sub-colony and season.
  - standard_ordinal_return_1 / standard_ordinal_return_2: standardized first presence for one bird and two birds.

- Spatial context
  - sub_colony: sub-colony ID.
  - site_ID: site identifier within each sub-colony (IDs are sub-colony specific).

- Occupancy and presence metrics
  - success: whether breeding at the site in the following season was successful (1) or unsuccessful (0) during the current non-breeding period.
  - ordinal_time / standard_time: relative time investment at a site, based on images with birds present.
  - standard_time_1 / standard_time_2: standardized relative time investment for one bird or two birds.
  - standard_days / standard_days_1 / standard_days_2: mean-centred, scaled proportion of survey days with birds present (overall, or with one or two birds).
  - prop_days / prop_days_1 / prop_days_2: proportion of survey days with one or more birds present (overall, or with one/two birds).
  - standard_days_any / standard_days_not_present / prop_days_any / no_days_any: standardized metrics for days with any birds present, days with no birds, and related proportions.

- Bird counts per image and presence status
  - no_images_1 / no_images_2: number of time-lapse images with exactly one or two birds.
  - no_images_any: number of images with one or more birds.
  - no_images_not_present: number of images with no birds.
  - standard_time: mean-centred and scaled relative time investment across all occupancy days.

- Derived site quality and presence timing
  - standard_quality: mean-centred and scaled site quality relative to sub-colony and season.
  - no_days_1 / no_days_2: number of days with only one bird or two birds present in at least one image.
  - no_days_any: number of days with at least one bird present.
  - no_days_not_present: number of days with no birds observed.

## Data preparation and standardization
- Several fields (prefixed with standard_) are mean-centred and scaled relative to each sub-colony and study season to enable cross-site comparisons.
- NA values indicate missing data; handle accordingly in analyses and maps.
- The dataset combines counts, presence/absence metrics, and timing metrics derived from time-lapse imagery.

## GIS usage and application
- Connect with spatial layers using site_ID and sub_colony to create site- and sub-colony level occupancy maps.
- Build temporal maps and animations across seasons to visualize changes in occupancy, occupancy duration, and timing of first presence.
- Use standardised metrics (standard_*) to compare across sites with differing sampling effort or season length.
- Derive quality and occupancy indicators (e.g., site quality, occupancy days, proportion of days with birds) for habitat or conservation analyses.
- Combine with other spatial datasets (habitat features, protection status, proximity to colonies) for risk assessments or policy-focused visuals.

## Challenges and considerations for GIS specialists
- Data are distributed across multiple sites and sub-colonies; plan data joins and key consistency (site_ID, sub_colony).
- Large or complex datasets may require chunking or partitioning for efficient mapping and processing.
- Data standards are essential to enable cross-season comparisons; leverage standard_* fields for normalized analyses.
- Data cleaning and transformation are often required to prepare for visualization and analysis.

## Practical notes for mapping and analysis
- Use season and ordinal_return fields to create season-specific occupancy layers and time-sliced maps.
- Use presence metrics (no_images_any, no_days_any, prop_days) to visualize occupancy intensity and effort.
- Interpret standard_ fields as relative measures; they are not raw counts but standardized indicators suitable for cross-site comparisons.
- Be mindful of NA values; decide on imputation or exclusion rules for spatial analyses and map rendering.