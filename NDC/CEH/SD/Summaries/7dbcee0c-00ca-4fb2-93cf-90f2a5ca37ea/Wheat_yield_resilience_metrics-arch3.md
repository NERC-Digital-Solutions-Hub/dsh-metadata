# Yield_Resilience_Stats_wheat.csv

## Overview and purpose
- Dataset on resilience of wheat yields in England derived from the Defra Cereals and Oilseeds production survey of commercial farms (2008–2017).
- Metrics are summarized at 10km x 10km grid cells (hectads) to explore how landscape structure affects yield resilience.
- Provides mean yield, relative yield, yield stability, and resistance to an extreme event (the 2012 weather).
- Includes the number of samples per year per hectad to enable assessment of sampling biases.
- Only hectads with data from at least one sampled holding in every year are included; anonymity constraints remove hectads with too many identifying risks (<9 holdings across the time series).

## Data collection, aggregation, and sampling
- Data originate from a stratified random sample of farm holdings, collected during Defra’s annual June census of the English agricultural sector.
- Holdings coordinates locate each sample to 1 km; dataset obtained under confidentiality by UKCEH.
- Data cleaned to remove anomalous yields (e.g., zeros, whole crop silage harvests, obvious outliers).
- Due to annual rotation of the random sample, few holdings appear across all 10 years; data are aggregated to mean annual yield per 10 km x 10 km hectad to reflect local practices and preserve anonymity.
- 315 hectads meet the minimum time-series data requirement; 137 hectads are retained for analysis after applying sampling-threshold filters to balance sample size and reduce biases.

## Calculation of resilience metrics
- Broad definition used: resilience as the agricultural system’s ability to maintain consistent yields despite environmental perturbations.
- Three metrics computed for each eligible hectad:
  - Relative yield: average difference between the hectad’s annual yield and the national average annual yield (expressed as a percentage).
  - Stability: inverse of the absolute percentage difference between a year’s yield and the moving average of surrounding years; averaged across the time series.
  - Resistance: inverse of the absolute percentage difference between a year’s yield and the average yield of surrounding years; used to capture response to an extreme event (e.g., 2012 heavy rainfall).
- All three metrics are scaled so that larger values indicate greater resilience.

## Data structure and contents
- File: Yield_Resilience_Stats_wheat.csv
- Key columns:
  - Hectad: OS grid reference (decimal)
  - Mean.Yield: mean yield over the time series (tonnes per hectare)
  - Relative.Yield: average difference between annual and national average yield
  - Stability: resilience metric (as defined above)
  - Resistance: resilience metric (as defined above)
  - 2008–2017: yearly counts of sampled holdings in that hectad
  - Filter: TRUE/FALSE indicating whether the hectad meets the adequate sampling criteria
  - Number.of.holdings: total unique holdings contributing to metrics across the time series

## Data quality, anonymity, and governance
- Data cleaned to remove anomalies and preserve anonymity (yields attributed only to aggregated hectads, not individual holdings).
- Anonymity constraint: hectads with fewer than 9 holdings across the time series are excluded.
- Sampling adequacy is tracked with per-year counts and the Filter flag to identify reliable areas for analysis.
- The dataset supports transparency in data sources and processing, aligning with broader data governance practices essential for monitoring frameworks.

## Relevance for monitoring frameworks
- Provides a structured, transparent set of resilience metrics that can be integrated into environmental health monitoring frameworks.
- Facilitates assessment of data gaps, metadata needs, and governance requirements (e.g., data sharing and standardization) when evaluating policy impacts on agricultural resilience.
- Demonstrates practical handling of data quality, anonymization, and spatial-temporal aggregation to enable robust policy-relevant insights while preserving respondent confidentiality.