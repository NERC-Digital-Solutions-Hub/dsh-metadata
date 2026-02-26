# Historic Droughts Inventory of drought references for Historic Standardised Precipitation Index time series for IHU hydrometric areas (1862-2015) - version 2

## Purpose and scope
- Presents time series of Standardised Precipitation Index (SPI) for IHU (Integrated Hydrological Units) hydrometric areas.
- SPI calculated for accumulation periods of 1, 3, 6, 9, 12, 18, and 24 months, for each of the twelve calendar months.
- Coverage: 1862 to 2015; standard fitting period: 1961–2010.
- Data stored in CSV format; designed to support drought monitoring and portal integration.

## Key updates in version 2
- Underlying rainfall data switched from CEH-GEAR to Met Office 5 km rainfall grids.
- For 1960–2000, new monthly rainfall grids derived from Met Office daily grids due to local data issues.
- Added 9-month accumulation period to SPI calculations.

## Calculation and methodology
- SPI defined as the cumulative probability of precipitation for a given accumulation period (McKee et al., 1993).
- For each location, SPI computed for 7 durations × 12 months (84 time series per location).
- Gamma distribution fitted to each time series using L-moments (via a modified R SCI package) to estimate parameters; data transformed to standard normal scores (mean 0, sd 1).
- SPI values truncated to -5 to +5; typical range is within -2 to +2 (95% of values).
- Notes on methodological cautions:
  - Gamma distribution may not always be optimal for the UK; alternatives (e.g., Pearson Type III, Tweedie) exist and could be used in future.
  - Accumulation periods >12 months involve overlapping data, introducing autocorrelation.
  - Serial correlation may affect trend analyses; appropriate statistical treatment is advised.

## Data sources
- IHU hydrometric areas (Kral et al., 2015) as spatial units.
- Met Office 5 km monthly rainfall grids, incorporating:
  - UKCP09 data (1910–1959, 2001–2011)
  - 1960–2000 grids derived from daily rainfall data
  - 2012–2015 unpublished/rescued updates
  - Historic rainfall data digitised for 1862–1909

## Data structure and format
- Storage format: CSV.
- Columns: RID, POLYGONID (IHU hydrometric area ID), THEDATETIME, plus 7 sets of SPI values corresponding to the 7 accumulation periods across 12 months.
- SPI values are dimensionless normal scores; range typically within -5 to +5; -9999 denotes No Data.

## Context and purpose within projects
- Produced under DrIVER (Drought Impacts: Vulnerability thresholds in monitoring and Early warning Research) and Historic Droughts projects.
- Aims to advance drought research and support drought monitoring/early warning tools.
- Motivates incorporation into the CEH droughts portal; enables comparison and aggregation of drought indicators across UK regions.

## Applications for analysts
- Enables monitoring of meteorological drought severity across UK IHU areas over long timescales.
- Facilitates multi-temporal and multi-scalar drought assessment (short-term to multi-year).
- Supports integration with other drought-related datasets for policy, water management, agriculture, and industry planning.
- Provides a standardized reference for cross-sector understanding of historical drought events and drivers.

## Data quality, limitations, and caveats
- Autocorrelation due to overlapping data in longer accumulation periods; affects statistical independence assumptions.
- Choice of gamma distribution may be revisited in future versions; other distributions may better fit UK data.
- Users should account for serial correlation when performing trend analyses or frequency assessments.

## Acknowledgments
- Joint effort from DrIVER, Historic Droughts, and IMPETUS projects; funding details listed in the document.