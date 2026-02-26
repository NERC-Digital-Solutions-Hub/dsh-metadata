# Historic Gridded Standardised Precipitation Index for the United Kingdom 1862-2015 (generated using gamma distribution with standard period 1961-2010)

## Overview
- 5km gridded Standardised Precipitation Index (SPI) data for the United Kingdom, spanning 1862–2015.
- SPI calculated for accumulation periods of 1, 3, 6, 12, 18, and 24 months, for each of the 12 calendar months.
- Data stored in NetCDF4 format; SPI values are unitless normal scores (mean 0, sd 1); values truncated to [-5, 5].
- Standard gamma distribution fitted (via L-moments) to annual accumulation time series; methodology unchanged from the earlier dataset despite data source changes.

## Purpose and context
- Produced under the Historic droughts project to enable cross-disciplinary analysis of past UK droughts and support drought management tools.
- SPI is a widely used drought indicator recommended by the WMO for monitoring meteorological drought; enables assessment of drought/wet spell rarity and spatial propagation.

## Data sources and provenance
- Primary rainfall inputs: Met Office 5km monthly gridded rainfall data.
- Data composition: UKCP09 data (1910–2011), unpublished Met Office updates (2012–2015), rescued historical rainfall data (1862–1909).
- This version replaces CEH-GEAR-based rainfall data (used in earlier SPIgamma61-10) with the Met Office gridded rainfall to derive SPI.

## Methodology
- SPI calculation follows McKee et al. (1993): transform precipitation totals for each location and duration into a normal score via a fitted gamma distribution.
- Gamma parameters estimated using L-moments (to address issues with maximum likelihood in some cases).
- For each location, 72 time series are produced (6 durations × 12 months).
- Autocorrelation considerations acknowledged due to overlapping data, especially for longer durations; implications for trend analyses and frequency interpretation.

## Data format and structure
- File format: NetCDF4, following CEH gridded conventions.
- Structure: two-dimensional UK grids with 12 monthly grids per year; one file per accumulation period.
- Projection: British National Grid.
- Data values: SPI normal scores in the range typically within [-5, 5].

## Temporal and spatial coverage
- Spatial resolution: 5 km grid over the United Kingdom.
- Temporal coverage: 1862–2015.
- Accumulation periods covered: 1, 3, 6, 12, 18, and 24 months (with corresponding monthly mappings).

## Data quality, limitations and caveats
- Gamma distribution is widely used but not universally the best fit for UK data; recent work suggests Pearson type 3 or Tweedie may be more adequate in some cases.
- Overlapping data for accumulation periods >12 months introduces autocorrelation; users should account for serial correlation in trend or frequency analyses.
- SPI units are dimensionless; interpretation relies on standard normal scoring and context of accumulation period.

## Usage and governance considerations
- Data governance: clearly documented data provenance, data lineage, and methodological choices (gamma with L-moments; standard period 1961–2010).
- Reproducibility: methodology and data sources described, enabling reproducible SPI calculations and potential future updates with alternative distributions.
- Documentation and acknowledgments tied to supported projects (Historic droughts, DrIVER, IMPETUS) and related literature. Potential future versions may adopt different distributions if justified.

## Access and references
- Related datasets and prior versions cited (e.g., SPIgamma61-10; CEH-GEAR); detailed references provided for methodological choices and supporting literature.