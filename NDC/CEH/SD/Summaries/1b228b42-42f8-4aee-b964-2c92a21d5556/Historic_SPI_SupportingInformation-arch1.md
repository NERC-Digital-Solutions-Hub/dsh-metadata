# Supporting Information

## I. Brief Description of the dataset
- Five-kilometre gridded Standardised Precipitation Index (SPI) data for the United Kingdom, a drought index based on the probability of precipitation for various accumulation periods.
- SPI calculated for accumulation periods: 1, 3, 6, 9, 12, 18, 24 months; each period computed for all twelve calendar months.
- Standard gamma distribution with a fitting period of 1961-2010; dataset covers 1862-2015; stored in NetCDF4 format.
- SPI values are normalized (mean 0, standard deviation 1), unitless, truncated to range [-5, 5].

- Version notes:
  - This dataset differs from the previously published SPIgamma61-10 by using Met Office 5km rainfall grids instead of CEH-GEAR; underlying rainfall data updated via historic rainfall/temperature grids.
  - In version 2, the 1960-2000 monthly rainfall data were revised due to local issues; new monthly grids derived from daily rainfall grids; a 9-month accumulation was added.

## II. Motivation
- Generated under the Historic droughts project to develop a cross-disciplinary understanding of past UK droughts and improve tools for future drought management.
- SPI helps define and monitor drought by indicating rarity for any location and time scale, and can identify anomalously wet periods.
- Different accumulation periods provide insights into short-term (1-3 months), mid-term (6-9 months), and long-term (12+ months) moisture patterns, relating to soil moisture, crop stress, streamflows, reservoir levels, and groundwater signals.

## III. Data Sources
- Met Office 5km monthly rainfall gridded data, combining:
  - UKCP09 data (1910-1959 and 2001-2011)
  - Monthly rainfall grids derived from Met Office daily grids (1960-2000)
  - Unpublished updates (2012-2015)
  - Rescued data from Historic Droughts project (1862-1909)

## III.2 Method for deriving the SPI grids
- SPI calculation follows McKee et al. (1993): probability-based, assigned to the month ending the accumulation period.
- For each grid cell, 84 time series are created (7 durations × 12 months); gamma distribution fitted via L-moments (instead of MLE) using modified R SCI package.
- Transformation to a normal distribution yields the SPI (normal scores, mean 0, stdev 1).
- Extreme SPI values are truncated at ±5.
- Notes on distribution choice: gamma widely used, but recent work suggests Pearson III or Tweedie may be more adequate for the UK; gamma remains standard in drought research for now.
- Autocorrelation considerations:
  - For durations >12 months, overlapping data cause serial correlation in the underlying time series.
  - Monthly SPIs concatenated across months are also likely autocorrelated; caution advised for trend analyses.
- Standard fitting period: 1961-2010.

## IV. Format of the SPI dataset
- Stored in NetCDF4 format, CEH gridded conventions.
- UK-wide two-dimensional grids with twelve monthly grids per year; one file per accumulation period.
- Projection: British National Grid.
- SPI values are unitless normal scores; no units; range limited to [-5, 5].

## V. Acknowledgments
- Project outcomes from DrIVER (NERC NE/L010038/1), Historic Droughts (NE/L01016X/1), and IMPETUS (NE/L010267/1).