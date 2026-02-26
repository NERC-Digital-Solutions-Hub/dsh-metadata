# Historic Droughts Inventory of drought references for Historic Standardised Precipitation Index time series for IHU hydrometric areas (1862-2015) - version 2

## Brief description of the dataset
- Time series of Standardised Precipitation Index (SPI) for the IHU (Integrated Hydrological Units) hydrometric areas.
- SPI calculated for accumulation periods of 1, 3, 6, 9, 12, 18, and 24 months, with calculations for each of the 12 calendar months.
- Standard fitting period: 1961-2010; dataset spans 1862-2015; data stored in CSV format.
- SPI values are normal scores (mean 0, sd 1), units-free, truncated to -5 to +5; -9999 denotes no data.

## Context of the dataset
- Produced under two projects: DrIVER (Drought Impacts: Vulnerability thresholds in monitoring and Early warning Research) and Historic Droughts (part of the UK Drought and Water Scarcity Programme).
- Historic Droughts Inventory combines:
  - Hydro-meteorological timelines (rainfall, river flows, groundwater) for consistent drought indicators back to the 19th century.
  - References to past droughts from newspapers, legislation, agricultural media, and oral histories, to illuminate drivers, impacts, and responses over time.
- Aimed to provide a common reference for policy makers, water companies, agriculture, and industry; enables cross-sectoral, transparent drought planning.

## Motivation
- Designed to be incorporated into the CEH droughts portal.
- Aggregating SPI over IHU areas enables focused drought analysis for specific regions.
- SPI serves as a widely used drought metric (with multiple accumulation periods) for short- to long-term moisture assessment and monitoring.

## Data sources
- IHU hydrometric areas (Kral et al., 2015) as the spatial framework.
- Met Office 5 km monthly rainfall grids, including:
  - UKCP09 data (1910-1959, 2001-2011).
  - Monthly grids from Met Office daily grids (1960-2000).
  - Unpublished updates (2012-2015) and rescued data (1862-1909) for historic coverage.

## Method for deriving the SPI grids
- SPI calculation follows McKee et al. (1993): fits a gamma distribution to precipitation totals for each location and duration, then transforms to a normal score.
- Estimation uses L-moments (instead of MLE) due to fit issues in some cases; implemented via a modified R package SCI.
- Data are aggregated by end month (e.g., 6-month SPI for July 1998 uses precipitation Feb–Jul 1998).
- Serial correlation considerations:
  - For longer durations (e.g., 18, 24 months), overlapping data introduce autocorrelation.
  - Monthly SPIs constructed from consecutive months may also be autocorrelated; users should account for this in trend analyses.
- Distribution caveat: gamma distribution is still widely used and accepted, though UK-specific tests show limitations; alternative distributions (e.g., Pearson Type III, Tweedie) may be explored in future versions.
- Standard period for fitting: 1961-2010.

## Format of the dataset
- CSV file with 10 columns:
  - RID (row identifier)
  - POLYGONID (IHU hydrometric area ID)
  - THEDATETIME (date/time)
  - Columns 4-10: SPI values for the different durations and months (7 durations × 12 months = 84 time series per location)
- SPI values are unitless normal scores; range limited to -5 to +5; -9999 indicates No Data.

## Usage and governance considerations for Data Leaders
- Provides a robust, cross-sector knowledge base combining drought indicators with historical drought references.
- Facilitates data discoverability and integration into multi-stakeholder portals (e.g., CEH droughts portal).
- Supports governance around data lineage, quality (gamma fitting approach, data sources, updates), and metadata for discoverability.
- Encourages awareness of data limitations (distribution choice, autocorrelation) and the potential need for alternative distributions in future updates.
- Enables assessment of data gaps and granularity needs by region (IHU areas) and time scales, informing collaboration and data-sharing strategies.

## Acknowledgements
- Funded by DrIVER (Belmont Forum) and Historic Droughts (NERC Drought and Water Scarcity Programme); IMPETUS also involved.

## References
- Barker et al. (2015); Gudmundsson & Stagge (2014); Hayes et al. (2011); Keller et al. (2015); Kral et al. (2015); McKee et al. (1993); National Drought Mitigation Center (2015); Stagge et al. (2015); Tanguy et al. (2015, 2014)