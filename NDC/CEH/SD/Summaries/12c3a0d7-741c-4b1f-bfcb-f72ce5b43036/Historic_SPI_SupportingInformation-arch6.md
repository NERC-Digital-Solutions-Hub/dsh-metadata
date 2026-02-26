# Historic Gridded Standardised Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for the United Kingdom (1862-2015) - version 3

## Overview
- 5 km gridded SPI data for the United Kingdom, a drought index based on precipitation probability for various accumulation periods.
- Accumulation periods: 1, 3, 6, 9, 12, 18, 24 months; calculated for each of the twelve calendar months.
- Standard distribution fitted: gamma distribution (via L-moments) using the 1961-2010 period.
- Output as NetCDF4; British National Grid projection; normal scores (mean 0, sd 1) with no units.
- Coverage: 1862-2015.

## Motivation
- Produced under the Historic droughts project to understand past UK droughts and improve tools for drought management.
- SPI facilitates spatial analysis of droughts, detection of rare events, and assessment of long- vs short-term moisture conditions.
- SPI values inform about short-term to multi-year precipitation patterns and associated impacts on soil moisture, streamflows, and reservoirs.

## Data sources
- Met Office 5 km monthly rainfall gridded data.
  - Derived from UKCP09 data (1910-1959; 2001-2011) and 1960-2000 daily grids.
  - Unpublished updates (2012-2015) and historic data rescues (1862-1909).
- Historical context: transition from CEH-GEAR in earlier versions to Met Office rainfall data for this version.

## Method for deriving the SPI grids
- SPI computed from cumulative precipitation totals for each location and accumulation period.
- For each location: 84 time series (7 durations × 12 months) are created.
- Distribution fitting: gamma distribution estimated with L-moments (via modified SCI R package) to convert to normal scores (mean 0, sd 1).
- Extremes: SPI values outside -5 to +5 are truncated.
- Serial considerations:
  - Overlaps in data for longer accumulations (e.g., 18–24 months) induce autocorrelation.
  - New monthly SPIs concatenated across months are also likely autocorrelated; implications for trend analyses should account for this.
- Note: Although gamma is widely used, it may not be the best fit for UK data; alternatives (e.g., Pearson type 3, Tweedie) exist and could be explored in future versions.

## Format and structure
- File format: NetCDF4 following CEH gridded dataset conventions.
- Structure: two-dimensional UK grids with 12 monthly grids per year; one file per accumulation period.
- Grid system: British National Grid.
- Data units: SPIs are normal scores with no units; range limited to -5 to +5.

## Version history and data quality notes
- Version 3 updates:
  - Underlying monthly rainfall data updated: replaced CEH-GEAR with Met Office 5 km grids.
  - New monthly rainfall grids derived for 1960-2000 using Met Office daily grids.
  - Added 9-month accumulation period.
- Version 2 is superseded by Version 3 due to a transfer error that affected SPI18 data; Version 3 corrects this.

## Data usage considerations
- SPIs are intended for drought monitoring and comparative analysis across time scales; interpretation varies by accumulation period.
- Be mindful of serial correlation due to overlapping data when conducting trend analyses or frequency assessments.
- Gamma-based SPI may have limitations; consider validating with alternative distributions for specific applications.

## Acknowledgments
- Joint effort from DrIVER, Historic Droughts, and IMPETUS projects (NERC grants NE/L010038/1, NE/L01016X/1, NE/L010267/1).