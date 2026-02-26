# Overview

- Objective and scope
  - Dataset on resilience of wheat yields in England derived from Defra’s annual Cereals and Oilseeds production survey of commercial farms (2008–2017).
  - Aims to explore how landscape structure influences yield resilience; metrics are calculated at 10km × 10km grid cells (hectads).

- Spatial and temporal coverage
  - Time-series: 2008–2017.
  - Spatial resolution: 10km × 10km hectads (Ordnance Survey grid cells).
  - 315 hectads have data across the full time-series; 137 are deemed sufficiently well-sampled for robust analyses.

- Data collection and anonymization
  - Collected by Defra via a stratified random sample of farm holdings as part of the June agricultural census.
  - Original data include average winter wheat yield per holding with coordinates at ~1 km.
  - Data cleaned to remove anomalies and aggregated to mean annual yield per hectad to preserve anonymity (a new random sample is drawn each year, limiting cross-year continuity).

- Resilience metrics (calculated per eligible hectad)
  - Relative Yield: average difference between annual yield and national average annual yield, expressed as a percentage.
  - Stability: inverse of the average absolute percentage difference between each year’s yield and the moving average of adjacent years.
  - Resistance: inverse of the absolute percentage difference between a year’s yield and the moving average of adjacent years, with 2012 used as a notable disturbance (extremely heavy rainfall).

- Data structure and contents
  - Single CSV file: Yield_Resilience_Stats_wheat.csv.
  - Key columns:
    - Hectad (OS grid reference)
    - Mean.Yield (tonnes per hectare, time-series mean)
    - Relative.Yield, Stability, Resistance (resilience metrics; larger is more resilient)
    - 2008–2017: Number of sampled holdings per hectad per year
    - Filter (TRUE/FALSE): indicates adequacy of sampling for further analysis
    - Number.of.holdings: total unique holdings contributing to metrics across the time series
  - Additional notes:
    - No hectad with data from fewer than nine holdings across the time series is included (Defra anonymity threshold is generally <5, but a stricter threshold of 9 is used here for robustness).
    - Data include sampling counts to assess and control for sampling bias.

- Data quality, filtering, and use considerations
  - A subset of 137 hectads is used for analyses to minimize biases related to sample size and its relationship with mean yield.
  - Because a new random sample is drawn each year, cross-year continuity is limited, which affects longitudinal inferences at the hectad level.
  - Sampling counts enable bias assessment and filtering; the Filter column helps identify hectads suitable for further analysis.

- Practical applications for analysts
  - Examine correlations between resilience metrics (Relative.Yield, Stability, Resistance) and landscape or management variables.
  - Model how landscape structure affects yield resilience across hectads.
  - Use per-hectad sampling data to assess and correct for potential sampling biases in regional resilience analyses.
  - Leverage the anonymized, aggregated 10km grid data to ensure privacy while conducting spatial resilience studies.