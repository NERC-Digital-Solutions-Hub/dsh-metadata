# Historic Gridded Standardised Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for the United Kingdom (1862-2015) - version 3

## Overview
- 5 km gridded Standardised Precipitation Index (SPI) data for the United Kingdom, a drought index based on precipitation probability for various accumulation periods.
- Coverage: 1862–2015; standard fitting period: 1961–2010; data stored as NetCDF4.
- SPI values are normalised (mean 0, standard deviation 1) with no units and limited to -5 to +5.
- Multiple accumulation periods (1, 3, 6, 9, 12, 18, 24 months) for each of the 12 calendar months; results stored as 84 time series per grid cell (7 durations × 12 months).

## What’s new in version 3
- Underlying rainfall data switched from CEH-GEAR to Met Office 5 km rainfall grids, enabling higher-quality historic rainfall inputs.
- Monthly rainfall grids for 1960–2000 re-derived from Met Office daily grids; 2012–2015 updates provided by Met Office; historic rainfall data rescues included (1862–1909).
- Added 9-month accumulation period.
- Version 3 supersedes version 2 due to a data-transfer error that affected SPI18 in version 2.

## Data sources
- Met Office 5 km monthly rainfall gridded data, incorporating:
  - UKCP09 data (1910–1959 and 2001–2011)
  - Monthly rainfall grids from daily grids (1960–2000)
  - Unpublished Met Office updates (2012–2015)
  - Rescued data for 1862–1909

## Method for deriving the SPI grids
- SPI calculation follows McKee et al. (1993): for each location, compute cumulative precipitation over accumulation periods (1, 3, 6, 9, 12, 18, 24 months) ending in each calendar month.
- For each location and duration, fit a gamma distribution to the historical precipitation series using L-moments (instead of maximum likelihood) to estimate parameters (via a modified R SCI package).
- Transform to standard normal scores (mean 0, sd 1) to produce the SPI.
- Extreme values (absolute SPI > 5) are truncated.
- Note: For UK, gamma distribution may not always be ideal; recent work suggests alternatives (e.g., Pearson type 3, Tweedie). Future versions may explore different distributions.
- Serial correlation considerations:
  - Accumulations >12 months involve overlapping data, creating potential autocorrelation.
  - Concatenated monthly SPIs are also likely autocorrelated; use caution for trend analyses.

## Dataset format and structure
- Format: NetCDF4 following CEH gridded dataset conventions.
- Spatial framework: British National Grid; two-dimensional UK grids.
- Temporal structure: one yearly file per accumulation period; each file contains 12 monthly grids.
- Data accessibility: SPI values are unitless normal scores within -5 to +5.

## Motivation and use
- Part of the Historic droughts project (NE/L01016X/1) aiming to understand past UK droughts to improve future drought management tools.
- SPI as a drought indicator helps:
  - Assess rarity and severity of droughts at different time scales.
  - Identify spatial patterns and propagation of drought events.
  - Inform analyses related to soil moisture, crop stress, streamflows, reservoir levels, and groundwater over varying horizons.

## Notes on interpretation and limitations
- The standard fitting period is 1961–2010; dataset covers 1862–2015.
- While gamma distribution is widely used and recommended, its suitability varies; future iterations may adopt other distributions.
- Overlap in data for longer accumulation periods introduces autocorrelation; results should account for this in statistical analyses.
- SPIs are designed to facilitate drought monitoring and comparisons across time scales, with explicit caveats regarding independence and serial correlation.

## Acknowledgments
- Collaborative outcomes from DrIVER, Historic Droughts, and IMPETUS projects (NERC grants NE/L010038/1, NE/L01016X/1, NE/L010267/1).