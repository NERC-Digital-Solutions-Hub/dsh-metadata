# Historic Droughts Inventory of drought references for Historic Standardised Precipitation Index time series for IHU hydrometric areas (1862-2015) - version 2

## Brief description of the dataset
- Time series of Standardised Precipitation Index (SPI) for the Integrated Hydrological Units (IHU) hydrometric areas, covering 1862–2015.
- SPI calculated for accumulation periods: 1, 3, 6, 9, 12, 18, 24 months, for each of the 12 calendar months.
- Standard period used to fit the gamma distribution: 1961–2010.
- SPI values are normal scores (mean 0, SD 1), unitless, truncated at ±5; no data coded as -9999.
- Data stored in CSV format with 10 columns per time series entry.

## Context of the dataset
- Part of two projects: DrIVER (Drought Impacts: Vulnerability thresholds in monitoring and Early-warning Research) and Historic Droughts (UK droughts and water scarcity, 2014–2018).
- DrIVER aimed to improve drought monitoring and early warning; Historic Droughts sought a cross-disciplinary understanding of past UK droughts to improve future management.
- The Historic Droughts Inventory combines hydro-meteorological timelines with references to past droughts (from newspapers, legislation, agricultural media, oral histories) to enable multi-sectoral understanding for policy makers, regulators, and water managers.
- Structure of the Inventory mirrors European Drought Impact Inventory concepts, adapted to hold various drought references beyond impacts.

## Inventory
- Two main elements used together:
  1) Hydro-meteorological timelines of rainfall, river flows, and groundwater with consistent drought indicators over the 19th–21st centuries.
  2) References to past droughts across centuries, including sources and links to full materials, enabling understanding of drivers, impacts, and responses.

## Motivation
- Dataset produced for incorporation into a CEH droughts portal.
- Aggregating SPI over IHU areas enables study of drought within defined regions.
- SPI is a widely used meteorological drought index endorsed by the WMO; multi-duration SPI provides varied insight into short- to long-term moisture conditions and related hydrological impacts.

## Data sources
- IHU hydrometric areas (Kral et al., 2015) as the spatial framework.
- Met Office 5 km monthly rainfall grids, incorporating historical and rescues:
  - UKCP09 data (1910–1959, 2001–2011)
  - Monthly rainfall grids derived from daily grids (1960–2000)
  - Unpublished Met Office updates (2012–2015)
  - Rescued data for 1862–1909

## Method for deriving the SPI grids
- SPI calculated per McKee et al. (1993) as the cumulative probability of precipitation for a given accumulation period, ending in the relevant month.
- For each location, SPI computed for 1, 3, 6, 9, 12, 18, 24 months across all 12 months (84 time series per grid cell).
- Gamma distribution fitted to each time series using L-moments to estimate parameters (to avoid failures of maximum likelihood in some cases).
- SPI transformation to a standard normal distribution (mean 0, SD 1); truncation of extremes at ±5.
- Calculation tool: R package SCI, modified to use L-moments instead of MLE.
- Notes on limitations:
  - Gamma distribution may fail Shapiro–Wilk tests in the UK; alternatives like Pearson III or Tweedie can be considered in future.
  - For durations >12 months, overlapping data cause serial correlation in the underlying time series; implications for trend analyses should account for this.
  - The dataset covers 1862–2015, enabled by historic rainfall data digitisation; standardization period remains 1961–2010.

## Format of the dataset
- CSV format with 10 columns:
  - RID: row identifier
  - POLYGONID: IHU hydrometric area ID
  - THEDATETIME: date/time
  - Columns 4–10: SPI values for the different temporal aggregations
- SPI values are unitless normal scores, range -5 to +5; -9999 indicates No Data.

## Acknowledgements
- Joint effort from DrIVER (Belmont Forum), Historic Droughts (NERC Drought and Water Scarcity Programme), and IMPETUS (NERC).