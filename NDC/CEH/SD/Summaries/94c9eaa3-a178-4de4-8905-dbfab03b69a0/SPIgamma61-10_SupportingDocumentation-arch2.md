# Supporting Information

- I. Brief Description of the dataset
  - Contains 1km and 5km gridded Standardised Precipitation Index (SPI) data for Great Britain.
  - SPI is a drought index based on the probability of precipitation for specified accumulation periods (1, 3, 6, 12, 18, 24 months) calculated for each of the 12 calendar months.
  - Baseline period used to fit the gamma distribution: 1961-2010.
  - Coverage: 1961-2012.
  - Data format: NetCDF4, stored on a THREDDS server; available at the DOI provided.

- II. Motivation
  - Derived within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
  - SPI defines and monitors drought by assessing rarity at chosen timescales; can also identify anomalously wet periods.
  - Enables spatial analysis of drought, tracking its evolution over time, and identifying affected areas within an early warning and monitoring system.
  - Different accumulation periods provide different information:
    - 1-month SPI: short-term soil moisture and crop stress.
    - 3-month SPI: short- to medium-term moisture, seasonal context.
    - 6-month SPI: medium-term trends, potential links to streamflows and reservoir levels.
    - 12-month SPI: long-term precipitation patterns linked to water resources.
    - 18/24-month SPI: longer-term patterns, groundwater context.
  - Two spatial resolutions (1km and 5km) cater to local vs. regional analyses; 1km for fine-scale studies, 5km for quicker regional assessments.

- III.1 Data Sources
  - CEH-GEAR (CEH-Gridded Estimates of Areal Rainfall) used to derive gridded SPI (monthly rainfall grids).

- III.2 Method for deriving the SPI grids
  - SPI calculation follows McKee et al. (1993): transforms cumulative precipitation to a normal distribution with mean 0 and stdev 1.
  - For each location and accumulation period, 72 time series are created (6 durations × 12 months).
  - A gamma distribution is fitted to each time series using L-moments to estimate parameters (via a modified R SCI package to rely on L-moments).
  - SPI values are unitless “normal scores”; values are truncated at ±5.
  - Note: while gamma is widely used for Europe, recent work suggests other distributions (e.g., Pearson type 3, Tweedie) may better fit UK data; gamma remains in use for this dataset.
  - Overlapping data for accumulation periods >12 months introduce autocorrelation; SPIs for different months/periods should account for this in analyses.
  - Base distribution fitting uses 1961-2010; data cover 1961-2012 due to rainfall data density and focus on drought impacts; CEH-GEAR data span 1890-2012.

- IV. Format of the SPI dataset
  - NetCDF4 format adhering to CEH gridded dataset conventions.
  - Structure: two-dimensional GB grids with twelve monthly grids per year; one yearly file per accumulation period.
  - Projection: British National Grid.
  - SPI values: standard normal scores (mean 0, sd 1), unitless; range limited to -5 to +5.
  - Accessible via THREDDS server; DOI provided.

- V. Use of the data
  - Data access is governed by terms and conditions; citation required.
  - Citation: Tanguy et al. (2015) for Gridded Standardized Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for Great Britain [SPIgamma61-10].
  - Data available and usage terms at the provided DOI link.

- VI. Acknowledgments
  - Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
  - Funding: Natural Environment Research Council (award NE/L010038/1) under the Belmont Forum initiative.

- References
  - Key sources include McKee et al. (1993) on SPI, Hayes et al. (2011) Lincoln Declaration, Barker et al. (2015), Svensson et al. (2015), and CEH-GEAR-related literature.