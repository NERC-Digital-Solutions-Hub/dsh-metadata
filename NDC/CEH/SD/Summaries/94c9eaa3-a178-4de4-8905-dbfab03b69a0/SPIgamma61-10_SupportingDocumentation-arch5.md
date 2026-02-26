# Supporting Information

- I. Brief Description of the dataset
  - 1km and 5km gridded Standardised Precipitation Index (SPI) data for Great Britain.
  - SPI is a drought index based on the probability of precipitation for a given accumulation period.
  - Accumulation periods: 1, 3, 6, 12, 18, 24 months; computed for each of the twelve calendar months.
  - Gamma distribution fitted on a standard period of 1961–2010.
  - Dataset covers 1961–2012.
  - Data format: NetCDF4; hosted on a THREDDS server; available at the provided DOI link.

- II. Motivation
  - Derived within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) to assess drought indices in relation to impacts data within a monitoring and early warning system.
  - SPI helps define and monitor drought, determine rarity of drought at various time scales, and identify anomalously wet periods.
  - SPI across multiple time scales enables analysis of short-, medium-, and long-term moisture trends and their relation to impacts (e.g., soil moisture, crop stress, streamflows, reservoir levels, groundwater).
  - Two resolutions (1km and 5km) address different scientific and stakeholder needs: 1km for local analyses; 5km for smaller file sizes and regional studies.

- III.1 Data Sources
  - CEH-GEAR: Gridded estimates of areal rainfall used to derive the SPI (monthly rainfall grids).

- III.2 Method for deriving the SPI grids
  - SPI calculation follows McKee et al. (1993): based on cumulative probability of precipitation; SPI for a given accumulation period ends in the corresponding month (e.g., 6-month SPI for July 1998 uses precipitation from Feb–Jul 1998).
  - For each location, SPI calculated for 1, 3, 6, 12, 18, 24 months across 12 calendar months, yielding 72 time series per grid cell.
  - A statistical distribution (gamma) fitted to each time series; parameters estimated with L-moments (instead of MLE) using a modified R SCI package.
  - SPI is transformed to a normal distribution with mean 0 and SD 1 (normal scores); SPI values truncated to the range -5 to +5.
  - Approximately 95% of SPIs fall within -2 to +2; about 68% within -1 to +1.
  - Note on distribution choice: gamma is widely used and accepted in drought research, but recent work suggests other distributions (e.g., Pearson type 3, Tweedie) may be more suitable for the UK in some cases; future versions may use different distributions if justified.
  - Autocorrelation caveats: for durations >12 months, overlapping data lead to shared data between consecutive values; SPIs for a given duration may be autocorrelated; concatenated monthly SPIs are also likely autocorrelated and should account for this in trend analyses.
  - Data period considerations: 1961–2010 used to fit the distribution; dataset covers 1961–2012. The 1961 start is due to sparser rainfall data prior to that date and limited impact data availability; focus is on drought indicators and impacts within the DrIVER project.

- IV. Format of the SPI dataset
  - NetCDF4 format, following CEH gridded dataset conventions.
  - Structure: two-dimensional grids over Great Britain, with twelve monthly grids per year; one yearly file per accumulation period.
  - Projection: British National Grid.
  - Data values: SPI normal scores (mean 0, SD 1), unitless, range -5 to +5.
  - Hosting: THREDDS server; accessible via the provided DOI.

- V. Use of the data
  - Terms and conditions apply; full terms available at the provided DOI.
  - Required citation: Tanguy, M. et al. (2015). Gridded Standardized Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for Great Britain [SPIgamma61-10]. NERC EIDC. doi:...
  - Acknowledgement of the DrIVER project and funding: Natural Environment Research Council (award NE/L010038/1).

- VI. Acknowledgments
  - Outcome of the DrIVER project; funded by NERC as part of Belmont Forum initiative.

- References (selected)
  - Barker et al. (2015); Svensson et al. (2015); Tanguy et al. (2014, 2015); McKee et al. (1993); Hayes et al. (2011); Stagge et al. (2015); Gudmundsson & Stagge (2014).