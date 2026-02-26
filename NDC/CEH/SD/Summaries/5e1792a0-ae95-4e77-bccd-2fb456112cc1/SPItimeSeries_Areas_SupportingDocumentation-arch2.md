# Supporting Information

## I. Brief Description of the dataset
- Time series of Standardised Precipitation Index (SPI) for the Integrated Hydrological Units (IHU) hydrometric areas (IHU approach by Kral et al., 2015).
- SPI is a drought index based on the probability of precipitation for various accumulation periods (1, 3, 6, 12, 18, 24 months) and is calculated for each of the twelve calendar months.
- Gamma distribution fitted over the 1961-2010 standard period; SPI data cover 1961-2012.
- Data stored in CSV format.

## II. Motivation
- Created to be incorporated into a CEH droughts portal; enables aggregation of SPI over IHU hydrometric areas to study drought within specific regions.
- SPI is a widely used drought-monitoring tool; identifies drought rarity at chosen time scales and can indicate anomalously wet periods (as endorsed by the WMO).
- Interpretation by accumulation period:
  - 1-month SPI: short-term, relates to soil moisture and crop stress.
  - 3-month SPI: short/medium-term moisture conditions and seasonal precipitation.
  - 6-month SPI: medium-term trends, potential links to streamflow and reservoirs.
  - 12-month SPI: long-term precipitation patterns, linked to streamflows and reservoirs.
  - 18- and 24-month SPI: longer-term patterns, associated with groundwater levels.

## III. Data Sources
### III.1 Data Sources
- IHU hydrometric areas (UK) as the primary spatial framework (Kral et al., 2015).
- CEH-GEAR: 1 km resolution daily and monthly areal rainfall estimates for the UK (Tanguy et al., 2014; Keller et al., 2015).
- CEH-GEAR monthly rainfall grids used to derive area-averaged rainfall time series for each IHU, which feed the SPI calculation.

### III.2 Method for deriving the SPI grids
- SPI definition per McKee et al. (1993): based on cumulative probability of precipitation for a given accumulation period; assignment to the month ending that accumulation.
- For each IHU, SPI calculated for 1, 3, 6, 12, 18, 24 months across all 12 calendar months (72 time series per area).
- Distribution fitting: gamma distribution fitted to historic precipitation accumulations; L-moments used to estimate parameters (to improve robustness where MLE fails).
- SPI computation uses a transformation to a standard normal distribution (mean 0, sd 1); resulting SPIs are unitless normal scores, truncated to ±5.
- Note on distribution choice: gamma widely used and endorsed for Europe, but UK-specific studies suggest other distributions (e.g., Pearson III, Tweedie) may be more suitable; gamma remains the current approach with potential future updates.
- Serial correlation considerations: overlapping data in longer accumulation periods causes autocorrelation; concatenated monthly SPIs from consecutive months are also likely autocorrelated—impactful for trend analyses.
- Standard fitting period: 1961-2010; SPI dataset covers 1961-2012. CEH-GEAR rainfall data cover 1890-2012; SPI starts at 1961 due to sparser pre-1961 rainfall network.

## IV. Format of the dataset
- CSV file containing SPI time series for IHU hydrometric areas (1961-2012).
- Columns: RID (row identifier), POLYGONID (IHU area ID for joins with shapefiles), THEDATETIME (date/time), and sixteen? (actually six) columns corresponding to the different temporal aggregations of SPI (1, 3, 6, 12, 18, 24 months across 12 months).
- SPI values are normal scores with mean 0 and sd 1, unitsless; range limited to -5 to +5.
- No Data coded as -9999.
- The dataset supports joining to spatial units via POLYGONID.