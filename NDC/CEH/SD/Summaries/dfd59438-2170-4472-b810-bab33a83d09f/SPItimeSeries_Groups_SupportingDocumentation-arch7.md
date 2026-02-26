# The Standardised Precipitation Index time series for IHU Groups (1961-2012) dataset

## Overview
- Time series of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) Groups.
- Covers 1961–2012; data stored as CSV.
- For each IHU group, 72 SPI time series are produced (6 accumulation periods × 12 calendar months).

## Purpose and use
- Created to support incorporation into a CEH droughts portal and to enable drought analysis within specific areas of interest.
- SPI provides a standardized measure of precipitation anomalies, useful for monitoring meteorological droughts and identifying unusually wet periods.
- Different accumulation periods yield information on short-, medium-, and long-term moisture and related impacts (soil moisture, crops, streamflows, reservoirs).

## Data scope and structure
- Accumulation periods: 1, 3, 6, 12, 18, 24 months; calculated for each of the 12 calendar months.
- Resulting in 72 time series per IHU group.
- Data units: SPI as normal scores (mean 0, standard deviation 1); no physical units.
- Value range: limited to -5 to +5; -9999 indicates No Data.
- Spatial units: IHU Groups (average ~400 km²); POLYGONID used for joining to IHU shapefiles.

## Data sources
- IHU Groups (Kral et al., 2015) as the spatial reference units.
- CEH-GEAR: 1 km daily/monthly areal rainfall estimates used to derive area-averaged rainfall time series for each IHU group.

## Methodology
- SPI calculation follows McKee et al. (1993): based on cumulative precipitation totals for each accumulation period.
- Gamma distribution fitted to historic accumulation time series; parameters estimated with L-moments (via modified SCI R package) to improve robustness where maximum likelihood fails.
- Transformation to a normal distribution yields SPI values (normal scores).
- Note: Although gamma is widely used, some studies suggest other distributions (e.g., Pearson type III, Tweedie) may be more appropriate for the UK; future versions may use alternative distributions.
- For accumulation periods > 12 months, overlapping data cause autocorrelation in the series. Serial correlation may affect frequency analyses; concatenated monthly SPIs can be strongly autocorrelated.

## Temporal and data period details
- Distribution fitting period: 1961–2010.
- SPI dataset period: 1961–2012.
- CEH-GEAR rainfall data used extends back to 1890–2012, but SPI starts in 1961 due to sparser pre-1961 observations and higher uncertainty.

## Data format and content (CSV)
- Columns:
  - RID: row identifier
  - POLYGONID: IHU group ID (join key for shapefile integration)
  - THEDATETIME: date and time
  - Columns 4–9: SPI values for the six accumulation periods across the twelve months
- SPI values are unitless normal scores; range limited to -5 to +5.
- -9999 denotes No Data.

## GIS considerations and workflow
- Data are joinable to IHU shapefiles via POLYGONID, enabling map-based visualizations of drought conditions by group and time.
- Suitable for map-based data products and dashboards in a drought portal, with attention to temporal autocorrelation in analyses.

## Quality notes and caveats
- Potential autocorrelation due to overlapping accumulation periods, especially for longer durations.
- Serial correlation in concatenated monthly SPIs; adjust methods when performing trend analyses.
- Data gaps and resolution considerations; while CEH-GEAR provides high-resolution rainfall data, pre-1961 data are sparser, influencing reliability prior to 1961.

## References
- Barker et al. (2015); Gudmundsson & Stagge (2014); Hayes et al. (2011); Keller et al. (2015); Kral et al. (2015); McKee et al. (1993); Stagge et al. (2015); Svensson et al. (2015); Tanguy et al. (2014, 2015).