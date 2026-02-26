# Historic Gridded Standardised Precipitation Index for the United Kingdom 1862-2015 (generated using gamma distribution with standard period 1961-2010)

- A 5 km gridded Standardised Precipitation Index (SPI) dataset for the United Kingdom, covering 1862–2015.
- SPI is a drought index based on the probability of precipitation for various accumulation periods (1, 3, 6, 12, 18, 24 months) across all calendar months.
- Data stored in NetCDF4 format on the British National Grid; one yearly file per accumulation period; 12 monthly grids per year.

## Overview and purpose

- Created within the Historic droughts project to enable spatial analysis of droughts and their propagation over time.
- SPI allows assessment of drought rarity or wet periods at different time scales, aiding drought management and historical analysis.
- Provides a tool for identifying severely affected areas and long-term precipitation patterns.

## Data sources and provenance

- Met Office 5 km monthly rainfall grids used to derive SPI.
  - Includes UKCP09 data (1910–2011), unpublished updates (2012–2015), and historic data rescued for 1862–1909.
- This version differs from the 2015 publication that used CEH-GEAR rainfall estimates; the methodology remains the same.

## Methodology (SPI calculation)

- SPI follows McKee et al. (1993): fit a gamma distribution to the accumulation-period precipitation series for each grid cell and calendar month.
- Estimation uses L-moments (instead of maximum likelihood) to fit gamma parameters due to some instability with MLE in isolated cases.
- Transformation to a normal distribution yields SPI values (mean 0, std dev 1; units are not defined).
- SPI values are truncated at +/- 5 for extremes.
- For each grid cell, SPI is computed for six accumulation periods and for twelve calendar months, yielding 72 time series per location.
- Software: modified R package SCI to apply L-moments parameter estimates.
- Note on distribution choice: gamma is widely used and accepted, but recent work suggests alternatives (e.g., Pearson Type III, Tweedie) may be more adequate for the UK; future versions may use different distributions if justified.

## Time series structure and statistical considerations

- Accumulation periods over 12+ months use overlapping annual precipitation series, introducing potential autocorrelation.
- Serial correlation is possible in SPIs calculated for consecutive months; this affects independence assumptions used in some frequency analyses.
- SPIs for different calendar months are derived from the same underlying data series, especially for longer accumulation periods.

## Data format and metadata

- File format: NetCDF4 following CEH gridded dataset conventions.
- Spatial projection: British National Grid.
- Structure: two-dimensional grids; 12 monthly grids in each yearly file; one file per accumulation period.
- Values: SPI normal scores with no units; range limited to -5 to +5.

## Use, interpretation, and caveats

- Applications include drought monitoring, spatial analysis of drought propagation, and long-term precipitation pattern studies.
- Interpretation depends on accumulation period; shorter SPI reflects short-term moisture and potential agricultural stress, longer SPI relates to reservoir levels and groundwater.
- Caution due to potential autocorrelation and distribution choice; results may evolve with future methodological updates.

## Provenance, updates, and acknowledgments

- Part of the Historic Droughts project (NE/L01016X/1) and related initiatives (e.g., DrIVER, IMPETUS).
- Acknowledges data sources and supporting references related to drought indices, distributions, and gridded rainfall datasets.

## Practical considerations for data leadership

- Emphasizes governance around data provenance, metadata, discoverability, and versioning.
- Encourages consideration of alternative distributions in future releases and documentation of methodological choices.
- Highlights potential collaborations for improving data quality and coverage, given historical data gaps and data protection considerations.