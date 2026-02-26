# Historic Droughts Inventory of drought references for Historic Standardised Precipitation Index time series for IHU Groups (1862-2015) - version 2

## Overview
- Provides time series of the Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) groups from 1862 to 2015.
- SPI computed for multiple accumulation periods (1, 3, 6, 9, 12, 18, 24 months) across 12 calendar months.
- Data are normalised (z-scores) with no units, truncated to the range -5 to 5.

## What the dataset contains
- Time series of SPI for each IHU group, enabling drought assessment over specific hydrometric areas.
- Dataset is stored in CSV format with 10 columns: RID, POLYGONID, THEDATETIME, and columns 4–10 containing different SPI aggregations.
- SPI values are “normal scores” (mean 0, SD 1); missing data indicated by -9999.
- Aimed to support aggregation of SPI over IHU groups for area-specific drought analysis.

## Context and Project Background
- Generated within two projects:
  - DrIVER: Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research, focusing on drought monitoring and early warning systems.
  - Historic Droughts: UK-led project (2014–2018) to understand past droughts and develop tools for managing droughts and water scarcity.
- Historic Droughts Inventory includes:
  - Hydro-meteorological timelines (rainfall, river flows, groundwater) for past drought indicators.
  - References to droughts from 19th century to present (newspaper, legislation, agricultural media, oral histories).
- Inventory designed to be a common reference for policymakers, water suppliers, agriculture, and industry to enable consistent drought planning.

## Data Sources
- IHU groups (Kral et al., 2015): UK hydrological reference units at a finer spatial scale.
- Met Office 5 km monthly rainfall grids: primary rainfall input for SPI calculation, incorporating historical digitisation and gridding efforts.
- Supplementary datasets include UKCP09-based grids and data rescued or updated during the Historic Droughts project (1862–1909, 1910–2015).

## Methodology
- SPI definition follows McKee et al. (1993): based on the cumulative probability of precipitation over a chosen accumulation period ending in a given month.
- For each location, SPI calculated for 7 accumulation periods (1, 3, 6, 9, 12, 18, 24 months) across 12 calendar months (84 time series per location).
- Gamma distribution parameters estimated with L-moments (via a modified R SCI package) to fit precipitation data; normalization yields SPI values.
- Distribution is truncated at +/- 5; 95% of values are expected within -2 to 2.
- Standard reference period to fit the distribution is 1961–2010.
- Notes on limitations:
  - Gamma distribution may fail Shapiro-Wilk tests for UK data; alternatives (Pearson Type 3, Tweedie) exist but gamma remains widely used.
  - Overlapping data for longer accumulation periods creates autocorrelation; SPIs ending in each month are not independent for longer-than-one-year accumulations.
  - Potential for autocorrelation in concatenated SPIs across months; may affect trend analyses.

## Data Format and Structure
- CSV format with 10 columns (RID, POLYGONID, THEDATETIME, plus seven SPI aggregation columns corresponding to different time scales).
- SPI values are unitless normal scores, range limited to -5 to 5; -9999 denotes No Data.

## Version History and Changes
- Version 2 differs from the earlier SPI_IHU_groups dataset (1961–2012) by:
  - Using Met Office 5 km rainfall grids instead of CEH-GEAR for the underlying rainfall data.
  - Updating monthly rainfall data for 1960–2000 based on daily grids, plus new 9-month accumulation period added.
- Standard period for distribution fitting remains 1961–2010; dataset period remains 1862–2015.
- Data are part of ongoing efforts to improve drought indicators and historical drought understanding.

## Applications and Use
- Supports drought monitoring and early warning through integration into CEH droughts portal.
- Enables aggregation of SPI over IHU hydrometric areas to study droughts for specific regions.
- Provides a standardized, multi-temporal drought index reference for policy makers, water managers, and researchers.

## Limitations and Considerations for Data Leaders
- Data heterogeneity and potential gaps in historical records; data quality depends on historical gridded rainfall inputs.
- Statistical model choice (gamma distribution) may not be optimal in all UK contexts; consider alternative distributions for future versions.
- Autocorrelation effects due to overlapping time periods; incorporate appropriate methods when performing trend or frequency analyses.
- Metadata and licensing details are not specified here; verify governance, provenance, and data access terms for institutional use.