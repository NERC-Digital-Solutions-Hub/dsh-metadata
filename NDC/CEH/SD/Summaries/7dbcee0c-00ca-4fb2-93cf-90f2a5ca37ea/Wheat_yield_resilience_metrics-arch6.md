# Overview

- Purpose of the dataset
  - Provides resilience metrics for England wheat yields from 2008–2017, summarised at 10km x 10km hectad resolution to explore how landscape structure influences yield resilience.
  - Includes per-hectad sampling information to enable bias assessment and filtering.

- Data scope and scope of metrics
  - Temporal: 2008–2017 (10-year time-series).
  - Spatial: England, 10km x 10km hectads; yields aggregated to mean annual yield per hectad to preserve anonymity.
  - Metrics (higher values indicate greater resilience):
    - Mean.Yield: mean yield across the time series.
    - Relative.Yield: average difference between annual and national average yield (as a percentage).
    - Stability: inverse of the mean absolute difference between yearly yield and a nearby moving average.
    - Resistance: inverse of the absolute difference between a year’s yield and the nearby moving average, with emphasis on resilience to extreme events (e.g., 2012).

- Data collection and processing
  - Source: Defra cereals and oilseeds production survey (June census) of a stratified random sample of farm holdings.
  - Data details: yield per holding with 1km coordinates; anonymised and cleaned (removal of anomalies such as zero values and obvious outliers).
  - Anonymity and formatting: because a new random sample is drawn each year, data were aggregated to 10km x 10km cells; this supports anonymity and enables time-series resilience analysis.
  - Masked periods and sampling: 315 hectads have data for all years, but only 137 are deemed sufficiently well-sampled for robust analysis.

- Data structure and contents
  - File: Yield_Resilience_Stats_wheat.csv
  - Columns:
    - Hectad: OS grid reference (decimal)
    - Mean.Yield: mean yield across 2008–2017 (tonnes/ha)
    - Relative.Yield: average difference from national annual yield (percentage)
    - Stability: year-to-nearby-year yield stability (inverse percentage)
    - Resistance: resilience to year-to-nearby-year yield perturbations (inverse percentage)
    - 2008–2017: number of sampled holdings per year
    - Filter: TRUE/FALSE indicating adequate sampling for further analysis
    - Number.of.holdings: total unique holdings contributing to metrics across the series

- Sampling adequacy and quality controls
  - Anonymity rule: no hectad included with data from fewer than 9 holdings across the time series.
  - Well-sampled subset: analyses used 137 hectads deemed sufficiently well-sampled to minimise biases related to sample size and mean yield.
  - Filtering criteria: to be considered adequately sampled (Filter = TRUE), hectads must not have more than one year with a single sample and not more than two years with fewer than three samples.

- Practical considerations for use
  - Data quality and biases: use Number.of.holdings and Filter flags to assess and filter potential biases due to uneven sampling.
  - Dataset scope: original dataset includes 315 hectads with complete time-series data; robust analyses focus on the 137 well-sampled hectads.
  - Applications: suitable for analysing how landscape and sampling structure relate to yield resilience and for creating data products that enable end users to explore resilience across space and time.