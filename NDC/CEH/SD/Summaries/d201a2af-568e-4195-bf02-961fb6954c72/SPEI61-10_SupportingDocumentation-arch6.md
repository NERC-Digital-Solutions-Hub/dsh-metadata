# Supporting Information

- I. Brief Description of the dataset
  - 1km and 5km gridded Standardised Precipitation-Evapotranspiration Index (SPEI) data for Great Britain; drought index based on Climatic Water Balance (precipitation minus evapotranspiration) for various accumulation periods (1, 3, 6, 12, 18, 24 months) and for each of twelve calendar months.
  - Time series are likely autocorrelated due to accumulation and overlapping data; values are normalised (“normal scores”) with mean 0 and std dev 1; values truncated at +/-5.
  - Standard period used to fit the distribution: 1961–2010; dataset covers 1961–2012.
  - Data format: NetCDF4, stored on the CEH-THREDDS-WATER server.

- II. Motivation
  - Developed within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research) to assess drought indices in relation to impacts data for monitoring and early warning.
  - SPEI provides info at multiple timescales (1–24 months) and can be more broadly applicable than SPI by incorporating evapotranspiration.
  - Dual-resolution approach (1km for local analysis; 5km for regional studies) to meet different scientific and stakeholder needs.

- III.1 Data Sources
  - CEH-GEAR: 1km resolution gridded areal rainfall estimates for the UK (monthly grids used for SPEI derivation).
  - CHESS PET: Potential evapotranspiration dataset for Britain.

- III.2 Method for deriving the SPEI grids
  - SPEI computed from the cumulative probability of Climatic Water Balance (CWB) for each location and accumulation period; assignment to the month in which the accumulation ends (e.g., 6-month SPEI ending July 1998 uses Feb–Jul 1998 CWB).
  - 72 time series per location (6 durations × 12 months); distributions fitted to historic CWB accumulations using the generalised logistic distribution (log-logistic).
  - Parameter estimation via the SCI R package (maximum likelihood; fallback to L-moments or method of moments if needed); transform to normal scores (mean 0, sd 1).
  - Extreme SPEI values truncated beyond +/-5; most SPEIs lie within -2 to +2 (about 95%).
  - Note on autocorrelation: overlapping data for longer durations cause serial correlation; concatenated monthly SPEI series are also likely autocorrelated.
  - Data availability window: 1961–2012 (limited by CHESS PET and CEH-GEAR data); standard fitting period 1961–2010.

- IV. Format of the SPEI dataset
  - NetCDF4 format following CEH gridded conventions.
  - Structure: two-dimensional spatial grids for Great Britain with twelve monthly grids per yearly file; one yearly file per accumulation period.
  - Projection: British National Grid.
  - Data are SPEI normal scores (no units) in the range -5 to +5.

- V. Acknowledgments
  - Outcome of the DrIVER project; funded by the Natural Environment Research Council (NE/L010038/1) as part of the Belmont Forum initiative.
  - References provide the theoretical and methodological context for SPEI and related drought indices.