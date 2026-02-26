# Gridded Standardized Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for Great Britain [SPIgamma61-10]

## Overview
- 1km and 5km gridded SPI data for Great Britain (a drought index based on precipitation probability).
- SPI calculated for accumulation periods of 1, 3, 6, 12, 18, and 24 months, each for all 12 calendar months.
- Data period: 1961–2012; distribution fitting uses a 1961–2010 standard period.
- Stored as NetCDF4 files on a THREDDS server; accessible via DOI.

## Motivation and use
- Developed within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- SPI enables assessment of drought rarity or unusually wet periods and supports spatial analysis, temporal propagation, and identification of affected areas in monitoring and early warning systems.
- Different time scales provide short-, medium-, and long-term moisture context.

## Data content and structure
- Two spatial resolutions: 1km (local/small-area analysis) and 5km (regional-scale, smaller files).
- For each location, 72 time series: 6 accumulation periods × 12 months.
- SPI is computed as a gamma-distribution-based index (via L-moments for parameter estimation), transformed to standard normal scores (mean 0, stdev 1) with no units.
- Values truncated to the range [-5, 5].
- Data are organized as two-dimensional grids (Great Britain) with one yearly NetCDF file per accumulation period; projected to the British National Grid.

## Methodology notes
- Gamma distribution used for fitting, with L-moments for parameter estimation (note: some UK-specific studies suggest alternative distributions may be more adequate; gamma remains widely used for now).
- Accumulation periods >12 months involve overlapping annual data, introducing potential autocorrelation.
- Serial correlation considerations: SPIs ending each calendar month can be concatenated into monthly series, but they may be autocorrelated; account for this in trend analyses.

## Data sources and derivation
- Primary rainfall input: CEH-GEAR (Gridded Estimates of Areal Rainfall).
- SPI calculation follows McKee et al. (1993); end-of-period month alignment defined for each accumulation period.

## Format, access, and usage
- Format: NetCDF4; two-dimensional grids with 12 monthly grids per year; one file per accumulation period.
- Projection: British National Grid.
- Access: Data hosted on THREDDS server; DOI provided.
- Data are “normal scores” (no units) and suitable for cross-location comparisons and visualization.

## Use and citation
- Terms of use apply; cite: Tanguy et al. (2015) Gridded Standardized Precipitation Index (SPIgamma61-10) in NERC EIDC.
- Full data terms and licensing available at the provided DOI.

## Acknowledgments and funding
- Project DrIVER; funded by Natural Environment Research Council (NE/L010038/1) as part of Belmont Forum collaboration.

## References (context)
- Several methodological and data source references are provided, including works on CEH-GEAR, SPI interpretation, and distributions for drought indices.