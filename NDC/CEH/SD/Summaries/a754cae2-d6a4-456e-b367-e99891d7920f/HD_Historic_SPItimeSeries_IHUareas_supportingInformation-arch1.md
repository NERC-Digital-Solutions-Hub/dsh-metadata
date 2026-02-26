# Historic Droughts Inventory of drought references for Historic Standardised Precipitation Index time series for IHU hydrometric areas (1862-2015) - version 2

- This document describes a time series dataset of the Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) hydrometric areas in the UK, spanning 1862–2015.
- SPI is calculated for multiple accumulation periods (1, 3, 6, 9, 12, 18, 24 months) and for each of the twelve calendar months, resulting in 84 time series per location.

- Purpose and context
  - Produced as part of the DrIVER project and the Historic Droughts project to advance drought research and support decision-making.
  - Aims to facilitate drought monitoring, historical drought analysis, and跨-sector understanding for policy makers, water suppliers, and researchers.
  - Supports inclusion in the CEH droughts portal and enables study of drought over specific areas of interest by aggregating SPI across IHU hydrometric areas.

- Data content and format
  - Data are stored as normal scores (SPI) with mean 0 and standard deviation 1, unitless, truncated to -5 to +5.
  - File format: CSV with 10 columns:
    - RID (row identifier)
    - POLYGONID (IHU hydrometric area ID)
    - THEDATETIME (date/time)
    - SPI columns for each accumulation period (7 columns corresponding to 1, 3, 6, 9, 12, 18, 24 months across all months)
    - No-data value coded as -9999

- Methodology
  - SPI calculation follows McKee et al. (1993): use cumulative precipitation for each accumulation period ending in a given month, for each location.
  - Data series (84 per location) are fitted with a gamma distribution using L-moments (instead of MLE) to estimate parameters.
  - Transformation to a standard normal distribution yields the SPI values.
  - Serial considerations: overlapping data for longer accumulation periods introduces autocorrelation; SPIs for consecutive months may also be autocorrelated if concatenated, which should be accounted for in trend analyses.
  - Truncation of extreme values to maintain numerical stability; most SPIs fall within -2 to +2.

- Data sources and underlying rainfall data
  - IHU hydrometric areas (UK reference units)
  - Met Office 5 km monthly rainfall grids
  - Historical and rescue data from Met Office for 1862–1909
  - UKCP09-derived data for 1910–1959 and 2001–2011
  - Unpublished Met Office updates (2012–2015)
  - Methodological notes indicate improvements over previous versions (see below)

- Version 2 specifics (versus previous SPI_IHU_HA dataset)
  - Underlying rainfall data changed: from CEH-GEAR to Met Office 5 km rainfall grids.
  - New monthly rainfall grids for 1960–2000 derived from daily Met Office grids; improved data quality for that period.
  - Accumulation period extended to 9 months (in addition to 1, 3, 6, 12, 18, 24 months).

- Temporal and spatial coverage
  - Temporal extent: 1862–2015
  - Spatial unit: IHU hydrometric areas (coarsest IHU spatial resolution)

- Data provenance and acknowledgements
  - Joint effort from DrIVER, Historic Droughts, and IMPETUS projects
  - Funding and project details acknowledged, with related publications and data centre references provided

- References and context for use
  - SPI is a widely used drought index recommended for meteorological drought monitoring
  - The dataset supports multi-temporal analysis of drought and wet periods at regional hydrological scales
  - Caveats noted regarding distribution choice (gamma), potential need for alternative distributions in future versions, and independence assumptions for long accumulation periods

- Access and usability
  - Data designed for integration with drought portals and GIS workflows
  - Structured to enable joining time series to IHU shapefiles via POLYGONID
  - Emphasizes traceability of data sources and potential for discoverability of datasets through metadata and portals