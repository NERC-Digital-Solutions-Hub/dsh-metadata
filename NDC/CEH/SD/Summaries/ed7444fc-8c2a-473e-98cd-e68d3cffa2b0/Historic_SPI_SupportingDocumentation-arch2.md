# Historic Gridded Standardised Precipitation Index for the United Kingdom 1862-2015 (generated using gamma distribution with standard period 1961-2010)

## Overview
- 5 km gridded Standardised Precipitation Index (SPI) data for the United Kingdom, covering 1862–2015.
- SPI calculated for accumulation periods of 1, 3, 6, 12, 18, and 24 months, with a separate set of grids for each calendar month.
- Standard gamma distribution fit uses 1961–2010 as the reference period.
- Data stored in NetCDF4 format on the British National Grid; outputs are unitless normal scores (mean 0, sd 1) with values truncated to ±5.

## Data sources and Method
- Data sources: Met Office 5 km monthly rainfall grids. Includes UKCP09 data (1910–2011), unpublished 2012–2015 updates, and historic data (1862–1909) rescued for the project.
- SPI calculation:
  - Based on McKee et al. (1993); 72 time series per grid cell (6 durations × 12 months).
  - Gamma distribution fitted using L-moments (via a modified SCI R package) to convert to normal scores.
  - SPI values represent the rarity of precipitation (or wet periods) for each accumulation period ending in a given month.
- Temporal framing:
  - Reference period for distribution fitting: 1961–2010.
  - Time coverage: 1862–2015.
- Notes on data quality:
  - Although gamma distribution is common for SPI, UK-specific work indicates potential fit issues; alternative distributions (e.g., Pearson type 3, Tweedie) may be explored in future versions.
  - Overlap in data for longer durations (e.g., 18–24 months) can introduce autocorrelation; SPIs for consecutive months may also be autocorrelated when concatenated.

## Format and structure
- Format: NetCDF4, CEH gridded dataset conventions.
- Structure: For each accumulation period, one yearly NetCDF file containing 12 monthly grids; outputs are 2D UK grids projected on the British National Grid.
- Values: Normal scores with no units; range truncated to [-5, 5].

## Purpose and applications
- Supports cross-disciplinary understanding of historic droughts and development of drought management tools (Historic droughts project).
- SPI enables:
  - Definition and monitoring of meteorological drought.
  - Assessment of drought rarity at multiple time scales.
  - Identification of spatial patterns, propagation over time, and severely affected areas.
  - Analysis of short- to long-term moisture conditions (1–24 months) and their relation to soil moisture, crop stress, streamflows, and reservoir levels.

## Data quality, limitations, and considerations for analysts
- Be aware of autocorrelation in long-duration SPI series due to overlapping data, particularly for trend analyses.
- The ongoing use of gamma distribution is justified by community standards, but alternative distributions may be more appropriate for UK data in future updates.
- When integrating with other datasets, account for temporal and spatial resolution differences and potential serial correlation.

## Data provenance and access
- Produced under the Historic Droughts project (NE/L01016X/1) with related grants (e.g., Belmont Forum initiative, DrIVER, IMPETUS).
- Documentation provides detailed methodological notes, data provenance, and references for further reading.
- Dataset adheres to CEH gridded conventions and is designed for incorporation into environmental monitoring portals and analysis workflows.

## Related datasets and future work
- This dataset differs from the earlier SPIgamma61-10 primarily in the rainfall input data (Met Office 5 km vs CEH-GEAR); methodology remains the same.
- Future versions may explore different statistical distributions to improve fit for UK data.