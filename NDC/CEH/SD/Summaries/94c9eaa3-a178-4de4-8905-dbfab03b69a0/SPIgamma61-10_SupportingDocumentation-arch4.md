# Supporting Information

## I. Brief Description of the dataset
- 1 km and 5 km gridded Standardised Precipitation Index (SPI) data for Great Britain; SPI is a drought index based on precipitation probability for specified accumulation periods (McKee et al., 1993).
- SPI calculated for accumulation periods: 1, 3, 6, 12, 18, 24 months; for each of 12 calendar months.
- Standard period used to fit the gamma distribution: 1961–2010.
- Dataset coverage: 1961–2012.
- Format: NetCDF4; stored on a THREDDS server; available via doi link.

## II. Motivation
- Derived within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) to assess drought indices relative to impacts data in a monitoring and early warning system.
- SPI helps define/monitor drought and determine rarity of events at given time scales; also identifies anomalously wet periods.
- Enables spatial analysis of drought, study of its propagation, and identification of severely affected areas within EW&M systems.
- Different accumulation periods provide distinct insights (short-term to long-term moisture conditions).
- Two resolutions (1 km and 5 km) cater to local/small-area analyses and regional studies, respectively.

## III. Data Sources
- CEH-GEAR: CEH-Gridded Estimates of Areal Rainfall (monthly rainfall grids) used to derive gridded SPI.

### III.2 Method for deriving the SPI grids
- SPI computed per McKee et al. (1993) as the cumulative probability of precipitation, assigned to the month in which the accumulation period ends.
- For each location: SPI calculated for 1, 3, 6, 12, 18, 24 months across all 12 months (72 time series per location).
- Distribution fitted to each time series using the gamma distribution; parameters estimated with L-moments (instead of maximum likelihood) via a modified R package SCI.
- SPI transformed to a normal distribution with mean 0 and stdev 1 (normal scores); values truncated at ±5 due to uncertainty at extremes.
- Note: gamma distribution historically used in Europe; UK-specific tests (Shapiro–Wilk) suggest potential better distributions (e.g., Pearson Type 3, Tweedie) though gamma is retained here. Overlapping data for longer durations can introduce autocorrelation.
- Data period for distribution fitting: 1961–2010; actual data cover 1961–2012; justification: sparser pre-1961 rain-gauge network and focus on drought impacts relationships.

## IV. Format of the SPI dataset
- NetCDF4 format following CEH gridded dataset conventions.
- Two-dimensional grids for Great Britain; twelve monthly grids per year; one yearly file per accumulation period.
- Projection: British National Grid.
- SPI values are unitless normal scores with mean 0 and stdev 1; range limited to -5 to +5.
- Data hosted on a THREDDS server; available via doi link.

## V. Use of the data
- Terms and conditions of use apply; citation required when using the data:
  Tanguy, M., et al. (2015). Gridded Standardized Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for Great Britain [SPIgamma61-10]. NERC Environmental Information Data Centre. doi:10.5285/94c9eaa3-a178-4de4-8905-dbfab03b69a0

## VI. Acknowledgments
- Output of the DrIVER project; funded by the Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.

## References (selected)
- Barker et al. (2015); Svensson et al. (2015); Gudmundsson & Stagge (2014); Hayes et al. (2011); Keller et al. (2015); McKee et al. (1993); Stagge et al. (2015).