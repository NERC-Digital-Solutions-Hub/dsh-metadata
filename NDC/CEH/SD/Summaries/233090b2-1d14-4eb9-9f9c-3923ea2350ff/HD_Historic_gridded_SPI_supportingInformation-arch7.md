# Historic Droughts Inventory of drought references for Historic Gridded Standardised Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for the United Kingdom (1862-2015) - version 4

## Overview
- 5 km gridded Standardised Precipitation Index (SPI) data for the United Kingdom, a drought index based on precipitation probability for different accumulation periods.
- Accumulation periods: 1, 3, 6, 9, 12, 18, 24 months; each analyzed for all 12 calendar months.
- Standard period used to fit the gamma distribution: 1961-2010.
- Temporal coverage: 1862–2015.
- Data format: NetCDF4, projected on the British National Grid.

## What’s new in version 4
- Underlying rainfall data updated from CEHGEAR to Met Office 5 km rainfall grids.
- New monthly rainfall grids for 1960–2000 derived from Met Office daily grids; 2012–2015 updates included.
- Accumulation period of 9 months added.
- Some issues in the 1960–2000 Met Office monthly grids resolved.

## Data sources
- Met Office 5 km monthly rainfall gridded data (combining UKCP09 data; 1910–1959, 2001–2011; unpublished updates 2012–2015; rescued data 1862–1909).

## Method for SPI derivation
- SPI calculation follows McKee et al. 1993: for each grid cell, compute precipitation totals for 7 durations x 12 months (84 time series).
- Fit gamma distribution to each series using L-moments (via a modified R SCI package) to obtain parameters.
- Transform to a normal distribution (mean 0, sd 1); SPI values are unitless normal scores.
- SPI values truncated at ±5 due to extreme uncertainty.
- Note: while gamma is widely used, UK-specific tests suggest some distributions (e.g., Pearson Type III, Tweedie) may be more appropriate in some cases; gamma remains the current standard for this dataset.

## Calculation details and caveats
- For durations >12 months, the underlying precipitation series includes overlapping data, leading to potential autocorrelation.
- Serial correlation is present in both monthly SPIs and longer-duration series; users should account for this in trend analyses.
- The standard fitting period is 1961–2010; data cover 1862–2015.

## Data format and structure
- NetCDF4 files; two-dimensional UK grids.
- One yearly file per accumulation period; each file contains 12 monthly grids.
- Projection: British National Grid.
- SPI values are unitless normal scores in the range approximately within -5 to +5; most values fall within -2 to +2.

## Context and motivation
- Produced under the DrIVER project (Drought Impacts: Vulnerability thresholds in monitoring and Early warning Research) and the Historic Droughts project (NERC Drought and Water Scarcity Programme).
- SPI enables spatial analysis of drought severity, propagation over time, and identification of affected areas; supports drought monitoring and early warning initiatives.

## Applications for GIS work
- Map-based visualization of drought risk and moisture conditions across the UK at multiple time scales.
- Multi-temporal analysis by accumulating periods (1–24 months) across 12 months, enabling seasonal and long-term drought assessment.
- Integration with the Historic Droughts Inventory for cross-sectoral planning and policy support (hydrometeorological timelines and historical references).

## Acknowledgements and references
- Acknowledges funding from DrIVER, Historic Droughts, and IMPETUS.
- References include foundational SPI methodology and related drought index literature (McKee et al., Stagge et al., Barker et al., Gudmundsson & Stagge, Hayes et al., and others).