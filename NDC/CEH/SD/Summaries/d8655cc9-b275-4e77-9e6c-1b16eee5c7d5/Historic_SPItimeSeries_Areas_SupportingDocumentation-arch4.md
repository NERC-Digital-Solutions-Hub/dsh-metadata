# Supporting Information

- This document describes the SPI time series for the Integrated Hydrological Units (IHU) hydrometric areas, including data sources, methods, format, and caveats.

## Overview of the dataset
- Time series of Standardised Precipitation Index (SPI) for IHU hydrometric areas (IHU_HA).
- Coverage: 1862 to 2015; standard period for fitting the gamma distribution: 1961-2010.
- SPI computed for accumulation periods of 1, 3, 6, 12, 18, and 24 months, each for all 12 calendar months.
- 72 precipitation time series per location (6 durations × 12 months) are derived.
- Values are standard normal scores (mean 0, SD 1), unitless, truncated to the range -5 to 5; -9999 denotes No Data.
- Aimed to support incorporation into a CEH droughts portal for area-specific drought analysis.

## Data sources
- IHU hydrometric areas: UK hydrological reference units (coarsest spatial resolution of IHU).
- Met Office 5 km monthly rainfall grids: combinations of UKCP09 data (1910-2011), unpublished Met Office updates (2012-2015), and Historic Droughts project data (1862-1909).
- Note: This version uses Met Office rainfall data rather than CEH-GEAR data used in the earlier dataset.

## Methodology
- SPI calculation follows McKee et al. (1993): based on the cumulative probability of precipitation for a given accumulation period.
- For each location and month, the aggregation periods are fitted with a gamma distribution using L-moments (instead of MLE) to estimate parameters.
- The R package SCI (with L-moments) is used after modification.
- Transformation to a normal distribution yields the SPI normal scores; outliers are capped at ±5.
- Considerations:
  - For accumulation periods >12 months, overlapping data cause serial correlation in the underlying series.
  - Serial correlation also arises if monthly SPIs are concatenated for trend analyses.
  - While gamma distribution is commonly used, newer distributions (e.g., Pearson type 3, Tweedie) may be more adequate in some UK cases; gamma is retained for consistency, with potential future updates.
- Time alignment: the SPI for a given duration ending in a month refers to precipitation totals over the preceding months (e.g., 6-month SPI for July 1998 covers Feb–Jul 1998).

## Dataset format and structure
- File format: CSV.
- Columns (9 total): RID, POLYGONID (IHU hydrometric area ID), THEDATETIME (date/time), and six SPI columns corresponding to the accumulation periods (1, 3, 6, 12, 18, 24 months).
- Data are unitless normal scores; values outside -5 to 5 are truncated.
- NoData value: -9999.

## Temporal scope and data provenance
- Data period: 1862–2015.
- Data refinement: standard fitting period 1961–2010; extended back to 1862–2015 via historic digitisation and gridding.
- This dataset forms a joint output from multiple projects (DrIVER, Historic Droughts, IMPETUS).

## Usage considerations and caveats
- Intended for drought monitoring and portal integration; suitable for assessing drought/wet periods across IHU areas.
- Users should account for:
  - Autocorrelation and non-independence in longer-duration SPIs due to overlapping data.
  - Potential improvements by adopting alternative distributions in future versions.
- The SPI interpretation varies by duration (short-term vs. long-term drought signals), with shorter durations indicating soil moisture/crop stress and longer durations relating to streamflows, reservoirs, and groundwater patterns.

## Acknowledgments and references
- Acknowledgments: DrIVER, Historic Droughts, and IMPETUS projects (NERC/Gov.uk initiatives).
- Key references include McKee et al. (1993), Barker et al. (2015), Svensson et al. (2015), Gudmundsson & Stagge (2014), Hayes et al. (2011), and related CEH and UK drought literature.