# Supporting Information

## I. Brief Description of the dataset
- 1 km and 5 km gridded Standardised Precipitation-Evapotranspiration Index (SPEI) data for Great Britain.
- SPEI is a drought index based on Climatic Water Balance (CWB = precipitation − evapotranspiration) over defined accumulation periods.
- SPEI calculated for accumulation periods: 1, 3, 6, 12, 18, 24 months; each period is computed for all 12 calendar months.
- Time series are autocorrelated due to the accumulation periods and the standardisation process.
- Standard period used to fit distributions: 1961–2010; dataset covers 1961–2012.
- Data format: NetCDF4, stored on the CEH-THREDDS-WATER server.
- Projections: British National Grid; values are unitless “normal scores” with mean 0 and stdev 1; range limited to −5 to 5.

## II. Motivation
- Produced within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) to assess drought indices alongside impacts data for monitoring and early warning.
- SPEI accounts for evapotranspiration, unlike SPI, enabling assessment of water deficit/surplus across multiple time scales.
- Useful for various drought-related analyses (short-, mid-, and long-term moisture conditions) and for integration into map-based GIS products.
- Two spatial resolutions (1 km and 5 km) meet different GIS needs: 1 km for local/site analyses; 5 km for regional studies and faster data handling.
- SPEI has been broadly applied in drought monitoring and related hydrological, ecological, and agricultural contexts.

## III. Data Sources
- CEH-GEAR: Gridded daily/monthly areal rainfall estimates for the UK.
- CHESS PET: Potential evapotranspiration dataset for Great Britain (1961–2012).

## IV. Method for deriving the SPEI grids
- SPEI computed as the cumulative distribution of CWB for each accumulation period, assigned to the month ending that period (e.g., 6-month SPEI ending July 1998 uses Feb–Jul 1998 CWB).
- For each grid cell and each duration (1, 3, 6, 12, 18, 24 months) and each month, 72 time series are produced.
- Distributions fitted to CWB series using the generalised logistic distribution (log-logistic). Debate around using GEV; delayed by Vicente-Serrano & Beguería (2015) due to tail behavior and fitting performance.
- Parameter estimation via the SCI R package (maximum likelihood; fallback to L-moments or method of moments if needed).
- SPEI values are transformed to standard normal scores (mean 0, sd 1); unitsless.
- Extreme values (|SPEI| > 5) truncated to ±5.
- For accumulation periods > 12 months, series are based on overlapping data, inducing autocorrelation.
- When constructing concatenated monthly SPEI series for trend analyses, account for serial correlation.
- Standard reference period for fitting: 1961–2010; data period: 1961–2012 (to align with CHESS PET and CEH-GEAR data).

## V. Format of the SPEI dataset
- Stored in NetCDF4 format, following CEH gridded dataset conventions.
- Structure: two-dimensional spatial grids covering Great Britain; 12 monthly grids per yearly file; one yearly file per accumulation period.
- Projection: British National Grid.
- Values: normal scores with mean 0 and sd 1; range −5 to 5.
- Access: CEH-THREDDS-WATER server (URL provided in the document).

## VI. Acknowledgments
- Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Funding: Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.