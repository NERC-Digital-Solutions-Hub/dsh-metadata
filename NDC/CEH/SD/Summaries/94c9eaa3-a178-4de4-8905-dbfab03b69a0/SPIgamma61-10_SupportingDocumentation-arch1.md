# Supporting Information

- I. Brief Description of the dataset
  - 1 km and 5 km gridded Standardised Precipitation Index (SPI) data for Great Britain, a drought index based on precipitation probability for a given accumulation period.
  - SPI calculated for accumulation periods: 1, 3, 6, 12, 18, 24 months; each period computed for all 12 calendar months.
  - Gamma distribution fitted to historical precipitation accumulations; standard fitting period 1961–2010.
  - Coverage spans 1961–2012; data stored in NetCDF4 format, on a THREDDS server, available at the provided DOI URL.
  
- II. Motivation
  - Derived within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) to assess drought indices in relation to impacts data for a monitoring and early warning system.
  - SPI enables assessment of drought rarity at different time scales and identification of anomalously wet periods.
  - Two spatial resolutions (1 km and 5 km) address different scientific and stakeholder needs: 1 km for local analyses, 5 km for regional studies and quicker manipulation.

- III.1 Data Sources
  - CEH-GEAR: CEH-Gridded Estimates of Areal Rainfall used as the rainfall input for deriving gridded SPI.

- III.2 Method for deriving the SPI grids
  - SPI computed as defined by McKee et al. (1993): for each location, 72 time series (6 durations × 12 months) are created.
  - For each time series, a gamma distribution is fitted using L-moments (instead of maximum likelihood) to estimate parameters; the R SCI package is modified for L-moments.
  - SPI values are transformed to a normal distribution with mean 0 and standard deviation 1 (unitless); values are truncated at ±5.
  - About 95% of SPIs fall within -2 to +2; ~68% within -1 to +1.
  - Note: recent work suggests alternative distributions (e.g., Pearson type 3, Tweedie) may be more adequate for the UK, but gamma remains widely used; future versions may adopt other distributions if justified.
  - For accumulation periods >12 months, overlapping data lead to autocorrelation in the underlying time series; concatenated SPIs across months can be autocorrelated; interpret accordingly (e.g., for trend analysis, account for serial correlation).
  - Start year 1961 chosen because prior to then rainfall data were too sparse and impact data were limited; focus aligned with DrIVER objectives.

- IV. Format of the SPI dataset
  - NetCDF4 format following CEH gridded dataset conventions.
  - Two-dimensional grids covering Great Britain; 12 monthly grids per year; one yearly file per accumulation period.
  - Projected on the British National Grid.
  - SPI values are normal scores (mean 0, sd 1), unitless; range limited to [-5, 5].
  - Dataset hosted on a THREDDS server; access via the stated DOI URL.

- V. Use of the data
  - Terms and conditions apply; data users must cite: Tanguy et al. (2015) “Gridded Standardized Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for Great Britain [SPIgamma61-10].”
  - Full terms and conditions accessible at the DOI URL.

- VI. Acknowledgments
  - Outcome of the DrIVER project; funded by the Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.

- References (selected)
  - Barker et al. (2015); Gudmundsson & Stagge (2014); Hayes et al. (2011); Keller et al. (2015); McKee et al. (1993); Stagge et al. (2015); Svensson et al. (2015); Tanguy et al. (2014, 2015).