# Historic Gridded Standardised Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for the United Kingdom (1862-2015) - version 3

## I. What this dataset is
- A 5 km gridded Standardised Precipitation Index (SPI) dataset for the United Kingdom, a drought index based on the probability of precipitation for specified accumulation periods.
- Calculated for accumulation periods of 1, 3, 6, 9, 12, 18, and 24 months, with a separate time series for each of the 12 calendar months.
- SPI values are transformed to a normal distribution (mean 0, standard deviation 1) and stored as NetCDF4 files on the British National Grid.
- Range: -5 to +5; no units.

## II. Motivation and intended use
- Originates from the Historic droughts project to develop cross-disciplinary understanding of past UK droughts and to improve tools for drought management and planning.
- SPI enables assessment of drought rarity at multiple time scales and identification of anomalously wet periods.
- Different accumulation periods provide insights from short-term soil moisture to long-term groundwater, aiding spatial analysis and tracking drought propagation over time.

## III. Data sources and SPI derivation method
- Data sources
  - Met Office 5 km monthly rainfall gridded data, incorporating:
    - UKCP09 data (1910-1959 and 2001-2011)
    - Monthly rainfall grids derived from Met Office daily grids (1960-2000)
    - Unpublished Met Office updates (2012-2015)
    - Historic Droughts project rescued data (1862-1909)
- Method for deriving SPI
  - For each grid cell, SPI time series are created for each duration (7 durations) and each month (12 months) → 84 time series per cell.
  - For each time series, a gamma distribution is fitted to the historical precipitation accumulations using L-moments (via a modified R SCI package) to estimate parameters.
  - SPI is computed by transforming the gamma-fitted values to normal scores (mean 0, sd 1).
  - Extreme values are truncated at +/- 5.
  - Note: While gamma is common for SPI, some studies indicate other distributions may be more appropriate for the UK; the gamma-based approach remains in use here, with potential future updates.
- Temporal and data caveats
  - For durations longer than 12 months, the underlying annual series include overlapping data, creating potential autocorrelation.
  - SPIs for different months can also be autocorrelated when concatenated for trend analyses.
  - Standard period used to fit distributions is 1961-2010; dataset covers 1862-2015.
- Version differences
  - Version 3 differs from the earlier dataset by using Met Office 5 km rainfall grids rather than CEH-GEAR data.
  - Version 3 also updates the 1960-2000 rainfall data and adds the 9-month accumulation period.
  - Version 2 is superseded by version 3 (SPI18 issue due to a transfer error).

## IV. Dataset format and structure
- Format: NetCDF4
- Structure: two-dimensional UK grids with twelve monthly grids per year; one yearly file per accumulation period.
- Projection: British National Grid.
- Content: SPI values (normal scores, unitless) for each grid cell, for each month and duration.
- Data range: -5 to +5 (values outside this range are clipped).

## V. Temporal coverage and data quality considerations
- Temporal coverage: 1862–2015
- Key quality notes
  - Serial autocorrelation concerns for long-duration SPIs due to overlapping data periods.
  - Some issues identified with 1960-2000 monthly rainfall grids; addressed in data updates.
  - Although gamma distribution is widely used for SPI, future versions may explore alternatives (e.g., Pearson Type III, Tweedie) if justified by method validation.

## VI. Version history, limitations and governance
- Version 3 supersedes Version 2; differences include updated rainfall input data and the addition of a 9-month accumulation.
- Relationship to other datasets: differs from SPIgamma61-10 due to the underlying rainfall dataset (Met Office historic rainfall grids vs CEH-GEAR).
- Governance implications: designed to support monitoring and decision-making for drought risk and management, with transparent methodology and data provenance.

## VII. Acknowledgments
- Joint outcomes from the DrIVER, Historic Droughts, and IMPETUS projects, funded by NERC and associated initiatives.