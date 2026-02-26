# Supporting Information

- This document describes a 5 km gridded Standardised Precipitation Index (SPI) dataset for the United Kingdom, produced under Historic Droughts projects, with updated precipitation data and extended accumulation periods.
- It clarifies differences from the previous SPI dataset and notes on version 2 changes.

## I. Brief Description of the dataset

- 5 km gridded SPI data for the UK, a drought index based on precipitation accumulation probability.
- SPI calculated for accumulation periods: 1, 3, 6, 9, 12, 18, 24 months; computed for each of the 12 calendar months.
- Standard gamma distribution fit used with 1961-2010 as the fitting period.
- Temporal coverage: 1862 to 2015.
- Spatial coverage: United Kingdom, stored as NetCDF4 format.
- Data are normal scores (mean 0, standard deviation 1) with no units, limited to -5 to +5.
- Data structure: two-dimensional grids with twelve monthly grids in each yearly file; one file per accumulation period.
- Projection: British National Grid (BNG).

## II. Motivation

- Produced within the Historic droughts project to understand past UK droughts and improve tools for drought management.
- SPI supports monitoring meteorological drought, identifying rare dryness or wet events, and assessing spatial propagation of droughts.
- SPI at multiple timescales provides different insights:
  - 1-month: short-term moisture and potential crop stress.
  - 3-month: short- to medium-term moisture and seasonal context.
  - 6–9 month: medium-term trends relating to streamflows/reservoirs.
  - 12–24 month: long-term precipitation patterns linked to groundwater and reservoir levels.

## III. Data Sources

- Met Office 5 km monthly rainfall gridded data.
  - Combines UKCP09 data (1910-1959, 2001-2011).
  - Monthly rainfall grids derived from Met Office daily grids (1960-2000).
  - Unpublished updates (2012-2015) and rescued data from Historic Droughts project (1862-1909).

## IV. Method for deriving the SPI grids

- SPI defined as the cumulative probability for a given precipitation amount, for each accumulation period ending in a calendar month.
- For each location, SPI is calculated for 7 durations x 12 months = 84 time series.
- Gamma distribution fitted to each time series using L-moments (instead of maximum likelihood) to estimate parameters; implementation via a modified R package SCI.
- Transformation to a normal distribution to obtain “normal scores” with mean 0, sd 1; extreme values (|SPI| > 5) truncated.
- Notes on distribution choice:
  - Gamma distribution widely used and recommended for Europe, but recent work suggests other distributions (e.g., Pearson Type 3, Tweedie) may be more suitable for the UK.
  - This dataset retains gamma-based SPI for consistency; future versions may explore alternative distributions.
- Temporal dependencies:
  - For durations > 12 months, overlapping data means potential autocorrelation in the underlying series.
  - SPIs are computed per calendar month; concatenating months can also introduce autocorrelation, which should be accounted for in trend analyses.

## V. Format of the SPI dataset

- NetCDF4 format following CEH gridded dataset conventions.
- Structure: UK-wide two-dimensional grids; 12 monthly grids per year; one yearly file per accumulation period.
- Projection: British National Grid.
- Data representation: SPI normal scores, range limited to -5 to +5, no units.

## VI. Acknowledgments

- DrIVER project: Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research (NERC NE/L010038/1).
- Historic Droughts project: NE/L01016X/1.
- IMPETUS project: NE/L010267/1.

## Notes on dataset versions

- Note 1: Difference from the previously published SPIgamma61-10 dataset is the underlying rainfall data. The previous version used CEH-GEAR; this version uses Met Office 5 km rainfall grids. Under Historic Droughts, historic rainfall and temperature data were digitised to support higher-quality grids, motivating the change. Calculation methodology for SPI remains the same.
- Note 2: In version 2, underlying monthly rainfall data for 1960–2000 were updated due to localised issues in the original Met Office grids. New monthly rainfall grids were derived from daily grids, and a 9-month accumulation period was added to version 2.