# Yield_Resilience_Stats_wheat.csv

## Overview
- Dataset on resilience of wheat yields in England, derived from the Defra Cereals and Oilseeds production survey of commercial farms.
- Time-series coverage: 2008–2017 (10 years).
- Spatial resolution: 10km x 10km grid cells (hectads).
- Metrics per hectad: Mean.Yield, Relative.Yield, Stability, and Resistance, calculated to assess resilience to environmental perturbations (including the extreme 2012 weather event).
- Sampling: includes the number of samples per year per hectad; designed to allow exploration of sampling biases.
- Accessibility: anonymised data with safeguards; 315 hectads have data for all years, with 137 deemed sufficiently well-sampled for robust analysis.
- Purpose: to explore the impact of landscape structure on yield resilience; supports understanding of data quality and limitations for reuse.

## Data collection, aggregation and sampling
- Source: Defra survey of stratified random sample of farm holdings; coordinates to 1km resolution.
- Confidentiality: data obtained by UKCEH under a confidentiality agreement with Defra; anonymisation is maintained.
- Data cleaning: removal of anomalous yields (zeros, whole-crop silage, obvious outliers).
- Aggregation: individual holdings aggregated to mean annual yield per 10km x 10km hectad to protect anonymity and account for non-consecutive yearly data.
- Coverage: data extended across 2008–2017; 315 hectads meet the minimum requirement of at least one sampled holding each year; 137 hectads are sufficiently well-sampled for robust analyses.
- Sampling thresholds: chosen so as to maximize usable data while reducing bias:
  - No more than one year with a single sample.
  - No more than two years with fewer than three samples.
- Metadata: includes Total Number of Holders (Number.of.holdings) contributing to metrics, and yearly sample counts (2008–2017).

## Calculation of resilience metrics
- Definition: resilience is the agricultural system’s ability to maintain yields despite environmental perturbations.
- Three resilience metrics calculated per eligible hectad:
  - Relative.Yield: average difference between annual yield and national average annual yield (expressed as a percentage).
  - Stability: inverse of the absolute percentage difference between a year’s yield and the average yield over the adjacent years; averaged across the time series.
  - Resistance: inverse of the absolute percentage difference between a year’s yield and the average yield over the adjacent years; emphasizes response to the 2012 extreme weather event.
- Scale: all metrics designed so that larger values indicate greater resilience (i.e., using inverse values).

## Data structure
- File: Yield_Resilience_Stats_wheat.csv
- Key columns:
  - Hectad (OS Grid reference)
  - Mean.Yield (tonnes per hectare; mean across the time series)
  - Relative.Yield (percent difference from national average)
  - Stability (inverse percentage difference; year-to-neighborhood)
  - Resistance (inverse percentage difference; year-to-neighborhood)
  - 2008–2017 (per-year sampled holdings)
  - Filter (TRUE/FALSE) indicating adequate sampling for further analysis
  - Number.of.holdings (total unique holdings contributing across the time series)

## Data governance, privacy and usage
- Anonymity preserved by aggregating to hectads and reporting per-hectad metrics rather than individual holdings.
- Data handling aligned with Defra’s confidentiality requirements and the Agricultural Statistics Act 1979.
- Sampling information and filters included to enable assessment of potential biases and suitability for secondary analysis.
- Data provenance clearly documented: Defra survey data cleaned and transformed by UKCEH under confidentiality.

## Limitations and caveats
- Not all hectads have complete 10-year data; analyses emphasize the 137 well-sampled hectads to minimize bias.
- Possible biases related to sample size; relationships between sample size and mean yield are considered in thresholding.
- 2012 extreme weather event influences Resistance metric and interpretation of resilience to perturbations.
- Results are specific to England wheat yields and the methods used (spatial aggregation, anonymisation) may affect granularity and generalizability.