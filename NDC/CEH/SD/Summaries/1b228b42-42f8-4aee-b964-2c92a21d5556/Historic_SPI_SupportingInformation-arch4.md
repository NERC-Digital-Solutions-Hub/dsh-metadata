# Supporting Information

- This document provides detailed context and technical specifics for a 5 km gridded Standardised Precipitation Index (SPI) dataset for the United Kingdom, produced under the Historic droughts project to support cross-disciplinary understanding and drought management.

## Purpose and Context
- Aims to develop tools for analyzing historic UK droughts and improving future drought management.
- SPI is used to define and monitor meteorological drought and to identify anomalously wet periods.
- Enables spatial analysis of drought propagation, with multiple accumulation periods to capture short- to long-term moisture trends.

## Dataset Overview
- 5 km gridded SPI data for the UK, stored in NetCDF4 format on the British National Grid.
- Accumulation periods: 1, 3, 6, 9, 12, 18, 24 months; each period has 12 monthly grids per year.
- Temporal coverage: 1862 to 2015.
- Each grid cell yields 84 time series (7 durations × 12 months).
- SPI values are normalized (mean 0, std dev 1), unitless, and capped between -5 and +5.

## Data Sources
- Met Office 5 km monthly rainfall grids, combining:
  - UKCP09 data (1910-1959 and 2001-2011)
  - Monthly rainfall from Met Office daily grids (1960-2000)
  - Unpublished updates (2012-2015)
  - Historic Droughts project data (1862-1909)

## Calculation Method
- SPI calculation follows McKee et al. (1993): uses the probability of precipitation for a given accumulation period ending in a specific month.
- For each location, SPI is computed for 7 durations and 12 calendar months (84 time series).
- Gamma distribution fitted to each time series using L-moments (via a modified R SCI package) to estimate parameters.
- Transformation to normal scores (mean 0, stdev 1); truncation: |SPI| > 5 set to 5.
- Notes on distribution choice:
  - Gamma distribution widely used and accepted in Europe, though recent work suggests alternatives (e.g., Pearson Type III, Tweedie) may fit UK data better in some cases.
  - Future versions may explore other distributions if justified.
- Serial correlation considerations:
  - For durations > 12 months, data are overlapping, creating potential autocorrelation.
  - SPIs for successive months may also be autocorrelated if concatenated; users should account for this in trend analyses.

## Version History and Notes
- Note 1: Difference from earlier SPIgamma61-10 dataset is the underlying rainfall data (Met Office grids instead of CEH-GEAR); underpinning data updated via Historic Droughts digitisation.
- Note 2: In version 2, monthly rainfall data for 1960-2000 were re-derived from daily grids due to localised issues; a 9-month accumulation period was added.

## Data Format and Access
- Storage: NetCDF4 format, CEH grid conventions.
- Structure: Two-dimensional UK grids with 12 monthly grids per year; one yearly file per accumulation period.
- Projection: British National Grid.
- Data characteristics: Normal scores with no units; range limited to -5 to +5.

## Data Quality, Limitations, and Metadata
- Acknowledges potential data quality issues in historical rainfall grids and accumulation overlaps.
- Highlights the need to consider data provenance and updates when using the dataset.
- Metadata and discoverability are important for governance and re-use across organisations.

## Governance, Metadata, and Updates
- Acknowledgments: Collaboration across multiple projects (DrIVER, Historic Droughts, IMPETUS) and funding bodies (NERC).
- Emphasizes cross-project collaboration and potential future enhancements (e.g., alternate distributions) to improve data quality and utility.

## Use Cases and Applications
- Spatial drought mapping and analysis across the UK.
- Assessment of drought severity and timing at multiple time scales (short- to long-term).
- Support for climate and water resource planning, risk assessment, and sectoral policy work.

## References
- Barker et al. (2015); Gudmundsson & Stagge (2014); Hayes et al. (2011); Keller et al. (2015); McKee et al. (1993); National Drought Mitigation Center (2015); Stagge et al. (2015); Svensson et al. (2017); Tanguy et al. (2015); Tanguy et al. (2014).