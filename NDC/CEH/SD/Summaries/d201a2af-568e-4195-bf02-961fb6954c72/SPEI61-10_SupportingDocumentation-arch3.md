# Supporting Information

## Overview
- Presents gridded drought indicators (SPEI) for Great Britain at 1km and 5km resolution.
- SPEI is a drought index based on Climatic Water Balance (precipitation minus evapotranspiration) over multiple accumulation periods.
- Data span from 1961 to 2012, with a standard distribution fitting period of 1961–2010.

## Dataset Description
- SPEI calculated for accumulation periods: 1, 3, 6, 12, 18, and 24 months, each for all 12 calendar months.
- For each grid cell, 72 time series values are produced (6 durations × 12 months).
- Values are transformed to normal scores (mean 0, std dev 1) with no units; range limited to [-5, 5].
- Stored in NetCDF4 format on the CEH-THREDDS-WATER server.
- Two spatial resolutions provided: 1km for fine-scale/local analyses and 5km for regional drought assessment.

## Motivation and Monitoring Context
- Developed within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) to support drought monitoring and early warning.
- SPEI integrates evapotranspiration to capture water deficit/surplus, offering multi-scale drought perspectives that complement SPI.
- Suitable for linking drought signals with hydrological, agricultural, and ecological impacts; different timescales inform short-term to long-term water balance and groundwater considerations.

## Data Sources
- CEH-GEAR: gridded areal rainfall estimates (monthly) for the UK.
- CHESS PET: potential evapotranspiration dataset for Great Britain.

## Methodology
- SPEI computation follows Vicente-Serrano et al. (2010a): use cumulative CWB over each accumulation period ending in a given month.
- For each location and duration/month, fit a statistical distribution to historic CWB accumulations using the generalised logistic distribution (log-logistic) with maximum likelihood; fallback via L-moments or method of moments if needed.
- Transform fitted distribution to normal scores (mean 0, std 1); cap extreme values at ±5.
- Note on autocorrelation: >12-month accumulation periods use overlapping data, producing serial correlation in the underlying CWB series and in monthly SPEIs; this affects independence assumptions and should be accounted for in trend analyses.
- Standard fitting period: 1961–2010; data available for 1961–2012 due to data availability of inputs.

## Data Format and Access
- NetCDF4 format, CEH gridded dataset conventions.
- Structure: two-dimensional spatial grids with twelve monthly grids per year; one yearly file per accumulation period.
- Projection: British National Grid.
- Output: SPEI normal scores (no units), range [-5, 5].
- Accessibility: stored on the CEH-THREDDS-WATER server.

## Data Quality, Limitations, and Governance
- Acknowledges data gaps and the need for metadata to verify suitability for specific requirements.
- Autocorrelation in longer accumulation periods and across overlapping time windows is inherent and influences interpretation.
- Extreme values are truncated to maintain numerical stability; users should consider tail behavior and distribution choice when applying extreme event analyses.

## Acknowledgments and Funding
- Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Funding: Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.