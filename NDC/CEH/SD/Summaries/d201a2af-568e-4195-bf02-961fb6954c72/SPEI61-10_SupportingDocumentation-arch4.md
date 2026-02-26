# Supporting Information

## Overview
- Provides 1km and 5km gridded Standardised Precipitation-Evapotranspiration Index (SPEI) data for Great Britain.
- SPEI is a drought index based on Climatic Water Balance (CWB = precipitation minus evapotranspiration) for multiple accumulation periods.
- Data are stored as NetCDF4 on the CEH-THREDDS-WATER server and cover 1961–2012 (standard period for distribution fits: 1961–2010).

## Data contents and scope
- Two spatial resolutions: 1km and 5km grids.
- Accumulation periods: 1, 3, 6, 12, 18, 24 months, with each period calculated for all 12 calendar months.
- For each grid cell, 72 time series are produced (6 durations × 12 months).
- Data are presented as normal scores (mean 0, standard deviation 1; no units) and truncated to the range -5 to +5.
- Grid structure is two-dimensional, aligned to the British National Grid; one yearly NetCDF4 file per accumulation period.

## Method and data sources
- SPEI calculation follows Vicente-Serrano et al. (2010a), using cumulative CWB values ending in each month.
- For each location, the CWB time series is fitted with a statistical distribution; the generalised logistic distribution is used (with fit via the SCI R package; MLE, fallback to L-moments or method of moments if needed).
- Transformation converts the fitted distribution to normal scores (mean 0, SD 1).
- Extreme SPEI values are truncated at ±5.
- Data sources:
  - CEH-GEAR: gridded areal rainfall estimates (monthly data for UK).
  - CHESS PET: potential evapotranspiration dataset.
- Standardisation period for fitting: 1961–2010.
- Dataset period: 1961–2012 (limited by data availability from sources).

## Data format and structure
- Format: NetCDF4, CEH gridded dataset conventions.
- Structure: yearly files, each file containing 12 monthly grids for a given accumulation period.
- Projection: British National Grid.
- Values: SPEI normal scores with no units; range restricted to -5 to +5.

## Access, discoverability, and reuse
- Hosted on the CEH-THREDDS-WATER server (URL provided in the document).
- Intended for drought monitoring, climate impact analyses, hydrological and ecological studies, and supporting decision-making in drought-related contexts.

## Temporal aspects and cautions
- Long accumulation periods (e.g., 18, 24 months) involve overlapping data, introducing autocorrelation in the underlying CWB series.
- Monthly SPEI series (constructed by concatenating months) are also likely autocorrelated due to overlapping data.
- Users should account for serial correlation in trend analyses and frequency interpretations.

## Interpretation guidance by timescale
- 1-month SPEI: reflects short-term soil moisture and crop stress.
- 3-month SPEI: short- to medium-term moisture conditions (seasonal perspective).
- 6-month SPEI: medium-term CWB trends; may relate to reservoir levels.
- 12-month SPEI: long-term CWB patterns; linked to streamflows and reservoirs.
- 18–24-month SPEI: very long-term patterns; related to groundwater conditions.

## Acknowledgments
- Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Funding: Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.

## References (contextual)
- Methodological and data-source references include Vicente-Serrano et al. (2010a, 2010b, 2011, 2012, 2013), Stagge et al. (2015), and supporting datasets and tools (CEH-GEAR, CHESS-PET, SCI package).