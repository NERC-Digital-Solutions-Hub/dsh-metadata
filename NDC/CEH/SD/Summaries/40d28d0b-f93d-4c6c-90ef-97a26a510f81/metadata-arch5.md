# Ecol-Evol_Bennett_CommonGuillemot_occupancy-data.csv

- The dataset is an occupancy data file for common guillemot, using time-lapse observations and derived metrics to assess presence, breeding activity, and site use across sub-colonies and study seasons.

## Data structure and scope

- File type: CSV with null values indicated as NA.
- Timeframe: Non-breeding season context, e.g., season labeled as '2017_18' corresponds to Oct 1, 2017 to Mar 31, 2018.
- Hierarchy: Observations are linked to sub-colonies and sites within each sub-colony.
- Data types: Mix of raw counts (image-based observations, occupancy days) and standardized (mean-centered and scaled) variables intended for cross-site comparisons.
- Primary purpose: Document occupancy, timing, and breeding-related metrics derived from time-lapse imagery for ecological analysis.

## Key variables and their meanings

- Identifiers and timing
  - season: Non-breeding season label (e.g., '2017_18').
  - sub_colony: Sub-colony ID.
  - site_ID: Site identifier within each sub-colony (specific to sub-colony).
  - ordinal_laid: Ordinal day of the year when an egg was laid at the site in the breeding season during the non-breeding period.
  - standard_lay: Mean-centered and scaled lay date relative to sub-colony and study season.
  - success: Breeding success in the following season (1 = yes, 0 = no).
- Raw counts (image-based observations)
  - no_images_1: Number of time-lapse images with exactly one bird.
  - no_images_2: Number of time-lapse images with exactly two birds.
  - no_images_any: Number of images with one or more birds.
  - no_images_not_present: Number of images with no birds present.
  - no_days_1: Number of days the site was occupied by exactly one bird (in at least one image).
  - no_days_2: Number of days the site was occupied by exactly two birds (in at least one image).
  - no_days_any: Number of days the site was occupied by one or more birds (in at least one image).
  - no_days_not_present: Number of days with no birds present.
  - ordinal_return_1: First ordinal day of the season that only one bird was present at the site.
  - ordinal_return_2: First ordinal day of the season that two birds were present at the site.
  - ordinal_return_any: First ordinal day that a bird was present at the site.
- Standardized quality and timing metrics
  - standard_quality: Mean-centered and scaled site quality relative to sub-colony and study season.
  - standard_ordinal_return: Mean-centered and scaled first occupancy date relative to sub-colony and study season.
  - standard_time: Mean-centered and scaled relative time investment at a site, calculated from daily images with at least one bird present.
  - standard_days: Mean-centered and scaled proportion of survey days with one or more birds relative to sub-colony and season.
  - prop_days: Proportion of survey days with one or more birds.
- Per-bird presence strata (1 bird vs 2 birds)
  - standard_ordinal_return_1, standard_time_1, standard_days_1, prop_days_1: Standardized metrics for sites with exactly one bird.
  - standard_ordinal_return_2, standard_time_2, standard_days_2, prop_days_2: Standardized metrics for sites with exactly two birds.

## Data quality and standardization

- Consistency: Several fields use mean-centred and scaled values relative to sub-colony and study season to enable cross-site comparisons.
- Missing data: NA denotes missing values across all fields.
- Documentation style: The dataset provides explicit definitions for each column, including what is counted (images, days) and how time is encoded (ordinal days, non-breeding season framing).

## Data governance and stewardship considerations

- Metadata needs: Ensure alignment of field names and meanings across related datasets; verify handling of NA values and the definitions of standardized variables.
- Data quality checks: Validate that image-count and occupancy-day counts are consistent with raw observations and that standardization references (sub-colony and season) are applied uniformly.
- Interoperability: Variables use consistent naming for occupancy and timing metrics; be mindful of potential minor naming inconsistencies (e.g., spacing in some names) when integrating with other data holdings.
- Sharing and updates: The dataset implies ongoing data processing (raw counts and standardized metrics); establish procedures for updating standard metrics and re-running standardization as new seasons are added.
- User needs alignment: The dataset combines raw observational data with standardized descriptors to support cross-site analyses, aligning with data stewards’ aim to ensure usable, well-described datasets for discovery and reuse.