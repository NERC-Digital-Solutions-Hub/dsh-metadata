# Historic Droughts Inventory of drought references for Historic Standardised Precipitation Index time series for IHU Groups (1862-2015) - version 2

## Overview
- Time series of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) groups, covering 1862–2015.
- SPI calculated for multiple accumulation periods (1, 3, 6, 9, 12, 18, 24 months) across all 12 calendar months, yielding 84 series per location.
- Data intended for drought monitoring, research, and to support multi-sector drought understanding within the CEH droughts portal.

## What the dataset contains
- 84 precipitation time series per location (7 durations × 12 months).
- SPI values are normal scores (mean 0, sd 1), unitless and truncated to [-5, 5].
- Data stored in CSV format with 10 columns:
  - RID (row identifier)
  - POLYGONID (IHU group ID)
  - THEDATETIME (date)
  - SPI time series for each accumulation period (7 columns)
  - -9999 denotes No Data

## Calculation method
- SPI defined as the probability of observed precipitation for a given accumulation period (McKee et al., 1993).
- Accumulation periods end in the month specified (e.g., 6-month SPI for July 1998 covers Feb–Jul 1998).
- Gamma distribution fitted to each time series using L-moments (via a modified R SCI package), with parameters estimated to transform data to a standard normal distribution.
- Standard fitting period: 1961–2010.
- Data cover 1862–2015; back to 1862 made possible by historic rainfall data digitised/gridded by Met Office.
- Values beyond ±5 are truncated; approximately 95% of SPIs fall within [-2, 2].

## Data sources and provenance
- IHU groups (Kral et al., 2015) as the spatial reference framework.
- Met Office 5 km monthly rainfall grids, including:
  - UKCP09-derived data (1910–1959, 2001–2011)
  - Monthly grids from Met Office daily grids (1960–2000)
  - Unpublished updates (2012–2015)
  - Rescue data for 1862–1909
- Underpinning projects:
  - DrIVER (Drought Impacts: Vulnerability thresholds in monitoring and Earlywarning Research)
  - Historic Droughts (part of UK NERC programmes)
  - IMPETUS (NERC grant support)

## Context and purpose
- Part of the Historic Droughts Inventory, a knowledge base of past drought characteristics, drivers, impacts, and responses intended to support policy, water supply planning, agriculture, and industry.
- The SPI dataset enables aggregation over IHU hydrometric areas to study drought patterns for specific regions of interest.
- Aims to advance drought research and provide consistent, comparable drought indicators across time and space.

## Temporal and spatial scope
- Spatial: Integrated Hydrological Units (IHU) groups, metadata aligned to POLYGONID for joins with shapefiles.
- Temporal: 1862–2015; standard distribution fit uses 1961–2010 as reference.

## Format and data structure details
- CSV format with 10 columns:
  - RID, POLYGONID, THEDATETIME, and seven SPI aggregations (plus 3 additional placeholders depending on implementation)
- SPI values are unitless, standardized scores, and can be used for trend and anomaly analyses.
- No data value coded as -9999.

## Usage, applications, and caveats
- Intended for integration into a CEH droughts portal; supports multi-area drought analysis and policy-relevant interpretation.
- Important considerations:
  - For 12+ month accumulations, overlapping data introduces potential autocorrelation in the underlying time series.
  - Monthly SPIs derived from overlapping annual data can introduce serial correlation in concatenated series, which should be accounted for in trend analyses.
  - Although gamma distribution is widely used for SPI, some UK-specific assessments suggest other distributions (e.g., Pearson type 3, Tweedie) may be more appropriate in certain cases; future versions may explore alternatives.

## Limitations and notes
- Underlying rainfall data changes between version 1 and version 2 (Met Office 5 km grids replace CEH-GEAR), affecting the SPI calculations beyond the temporal extension.
- The accumulation-period approach and data handling choices (e.g., truncation, distribution fitting) influence extreme value representation and interpretation.

## Projects and acknowledgments
- Projects: DrIVER, Historic Droughts, IMPETUS.
- Funding: NERC and Belmont Forum initiatives; CEH and partner institutions contributed to data development and dissemination.

## References (key sources)
- McKee et al. (1993) on SPI methodology
- Stagge et al. (2015) on SPI distributions
- Svensson et al. (2015), Barker et al. (2015) on distribution fitting for UK data
- Kral et al. (2015); Tanguy et al. (2015, 2014) on IHU groups and gridded rainfall estimates
- Haynes et al./Lincoln Declaration references on drought indices
- CEH-GEAR and related Met Office data contributions