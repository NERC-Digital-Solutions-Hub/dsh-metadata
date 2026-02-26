# Supporting Information

## I. Brief Description of the dataset
- Time series of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) hydrometric areas.
- SPI calculated for accumulation periods: 1, 3, 6, 12, 18, 24 months; each period calculated for all 12 calendar months.
- Gamma distribution fitted to historic precipitation accumulations (1961-2010 standard period).
- Dataset period: 1961–2012; data stored in CSV format.

## II. Motivation
- Designed to be incorporated into a CEH droughts portal; enables aggregation of SPI over IHU hydrometric areas to study drought in defined regions.
- SPI is a widely used drought tool from McKee et al. (1993); helps assess rarity of drought or anomalously wet periods.
- Different SPI time scales provide varying insights:
  - 1-month: short-term soil moisture/crop stress.
  - 3-month: short- to mid-term moisture/seasonal precipitation.
  - 6-month: medium-term trends, potential signals in streamflow/reservoirs.
  - 12-month: long-term precipitation patterns, linked to streamflows/reservoirs.
  - 18/24-month: longer-term precipitation and groundwater signals.

## III. Data Sources
- IHU hydrometric areas (UK) as spatial reference units.
- CEH-GEAR: 1 km resolution daily/monthly areal rainfall estimates used to derive area-averaged rainfall time series for each IHU area.

### III.2 Method for deriving the SPI grids
- SPI defined as the cumulative probability of precipitation for a given accumulation period; values are transformed to normal scores (mean 0, sd 1).
- For each IHU area, compute SPI for 1, 3, 6, 12, 18, 24 months across all 12 months -> 72 time series per area.
- Distribution fitting: gamma distribution estimated with L-moments (preferred over maximum likelihood in some cases); parameters implemented via a modified R SCI package.
- SPI truncation: values limited to -5 to +5.
- About 95% of SPI values fall within -2 to +2; about 68% within -1 to +1.
- Note on distributions: while gamma is common and recommended, UK-specific work shows gamma may fail normality tests for some cases; alternatives (e.g., Pearson type 3, Tweedie) exist and may be used in future versions.
- Autocorrelation considerations:
  - For >12-month SPI, underlying annual series overlap, creating potential autocorrelation.
  - Concatenated monthly SPIs can be highly autocorrelated; account for serial correlation in trend analyses.
- Temporal scope:
  - Distribution fitting uses 1961–2010; SPI series cover 1961–2012 due to data availability variations.

## IV. Format of the dataset
- File type: CSV.
- Columns: 9 total.
  - RID: row identifier.
  - POLYGONID: IHU hydrometric area ID (use for joins with shapefiles).
  - THEDATETIME: date/time stamp.
  - Columns 4–9: different SPI aggregations (the six accumulation-period SPI values for each month).
- Data values: SPI normal scores (mean 0, sd 1), unitless; range restricted to -5 to +5.
- No data value encoded as -9999.

## Additional context and cautions
- The 1961–2010 period is the standard fit window due to sparse early raingauge data; the actual dataset extends to 2012.
- Users should be aware of potential data access and reproducibility considerations:
  - Data sources include IHU definitions and CEH-GEAR rainfall estimates.
  - Some methodological choices (gamma distribution, L-moments) are justified but have alternatives noted for future work.
  - Serial correlation and overlapping data may affect certain statistical analyses (e.g., trend testing).