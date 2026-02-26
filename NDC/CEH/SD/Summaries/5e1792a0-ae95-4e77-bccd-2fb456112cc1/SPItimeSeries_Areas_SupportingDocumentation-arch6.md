# Supporting Information

## I. Brief Description of the dataset
- Time series of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) hydrometric areas.
- SPI is a drought index based on precipitation probability for various accumulation periods (1, 3, 6, 12, 18, 24 months), each computed for all 12 calendar months.
- Fitted gamma distribution over a standard period (1961-2010) using L-moments; dataset covers 1961-2012.
- Data stored in CSV format.

## II. Motivation
- Derived to be incorporated into a CEH droughts portal; aggregation of SPI over IHU areas enables area-specific drought analysis.
- SPI helps define and monitor drought by assessing rarity of precipitation deficits/excess over chosen time scales.
- SPI time scales provide different insights:
  - 1-month: short-term moisture and crop stress.
  - 3-month: short- to medium-term moisture, seasonal precipitation.
  - 6-month: medium-term trends, potential ties to streamflows/reservoirs.
  - 12-month: long-term precipitation patterns linked to streamflows/reservoirs.
  - 18/24-month: even longer-term patterns, related to groundwater.

## III.1 Data Sources
- IHU hydrometric areas (UK) as spatial units.
- CEH-GEAR: 1 km resolution daily/monthly areal rainfall estimates used to derive area-averaged rainfall for each IHU area, feeding SPI calculation.

## III.2 Method for deriving the SPI grids
- SPI calculated as the cumulative probability of precipitation for a given accumulation period, assigned to the month in which that period ends (e.g., 6-month SPI for July 1998 covers Feb–Jul 1998).
- For each IHU area, SPI computed for six durations (1, 3, 6, 12, 18, 24 months) and 12 months, yielding 72 time series per IHU area.
- Gamma distribution fitted to each time series; L-moments used to estimate parameters (instead of maximum likelihood) due to occasional poor fits.
- SPI transformation to a normal distribution (mean 0, std dev 1); SPIs are dimensionless, truncated at ±5.
- About 95% of SPIs fall within -2 to 2; ~68% within -1 to 1.
- Note: gamma distribution, while common, may not be optimal for UK data; alternative distributions (e.g., Pearson type 3, Tweedie) may be explored in future versions.
- Accumulation periods >12 months involve overlapping annual data, causing potential autocorrelation; care needed for independence assumptions in frequency analyses.
- Serial correlation considerations: concatenated SPIs across months are likely autocorrelated due to overlapping data; trend analyses should account for this.
- Standard period to fit distribution: 1961–2010; data coverage: 1961–2012 (pre-1961 data uncertain due to sparser raingauge network).

## IV. Format of the dataset
- CSV file containing SPI time series for IHU hydrometric areas (1961–2012).
- Columns:
  - RID: row identifier
  - POLYGONID: IHU hydrometric area ID (for joining with shapefiles)
  - THEDATETIME: date and time
  - Columns 4–9: different temporal aggregations of SPI
- SPI values are normal scores from a standard normal distribution (mean 0, sd 1), no units.
- Range: -5 to +5; -9999 denotes No Data.

## References
- Barker, L.J., et al. (2015); UK drought indicators
- Gudmundsson, L. & Stagge, J. H. (2014); SCI R package
- Hayes, M. et al. (2011); Lincoln Declaration on Drought Indices
- Keller, V. D. J., et al. (2015); CEH-GEAR dataset
- Kral, F., et al. (2015); Integrated Hydrological Units
- McKee, T. B., et al. (1993); SPI methodology
- National Drought Mitigation Center (2015); SPI interpretation
- Stagge, J. H., et al. (2015); candidate distributions for drought indices
- Svensson, C., et al. (2015); ongoing work
- Tanguy, M., et al. (2014, 2015); CEH-GEAR and related methods