# Supporting Information

- Dataset purpose and content
  - Time series of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) groups (SPI_IHU_groups).
  - SPI calculated for accumulation periods: 1, 3, 6, 12, 18, 24 months, each for all 12 calendar months (72 series per location).
  - Time period: 1862 to 2015 (standard reference period for fitting: 1961–2010).
  - Data stored in CSV format; SPI values are normal scores (mean 0, SD 1), unitless, typically within -2 to +2; values capped at +/-5; -9999 indicates No Data.

- Motivation and use case
  - Developed to support incorporation into CEH droughts portal.
  - Aggregates SPI over IHU groups to study drought/wetness over defined areas.
  - SPI is a widely used drought index recommended for meteorological drought monitoring; different time scales provide short- to long-term moisture context (e.g., 1-month relates to short-term soil moisture; 12-month relates to long-term precipitation patterns and reservoir/streamflow context).

- Data sources
  - IHU groups (Kral et al. 2015) as the hydrological spatial reference units.
  - Met Office 5 km monthly rainfall grids (UKCP09 data 1910–2011, additional Met Office updates 2012–2015, historic data 1862–1909).

- Methodology (how SPI is derived)
  - SPI calculated following McKee et al. (1993): based on cumulative precipitation for each accumulation period ending in a given month.
  - For each location and each accumulation period, 12 monthly time series are created (72 series total per location).
  - Gamma distribution fitted to the historic precipitation series using L-moments (instead of maximum likelihood) to estimate parameters (via a modified R package SCI).
  - Transformation to a standard normal distribution to obtain SPI (mean 0, SD 1).
  - Truncation at -5 and +5 to handle tails.
  - Acknowledgement: gamma distribution is widely used and recommended in Europe, but some studies suggest alternative distributions (e.g., Pearson type 3, Tweedie) may be more suitable for the UK; future versions may explore other distributions.

- Statistical notes and caveats
  - For accumulation periods > 12 months, overlapping data create autocorrelation in the underlying precipitation series.
  - SPI time series for a given duration are not strictly independent; concatenated monthly SPIs are also likely autocorrelated.
  - These autocorrelation properties should be accounted for in trend analyses or frequency assessments.

- Data format and structure
  - SPI_IHU_groups dataset stored as CSV with 9 columns:
    - RID: row identifier
    - POLYGONID: IHU group ID (join key to shapefiles)
    - THEDATETIME: date/time
    - Columns 4–9: SPI values for the six accumulation periods across twelve months (the six durations x twelve months)
  - SPI values are normal scores (mean 0, SD 1), no units, range limited to -5 to +5, with -9999 as No Data.

- GIS usage and integration
  - Designed for integration with IHU shapefiles using POLYGONID to map spatial drought/wetness patterns.
  - Useful for creating map-based visualisations and dashboards (e.g., drought portals) and for spatial analysis across UK hydrological units.

- Acknowledgments
  - Joint outcome from projects DrIVER, Historic Droughts, and IMPETUS (funding details provided in the document).

- References (contextual)
  - Key methodological and data sources include McKee et al. (1993), Stagge et al. (2015), Svensson et al. (2015, 2016), Barker et al. (2015), Gudmundsson & Stagge (2014), Hayes et al. (2011), and related CEH and Met Office datasets.