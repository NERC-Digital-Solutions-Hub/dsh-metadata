# Supporting Information

- This document details a time series dataset of the Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) groups in the UK, covering 1862–2015 and calculated for multiple accumulation periods and calendar months.
- The SPI is used to define and monitor droughts by expressing precipitation rarity on various timescales.

## I. Brief Description of the dataset

- SPI time series for IHU groups (Kral et al., 2015) across accumulation periods: 1, 3, 6, 12, 18, and 24 months, each for all 12 calendar months.
- Standard period for gamma distribution fitting: 1961–2010.
- SPI values are normal scores (mean 0, std dev 1), with no units; ranges are limited to -5 to +5; missing data are coded as -9999.
- The dataset enables analysis of drought intensity at different temporal scales within specific IHU groups.

## II. Motivation

- Created to be incorporated into a CEH droughts portal, enabling aggregation of SPI over IHU groups to study drought within defined geographic areas.
- SPI is a widely used drought indicator (WMO-recommended) that helps assess rarity/severity of droughts and periods of anomalously wet conditions.
- Different accumulation periods offer distinct insights:
  - 1-month: short-term moisture and soil/crop stress
  - 3-month: short- to medium-term moisture and seasonal precipitation
  - 6-month: medium-term trends, potential links to streamflow and reservoirs
  - 12-month: long-term precipitation patterns, linked to streams/reservoirs
  - 18–24-month: longer-term precipitation and groundwater implications

## III. Data Sources

- IHU groups: UK Integrated Hydrological Units framework (Kral et al., 2015); typical group size ~400 km²; groups defined by major rivers and local geographic features.
- Met Office 5 km monthly rainfall grids:
  - UKCP09 data (1910–2011)
  - Unpublished updates (2012–2015)
  - Historic Droughts project data (1862–1909)
- Historic rainfall and temperature data digitised to support long historical coverage.

## III.2 Method for deriving the SPI grids

- SPI calculation follows McKee et al. (1993): based on the cumulative probability of precipitation for a given accumulation period ending in a specific month.
- For each location (grid cell): compute SPI for 1, 3, 6, 12, 18, 24 months, each across 12 calendar months (72 time series per location).
- Gamma distribution fitted to each time series using L-moments (instead of maximum likelihood) to estimate parameters; this is implemented by a modified R package SCI (Gudmundsson & Stagge, 2014).
- Transformation to a normal distribution yields SPI values (normal scores).
- Truncation applied: SPI values outside ±5 set to the nearest bound.
- Notes on distribution choice:
  - Gamma distribution commonly used and recommended for Europe, but some UK-specific studies find it sometimes fails normality tests; alternatives (e.g., Pearson type 3, Tweedie) may be explored in future if justified.
- Data structure considerations:
  - For durations > 12 months, the corresponding precipitation series overlaps between successive values, causing potential autocorrelation.
  - Serial correlation is present in monthly series constructed from overlapping data; this should be accounted for in trend analyses.

## IV. Format of the [SPI_IHU_groups] dataset

- Stored as CSV with 9 columns:
  - RID: row identifier
  - POLYGONID: IHU group ID (used for joins with IHU shapefiles)
  - THEDATETIME: date and time
  - Columns 4–9: six SPI aggregations (one per accumulation period across the 12 months)
- SPI values are normal scores (mean 0, std dev 1), no units; range limited to -5 to +5.
- -9999 indicates No Data.

## V. Acknowledgments

- Outputs result from collaborations including DrIVER (NERC Belmont Forum), Historic Droughts (NERC), and IMPETUS (NERC). Specific grant numbers are provided for each project.