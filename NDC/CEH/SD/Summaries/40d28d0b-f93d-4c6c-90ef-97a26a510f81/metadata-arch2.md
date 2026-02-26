# Ecol-Evol_Bennett_CommonGuillemot_occupancy-data.csv

## Overview
- A dataset detailing occupancy and breeding-related metrics for Common Guillemots across sub-colonies and sites.
- Data derived from time-lapse imagery to assess presence of birds, occupancy duration, and breeding outcomes within defined seasons.
- Designed to support standardized comparisons across sub-colonies and study seasons, aligned with environmental monitoring aims.

## Data structure and key variables
- season: Non-breeding season label (e.g., '2017_18'), spanning Oct 1 to Mar 31 of the following year.
- sub_colony: Sub-colony ID.
- site_ID: Site identifier within each sub-colony (specific to each sub-colony).
- ordinal_laid: Ordinal day of year when an egg was laid in the breeding season following the non-breeding period.
- standard_lay: Mean-centred and scaled lay date relative to sub-colony and study season.
- success: Breeding outcome in the season following the current non-breeding period (1 = success, 0 = unsuccessful).
- no_images_1: Number of time-lapse images with exactly one bird present.
- no_images_2: Number of time-lapse images with exactly two birds present.
- no_images_any: Number of images with one or more birds present.
- no_images_not_present: Number of images with no birds present.
- no_days_1: Number of days the site was occupied by exactly one bird (at least one image per day).
- no_days_2: Number of days the site was occupied by exactly two birds (at least one image per day).
- no_days_any: Number of days the site was occupied by one or more birds.
- no_days_not_present: Number of days with no birds present.
- ordinal_return_1: First ordinal day of the season with exactly one bird present.
- ordinal_return_2: First ordinal day of the season with exactly two birds present.
- ordinal_return_any: First ordinal day of the season with any bird present.
- standard_quality: Mean-centred and scaled site quality relative to sub-colony and study season.
- standard_ordinal_return: Mean-centred and scaled first-appearance date of any presence relative to sub-colony and season.
- standard_time: Mean-centred and scaled relative time investment at a site (ratio of images on days with occupancy to images on days with any presence) per sub-colony and season.
- standard_days: Mean-centred and scaled proportion of survey days with at least one bird present.
- prop_days: Proportion of survey days with one or more birds present.
- standard_ordinal_return_1: Mean-centred and scaled ordinal_return_date_1 for single-bird occupancy relative to sub-colony and season.
- standard_time_1: Mean-centred and scaled time investment for one-bird occupancy (relative to sub-colony and season).
- standard_days_1: Mean-centred and scaled proportion of days with exactly one bird present.
- prop_days_1: Proportion of survey days with exactly one bird present.
- standard_ordinal_return_2: Mean-centred and scaled ordinal_return_date_2 for two-bird occupancy relative to sub-colony and season.
- standard_time_2: Mean-centred and scaled time investment for two-bird occupancy relative to sub-colony and season.
- standard_days_2: Mean-centred and scaled proportion of days with exactly two birds present.
- prop_days_2: Proportion of survey days with exactly two birds present.

## Temporal framing
- The dataset uses a non-breeding season frame, with related breeding-season metrics anchored to that period.
- Example season notation (2017_18) corresponds to Oct 1, 2017 to Mar 31, 2018.

## Derived metrics and standardisation
- Many fields are mean-centred and scaled relative to each sub-colony and study season, enabling cross-site and cross-season comparisons.
- Separate standardised fields exist for single-bird and two-bird occupancy scenarios (e.g., standard_time_1, standard_days_2) to capture different occupancy patterns.

## Data quality and interpretation
- Null values are indicated by 'NA'.
- Variables are based on counts from time-lapse imagery and interpreted to reflect occupancy, timing of presence, and breeding outcomes.

## Use for monitoring and analysis
- Supports consistent reporting of environmental health indicators related to seabird occupancy and breeding success.
- Facilitates categorisation of environmental health against standards and tracking of policy/performance over time.
- Outputs can be presented in clear formats (reports, maps, charts) for monitoring bodies and stakeholders.

## Data access and sharing considerations
- The dataset is structured for storage and upload to appropriate data portals, aligning with standard monitoring practice.
- Emphasises the importance of combining this occupancy data with other relevant datasets to increase value and accessibility of underlying data.