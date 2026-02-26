# Historic Gridded Standardised Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for the United Kingdom (1862-2015) - version 3

## Overview
- 5 km gridded SPI dataset for the United Kingdom, covering 1862–2015.
- SPI calculated for accumulation periods of 1, 3, 6, 9, 12, 18, and 24 months, for all 12 calendar months.
- Standard gamma distribution fitted using 1961–2010 to obtain SPI normal scores (mean 0, stdev 1); values limited to -5 to +5.
- Data stored in NetCDF4 format on the British National Grid; two-dimensional UK grids with 12 monthly grids per year, one file per accumulation period.

## What the dataset is for
- Supports spatial analysis of droughts, their temporal propagation, and identification of severely affected areas.
- Enables assessment of drought and wet spells at multiple time scales, informing drought management and policy planning.
- Part of the Historic Droughts project to improve tools for managing droughts in the UK and to provide cross-disciplinary insights.

## Data and methodology
- Data sources (III.1): Met Office 5 km monthly rainfall grids, combining UKCP09 data (1910–1959, 2001–2011), 1960–2000 monthly grids from daily data, updates (2012–2015), and rescued data (1862–1909).
- Method (III.2):
  - SPI computed as cumulative precipitation probability for each location and accumulation period.
  - For each grid cell, 84 time series (7 durations × 12 months) are created; a gamma distribution is fitted to each series using L-moments (via a modified R SCI package).
  - Data transformed to normal scores; values are non-dimensional.
  - Serial considerations: overlapping windows introduce autocorrelation; this affects independence assumptions in frequency analysis.
  - Note: while gamma is commonly used and broadly accepted, newer studies suggest other distributions (e.g., Pearson type 3, Tweedie) may be more suitable for the UK; current version uses gamma with potential future updates.
- Accumulation periods and scope: SPI values are calculated for 1, 3, 6, 9, 12, 18, and 24 months; 84 series per grid cell ending each month.
- Standard period for fitting: 1961–2010.
- Time coverage: 1862–2015.

## Format and structure
- Format: NetCDF4, CEH gridded dataset conventions.
- Projection/grid: British National Grid.
- Organization: yearly files; each file contains 12 monthly grids for each accumulation period; two-dimensional UK extent.

## Version history and changes
- Version 3 updates:
  - Underlying rainfall data migrated to Met Office 5 km grids.
  - Monthly rainfall data for 1960–2000 revised due to local issues; new monthly grids derived from daily data.
  - Accumulation period 9 months added (now includes 1, 3, 6, 9, 12, 18, 24).
- Version 2 is superseded by Version 3 due to corrected data transfers and SPI18 file issues.

## Usage considerations for data leaders
- Governance and provenance: traceable data lineage from Met Office sources; clearly documented changes across versions.
- Data quality and standards: gamma distribution historically used; awareness of potential better-fitting distributions; consider validating distribution choice for specific applications.
- Discoverability and metadata: NetCDF4 with standard CEH conventions; ensure metadata supports discoverability across data platforms and partners.
- Analysis cautions: expect autocorrelation in long accumulation periods due to overlapping data; adjust trend analyses accordingly.
- Collaboration and reuse: dataset supports cross-sector drought monitoring and policy analysis; potential integration with other UK drought indicators (e.g., hydrological proxies) with attention to methodological differences.

## Acknowledgments and references
- Acknowledges the Historic Droughts, DrIVER, and IMPETUS projects and NERC funding.
- Key references include: McKee et al. (1993) on SPI definition; Stagge et al. (2015) on candidate distributions; Svensson et al. (2017); Barker et al. (2015); Hayes et al. (2011); and related CEH-GEAR and SPI literature.