# Historic Droughts Inventory of drought references for Historic Gridded Standardised Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for the United Kingdom (1862-2015) - version 4

## Overview
- 5 km gridded Standardised Precipitation Index (SPI) data for the United Kingdom, a drought index based on precipitation probability.
- SPI calculated for accumulation periods: 1, 3, 6, 9, 12, 18, 24 months; for each of 12 calendar months.
- Standard fitting period: 1961-2010; dataset covers 1862-2015; data stored as NetCDF4.
- Outputs are dimensionless “normal scores” with mean 0 and standard deviation 1; values truncated to +/-5.

## Data content
- For each grid cell, 84 time series are produced (7 durations x 12 months).
- Structure: two-dimensional grids across the UK; one yearly NetCDF4 file per accumulation period; British National Grid projection; 12 monthly grids per year within each file.
- SPI values are the end-of-month accumulation period values (e.g., 6-month SPI for July 1998 covers Feb–Jul 1998).

## Methodology
- SPI defined from McKee et al. (1993); SPI derivation uses cumulative precipitation for each accumulation period and month.
- Distribution fitting: gamma distribution estimated with L-moments (via modified R SCI package) to produce normal scores.
- Autocorrelation considerations: overlapping data for longer periods induces serial correlation; implications noted for trend analysis.
- Extreme values are truncated at +/-5 due to distributional uncertainty.
- While gamma distribution is widely used and supported, recent work suggests other distributions may be better for UK data; current version retains gamma by convention.

## Data sources and changes (Version 4)
- Underlying monthly rainfall data: Met Office 5 km gridded rainfall data.
  - Composition: UKCP09 data (1910-1959 and 2001-2011), monthly grids from daily grids (1960-2000), rescued data (1862-1909), unpublished updates (2012-2015).
- Version 4 changes:
  - Switched from CEH-GEAR rainfall inputs to Met Office 5 km grids.
  - Updated monthly rainfall data for 1960-2000 via daily grids; added a 9-month accumulation period.
  - Version 2 and Version 3 superseded due to minor data issues.
- Motivation: part of Historic Droughts project and DrIVER initiative to improve drought monitoring and early warning.

## Context and purpose
- Part of DrIVER (Drought Impacts: Vulnerability thresholds in monitoring and Earlywarning Research) and Historic Droughts projects.
- Aims to support drought monitoring, spatial analysis of drought propagation, and identification of affected areas.
- Historic Droughts Inventory complements a hydro-meteorological timeline with 19th-century to present drought references, enabling cross-sector understanding and consistent planning for policy, water supply, agriculture, and industry.

## Format and access
- File format: NetCDF4, CEH gridded conventions.
- Spatial reference: British National Grid; grid-based UK coverage.
- Outputs intended for storage, sharing, and integration with monitoring portals and policy tools.

## Limitations and considerations for analysts
- Gamma distribution may not perfectly fit UK precipitation in all cases; alternative distributions (e.g., Pearson type 3, Tweedie) exist and could be pursued in future updates.
- Autocorrelation in SPI time series for longer accumulation periods should be accounted for in trend analyses.
- Serially correlated monthly series may be used for trend analysis but require appropriate statistical treatment.

## Practical applications for environmental monitoring
- Enables spatial and temporal monitoring of meteorological drought across the UK at multiple time scales.
- Facilitates cross-temporal comparisons of drought severity and duration, informing resource management and policy decisions.
- Supports integration with the Historic Droughts Inventory for multi-sector drought analysis, drivers, impacts, and responses.

## Acknowledgements and references
- Acknowledges DrIVER and Historic Droughts project funding (NERC/Belmont Forum collaborations) and contributing institutions.
- Key references include foundational SPI methodology and distribution considerations (McKee et al. 1993; Stagge et al. 2015; Svensson et al. 2017; Barker et al. 2015).