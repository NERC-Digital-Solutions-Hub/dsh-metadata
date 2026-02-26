# Standardised Precipitation Index time series for IHU Groups (1961-2012)

## I. Brief Description of the dataset
- Time series of Standardised Precipitation Index (SPI) for Integrated Hydrological Unit (IHU) groups in the UK.
- SPI calculated for accumulation periods: 1, 3, 6, 12, 18, 24 months, each for all 12 calendar months.
- Distribution fitted: gamma distribution (1961-2010 period used to fit parameters; L-moments for parameter estimation; R package SCI with L-moments).
- Data span: 1961–2012; stored in CSV format; 72 time series per IHU group (6 durations × 12 months).
- SPI values are normal scores (mean 0, stdev 1), truncated to [-5, +5]; no units; -9999 indicates No Data.
- Data can be used for drought and wet-period analysis, with awareness of overlapping-year data causing autocorrelation for longer accumulation periods.

## II. Motivation
- Developed for the CEH droughts portal to enable area-specific drought analysis by aggregating SPI over IHU groups.
- SPI widely used for drought monitoring; endorsed by WMO.
- Time-scale interpretation ranges from short-term (1-month) to long-term (24-month) and relates to soil moisture, seasonal trends, streamflow, reservoirs, and groundwater.

## III.1 Data Sources
- IHU groups (Kral et al. 2015): UK hydrological reference units; groups ~400 km2; naming based on major rivers and counties.
- CEH-GEAR: 1 km resolution daily/monthly areal rainfall estimates used to derive area-averaged rainfall for each IHU group.

## III.2 Method for deriving the SPI grids
- SPI computation follows McKee et al. (1993): precipitation totals are transformed to a gamma distribution; the accumulation period ending month receives the corresponding SPI value.
- 72 time series per IHU group (6 durations × 12 months); parameters estimated via L-moments; distribution fitted using gamma (despite some evidence for alternative distributions).
- Transformation to normal scores yields unitless SPIs; values truncated at ±5; typical range is within -2 to +2 (95% within this range).
- Potential limitations:
  - Autocorrelation from overlapping data for periods >12 months.
  - Serial correlation in concatenated monthly SPIs; use trend analyses with caution.
  - Gamma distribution may not always be the best fit; alternatives like Pearson type 3 or Tweedie suggested by some studies.
- Standard fitting period: 1961–2010; data cover 1961–2012 due to data availability and network density considerations.

## IV. Format of the dataset
- File format: CSV.
- Columns: RID, POLYGONID (IHU group ID for joining with shapefiles), THEDATETIME, plus six SPI aggregations (columns 4–9).
- SPI values are unitless normal scores (mean 0, sd 1); range limited to [-5, +5].
- No Data encoded as -9999.
- POLYGONID recommended for joining with IHU group polygons.

## References (key sources)
- CEH-GEAR, IHU groups, SPI methodology (Kral et al. 2015; Tanguy et al. 2014; Keller et al. 2015).
- McKee et al. (1993) for SPI definition; Stagge et al. (2015) on distributions; Svensson et al. (2015) on distribution considerations.
- R package SCI (Gudmundsson & Stagge, 2014) with L-moments adaptation.