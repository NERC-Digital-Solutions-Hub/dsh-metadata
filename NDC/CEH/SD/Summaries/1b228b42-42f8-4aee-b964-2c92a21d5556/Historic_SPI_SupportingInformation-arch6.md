# 5km gridded Standardised Precipitation Index (SPI) data for the United Kingdom

- Dataset provides 5 km gridded SPI data across the UK, a drought index based on precipitation probability for multiple accumulation periods, stored as NetCDF4 and projected on the British National Grid.
- SPI is calculated for accumulation periods of 1, 3, 6, 9, 12, 18, and 24 months, with separate monthly values for each calendar month, resulting in 84 time series per grid cell (7 durations × 12 months).
- SPI values are transformed to normal scores with mean 0 and standard deviation 1, and are truncated to the range [-5, 5], with no units.

I. Brief Description of the dataset

- Covers 1862–2015 and uses a standard fitting period of 1961–2010.
- Data format: NetCDF4; two-dimensional UK-wide grids; one yearly file per accumulation period; 12 monthly grids per year.
- The underlying data are monthly precipitation totals derived for each accumulation period ending in a given month.

II. Motivation

- Created within the Historic droughts project to understand past UK droughts and support future drought management.
- SPI enables assessment of drought rarity at multiple time scales and identification of unusually wet periods.
- Facilitates spatial analysis of drought propagation, hotspot identification, and association with streamflows, reservoirs, and soil moisture.

III. Data Sources

- Met Office 5 km monthly rainfall gridded data, combining:
  - UKCP09 data (1910–1959 and 2001–2011)
  - Monthly rainfall grids derived from Met Office daily grids (1960–2000)
  - Unpublished Met Office updates (2012–2015)
  - Rescued data for 1862–1909

III.2 Method for deriving the SPI grids

- SPI is computed as the cumulative probability of precipitation for each accumulation period, with final values corresponding to the end month of the accumulation period.
- For each location, SPI is calculated for 1, 3, 6, 9, 12, 18, 24 month accumulations across all 12 calendar months.
- A gamma distribution is fitted to each time series using L-moments (via a modified R SCI package) to obtain SPI values.
- Transformation to a normal distribution yields the final SPI “normal scores.”
- Extrema are truncated at ±5; most SPIs lie within ±2 (95% of data) or ±1 (68%).
- Note on distribution choice: while gamma is widely used and recommended for Europe, recent work suggests other distributions (e.g., Pearson type 3, Tweedie) may be more suitable for the UK in some cases.
- Accumulation period data for durations >12 months are based on overlapping yearly precipitation series, introducing potential autocorrelation; SPIs for a given duration reflect the relative severity within that duration but serial correlation should be accounted for in trend analyses.

IV. Format of the SPI dataset

- Stored in NetCDF4 format, following CEH gridded dataset conventions.
- Structure: UK-wide two-dimensional grids with twelve monthly grids per year; one yearly file per accumulation period.
- Projection: British National Grid.
- Data values: SPI normal scores with no units; range limited to [-5, 5].

V. Acknowledgments

- Joint outcomes from DrIVER (NERC grant NE/L010038/1), Historic Droughts (NE/L01016X/1), and IMPETUS (NE/L010267/1).

Notes for data users

- The dataset is designed to support spatial drought analysis across multiple time scales and long historical coverage, enabling cross-temporal and cross-spatial drought assessment and monitoring.
- Be mindful of potential autocorrelation in SPI time series for longer accumulation periods due to overlapping data; adjust analyses accordingly.
- Consider exploring alternative distributions for SPI in future work, given ongoing methodological evaluations of distribution suitability for UK precipitation.