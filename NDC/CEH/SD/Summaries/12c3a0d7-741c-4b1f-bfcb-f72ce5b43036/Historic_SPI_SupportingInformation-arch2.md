# Historic Gridded Standardised Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for the United Kingdom (1862-2015) - version 3

## Summary
- 5 km gridded SPI for the United Kingdom, a drought index based on precipitation probability for various accumulation periods (1, 3, 6, 9, 12, 18, 24 months) across 12 calendar months.
- Standard period for gamma distribution fitting: 1961-2010; spatial and temporal coverage: 1862-2015.
- Data stored as NetCDF4 with British National Grid projection; SPIs are dimensionless normal scores (mean 0, sd 1) with values typically between -2 and +2, truncated beyond ±5.
- Version 3 updates underlying rainfall data (Met Office 5 km grids) and monthly inputs, adds a 9-month accumulation period, and supersedes version 2 (which had a data transfer error).
- Derived within the Historic Droughts project to enable spatial analysis of drought propagation and to support drought monitoring and management tools.

## Data scope
- Geographic scope: United Kingdom (gridded analysis).
- Spatial resolution: 5 km.
- Temporal coverage: 1862–2015.
- Accumulation periods: 1, 3, 6, 9, 12, 18, 24 months (each with 12 calendar months).
- Format: NetCDF4, CEH gridded dataset conventions.

## Data sources and methodology
- Data sources:
  - Met Office 5 km monthly rainfall grids, including UKCP09-based data, 1960-2000 derived grids, 2012-2015 updates, and rescued data for 1862-1909.
- SPI calculation approach:
  - For each grid cell, compute accumulating rainfall over the 7 durations ending each month (84 time series per cell: 7 durations × 12 months).
  - Fit a gamma distribution to each time series using L-moments (via a modified R SCI package) to estimate parameters.
  - Transform to a standard normal distribution to obtain SPIs (normal scores).
  - Truncate extreme values at ±5 due to estimation uncertainty.
- Notes and caveats:
  - Gamma distribution is commonly used but may not always be optimal for UK data; other distributions (e.g., Pearson type 3, Tweedie) may be explored in future versions.
  - Long-duration SPIs (>12 months) involve overlapping data, introducing autocorrelation; serial correlation should be accounted for in trend analyses.
  - Independence assumptions for frequency analysis are challenged by overlapping data; SPIs describe relative drought/severity within the same duration.
- Standard period for distribution fitting: 1961–2010.

## Data format and access
- File structure: one yearly NetCDF4 file per accumulation period, containing 12 monthly grids per year.
- Spatial reference: British National Grid.
- Data content: SPI values as normal scores (mean 0, sd 1) with no units; range limited to -5 to +5.
- Format notes: Dataset adheres to CEH gridded dataset conventions.

## Use cases for monitoring and policy assessment
- Enables spatial analysis and mapping of drought intensity and progression over time.
- Facilitates cross-temporal and cross-space drought comparisons to support drought preparedness and response planning.
- Supports multi-timescale drought assessment, from short-term (1–3 months) to long-term (18–24 months) perspectives.
- Provides standardized outputs suitable for reporting environmental health and policy performance.

## Acknowledgments and references
- Funded and supported by: DrIVER (NE/L010038/1), Historic Droughts (NE/L01016X/1), and IMPETUS (NE/L010267/1).
- Relevant references include methodological and data-source papers on SPI, its distributions, and UK drought indicators (e.g., McKee et al., 1993; Barker et al., 2015; Svensson et al., 2017; Stagge et al., 2015).