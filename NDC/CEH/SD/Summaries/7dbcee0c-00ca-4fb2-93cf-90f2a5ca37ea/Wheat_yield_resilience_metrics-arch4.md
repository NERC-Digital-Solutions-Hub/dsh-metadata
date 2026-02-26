# Yield resilience of wheat yields in England

## Overview
- Dataset summarises resilience of winter wheat yields in England over 2008–2017 at 10km x 10km grid cells (hectads).
- Metrics provided: Mean.Yield, Relative.Yield, Stability, and Resistance to an extreme event (notably the 2012 heavy rainfall).
- Aimed at exploring the influence of landscape structure on yield resilience and enabling assessment of data coverage and biases.
- Hectads included only if they have data from at least 9 holdings across the time series; ensures anonymity and data quality.

## Data collection, aggregation, and sampling
- Data originate from Defra’s annual survey of a stratified random sample of farm holdings (June census), with coordinates at 1km resolution.
- UKCEH obtained the data under confidentiality; cleaning removed anomalous values (zeros, whole-crop silage, obvious outliers).
- Because a new random sample is drawn each year, results are aggregated to mean annual yield per 10km x 10km hectad to account for local variation and preserve respondent anonymity.
- 315 hectads had data from every year; 137 were deemed sufficiently well-sampled for robust analysis after applying sampling-threshold criteria.
- Sampling threshold for inclusion: no more than one year with a single sample and no more than two years with fewer than three samples.
- Data structure includes per-hectad yearly sample counts (2008–2017) and an explicit check of compliance with minimum sample requirements, plus a total count of unique holdings per hectad.

## Calculation of resilience metrics
- Resilience concept: the agricultural system’s ability to maintain yields despite environmental perturbation.
- Three metrics computed for each eligible hectad:
  - Relative.Yield: average difference between annual yield and national average annual yield (expressed as a percentage).
  - Stability: inverse of the average absolute percentage difference between a given year’s yield and the moving-average yield around that year.
  - Resistance: inverse of the absolute percentage difference between a year’s yield and the moving-average around that year, with 2012 used as an extreme-weather reference event.
- All metrics are structured so that larger values indicate greater resilience.

## Details of data structure
- File: Yield_Resilience_Stats_wheat.csv
- Core columns:
  - Hectad (OS grid reference)
  - Mean.Yield (tonnes per hectare)
  - Relative.Yield (percentage)
  - Stability (dimensionless)
  - Resistance (dimensionless)
  - 2008–2017: Number of sampled holdings per hectad per year
  - Filter (TRUE/FALSE): indicates whether the hectad meets adequate sampling criteria for further analysis
  - Number.of.holdings: total unique holdings contributing to the metrics across the time series
- Notes:
  - The dataset reflects masking to protect anonymity and includes data from 315 hectads, with 137 meeting stringent sampling criteria for robust analysis.
  - File name indicates focus on wheat resilience stats.

## Data quality and usage notes
- Data cleaned to remove anomalies; anonymity preserved by aggregating at hectad level rather than linking yields to individual holdings.
- Sampling counts enable users to assess potential biases due to varying sample sizes across hectads and years.
- An extreme-weather event (2012) is explicitly considered in the Resistance metric, highlighting the dataset’s ability to reflect resilience to perturbations.

## Practical implications for data leaders
- Governance and stewardship:
  - Clear anonymity constraints and per-year sampling counts support responsible data handling and transparency about limitations.
  - The explicit Filter flag helps prioritize robust, bias-aware analyses and reproducibility.
- Data strategy and discovery:
  - The dataset reveals how granular data (hectads) and temporal depth (2008–2017) enable landscape-scale resilience insights, but also underscores challenges in obtaining uniform sampling across space and time.
  - Metadata (sample counts, aggregation rationale, and anomaly removal steps) supports discoverability and proper use in analyses and policy discussions.
- Cross-functional value:
  - Useful for linking agricultural data with landscape planning, climate resilience, and policy evaluation.
  - Highlights potential needs for additional data collection or enhanced metadata to address gaps in granularity, coverage, and standardization across datasets.