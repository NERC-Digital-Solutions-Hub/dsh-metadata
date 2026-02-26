# Supporting Information

## Dataset overview
- Contains 1 km and 5 km gridded Standardised Precipitation-Evapotranspiration Index (SPEI) data for Great Britain.
- SPEI is a drought index based on Climatic Water Balance (precipitation minus evapotranspiration).
- Calculated for accumulation periods of 1, 3, 6, 12, 18, and 24 months, with a value computed for each of the twelve calendar months.
- Time series are likely autocorrelated due to the accumulation and standardisation process.
- Standardisation period used for fitting is 1961–2010; dataset covers 1961–2012.

## Format and storage
- Data stored in NetCDF4 format following CEH gridded dataset conventions.
- Structure: two-dimensional spatial grids covering Great Britain; twelve monthly grids per year; one yearly file per accumulation period.
- Projection: British National Grid.
- SPEI values are normal scores from a standard normal distribution (mean 0, sd 1), without units; truncated at ±5.
- Held on the CEH-THREDDS-WATER server.

## Data provenance and sources
- Data sources:
  - CEH-GEAR: gridded daily/monthly areal rainfall estimates for the UK.
  - CHESS PET: potential evapotranspiration dataset for Great Britain.
- Timeframe: data derived for 1961–2012; standardisation period 1961–2010.

## Derivation methodology
- SPEI defined as the cumulative Climatic Water Balance (CWB) over the specified accumulation period ending in a given month.
- For each grid cell, 72 SPEI time series are produced (6 durations × 12 months).
- For each time series, a statistical distribution is fitted to historic CWB accumulations using the generalised logistic (log-logistic) distribution.
- Parameter estimation via the SCI R package (maximum likelihood; fallback to L-moments; if needed, method of moments).
- Transformations convert the fitted distribution to normal scores (mean 0, sd 1).
- Outliers are truncated: |SPEI| > 5 set to ±5.
- Noted issues:
  - For durations > 12 months, data involve overlapping periods, introducing autocorrelation.
  - Concatenated monthly SPEIs can also be autocorrelated; use appropriate methods for trend analysis.

## Temporal and spatial characteristics
- Two resolutions available: 1 km (finer, local analyses) and 5 km (regional analyses; smaller files, faster loading).
- Spatial coverage: Great Britain.
- Temporal coverage: 1961–2012, with standard period 1961–2010 for distribution fitting.

## Data governance and stewardship considerations
- Data are hosted on CEH-managed infrastructure (CEH-THREDDS-WATER) with documentation following CEH conventions.
- Clear metadata, provenance, and processing notes are provided to support reuse and governance.

## Limitations and cautions for users
- Serial correlation due to overlapping data affects independence assumptions in frequency analysis.
- Autocorrelation considerations are important for trend analysis and interpretation of SPEI time series.
- Extreme SPEI values are more robustly represented with the chosen generalised logistic fit; extreme tails are sensitive to distribution choice.

## Acknowledgments and funding
- Result of the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Funding: Natural Environment Research Council (award NE/L010038/1) as part of Belmont Forum initiative.

## References (key)
- Vicente-Serrano et al. (2010a) on SPEI methodology.
- Stagge et al. (2015) on candidate distributions for climatological drought indices.
- Hosking & Wallis (1997) on regional frequency analysis (L-moments).
- CEH-GEAR and CHESS PET data sources.