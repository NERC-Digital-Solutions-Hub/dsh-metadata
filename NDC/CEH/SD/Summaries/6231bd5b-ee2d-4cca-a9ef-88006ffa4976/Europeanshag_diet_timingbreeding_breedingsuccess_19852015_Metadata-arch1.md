# JAE_Keogan_Europeanshag_phenologymismatch_shagdataset

- Purpose
  - Provides annual measures to study phenology and potential mismatch between European shag breeding timing and prey (sandeel) availability.
  - Supports analyses of how environmental variables (e.g., SST) relate to breeding phenology and fledging success.

- Key variables (shagdataset)
  - year: Year of observation.
  - laydate: Day of year when first egg in nest was laid.
  - chicks.fledged.first: Number of chicks fledged in the first clutch.
  - failedeggsfirst: Number of failed eggs in the first clutch (up to four).
  - Mean.Lay: Average lay date in each year.
  - relative.lay: Nest lay date relative to the annual mean lay date (in days).
  - SST.past / SST.present: Average February/March sea surface temperature for past year and current year.
  - pop.size: Population size in breeding pairs.
  - yearcentre: Year centered around the study’s average year.
  - chicks.fledged.all: Number of chicks fledged from all clutches.
  - failedeggsall: Number of failed eggs from all clutches.

- Key variables (dietdataset)
  - Year: Year of sampling.
  - Date: Day of sample collection (since Jan 1st).
  - Age: Chick or adult.
  - SST: Average February/March SST in the current year.
  - yearcentre: Year centered around the study’s average year.
  - meandate: Average date of sample collection in each year.
  - datediff: Sample collection date centered around the annual average sample date.
  - SE1:SE0_proportion: Proportion of 1+ sandeels relative to all sandeels in the sample.
  - logitSE1:SE0: Logit-transformed version of the above proportion.

- Key variables (bivariatedataset)
  - Year: Year of observation.
  - Species: Shag or sandeel.
  - chicks.fledged: Number of shag chicks fledged.
  - failedeggs: Number of potential failed eggs.
  - sandeelproportion: Proportion of 1+ sandeels relative to all sandeels in sample (shared concept with dietdataset).
  - dayofyear: Day of laying for shags or day of sample collection for sandeels.
  - Mean.Lay: Average lay date in each year.
  - Relative: Day of year (lay date or sample date) centered around the average lay date.

- Analytical opportunities
  - Examine correlations between lay date and SST (environmental driver).
  - Assess phenology mismatch by comparing shag lay dates with prey availability metrics (sandeel proportion, sampling dates).
  - Model predictive relationships for fledging success (chicks.fledged) using lay date, SST, and prey metrics.
  - Use year-centred and relative date variables to standardize across years.

- Data quality and integration considerations
  - Variables are defined at different levels and scales (annual summaries vs. sample-based measures; shag vs. diet vs. bivariate).
  - Alignment across datasets needed for integrated analyses (e.g., linking lay dates with prey proportions in corresponding years).
  - Derived metrics (relative.lay, yearcentre) require careful handling to avoid misinterpretation.
  - Metadata and data provenance are important for reproducibility and discoverability.

- Particular challenges to anticipate (analyst perspective)
  - Limited data at local scales may constrain fine-grained analyses.
  - Data stored across journals, reports, and local datasets may require effort to access and harmonize.
  - Differences in data formats and definitions across datasets (e.g., day of year vs. sampling date) demand standardisation.
  - Availability of multiple datasets may be uneven, necessitating extrapolation with caution.
  - Managing data privacy and documentation when combining datasets; ensuring reproducible data pipelines and metadata.