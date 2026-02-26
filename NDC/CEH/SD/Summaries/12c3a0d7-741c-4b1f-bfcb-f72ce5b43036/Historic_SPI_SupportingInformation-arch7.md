# Historic Gridded Standardised Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for the United Kingdom (1862-2015) - version 3

## Overview
- 5 km gridded SPI dataset for the United Kingdom, a drought index based on precipitation probability for specified accumulation periods.
- SPI calculated for accumulation periods 1, 3, 6, 9, 12, 18, 24 months, for each of the 12 calendar months.
- Stored as NetCDF4 files in grid format suitable for GIS analysis and map-based visualization.

## Data coverage and format
- Spatial: United Kingdom on the British National Grid (2D grids).
- Temporal: 1862–2015.
- Accumulation periods: 1, 3, 6, 9, 12, 18, 24 months (each with 12 monthly grids per year).
- Data format: NetCDF4, following CEH gridded conventions; values are normal scores (mean 0, stdev 1) with no units, range typically within -5 to +5.

## Data sources
- Met Office 5 km monthly rainfall grids (1960–2000 derived from daily grids; 1910–1959 and 2001–2011 from UKCP09; updates 2012–2015; historic rainfall data 1862–1909 rescued).
- Underlying rainfall data updated from CEH-GEAR in version 3 (now Met Office 5 km data).

## SPI calculation method
- Based on McKee et al. (1993): SPI is the cumulative probability of precipitation for each location and accumulation period.
- For each location, 84 time series are created (7 durations × 12 months).
- Gamma distribution fitted to each time series using L-moments (via modified R SCI package) to estimate parameters.
- SPI transformed to a normal distribution with mean 0 and sd 1 (normal scores); values truncated to -5 to +5 due to extreme uncertainties.
- Note: gamma distribution commonly used but may not pass certain normality tests for UK data; alternative distributions exist but gamma is retained for consistency with current practice.

## Data structure and access
- Files: one NetCDF4 file per accumulation period; each yearly file contains 12 monthly grids.
- Projection: British National Grid.
- Grids: 5 km resolution across the UK.

## Version history and changes
- Version 3: replaces underlying rainfall data with Met Office 5 km grids; updates to the monthly rainfall data for 1960–2000; adds 9-month accumulation period.
- Version 2: superseded by Version 3 due to data transfer error (SPI18 files missing and substituted by SPI12).

## Considerations and caveats
- For accumulation periods > 12 months, data are overlapping, introducing potential autocorrelation in the series.
- Serial correlation may affect trend analyses; concatenated monthly SPIs are likely autocorrelated.
- Indices reflect relative rarity/severity within each duration, not independent annual events.

## Applications for GIS specialists
- Create spatial drought maps and perform regional comparisons across the UK.
- Integrate SPI layers with other environmental or policy-relevant GIS datasets for planning and analysis.
- Support multi-temporal drought and moisture trend analyses using gridded spatial data.

## Acknowledgments
- Historic Droughts project (NE/L01016X/1), DRiVER initiative (NE/L010038/1), IMPETUS (NE/L010267/1), NERC funding.

## References
- Key references outlining SPI methodology, distributions, and related datasets (McKee et al., 1993; Stagge et al., 2015; Barker et al., 2015; Svensson et al., 2017; Hayes et al., 2011; Keller et al., 2015; Tanguy et al., 2014–2015).