# Supporting Information

## Overview
- 5km gridded Standardised Precipitation Index (SPI) dataset for the United Kingdom designed for map-based drought analysis.
- SPI is a drought index based on the probability of precipitation for specified accumulation periods, calculated per grid cell and month.

## Dataset details
- Accumulation periods: 1, 3, 6, 9, 12, 18, 24 months; each period has 12 calendar months, yielding 84 time series per grid cell.
- Spatial and temporal coverage: 1862–2015 across the United Kingdom; standard gamma distribution fit uses 1961–2010.
- Format and projection: NetCDF4; British National Grid (two-dimensional UK-wide grids); SPI values are normal scores with mean 0 and standard deviation 1, unitless and truncated to the range [-5, 5].

## Motivation and GIS relevance
- Enables spatial analysis of past droughts and their propagation over time; supports monitoring and management of droughts and associated water scarcity.
- SPI values at different time scales provide short-, medium-, and long-term moisture context for policy, planning, and public-facing maps.

## Data sources
- Met Office 5km monthly rainfall gridded data, incorporating:
  - UKCP09 data (1910–1959 and 2001–2011)
  - Monthly rainfall grids from Met Office daily grids (1960–2000)
  - Unpublished updates (2012–2015)
  - Historic Droughts project rescues (1862–1909)

## Method for deriving the SPI grids
- SPI calculation: follows McKee et al. (1993) by fitting a gamma distribution to the accumulation-period precipitation series for each grid cell and month.
- Parameter estimation: L-moments (instead of maximum likelihood) to derive gamma parameters; implemented via a modified R package SCI.
- Transformation: convert to standard normal scores (mean 0, stdev 1); truncation of extreme values at ±5.
- Notes on distribution choice: gamma distribution is widely used and accepted, but recent work suggests alternatives (e.g., Pearson type 3, Tweedie) may be more adequate for the UK; future versions may explore other distributions.
- Temporal structure considerations: for >12-month periods, the underlying annual precipitation series overlaps across successive values, introducing potential autocorrelation; serial correlation should be accounted for in trend analyses.

## Data format and structure
- File structure: NetCDF4 following CEH gridded conventions.
- Spatial structure: two-dimensional UK-wide grids; British National Grid projection.
- Temporal structure: one yearly file per accumulation period; each file contains 12 monthly grids for each year.
- Data characteristics: SPIs are unitless normal scores within [-5, 5], with no units.

## Caveats and statistical notes for GIS use
- Autocorrelation: overlapping time windows for longer accumulation periods cause serial correlation in SPI time series; treat for trend analyses accordingly.
- Independence assumption: not strictly met for long-duration SPIs; interpret drought/wlood anomalies within the context of their respective accumulation period and the same-period datasets.

## Acknowledgments and provenance
- Project collaboration: Historic droughts (NE/L01016X/1), DrIVER (NE/L010038/1), IMPETUS (NE/L010267/1).
- Part of efforts to develop tools for understanding historic droughts and informing future drought management.

## References (selected)
- McKee, T.B., Doesken, N.J., Kleist, J. (1993). The Relationship of Drought Frequency and Duration to Time Scales.
- Barker et al. (2015); Svensson et al. (2017); Stagge et al. (2015); Gudmundsson & Stagge (2014); Hayes et al. (2011).
- Tanguy et al. (2015, 2014) related to SPI datasets and UK rainfall datasets.