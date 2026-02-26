# Historic Droughts Inventory of drought references for Historic Standardised Precipitation Index time series for IHU Groups (1862-2015) - version 2

## Overview
- Time series dataset of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) Groups, covering 1862–2015.
- SPI calculated for accumulation periods: 1, 3, 6, 9, 12, 18, 24 months, for each of 12 calendar months (84 series per location).
- Data stored as CSV with 10 columns; values are normal scores (mean 0, SD 1), range limited to -5 to +5; -9999 denotes No Data.

## Spatial and temporal scope
- Spatial: IHU Groups (approximately 400 km2 per group; joinable via POLYGONID).
- Temporal: 1862–2019 (dataset period 1862–2015; standard period 1961–2010 used for distribution fitting).
- Data can be aggregated over IHU groups for area-specific drought analysis.

## Data content and SPI specifics
- For each location and month, SPI is computed for seven durations (1, 3, 6, 9, 12, 18, 24 months) ending in that month.
- SPI calculation uses a gamma distribution fitted with L-moments (via a modified SCI R package) and then transformed to a standard normal distribution.
- Extreme values are truncated at ±5; about 95% of values fall within -2 to +2.
- Accumulation periods > 12 months use overlapping annual precipitation series, introducing potential autocorrelation.

## Data sources and methodology
- Underlying rainfall data: Met Office 5 km gridded rainfall.
- Data sources include:
  - Met Office daily grids (1960–2000) and additional updates rescued for 1862–1909.
  - UKCP09-derived data (1910–1959; 2001–2011).
- SPI methodology follows McKee et al. (1993); distribution choice (gamma) aligns with Europe-wide practice, though alternative distributions may be explored in the future if justified.

## Format and data fields
- File format: CSV.
- Key fields:
  - RID: row identifier
  - POLYGONID: IHU Group ID (for joins to shapefiles)
  - THEDATETIME: Date/time
  - SPI columns: seven durations x twelve months (per the 84 time series)
- Data values: SPI normal scores; -9999 = No Data.

## Context and projects
- Produced as part of:
  - DrIVER project (Drought Impacts: Vulnerability thresholds in monitoring and Early warning Research)
  - Historic Droughts project (Drought and Water Scarcity Programme)
- Historic Droughts Inventory supports multi-sector understanding by linking hydro-meteorological timelines with drought references (historical drivers, impacts, and responses).

## Motivation and usage
- Intended for integration into CEH droughts portal.
- Enables aggregation of SPI over IHU groups to study drought characteristics for specific areas of interest.
- Supports policy, water management, and research through standardized, comparable drought indicators.

## Limitations and caveats
- Autocorrelation concerns due to overlapping data for longer accumulation periods.
- Gamma distribution may not always be the best fit for UK data; other distributions (e.g., Pearson III, Tweedie) could be explored in future versions.
- Serial correlation considerations apply if SPIs are used for trend analyses (e.g., constructed monthly series).

## Acknowledgements and references
- Acknowledges support from DrIVER, Historic Droughts, and IMPETUS projects (funding details provided in the document).
- References to methodological sources and data sets underpinning the SPI calculation and data sources (not exhaustively listed here).