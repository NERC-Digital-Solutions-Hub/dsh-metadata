# Historic Droughts Inventory of drought references for Historic Gridded Standardised Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for the United Kingdom (1862-2015) - version 4

- An updated 5 km gridded SPI dataset for the United Kingdom, covering 1862–2015.
- SPI calculated for accumulation periods of 1, 3, 6, 9, 12, 18, and 24 months, with each period computed for all 12 calendar months.
- SPI values are the standardized normal scores (mean 0, std dev 1) derived from gamma-distributed precipitation; values are unitless and truncated at ±5.
- Data stored in NetCDF4 format on the British National Grid; one yearly file per accumulation period, with 12 monthly grids per year.

## What’s new in version 4

- Underlying rainfall data switched from CEHGEAR to Met Office 5 km rainfall grids.
- Monthly rainfall data for 1960–2000 updated due to local issues; new monthly grids derived from Met Office daily grids.
- Added 9-month accumulation period.

## Data content and structure

- 5 km gridded Standardised Precipitation Index (SPI) data for the UK.
- Accumulation periods: 1, 3, 6, 9, 12, 18, 24 months; each period has 12 months, yielding 84 time series per grid cell.
- SPI calculation method uses the gamma distribution fitted via L-moments (via a modified R SCI package); data transformed to standard normal scores.
- Range of SPI values typically between -2 and +2; extreme values truncated to ±5.
- Projected onto the British National Grid; NetCDF4 format; two-dimensional grids with 12 monthly grids in each yearly file.

## Calculation methodology and caveats

- SPI defined per McKee et al. (1993); the end month marks the accumulation period.
- Gamma distribution used for fitting; L-moments employed due to some poor fits with maximum likelihood in isolated cases.
- Serial correlation considerations:
  - For accumulation periods > 12 months, overlapping data causes autocorrelation in the time series.
  - Concatenated monthly SPIs are also likely autocorrelated; use appropriate methods for trend analysis.
- Acknowledges that gamma distribution may not be optimal for the UK in all cases; alternative distributions (e.g., Pearson type 3, Tweedie) could be explored in future versions.

## Data sources

- Met Office 5 km monthly rainfall grids.
  - UKCP09 data (1910–1959 and 2001–2011) incorporated.
  - Met Office daily grids (1960–2000) and unpublished 2012–2015 updates used.
  - Historic rainfall data rescued by the Historic Droughts project (1862–1909).

## Context and projects

- Produced as part of two projects:
  - DrIVER: Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research ( Belmont Forum), focusing on drought monitoring and early warning systems.
  - Historic Droughts: UK-wide, four-year project (2014–2018) to understand past droughts and develop tools for future drought management.
- Historic Droughts Inventory comprises:
  - Hydro-meteorological timelines of rainfall, river flows, and groundwater for drought indicators.
  - References to past droughts from 19th century to present (newspaper, legislation, agricultural media, oral histories) for drivers, impacts, and responses.

## Format and accessibility

- NetCDF4 files, CEH gridded conventions.
- Data accessible for spatial drought analysis and cross-sector planning; datasets and metadata intended to be discoverable and usable in portals.

## Usage notes for analysts

- Suitable for spatial drought analysis, historical trend assessment, and cross-referencing hydro-meteorological indicators with socio-economic drivers and impacts.
- When using long accumulation periods (18–24 months), account for autocorrelation due to overlapping data.
- Consider exploring alternative distributions in future work if assumptions of gamma distribution are not met for specific regions or periods.

## Acknowledgements

- Support from DrIVER, Historic Droughts, and IMPETUS (NERC grants NE/L010038/1, NE/L01016X/1, NE/L010267/1 respectively).