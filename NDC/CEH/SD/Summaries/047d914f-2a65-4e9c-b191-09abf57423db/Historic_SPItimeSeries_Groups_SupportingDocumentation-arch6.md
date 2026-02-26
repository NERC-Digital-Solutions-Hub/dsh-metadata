# Supporting Information

- This document describes the SPI time series dataset for Integrated Hydrological Units (IHU) groups, including its motivation, data sources, calculation methods, data format, and acknowledgments.

## I. Brief Description of the dataset
- Time series of Standardised Precipitation Index (SPI) for IHU groups.
- SPI is a drought index based on the probability of precipitation for a given accumulation period (McKee et al., 1993).
- Accumulation periods: 1, 3, 6, 12, 18, 24 months; calculated for each of the twelve calendar months.
- Standard distribution fitted: gamma distribution (1961-2010 as the standard period).
- Coverage: 1862 to 2015 (data derived back to 1862 via historic data digitisation).
- Storage format: CSV.

## II. Motivation
- Designed for incorporation into the CEH droughts portal; allows analysis of drought over specific IHU areas by aggregating SPI.
- SPI is widely used to monitor meteorological drought and detect anomalously wet periods.
- Different SPI timescales provide varying insights:
  - 1-month: short-term moisture and crop stress.
  - 3-month: short- to mid-term moisture and seasonal precipitation.
  - 6-month: medium-term trends, potential link to streamflows and reservoirs.
  - 12-month: long-term precipitation patterns related to streamflows and reservoirs.
  - 18/24-month: longer-term precipitation patterns and groundwater implications.

## III. Data Sources
- IHU groups (Kral et al. 2015) as UK hydrological reference units.
- Met Office 5km monthly rainfall gridded data, combining:
  - UKCP09 data (1910-2011)
  - Unpublished Met Office updates (2012-2015)
  - Historic Droughts project data (1862-1909)

## III.2 Method for deriving the SPI grids
- SPI calculation follows McKee et al. (1993): based on cumulative probability of precipitation for each accumulation period.
- For each location (grid cell): 72 time series (6 durations × 12 months) are produced.
- Gamma distribution fitted using L-moments (to estimate parameters) instead of maximum likelihood.
- SPI values are transformed to standard normal scores (mean 0, sd 1); no units.
- Truncation: SPI values limited to [-5, +5].
- Typical range: about 95% of values within [-2, +2], ~68% within [-1, +1].
- Note on distribution choice: gamma is widely used but may not be optimal for the UK; alternatives (e.g., Pearson Type III, Tweedie) exist and may be used in future versions if justified.
- Overlaps and autocorrelation:
  - For periods >12 months, the underlying annual series overlaps, causing potential autocorrelation.
  - New monthly SPI series constructed from overlapping data are also likely autocorrelated; account for this in trend analyses.
- Standard period for fitting: 1961-2010.
- Data period: 1862-2015 (extended back using historic data digitised for the Historic Droughts project).

## IV. Format of the SPI_IHU_groups dataset
- Stored in CSV format.
- 9 columns total:
  - RID: row identifier
  - POLYGONID: IHU group ID (used to join with shapefiles)
  - THEDATETIME: date and time
  - Columns 4 to 9: six temporal aggregations of SPI (the dataset presents 6 SPI aggregations corresponding to the different accumulation periods/month combinations)
- SPI values are normal scores (mean 0, sd 1), no units.
- Value -9999 indicates No Data.

## V. Acknowledgments
- Joint outcomes from:
  - DrIVER project (NERC NE/L010038/1) as part of the Belmont Forum initiative
  - Historic Droughts (NERC NE/L01016X/1)
  - IMPETUS (NERC NE/L010267/1)

## References (key sources)
- Barker et al. (2015); Gudmundsson & Stagge (2014); Hayes et al. (2011); Keller et al. (2015); Kral et al. (2015); McKee et al. (1993); Stagge et al. (2015); Svensson et al. (2016); Tanguy et al. (2015, 2014).