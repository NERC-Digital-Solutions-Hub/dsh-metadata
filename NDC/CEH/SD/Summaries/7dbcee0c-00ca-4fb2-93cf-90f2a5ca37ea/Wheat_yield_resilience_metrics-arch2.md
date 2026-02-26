# Resilience of wheat yields in England

## Overview
- Dataset on resilience of winter wheat yields in England, derived from the Defra Cereals and Oilseeds production survey (2008–2017).
- Aggregated to 10 km × 10 km grid cells (hectads) to enable time-series resilience analysis while preserving anonymity.
- Metrics capture different aspects of resilience: mean yield, relative yield, yield stability, and resistance to an extreme weather event (2012).
- 315 hectads had at least one sampled holding in every year; 137 were deemed sufficiently well-sampled for bias-free analysis.
- Data collection and processing aimed to assess how landscape structure relates to yield resilience.

## Data collection, aggregation and sampling
- Original data from Defra's annual June census survey of a stratified random sample of farm holdings.
- Data span 2008–2017, with yield per holding located to 1 km; anonymized and confidentiality-protected.
- Years are aggregated to 10 km × 10 km hectads to reflect local spatial variation and protect anonymity.
- Anomalous yields removed (e.g., zero values, whole crop silage, obvious outliers).
- Hectads with fewer than 9 holdings across the time series are excluded to maintain anonymity and reduce bias.
- Selection of 137 well-sampled hectads used for the primary analyses; 315 hectads included overall for resilience metrics.

## Calculation of resilience metrics
- Broad definition: the agricultural system’s ability to maintain consistent yields despite environmental perturbations.
- Three metrics calculated for each eligible hectad:
  - Relative yield: average difference between the year's yield and national average yield (expressed as a percentage).
  - Yield stability: inverse of the absolute year-on-year difference around a moving average (aggregated over the time series).
  - Resistance: inverse of the absolute difference between a year’s yield and the moving-average surrounding that year, focusing on resilience to extreme events (notably 2012 rainfall).
- All three metrics are scaled so that larger values indicate greater resilience (using inverse values).

## Details of data structure
- Single CSV file: Yield_Resilience_Stats_wheat.csv
- Key columns:
  - Hectad: OS grid reference (decimal)
  - Mean.Yield: mean yield across 2008–2017 (t/ha)
  - Relative.Yield: average year-to-year deviation from national average (percent)
  - Stability: average inverse percentage deviation around the moving average
  - Resistance: inverse of year-to-year deviation around the moving-average context
  - 2008–2017: number of sampled holdings in each year for the hectad
  - Filter: TRUE/FALSE indicating whether the hectad meets adequate sampling criteria for further analysis
  - Number.of.holdings: total unique holdings contributing to the metrics across the time series

## Sampling thresholds and filtering
- Adequate sampling criteria:
  - No more than one year with a single sample
  - No more than two years with fewer than three samples
- These thresholds help balance maximum sample size with reducing biases related to small samples.
- 315 hectads meet minimum presence criteria; 137 are retained as well-sampled for robust analyses.

## Data quality and scope
- Data cleaned to remove anomalous values and ensure privacy (anonymity and confidentiality).
- Random yearly sampling means few holdings appear across all years; aggregation to hectads preserves locality patterns while enabling longitudinal analysis.
- 2012 extreme weather event used to illustrate resistance metric; acknowledges limitations of single-event framing.

## How to use
- Suitable for monitoring environmental health and policy performance over time by comparing resilience metrics across landscapes and over years.
- Can be combined with other environmental or landscape datasets to enhance the value of the underlying data beyond single-use analyses.
- The dataset includes sample counts per year and a filter flag to help assess and control for sampling biases before interpretation or sharing.