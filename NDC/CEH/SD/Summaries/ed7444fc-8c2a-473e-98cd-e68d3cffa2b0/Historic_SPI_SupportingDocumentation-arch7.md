# Historic Gridded Standardised Precipitation Index for the United Kingdom 1862-2015 (generated using gamma distribution with standard period 1961-2010)

## Overview
- 5 km gridded Standardised Precipitation Index (SPI) data for the United Kingdom, representing a drought index based on precipitation accumulation periods (1, 3, 6, 12, 18, 24 months) for each of the twelve calendar months.
- Spatial and temporal coverages: 1862–2015; data stored in NetCDF4 format on the British National Grid.
- SPI values are standardized scores (mean 0, standard deviation 1) with no units, truncated to the range -5 to +5.

## Data sources and derivation
- Underlying rainfall data: Met Office 5 km monthly gridded rainfall data. Source components include UKCP09 data (1910–2011), unpublished updates (2012–2015), and rescued historic data (1862–1909).
- Calculation methodology:
  - SPI computed as per McKee et al. (1993) for six accumulation periods across twelve months, yielding 72 time series per grid cell.
  - Gamma distribution fitted via L-moments (via a modified R SCI package) to estimate parameters.
  - Data transformed to normal scores (mean 0, sd 1); extreme values truncated at ±5.
- Model notes:
  - Gamma distribution is widely used and accepted, though some studies suggest alternatives (e.g., Pearson type 3, Tweedie) may be more adequate for the UK; future versions could explore alternatives.
  - For accumulation periods >12 months, overlapping data introduce serial autocorrelation; caution advised for trend analyses.

## Dataset format and structure
- Format: NetCDF4, following CEH gridded dataset conventions.
- Structure: two-dimensional UK grids with twelve monthly grids in each yearly file; one yearly file per accumulation period.
- Projection: British National Grid.
- SPI values: normal scores with no units, range limited to -5 to +5.

## Spatial and temporal coverage
- Geography: United Kingdom.
- Resolution: 5 km.
- Period: 1862–2015.
- Standard-fitted period for distribution: 1961–2010.

## Usage and interpretation for GIS
- Enables spatial analysis of drought occurrence and propagation, identification of the most severely affected areas, and assessment of drought at multiple time scales.
- Supports cross-temporal and cross-spatial drought assessments and integration with hydrological and water-resources planning.

## Important considerations for GIS workflows
- Large, continuous 5 km gridded dataset across many years; data availability may vary by period and source.
- Autocorrelation considerations due to overlapping data for longer accumulation periods; relevant when performing trend analyses.
- While gamma-based SPI is standard here, future work may consider alternative distributions for potentially improved fit.

## Acknowledgments
- Project collaborations include Historic Droughts (NE/L01016X/1), DrIVER, and IMPETUS; data contributions from Met Office and CEH-GEAR-based sources.