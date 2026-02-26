# Standardised Precipitation Index time series for Integrated Hydrological Units Hydrometric Areas (1961-2015)

## Overview
- Provides time series of SPI for IHU hydrometric areas to support drought monitoring and CEH droughts portal.
- Extends data coverage from 1862 to 2015; calculates SPI for accumulation periods of 1, 3, 6, 12, 18, and 24 months across all calendar months.
- Uses a consistent methodology across durations, enabling area-wide drought assessment within IHUs.

## Data content
- 72 time series per location (6 durations × 12 calendar months).
- Stored as CSV with 9 columns:
  - RID (row identifier)
  - POLYGONID (IHU hydrometric area ID; join key to shapefile)
  - THEDATETIME (date/time)
  - Columns 4–9: six SPI aggregations for the different durations
- SPI values are normal scores (mean 0, SD 1), unitless, truncated to [-5, 5].
- No Data value encoded as -9999.

## Data sources and lineage
- IHU hydrometric areas (Kral et al., 2015) as the spatial framework.
- Met Office 5 km monthly rainfall grids:
  - UKCP09 data (1910–2011)
  - Unpublished updates (2012–2015)
  - Historic Droughts project data (1862–1909)
- Digitised historic rainfall/temperature grids produced under Historic Droughts project to enable 1862–2015 coverage.
- This version differs from the earlier SPI_IHU_HA (1961–2012) primarily in the underlying rainfall data; methodology for SPI calculation is unchanged.

## Methodology
- SPI calculated per McKee et al. (1993) from the cumulative precipitation for each accumulation period ending in each month.
- Gamma distribution fitted to each time series (6 durations × 12 months) using L-moments (via a modified R SCI package) instead of maximum likelihood.
- Gamma distribution parameters estimated to transform data to a standard normal distribution (mean 0, SD 1).
- Extreme SPI values truncated at ±5.
- Standard fitting window: 1961–2010.
- Caution: For durations >12 months, overlapping data create autocorrelation; serial correlation can affect frequency analysis and trend assessments.
- Acknowledges potential limitations of the gamma distribution for UK data; alternatives (e.g., Pearson type 3, Tweedie) exist but gamma is retained for now.

## Data format and fields
- CSV format with 9 columns:
  - RID: row identifier
  - POLYGONID: IHU hydrometric area ID (join key)
  - THEDATETIME: date/time
  - Six SPI aggregations (one per accumulation duration for each calendar month)
- SPI values are unitless normal scores; range limited to -5 to 5; -9999 indicates No Data.

## Data governance, quality, and usage notes
- New version aligning with Met Office rainfall data; underway updates reflect improved historical rainfall grids.
- Notes on data quality:
  - Autocorrelation due to overlapping data for long durations; independence assumptions for frequency analysis may be violated.
  - Monthly SPIs concatenated across months are likely autocorrelated; account for this in trend analyses.
  - Gamma distribution may not be optimal for UK data; future versions may adopt alternative distributions.
- Suitable for integration into governance-enabled portals; SPI data can be joined to IHUs via POLYGONID for spatial analysis.

## Provenance, updates, and acknowledgments
- Jointly produced under DrIVER, Historic Droughts, and IMPETUS projects.
- Acknowledges funding sources and contributing data providers.

## References
- McKee et al. (1993); Stagge et al. (2015) on distribution choices; Smithsonian SCI R package (Gudmundsson & Stagge, 2014) and related drought index literature.
- CEH-GEAR and related UK rainfall datasets underpinning the rainfall inputs (Keller et al., 2015; Tanguy et al., 2014/2015).