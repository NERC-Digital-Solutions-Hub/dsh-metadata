# Standardised Precipitation Index time series for Integrated Hydrological Units Hydrometric Areas (1862-2015)

- Purpose and scope
  - Provides SPI time series for IHU hydrometric areas to support drought monitoring and spatial analysis in the CEH droughts portal.
  - Covers 1862–2015, with a standard distribution fitting period of 1961–2010.
  - SPI computed for six accumulation periods (1, 3, 6, 12, 18, 24 months) across all twelve calendar months (72 time series per location).

- Data content and format
  - Stored as CSV with 9 columns: RID, POLYGONID (IHU hydrometric area ID used for shapefile joins), THEDATETIME (date), and six SPI aggregations (one per chosen accumulation period).
  - SPI values are standard normal scores (mean 0, stdev 1), unitless, truncated to -5 to +5. -9999 denotes No Data.
  - Each location (grid cell) yields multiple time series corresponding to the different accumulation periods and end-months.

- Data sources and inputs
  - IHU hydrometric areas (Kral et al., 2015) as the spatial framework.
  - Met Office 5 km monthly rainfall grids (combining UKCP09 data, unpublished 2012–2015 updates, and historic droughts data for 1862–1909).

- Methodology
  - SPI calculation follows McKee et al. (1993): distribution of precipitation totals is modeled for each accumulation period and month.
  - Gamma distribution fitted using L-moments (via a modified R SCI package) to estimate parameters; data transformed to a standard normal distribution.
  - End-month assignment: SPI for a given accumulation period ends in the month in which that period completes (e.g., 6-month SPI for July 1998 uses Feb–Jul 1998 data).
  - Note: overlapping data for longer accumulation periods leads to autocorrelation; independence assumptions for frequency analysis are not met.

- Key considerations for GIS users
  - Join the SPI_IHU_HA data to IHU shapefiles using POLYGONID.
  - Visualize multiple SPI durations to assess short- to long-term drought/wetness patterns.
  - Be cautious with trend analyses due to serial autocorrelation from overlapping periods.
  - Consider alternative distributions (e.g., Pearson Type III, Tweedie) for future updates, though gamma remains the current standard.

- Limitations and caveats
  - Serial correlation arising from overlapping time series, especially for longer durations.
  - The gamma distribution, while widely used, may not always be the best fit for UK data; newer distributions could be explored.
  - Extreme SPI values are truncated at ±5; extreme events are still represented within this bound.

- Acknowledgments and references
  - Supported by DrIVER (NE/L010038/1), Historic Droughts (NE/L01016X/1), and IMPETUS (NE/L010267/1) projects.
  - References include McKee et al. (1993), Barker et al. (2015), Svensson et al. (2015), Gudmundsson & Stagge (2014), and related CEH-GEAR and IHU sources.