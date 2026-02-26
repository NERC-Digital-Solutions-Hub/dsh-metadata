# Supporting Information

## I. Brief Description of the dataset
- Time series of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) hydrometric areas.
- SPI calculated for accumulation periods: 1, 3, 6, 12, 18, 24 months; computed for each of the 12 calendar months.
- The standard gamma distribution fit uses the period 1961-2010; dataset covers 1961-2012.
- Data stored in CSV format.

## II. Motivation
- Designed to be incorporated into a CEH droughts portal; aggregating SPI over IHU hydrometric areas enables drought analysis for specific areas.
- SPI is a widely used drought index (monitors meteorological drought; useful for assessing rarity of droughts or periods of anomalously wet events).
- Interpreting SPI at multiple accumulation periods provides varying insights:
  - 1-month SPI: short-term moisture and soil/crop stress.
  - 3-month SPI: short- to medium-term moisture, seasonal precipitation.
  - 6-month SPI: medium-term trends, potential link to streamflows/reservoirs.
  - 12-month SPI: long-term precipitation patterns, linked to streams/reservoirs.
  - 18- and 24-month SPI: very long-term precipitation patterns, related to groundwater.

## III.1 Data Sources
- IHU hydrometric areas (UK) as spatial units.
- CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates used to derive area-averaged rainfall time series for each IHU area.

## III.2 Method for deriving the SPI grids
- SPI is computed from the cumulative precipitation over each accumulation period ending in a given month.
- For each IHU Hydrometric Area, SPI is calculated for 6 durations (1, 3, 6, 12, 18, 24 months) across 12 calendar months -> 72 time series per area.
- Distribution fitting: gamma distribution estimated with L-moments (instead of maximum likelihood) due to robustness; parameters estimated via an adapted R SCI package.
- SPI values transformed to a standard normal distribution (mean 0, sd 1); results are unitless “normal scores.”
- Truncation applied: SPI values capped at -5 and +5.
- Data range and interpretation: about 95% of SPIs fall within -2 to +2; ~68% within -1 to +1.
- Noted caveats:
  - Gamma distribution may not be optimal for the UK in all cases; other distributions (e.g., Pearson type 3, Tweedie) could be more appropriate in future versions.
  - For durations >12 months, overlapping data introduce autocorrelation; SPIs for longer durations use overlapping annual series.
  - Serial correlation may affect trend analyses; account for autocorrelation as needed.
- Standard fitting period: 1961-2010; SPI data cover 1961-2012 (sparser pre-1961 rainfall data).

## IV. Format of the dataset
- File format: CSV.
- Columns (9 total):
  - RID: row identifier.
  - POLYGONID: IHU hydrometric area ID (useful for joining to shapefiles).
  - THEDATETIME: date and time (month-end for each accumulation period).
  - SPI 1, SPI 3, SPI 6, SPI 12, SPI 18, SPI 24: the six temporal aggregations of SPI (columns 4–9).
- SPI values are normal scores (mean 0, sd 1), unitsless; range restricted to -5 to +5.
- No Data value encoded as -9999.

References
- Includes methodological notes and data sources (Kral et al. 2015; Tanguy et al. 2014/2015; Svensson et al. 2015; Barker et al. 2015).