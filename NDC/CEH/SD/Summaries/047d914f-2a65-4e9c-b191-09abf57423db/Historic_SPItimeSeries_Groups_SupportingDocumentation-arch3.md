# Supporting Information

## Overview
- Describes a dataset of Standardised Precipitation Index (SPI) time series for Integrated Hydrological Units (IHU) groups in the UK (1862–2015), intended for drought monitoring and inclusion in the CEH droughts portal.

## What the dataset contains
- SPI calculated for accumulation periods of 1, 3, 6, 12, 18, and 24 months.
- SPI computed for each of the twelve calendar months, producing 72 time series per location (6 durations × 12 months).
- SPI values are normal scores (mean 0, standard deviation 1) with units removed; range limited to -5 to +5.
- Data stored as CSV with 9 columns: RID, POLYGONID (IHU group ID), THEDATETIME (date/time), and six SPI aggregations ( Columns 4–9).

## Motivation and use
- Aims to support drought monitoring and analysis within a drought portal; aggregating SPI over IHU groups enables localized drought assessment.
- SPI is a widely used drought index, reflecting the rarity of precipitation deficits/surpluses at specified time scales and its interpretation varies by the accumulation period (short-term to long-term moisture and potential impacts on soil moisture, crops, streams, reservoirs, groundwater).

## Data sources and provenance
- IHU groups (Kral et al., 2015) as the spatial framework.
- Met Office 5 km monthly rainfall grids, combining:
  - UKCP09 data (1910–2011)
  - Unpublished Met Office updates (2012–2015)
  - Historic Droughts project datasets (1862–1909)

## Method for deriving SPI grids
- SPI calculation follows McKee et al. (1993): uses cumulative precipitation probabilities for each accumulation period.
- End-of-period convention: SPI for a given month/end date reflects precipitation from the preceding accumulation window.
- Gamma distribution fitted to each time series (L-moments estimation; SCI R package modified for L-moments).
- Data transformation to a normal distribution to produce SPI values.
- Truncation applied at ±5 to handle extreme values.
- Notes on limitations:
  - Gamma distribution often fails Shapiro-Wilk tests for UK data; alternatives (e.g., Pearson Type 3, Tweedie) exist but gamma remains in use for consistency.
  - For accumulation periods > 12 months, overlapping data creates autocorrelation; serial correlations should be accounted for in trend analyses.
- Standard fitting period: 1961–2010.

## Data format and contents
- CSV format with 9 columns:
  - RID: row identifier
  - POLYGONID: IHU group ID (used for joins with shapefiles)
  - THEDATETIME: date and time
  - Columns 4–9: different SPI aggregations (per the six accumulation periods across 12 months)
- SPI values are unitless normal scores; typical range is -2 to +2, but allowed to -5 to +5; -9999 denotes no data.

## Data quality, metadata and governance
- Metadata and provenance are explicit, enabling traceability to IHU groups and Met Office data sources.
- Public sharing of underlying data is a potential barrier noted; consistent with broader data governance needs in monitoring frameworks.
- Data quality considerations (metadata adequacy, transformation steps, and caveats about distribution choice and autocorrelation) are documented to support proper interpretation and reuse.

## Acknowledgments and references
- Projected collaborations: DrIVER, Historic Droughts, IMPETUS.
- funders: Natural Environment Research Council and Belmont Forum initiatives.

## Implications for monitoring frameworks
- Strengths for policy scrutiny:
  - Multi-temporal scales (1–24 months) provide nuanced drought signals.
  - Clear provenance (IHU groups, Met Office grids) supports reproducibility and governance.
  - Explicit methodology (L-moments, gamma distribution, SCI package) aids transparency and peer review.
  - Data format is structured for integration with GIS and drought dashboards.
- Considerations for implementation:
  - Ensure metadata completeness and data governance to facilitate sharing and reuse.
  - Be mindful of autocorrelation and distribution limitations when using SPI for trend analyses or threshold-based decision rules.
  - Plan for data updates and potential methodological revisions (alternative distributions) to maintain relevance.