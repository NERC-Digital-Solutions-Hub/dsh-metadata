# Ecol-Evol_Bennett_CommonGuillemot_occupancy-data.csv

## Overview
- Dataset capturing occupancy and breeding-related metrics for common guillemots across sub-colonies and non-breeding seasons.
- Uses NA to indicate missing values.
- Focuses on measures derived from time-lapse imagery, including bird presence, occupancy timing, and breeding outcomes.

## Key fields and meanings
- season: Non-breeding season label (e.g., '2017_18' from Oct 1 to Mar 31).
- sub_colony: Sub-colony ID.
- site_ID: Breeding site ID (specific to each sub-colony).
- ordinal_laid: Ordinal day of egg laying in the breeding season following the non-breeding season.
- standard_lay: Mean-centered and scaled lay date relative to sub-colony and study season.
- success: Breeding success in the following season (1 = yes, 0 = no).
- no_images_1 / no_images_2: Number of images showing exactly one or two birds.
- no_images_any: Number of images with one or more birds.
- no_images_not_present: Number of images with no birds.
- no_days_1 / no_days_2: Number of days with occupancy by exactly one or two birds (in at least one image).
- no_days_any: Number of days with occupancy by at least one bird.
- no_days_not_present: Number of days with no birds present.
- ordinal_return_1 / ordinal_return_2 / ordinal_return_any: First ordinal day of season with occupancy by one bird, two birds, or any occupancy.
- standard_quality: Mean-centered and scaled site quality relative to sub-colony and study season.
- standard_ordinal_return: Mean-centered and scaled ordinal_return_date relative to sub-colony and study season.
- standard_time: Mean-centered and scaled relative time investment (images per day with occupancy divided by images on days with any occupancy) relative to sub-colony and season.
- standard_days: Mean-centered and scaled proportion of survey days with occupancy by one or more birds.
- prop_days: Proportion of survey days with one or more birds present.
- standard_ordinal_return_1 / standard_time_1 / standard_days_1 / prop_days_1: Standardized metrics for occupancy by one bird.
- standard_ordinal_return_2 / standard_time_2 / standard_days_2 / prop_days_2: Standardized metrics for occupancy by two birds.

## Derived metrics and standardization
- Several fields are mean-centered and scaled relative to each sub-colony and study season, enabling comparability across sites and seasons.
- Combines raw counts (images, days, occupancy) with timing and quality indicators to support downstream analyses.

## Data quality and governance considerations
- Missing data represented as NA; ensure appropriate handling during analysis.
- Metadata (definitions and scale) embedded in field descriptions; critical for correct interpretation of standardized measures.
- Data are organized at per-site, per-sub-colony, per-season granularity, facilitating integration with broader data systems and cross-site comparisons.

## How this supports data strategy for a Data Leader
- Provides a comprehensive, standardized set of occupancy and breeding-related metrics essential for monitoring population dynamics.
- The standardized fields enable cross-site, cross-season comparisons and aggregation for reporting and policy support.
- Clear metadata and derived measures support transparent data products and iterative improvement based on user feedback.
- Facilitates data discovery and interoperability within a broader community of practice focusing on avian occupancy and breeding success.