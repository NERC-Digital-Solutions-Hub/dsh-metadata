# Ecol-Evol_Bennett_CommonGuillemot_occupancy-data.csv

## Overview
- Dataset provides occupancy data for Common Guillemots across sub-colonies and study seasons, derived from time-lapse imagery.
- Null values are indicated by 'NA'.

## Key variables and what they capture
- Identifiers
  - season: non-breeding season; format like '2017_18' (Oct 1 to Mar 31)
  - sub_colony: sub-colony ID
  - site_ID: site number within each sub-colony
- Breeding timing and success
  - ordinal_laid: ordinal day of year when an egg was laid in the breeding season following the season
  - standard_lay: mean-centred and scaled lay date relative to sub-colony and study season
  - success: whether breeding at the site in the following season was successful (1) or unsuccessful (0)
- Time-lapse imagery and daily occupancy
  - no_images_1, no_images_2: number of images with one bird and two birds present, respectively
  - no_images_any: images with one or more birds present
  - no_images_not_present: images with no birds present
  - no_days_1, no_days_2: days with occupancy by one bird; days with occupancy by two birds
  - no_days_any: days with one or more birds present
  - no_days_not_present: days with no birds present
- First occupancy timing
  - ordinal_return_1: first ordinal day of the season with only one bird present
  - ordinal_return_2: first ordinal day with two birds present
  - ordinal_return_any: first ordinal day with any bird present
- Quality and standardized metrics
  - standard_quality: mean-centred and scaled site quality relative to sub-colony and study season
  - standard_ordinal_return: mean-centred and scaled ordinal_return_date relative to sub-colony and season
  - standard_time: mean-centred and scaled relative time investment at a site (ratio of occupancy images to all images on days with birds) relative to sub-colony and season
  - standard_days: mean-centred and scaled proportion of survey days with any occupancy
  - prop_days: proportion of survey days with one or more birds present
- Per-bird occupancy and time metrics (two-bird breakdown)
  - standard_ordinal_return_1, standard_time_1, standard_days_1, prop_days_1: analogous metrics for days with exactly one bird
  - standard_ordinal_return_2, standard_time_2, standard_days_2, prop_days_2: analogous metrics for days with exactly two birds

## Practical interpretations for analysis
- Use to analyze occupancy dynamics across sites and seasons, including timing of occupancy and breeding outcomes.
- Compare single-bird versus multiple-bird occupancy patterns and associated time investments.
- Evaluate relationships between occupancy metrics (e.g., first occupancy timing, time investment) and breeding success.

## Data quality considerations
- Data may be patchy and come from multiple formats; handle 'NA' values consistently.
- Standardized fields are relative to sub-colony and study season; ensure correct interpretation when aggregating.
- Be mindful of potential inconsistencies in site_IDs across sub-colonies. 

## Potential data products and next steps (Data Support perspective)
- Dashboards showing occupancy by site and season, with filters for sub-colony and season.
- Heatmaps of occupancy timing (ordinal_return) and time investment (standard_time) across sites.
- Comparisons of breeding success by occupancy metrics (e.g., early vs late occupancy, single vs double occupancy).
- Self-serve reports and pivot tables enabling exploration of occupancy patterns and usage by end users.