# Historic Droughts Inventory of drought references for Historic Standardised Precipitation Index time series for IHU Groups (1862-2015) - version 2

- Overview
  - Time series of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) groups, covering 1862–2015.
  - SPI calculated for accumulation periods of 1, 3, 6, 9, 12, 18, and 24 months, for each of 12 calendar months.
  - Standard fitting period: 1961–2010; SPI values are unitless “normal scores” (mean 0, SD 1).
  - Data stored in CSV format; version 2 updates the underlying rainfall data and a new accumulation period.

- What the dataset contains
  - 84 time series per location (7 durations × 12 months) for each IHU group.
  - SPI values truncated to the range -5 to +5; -9999 indicates No Data.
  - Columns include:
    - RID (row identifier)
    - POLYGONID (IHU Group ID)
    - THEDATETIME (date/time)
    - SPI values for the 7 durations (monthly aggregations)

- Context and projects
  - Produces drought indicators as part of two projects:
    - DrIVER (Drought Impacts: Vulnerability thresholds in monitoring and Earlywarning Research)
    - Historic Droughts (UK drought and water scarcity research, 2014–2018)
  - Aims to support drought research nationally and internationally and to enable better drought monitoring and decision-making.

- Methodology
  - SPI definition follows McKee et al. (1993): based on the cumulative probability of precipitation for each location and accumulation period.
  - For each location, SPI computed for 1, 3, 6, 9, 12, 18, 24 months, for each calendar month (84 time series per cell).
  - Gamma distribution fitted to each time series; parameters estimated with L-moments (instead of MLE) using a modified R SCI package.
  - Transformation to a standard normal distribution (mean=0, SD=1) to obtain SPI; truncation at +/-5 due to uncertainty at extremes.
  - Note on limitations: gamma distribution commonly used but may not always be optimal for UK data; other distributions (e.g., Pearson type 3, Tweedie) could be explored in the future.
  - Serial correlation considerations: overlapping data for longer durations induce autocorrelation; care needed for trend analyses.

- Data sources
  - IHU groups (Kral et al., 2015) as the spatial framework.
  - Met Office 5 km monthly rainfall grids (1959–2011, plus additional updates):
    - UKCP09 datasets for 1910–1959 and 2001–2011
    - Met Office daily grids (1960–2000) and unpublished/rescued data (1862–1909)
  - The combination provides gridded rainfall data used to drive SPI calculations.

- Format and data products
  - CSV dataset with 10 columns: RID, POLYGONID, THEDATETIME, and seven SPI values corresponding to the accumulation periods.
  - SPI values are unitless, standard scores; required across the 7 durations and 12 months.

- Motivation and usage
  - Intended for incorporation into the CEH droughts portal.
  - Aggregating SPI over IHU groups enables drought analysis for specific areas of interest.
  - SPI serves as a primary drought monitoring tool, with interpretations linked to short-, medium-, and long-term moisture conditions.

- Acknowledgements and references
  - Joint outputs from DrIVER, Historic Droughts, and IMPETUS projects.
  - References include foundational SPI work (McKee et al., 1993), along with methodological and data source citations (Kral et al., 2015; Barker et al., 2015; Svensson et al., 2015; etc.).

- Inventory and broader context
  - Historic Droughts Inventory comprises:
    - Hydro-meteorological timelines of rainfall, river flows, and groundwater (consistent drought indicators extending back to the 19th century)
    - References to past droughts from newspapers, legislation, agricultural media, and oral histories
  - Designed as a common reference for policymakers, water utilities, agriculture, and industry to support transparent planning and cross-sector understanding.

- Data quality notes and limitations
  - Version 2 replaces certain underlying rainfall sources (Met Office grids) to improve historic coverage.
  - 1960–2000 monthly rainfall grids were recalculated from daily grids due to identified issues.
  - Accumulation periods beyond 12 months introduce overlapping data and potential autocorrelation; users should account for this in analyses.