# Standardised Precipitation Index time series for IHU Groups (1961-2012)

## Overview
- A time series dataset of the Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) groups in the UK.
- SPI calculated for accumulation periods of 1, 3, 6, 12, 18, and 24 months, with a separate series for each of the 12 calendar months, totaling 72 series per IHU group.
- Data span: 1961–2012 (fitting period 1961–2010).
- Stored in CSV format; SPI values are unitless normal scores (mean 0, sd 1) truncated to [-5, 5], with -9999 indicating No Data.

## Purpose and Use
- Intended to support incorporation into a CEH droughts portal and enable drought/ moisture condition monitoring over defined IHU regions.
- SPI provides a measure of drought or wetness rarity at multiple time scales, aiding short-, medium-, and long-term water availability assessments.

## Data Sources
- IHU groups (UK) as the spatial framework (roughly 400 km2 per group; defined by rivers and local areas).
- CEH-GEAR gridded rainfall estimates used to derive area-averaged rainfall time series for each IHU group.

## Method for Deriving SPI
- SPI computation follows McKee et al. (1993): calculate accumulation-period-specific precipitation, fit a gamma distribution to historical sums, then transform to a normal distribution to obtain SPI.
- Parameter estimation via L-moments (instead of maximum likelihood) due to stability for some cases; uses R SCI package modified to employ L-moments.
- Gamma distribution commonly used but acknowledged limitations for UK data; alternative distributions (e.g., Pearson type 3, Tweedie) may be considered in future versions if justified.
- For each IHU group:
  - 72 time series derived: 6 durations (1, 3, 6, 12, 18, 24 months) × 12 calendar months.
  - Each SPI value is assigned to the month in which the accumulation period ends (e.g., 6-month SPI for July refers to precip. Jan–Jul).
- Autocorrelation considerations:
  - Long-duration SPIs (>12 months) rely on overlapping data, introducing autocorrelation.
  - Concatenated monthly SPIs are also likely autocorrelated; appropriate adjustments are needed for trend analyses.

## Format and Dataset Contents
- File format: CSV.
- Key fields:
  - RID: Row identifier
  - POLYGONID: IHU group ID (for joining with shapefiles)
  - THEDATETIME: Date and time
  - SPI_1m, SPI_3m, SPI_6m, SPI_12m, SPI_18m, SPI_24m: SPI values for each accumulation period
- SPI values are unitless, with a range typically within [-2, 2], but allowed to extend to [-5, 5]; -9999 denotes No Data.

## Data Quality, Limitations, and Future Work
- Fitting period: 1961–2010; dataset covers 1961–2012 due to data availability.
- The gamma distribution is widely used but may not be optimal for all UK data; alternative distributions could be explored in future versions.
- Pre-1961 data are less reliable due to sparse raingauge networks.
- Serial correlation in long-duration SPIs and overlapping data can affect independence assumptions; users should account for autocorrelation in analyses (e.g., trend assessments).

## Practical Implications for Analysts Monitoring the Environment
- Provides a standardized, regionally aggregated drought/wetness indicator across multiple time scales for UK hydrological units.
- Facilitates cross-regional comparisons and temporal trend analyses within a consistent framework.
- Supports integration into monitoring dashboards and policy performance assessments focused on drought risk and water resource management.