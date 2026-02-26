# Historic Gridded Standardised Precipitation Index for the United Kingdom 1862-2015 (generated using gamma distribution with standard period 1961-2010)

## I. Brief Description of the dataset
- 5 km gridded Standardised Precipitation Index (SPI) data for the United Kingdom, covering 1862–2015.
- SPI is a drought index based on the probability of precipitation for specified accumulation periods: 1, 3, 6, 12, 18, and 24 months.
- For each accumulation period, SPI is calculated for each of the twelve calendar months (72 time series per grid cell).
- The standard period used to fit the gamma distribution is 1961–2010.
- SPI values are transformed to normal scores (mean = 0, standard deviation = 1) with no units; values are truncated at ±5.
- Data format: NetCDF4, British National Grid projection; each accumulation period has a separate yearly file containing 12 monthly grids.

## II. Motivation
- Produced within the Historic droughts project to understand past UK drought episodes and improve future drought management tools.
- SPI supports assessing the rarity of drought at chosen time scales and identifying anomalously wet periods.
- Enables spatial analysis of drought propagation over time and identification of severely affected areas.
- Different accumulation periods provide insights from short-term soil moisture and crop stress to long-term patterns related to streamflow, reservoirs, and groundwater.
- SPI is widely used and endorsed as a primary meteorological drought tool by the WMO.

## III. Data Sources and Method

### III.1 Data sources
- Met Office 5 km monthly rainfall gridded data.
- Composition includes UKCP09 data (1910–2011), unpublished Met Office updates (2012–2015), and rescued data for 1862–1909.

### III.2 Method for deriving the SPI grids
- SPI calculated from the cumulative precipitation totals for each accumulation period, ending in a given month (e.g., 6-month SPI for July 1998 covers Feb–Jul 1998).
- For each grid cell, 72 time series are produced (6 durations × 12 months).
- A gamma distribution is fitted to each time series using L-moments (to avoid ML failures in some cases).
- The R package SCI is used (modified to apply L-moments).
- Data are transformed to a standard normal distribution (mean 0, sd 1).
- Extreme SPI values are truncated at ±5.
- Note: gamma distribution, while traditional, may not always be the best fit for UK data; alternatives (e.g., Pearson type 3, Tweedie) exist and may be explored in the future.
- Accumulation periods > 12 months use overlapping annual data, introducing potential autocorrelation; SPIs for each calendar month are still valid for relative comparisons within the same duration, but trend analyses should account for serial correlation.

## IV. Format of the SPI dataset
- Stored in NetCDF4, following CEH gridded dataset conventions.
- Structure: two-dimensional UK grids with twelve monthly grids per year; one yearly file per accumulation period.
- Projection: British National Grid.
- SPI values are normal scores with no units, range typically within -5 to +5.

## V. Acknowledgments
- Joint outcomes from DrIVER (NERC NE/L010038/1), Historic Droughts (NE/L01016X/1), and IMPETUS (NE/L010267/1).

## References (selected)
- Barker et al., 2015; Gudmundsson & Stagge, 2014; Hayes et al., 2011; Keller et al., 2015; McKee et al., 1993; Stagge et al., 2015; Svensson et al., 2017.