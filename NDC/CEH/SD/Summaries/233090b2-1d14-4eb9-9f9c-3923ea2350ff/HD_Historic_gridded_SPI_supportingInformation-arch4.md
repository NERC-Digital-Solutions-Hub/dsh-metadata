# Historic Droughts Inventory of drought references for Historic Gridded Standardised Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for the United Kingdom (1862-2015) - version 4

- Overview
  - 5km gridded Standardised Precipitation Index (SPI) data for the United Kingdom, a drought index based on precipitation probability for various accumulation periods (1, 3, 6, 9, 12, 18, 24 months) across all 12 calendar months.
  - Standard period for distribution fitting: 1961-2010; spatial extent covers 1862-2015.
  - Data stored in NetCDF4 format on the British National Grid; 84 time-series per grid cell (7 durations x 12 months) each year file per accumulation period.

- Data provenance and context
  - Produced under two projects: DrIVER (Drought Impacts: Vulnerability thresholds in monitoring and Earlywarning Research) and Historic Droughts (part of the NERC Drought and Water Scarcity Programme).
  - Data sources include Met Office 5km monthly rainfall grids, Met Office daily grids (1960-2000), UKCP09-derived data (1910-1959, 2001-2011), and rescued data (1862-1909); updated 2012-2015.
  - Historic Droughts Inventory accompanies the SPI dataset as a knowledge base of past drought characteristics, drivers, impacts, and responses to support cross-sector understanding and planning.

- Methodology
  - SPI computed as the cumulative precipitation probability for each accumulation period; for each location, SPI is calculated for all 7 durations across 12 months (84 time series per grid cell).
  - Gamma distribution fitted to each time series using L-moments to estimate parameters (via a modified R SCI package); data transformed to normal scores (mean 0, stdev 1).
  - SPI values truncated to ±5 due to estimation uncertainty; typically 95% of values fall within -2 to 2.
  - Note: UK-specific research indicates the gamma distribution may not always be optimal (Shapiro-Wilk tests). Alternatives like Pearson type 3 or Tweedie may be more suitable in some cases; current dataset uses gamma as widely accepted in drought literature.
  - Complexities: for >12 month periods, data involve overlapping sums, introducing autocorrelation; serial correlation cautions apply for trend analyses.

- Data format and structure
  - NetCDF4 format following CEH conventions; two-dimensional grids with 12 monthly grids per year.
  - One yearly file per accumulation period; data projected on the British National Grid.
  - SPI values are unitless normal scores (mean 0, stdev 1) and are capped at -5 to +5.

- Data usage, accessibility, and governance
  - Intended to support spatial analysis of drought propagation, identification of severely affected areas, and longer-term drought and water resource planning.
  - Aims to enable cross-disciplinary understanding and better tools for drought monitoring and decision-making within policy, water supply, agriculture, and industry sectors.
  - Management considerations include data provenance, metadata, updates, and discoverability to ensure use by a wide data community.

- Data quality, limitations, and caveats
  - Localised issues identified in underlying Met Office 1960-2000 monthly rainfall data necessitated new monthly grids derived from daily data (1960-2000) and 2012-2015 updates.
  - Serial correlation due to overlapping accumulation periods; independence assumptions for frequency analysis are violated for longer durations.
  - While gamma distribution is used here, alternative distributions may be explored in future versions if justified.

- Project motivation and acknowledgement
  - SPI enables evaluation of drought rarity across timescales and supports monitoring of short- to long-term moisture conditions.
  - Dataset is a collaborative output from DrIVER and Historic Droughts projects, with contributors across multiple UK institutions; in-kind and financial support acknowledged.