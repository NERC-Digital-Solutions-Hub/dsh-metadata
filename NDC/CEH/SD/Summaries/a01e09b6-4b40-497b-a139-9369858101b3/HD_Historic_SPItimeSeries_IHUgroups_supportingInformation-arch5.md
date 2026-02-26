# Historic Droughts Inventory of drought references for Historic Standardised Precipitation Index time series for IHU Groups (1862-2015) - version 2

## Overview
- Presents SPI time series for Integrated Hydrological Units (IHU) Groups across 1862–2015, version 2.
- SPI computed for accumulation periods of 1, 3, 6, 9, 12, 18, 24 months, for every calendar month (84 series per location).
- Data stored as CSV; SPI values are normal scores (mean 0, SD 1), range approximately -5 to 5; -9999 indicates No Data.
- Calculations follow McKee et al. (1993) with gamma distribution fitted via L-moments; transformation to standard normal distribution performed.
- Notes on limitations: potential autocorrelation due to overlapping data windows; gamma distribution suitability discussed; alternative distributions may be used in future.

## Context and Projects
- Produced within two projects: DrIVER (Drought Impacts: Vulnerability thresholds in monitoring and Earlywarning Research) and Historic Droughts (NERC Drought and Water Scarcity Programme).
- Aims to support drought research and improved drought monitoring/early warning; intended for incorporation into a CEH droughts portal.

## Dataset Content
- SPI time series for IHU Groups (group-level hydrometric units, ~400 km² each).
- For each location, 84 time series (7 durations × 12 calendar months) are generated for the period 1862–2015.
- Data captured in a single CSV file with 10 columns:
  - RID (row identifier)
  - POLYGONID (IHU Group ID)
  - THEDATETIME (date)
  - SPI aggregations (seven temporal scales)

## Data Sources
- IHU Groups data (Kral et al., 2015).
- Met Office 5 km monthly rainfall grids, incorporating:
  - UKCP09-derived data (1910–1959, 2001–2011)
  - Monthly grids from daily grids (1960–2000)
  - Unpublished 2012–2015 updates
  - Historic gridded rainfall data for 1862–1909 (rescued data)

## Methodology
- SPI defined as the cumulative probability of precipitation for a given accumulation period; end-month convention.
- For each grid cell, compute 1,3,6,9,12,18,24-month SPIs for all 12 calendar months (84 series).
- Fit gamma distribution to each series using L-moments (via modified R SCI package); transform to standard normal distribution.
- Values truncated to [-5, 5] to handle extremes.
- Acknowledge that gamma distribution may not be optimal for all UK cases; alternative distributions (e.g., Pearson type 3, Tweedie) discussed for future versions.
- Note potential autocorrelation: overlapping data across long accumulation periods leads to non-independence; consider this in trend analyses.

## Format and Metadata
- CSV format with 10 columns: RID, POLYGONID, THEDATETIME, and seven SPI aggregations.
- SPI values are unitless normal scores; -9999 marks No Data.

## Motivation and Use
- Facilitates aggregation of SPI over specific hydrometric areas (IHU groups) to study drought characteristics locally.
- Supports drought monitoring, historical analysis, and portal-based dissemination through CEH droughts portal.

## Version 2 Changes and Rationale
- Underlying rainfall data switched from CEH-GEAR to Met Office 5 km grids, improving data quality for historical calculations.
- Addition of 9-month SPI accumulation period.
- Refined monthly rainfall data for 1960–2000; extended data derivation using daily grids and rescued historic data (1862–1909).
- Standard fitting period remains 1961–2010; dataset covers 1862–2015.

## Limitations and Considerations
- Serial correlation due to overlapping accumulation windows; caution for statistical analysis that assumes independence.
- SPI serials for longer durations (e.g., 18, 24 months) share data across periods, affecting frequency-analysis assumptions.
- Potential adaptation to alternative distributions in future versions if justified by UK-specific data characteristics.

## Acknowledgements and References
- Supported by DrIVER, Historic Droughts, and IMPETUS (NERC grants) with Belmont Forum involvement.
- Key references listed for SPI methodology, distributions, and data sources.