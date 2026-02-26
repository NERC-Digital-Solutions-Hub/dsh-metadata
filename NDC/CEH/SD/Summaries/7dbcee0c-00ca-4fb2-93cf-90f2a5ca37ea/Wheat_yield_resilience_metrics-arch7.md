# Overview

- Dataset on resilience of wheat yields in England (2008–2017), summarised at 10km × 10km hectad resolution.
- Metrics include mean yield, relative yield, yield stability, and resistance to an extreme event (20012 poor weather); calculated for hectads with sufficient data.
- Data derived from the Defra Cereals and Oilseeds production survey of commercial farms; anonymised and cleaned.

## What the dataset contains

- Metrics for each eligible hectad:
  - Mean.Yield: mean yield across the time series (tonnes per hectare)
  - Relative.Yield: average difference between annual and national average yield
  - Stability: inverse of year-to-neighbouring-average absolute percentage difference (yearly vs. nearby years)
  - Resistance: inverse of year-to-neighbouring-average absolute percentage difference around a specific year (captures 2012 event)
- Time-series data across 2008–2017 for each hectad.
- Sample counts per year (2008–2017) to assess sampling bias.
- A Filter flag indicating adequate sampling for further analysis.
- Number.of.holdings: total unique holdings contributing to metrics across the series.

## Data collection and anonymization

- Collected by Defra via a stratified random sample of farm holdings; coordinates to 1 km resolution.
- Data cleaned to remove anomalous values (e.g., zeros, whole-crop silage) and obvious outliers.
- Random yearly samples mean few holdings are observed in multiple years; data aggregated to 10 km × 10 km hectads to preserve anonymity per Defra’s requirements.

## Metrics calculated

- Relative yield: annual yield deviations from national average (as a percentage).
- Stability: durability of yield around a moving average (inverse percentage difference).
- Resistance: sensitivity to a notable adverse year (inverse percentage difference around surrounding years).
- Higher values denote greater resilience.

## Data structure and file

- Single CSV: Yield_Resilience_Stats_wheat.csv
- Key columns:
  - Hectad
  - Mean.Yield
  - Relative.Yield
  - Stability
  - Resistance
  - 2008 … 2017 (sample counts per year)
  - Filter (TRUE/FALSE)
  - Number.of.holdings

## Sampling adequacy and filtering

- 315 hectads have data from at least one sampled holding in every year (minimum to calculate resilience metrics); 137 of these are deemed sufficiently well-sampled for robust analysis.
- Sampling thresholds:
  - No more than one year with a single sample.
  - No more than two years with fewer than three samples.
- Defra anonymity rule: no hectad with data from fewer than 9 holdings across the time series (minimum level to protect anonymity, with a conditional threshold of <5 in certain contexts).

## How this supports GIS work

- Suited for map-based visualization of spatial resilience patterns across England.
- Can be joined to a 10 km hectad shapefile to produce thematic maps of:
  - Mean yield
  - Relative yield
  - Stability
  - Resistance
- Useful for exploring how landscape structure and spatial variation influence resilience, and for identifying regions with robust or fragile wheat yields.
- Availability of per-year sample counts enables assessment of data reliability and potential biases in mapped results.

## Cautions for use

- Data are anonymised; no attribution to individual holdings; some spatial detail is intentionally generalized to protect privacy.
- Not all hectads are equally well-sampled; 137 well-sampled hectads offer the most reliable insights, while others may be biased by sampling variance.
- The dataset reflects a single-year extreme event (2012) and may be sensitive to specific climatic episodes; interpret resistance in that context.
- A new random sample is drawn each year, so longitudinal continuity at the individual hectad level is limited.