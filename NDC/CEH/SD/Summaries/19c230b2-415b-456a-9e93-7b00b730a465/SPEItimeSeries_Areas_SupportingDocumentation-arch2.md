# SPEI_IHU_HA

## Brief Description
- Time series of Standardised Precipitation-Evapotranspiration Index (SPEI) for Integrated Hydrological Units (IHU) hydrometric areas.
- SPEI calculated for accumulation periods of 1, 3, 6, 12, 18, and 24 months, each across 12 calendar months.
- Standard period for fitting the distribution: 1961–2010.
- Dataset covers 1961–2012 and is stored in CSV format.

## Motivation
- Created to be incorporated into a CEH droughts portal; enables drought analysis over specific IHU areas.
- SPEI accounts for evapotranspiration, unlike SPI, providing a measure of water surplus/deficit for each period.
- Widely used for drought monitoring and various drought-related analyses (hydrological, ecological, agricultural, climate change studies).
- Information at multiple timescales supports short- to long-term drought assessment (1–24 months; potential links to streamflows, reservoirs, groundwater).

## Data Sources
- Integrated Hydrological Units (IHU) of the UK (Kral et al., 2015).
- CEH-Gear: gridded rainfall estimates for UK (Tanguy et al., 2014; Keller et al., 2015).
- CHESS PET dataset for potential evapotranspiration (Robinson et al., 2015, in prep).

## Method for deriving SPEI grids
- SPEI computed from Climatic Water Balance (CWB) = precipitation − evapotranspiration; assigned to the month ending the accumulation period.
- For each location, six accumulation periods x twelve months yield 72 CWB time series.
- Distribution fitted to historic CWB using the generalised logistic (log-logistic) distribution; preferred over GEV for gridded data in this context.
- Parameter estimation via the SCI R package (maximum likelihood; fallback to L-moments or moments as needed).
- SPEI transformed to normal scores (mean 0, sd 1); truncated at ±5.
- Autocorrelation considerations: overlapping data for long durations and monthly concatenations introduce serial correlation; pertinent for trend analyses.
- Dataset period (1961–2012) reflects data availability; standard fitting period is 1961–2010.

## Format of the [SPEI_IHU_HA] dataset
- CSV file with 9 columns: RID, POLYGONID (IHU hydrometric area ID), THEDATETIME, and six additional columns representing different SPEI aggregations.
- SPEI values are unitless normal scores (range −5 to 5); −9999 indicates No Data.

## Acknowledgments
- Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Funded by the Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.