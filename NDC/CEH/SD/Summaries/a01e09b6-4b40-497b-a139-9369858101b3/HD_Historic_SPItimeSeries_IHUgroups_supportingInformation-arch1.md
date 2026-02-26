# Historic Droughts Inventory of drought references for Historic Standardised Precipitation Index time series for IHU Groups (1862-2015) - version 2

## Overview
- Time series of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) Groups, spanning 1862–2015.
- SPI computed for accumulation periods of 1, 3, 6, 9, 12, 18, and 24 months, with data generated for each of the 12 calendar months.
- Standard period used to fit the gamma distribution is 1961–2010; SPI values are normalised (mean 0, sd 1) and unitless, typically within -2 to +2 (truncated to -5 to +5).
- Aims to support drought research and drought monitoring/early warning, and to enable aggregation of SPI over local areas for targeted analyses.

## Data content and calculation
- SPI derivation follows McKee et al. (1993): fitting a distribution to historical precipitation totals for each location and duration, then transforming to a normal score.
- 84 time-series per location (7 durations × 12 months) are produced.
- Calculations use the gamma distribution estimated via L-moments (via a modified R SCI package); note that alternative distributions (e.g., Pearson type 3, Tweedie) may be more appropriate in some UK cases but gamma remains the standard for this dataset.
- Data for each grid cell are linked to a corresponding IHU Group ID (POLYGONID) and timestamp (THEDATETIME).
- Acknowledges serial autocorrelation in longer-duration series due to overlapping data; cautions on independence assumptions for trend analyses.

## Context and Projects
- Produced within two UK/ international initiatives:
  - DrIVER (Drought Impacts: Vulnerability thresholds in monitoring and Earlywarning Research) under Belmont Forum funding.
  - Historic Droughts project (NERC) as part of the Drought and Water Scarcity Programme.
- Historic Droughts Inventory combines hydro-meteorological timelines with references to drought episodes, drivers, impacts, and responses from diverse sources.

## Data sources
- IHU Groups (Kral et al., 2015) as the spatial framework.
- Met Office 5 km rainfall grids, incorporating:
  - UKCP09-derived data (1910–1959 and 2001–2011)
  - Monthly grids derived from daily grids (1960–2000)
  - Unpublished Met Office updates (2012–2015)
  - Historic rainfall data rescued for 1862–1909

## Methodology
- SPI calculation: accumulation periods ending each calendar month; 84 series per location across all durations and months.
- Distribution fitting: gamma distribution using L-moments; transformation to normal scores; truncation at ±5.
- No data indicated by -9999.
- Notes on potential methodological updates in the future to include alternative distributions.

## Data format
- CSV format with 10 columns:
  - RID (row identifier)
  - POLYGONID (IHU Group ID)
  - THEDATETIME (date/time)
  - 7 SPI aggregates (one for each duration) across 12 months (total of 84 SPI values per location, stored as 7 columns in the file structure)
- SPI values are unitless normal scores in the range approximately -5 to +5.

## Version 2 changes
- Underlying rainfall input switched from CEH-GEAR to Met Office 5 km grids.
- 1960–2000 monthly rainfall grids revised using daily Met Office grids; newly derived monthly grids used for SPI.
- Added 9-month accumulation period to the dataset (version 2 expands or updates accumulation handling).
- Localised data issues for 1960–2000 resolved; extended historical coverage to 1862–2015.

## Motivation and applications
- Intended for incorporation into a CEH droughts portal.
- Enables aggregation of SPI over IHU groups to study drought characteristics for specific areas.
- SPI serves as a widely used drought indicator, useful for assessing short- to long-term moisture deficits and related impacts on hydrology, agriculture, and water resources.

## Limitations and considerations
- Serial correlation in long-duration SPIs due to overlapping time windows; careful treatment required for trend analyses.
- Gamma distribution may not perfectly fit UK precipitation; alternative distributions exist and could be explored in future releases.

## Acknowledgements
- DrIVER, Historic Droughts, and IMPETUS projects; funded by NERC and the Belmont Forum.