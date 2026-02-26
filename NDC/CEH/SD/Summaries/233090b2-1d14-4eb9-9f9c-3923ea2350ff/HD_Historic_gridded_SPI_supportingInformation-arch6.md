# Historic Droughts Inventory of drought references for Historic Gridded Standardised Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for the United Kingdom (1862-2015) - version 4

## Overview
- 5 km gridded Standardised Precipitation Index (SPI) data for the United Kingdom, a drought index based on precipitation probability.
- SPI computed for accumulation periods: 1, 3, 6, 9, 12, 18, 24 months, each for all twelve calendar months.
- Standard distribution fitting period: 1961-2010; dataset covers 1862-2015; stored in NetCDF4 format.

## What the dataset contains
- Gridded SPI values (unitless “normal scores” with mean 0, std dev 1) for each grid cell across the UK.
- 84 time series per location (7 durations × 12 months) used to derive SPI.
- Values truncated to the range -5 to +5.
- Data projection on the British National Grid.

## Calculation method
- SPI calculated as per McKee et al. (1993) using the gamma distribution fitted with L-moments.
- R package SCI modified to estimate gamma parameters via L-moments (instead of MLE).
- Transformation to a standard normal distribution to produce SPI values.
- For durations >12 months, overlapping accumulation periods introduce autocorrelation; SPIs for each calendar month are not fully independent.
- Note: gamma distribution, while standard, may be outperformed by other distributions (e.g., Pearson type 3, Tweedie) in some UK cases; current dataset uses gamma with scope for future alternatives.

## Data sources and processing
- Met Office 5 km monthly rainfall grids used as primary data source.
- Composition includes: UKCP09 data (1910-1959; 2001-2011), monthly rainfall from daily grids (1960-2000), unpublished Met Office updates (2012-2015), rescued data (1862-1909).
- New monthly rainfall grids for 1960-2000 derived from daily grids; 9-month accumulation period added in this version.

## Context and motivation
- Produced under DrIVER (Drought Impacts: Vulnerability thresholds in monitoring and Earlywarning Research) and Historic Droughts projects.
- Aims to advance drought research, monitoring, and decision support through spatial analysis of drought propagation and severity.
- Historic Droughts Inventory combines:
  - Hydro-meteorological timelines (rainfall, flows, groundwater) for drought indicators.
  - References to past droughts from diverse sources (newspapers, legislation, media, oral histories) to support policy and planning.
- Provides a common reference for policymakers, water suppliers, agriculture, and industry to enable consistent planning.

## Format and access
- File format: NetCDF4 (CEH gridded dataset conventions).
- Structure: one yearly file per accumulation period; two-dimensional UK grids with 12 monthly grids per year.
- Coverage: 1862–2015.
- Purpose: enables spatial drought analysis, temporal propagation studies, and identification of severely affected areas.

## Version history and notes
- Version 4:
  - Updated underlying rainfall data to Met Office 5 km grids.
  - Replaced 1960-2000 monthly rainfall grids with new data derived from daily grids.
  - Added 9-month accumulation period.
- Versions 2 and 3 superseded due to minor data issues.

## Important considerations for use
- Serial autocorrelation is present for longer accumulation periods due to overlapping data; affects independent statistical analyses.
- SPI values are model-based estimates with potential distribution alternatives; future versions may explore different distributions.
- Outputs are suitable for trend analysis, regional drought mapping, and informing multi-sector drought planning, with appropriate statistical handling of autocorrelation.

## Key references
- McKee et al. (1993); SPI definition.
- Stagge et al. (2015); candidate distributions for climatological drought indices.
- Svensson et al. (2017); distribution considerations for UK SPI.
- Tanguy et al. (2015, 2014); prior SPI datasets and CEH-GEAR rainfall estimates.
- Barker et al. (2015); drought indicators for UK catchments.
- Hayes et al. (2011); Lincoln Declaration on Drought Indices.