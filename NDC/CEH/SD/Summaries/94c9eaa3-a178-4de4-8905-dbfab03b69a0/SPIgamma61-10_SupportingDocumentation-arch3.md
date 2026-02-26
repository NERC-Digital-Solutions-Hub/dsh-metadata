# Supporting Information

- Dataset contains 1 km and 5 km gridded Standardised Precipitation Index (SPI) data for Great Britain.
- SPI is a drought index based on precipitation probability for varying accumulation periods (1, 3, 6, 12, 18, 24 months) and for each of the 12 calendar months.
- Standard period used to fit the gamma distribution: 1961-2010; dataset covers 1961-2012.
- Data format: NetCDF4, stored on a THREDDS server; available via the provided DOI link.

## I. Brief Description of the dataset

- SPI calculated as cumulative precipitation probability for chosen accumulation periods; assigned to the month the accumulation ends (e.g., 6-month SPI for July ends in July payoff).
- For each grid cell, 72 time series (6 durations × 12 months) are derived.
- Gamma distribution fitted to each time series using L-moments (via a modified R SCI package) to estimate parameters.
- Transformation to normal scores (mean 0, SD 1); SPI values are unitless and truncated at abs value of 5.
- Notes on distribution choice: gamma widely used and recommended for Europe, but some evidence suggests alternatives (Pearson type 3, Tweedie) may be better for the UK; current dataset uses gamma with potential for future updates.
- Accumulation periods >12 months involve overlapping data, introducing autocorrelation; monthly SPIs constructed similarly may be autocorrelated.
- Why 1961-2010 for fitting: data quality and network density prior to 1961 are poor; focus on drought indicators and impacts within the DrIVER project.

## II. Motivation

- Part of the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research), linking drought indices to impacts data for monitoring and early warning.
- SPI enables spatial analysis of drought propagation, identification of severely affected areas, and assessment across different time scales:
  - 1-month: relates to short-term soil moisture and crop stress.
  - 3-month: short- to medium-term moisture conditions.
  - 6-month: medium-term trends and potential links to streamflows and reservoir levels.
  - 12-month: long-term patterns tied to water resources.
  - 18/24-month: very long-term precipitation patterns, potential groundwater signals.
- Two spatial resolutions (1 km and 5 km) serve different scientific and stakeholder needs: local detail vs. regionally manageable data.

## III. Data Sources

- Primary source: CEH-GEAR (Gridded Estimates of Areal Rainfall) for monthly rainfall inputs.
- CEH-GEAR data underpin the gridded SPI derivation.

## IV. Method for deriving the SPI grids

- SPI calculated from historical precipitation accumulations; for each location, six accumulation periods and twelve months produce 72 time series.
- Gamma distribution fitted to each time series using L-moments; parameters estimated with a modified SCI R package.
- SPI computation involves transforming data to a standard normal distribution (mean 0, SD 1).
- Data handling decisions:
  - SPI values truncated to [-5, 5].
  - Acknowledgement that gamma distribution may not be optimal in all cases; alternative distributions discussed for future updates.
- Data structure considerations:
  - For >12-month periods, overlapping data create potential autocorrelation in the series.
  - Concatenated monthly SPIs are likely autocorrelated; trend analyses should account for this.
- Temporal coverage rationale:
  - 1961-2010 used for fitting; dataset extends to 2012 to support broader analyses.

## V. Format of the SPI dataset

- Stored in NetCDF4, following CEH gridded dataset conventions.
- Structure: two-dimensional Great Britain grids, with twelve monthly grids per year; one file per accumulation period.
- Projection: British National Grid.
- SPI values are normal scores (unitless) with range [-5, 5].
- Access: data hosted on a THREDDS server; available via the DOI link.

## VI. Use of the data

- Terms and conditions apply; full terms accessible at the provided DOI.
- Citation required if the data are used:
  Tanguy, M., et al. (2015). Gridded Standardized Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for Great Britain [SPIgamma61-10]. NERC Environmental Information Data Centre.
- Acknowledgment of the DrIVER project and NERC funding (award NE/L010038/1).

## Acknowledgments

- Outcome of the DrIVER project; funded by the Natural Environment Research Council.
- Project linked to Belmont Forum initiatives.