# Gridded Standardized Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for Great Britain [SPIgamma61-10]

## I. Brief Description of the dataset
- 1 km and 5 km gridded SPI data for Great Britain (drought index based on precipitation probability for given accumulation period).
- Accumulation periods: 1, 3, 6, 12, 18, 24 months; each period calculated for all 12 calendar months.
- Fitting period for the gamma distribution: 1961–2010; dataset covers 1961–2012.
- Data stored as NetCDF4 on a THREDDS server; accessible via DOI: 10.5285/94c9eaa3-a178-4de4-8905-dbfab03b69a0.

## II. Motivation
- Produced under the DrIVER project to assess drought indices relative to impacts data within a monitoring and early warning system.
- SPI provides a stateless, unitless measure of drought/wetness; useful for spatial analysis, tracking drought propagation, and identifying severely affected areas.
- Different time scales (1–24 months) capture short- to long-term moisture dynamics; supports both local and regional drought assessments.
- Two spatial resolutions (1 km for local detail; 5 km for quicker handling) to meet diverse scientific and stakeholder needs.

## III. Data Sources
- CEH-GEAR: Gridded estimates of areal rainfall (monthly grids) used as the rainfall input for SPI derivation.

## IV. Method for deriving the SPI grids
- SPI calculation follows McKee et al. (1993): based on cumulative probability of precipitation for each accumulation period ending in a given month.
- For each location, derive 72 time series: 6 durations × 12 months.
- Fit a gamma distribution to each time series using L-moments (preferred when MLE fails); parameter estimation via modified R SCI package.
- Transform to a standard normal distribution (mean 0, stdev 1); SPI values are “normal scores.”
- Truncate extreme values at +/-5.
- Note on limitations:
  - Gamma distribution may not always be the best fit (other distributions may be more suitable for the UK); current dataset uses gamma but future versions may use alternatives.
  - Overlapping data across long accumulation periods induces autocorrelation; independence assumptions for standard frequency analyses are not met.
  - 1961–2010 standard period chosen due to sparse prior raingauge coverage; dataset extends to 2012 for DrIVER context.

## V. Format of the SPI dataset
- NetCDF4 format conforming to CEH gridded dataset conventions.
- 2D GB grids with 12 monthly grids per year; one file per accumulation period.
- Projection: British National Grid.
- Data values: normal scores with no units; range limited to -5 to +5.
- Hosted on a THREDDS server; access via DOI: 10.5285/94c9eaa3-a178-4de4-8905-dbfab03b69a0.

## VI. Use of the data
- Terms and conditions apply; citation required: Tanguy et al. (2015) SPIgamma61-10, NERC Environmental Information Data Centre.
- Dataset supports spatial drought analysis, trend assessment, and integration with drought impact data within monitoring and early warning systems.

## Acknowledgments
- Funded by the Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative, under the DrIVER project.