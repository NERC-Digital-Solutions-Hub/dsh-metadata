# Supporting Information

- Overview: This dataset provides time series of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) groups, covering 1862–2015. It aggregates SPI over multiple accumulation periods (1, 3, 6, 12, 18, 24 months) for each of the twelve calendar months, resulting in 72 series per location. The underlying rainfall data were updated from CEH-GEAR to Met Office 5 km rainfall grids.

- Data purpose and context: Derived to support the CEH droughts portal. SPI helps define and monitor drought by indicating the rarity of precipitation deficits or wet spells across timescales, aiding users in assessing short- to long-term moisture conditions and their implications for hydrology and water resources.

- Data sources and provenance:
  - IHU groups (Kral et al., 2015) as the spatial framework.
  - Met Office 5 km monthly rainfall gridded data, incorporating UKCP09 data (1910–2011) and updated data (2012–2015), plus historic rainfall data (1862–1909) digitised for Historic Droughts.
  - The standard period used to fit the gamma distribution is 1961–2010.

- SPI calculation methodology:
  - SPI computed as per McKee et al. (1993) using the cumulative precipitation for each accumulation period ending in a given month.
  - For each location and duration, a gamma distribution is fitted (L-moments estimation) and transformed to a standard normal distribution (mean 0, sd 1).
  - Calculation implemented in an R package (SCI) with L-moments-based parameter estimation; data truncated at ±5 to avoid extreme values.
  - Note: gamma distribution, while widely used, may not always be the best fit for UK data; alternative distributions (e.g., Pearson III, Tweedie) are acknowledged, and future versions may explore them. Accumulations >12 months use overlapping data, introducing potential autocorrelation; SPIs are not independent across time.

- Data format and structure:
  - Stored as CSV with 9 columns:
    - RID (row identifier)
    - POLYGONID (IHU group ID; join key for shapefiles)
    - THEDATETIME (date)
    - Columns 4–9: SPI aggregations for the six durations across twelve months
  - SPI values are normal scores from a standard normal distribution (mean 0, sd 1), range constrained to [-5, 5]; -9999 denotes No Data.

- Interpretation and usage notes:
  - 1-month SPI: short-term moisture and soil/crop stress context.
  - 3-month SPI: short- to medium-term moisture and seasonal context.
  - 6-month SPI: medium-term trends; potential links to streamflows and reservoirs.
  - 12-month SPI: longer-term precipitation patterns; links to streamflows and reservoirs.
  - 18–24-month SPI: very long-term precipitation patterns; potential relevance to groundwater.
  - SPIs ending in a given month reflect the period ending that month; users should be aware of autocorrelation in longer periods due to overlapping data.

- Data quality, limitations, and caveats:
  - Serial correlation due to overlapping data for longer accumulation periods; affects frequency analysis assumptions.
  - Gamma distribution fit may not be optimal for all UK cases; future versions may use alternative distributions.
  - Daily/monthly aggregation and construction methods can introduce autocorrelation in trend analyses; appropriate statistical adjustments may be needed.

- Data access and integration:
  - Data can be connected to IHU group shapefiles via POLYGONID.
  - Designed to support drought monitoring and analysis within drought portals and related workflows.

- Versioning, updates, and provenance notes:
  - This release uses Met Office rainfall data, replacing CEH-GEAR as the underlying rainfall source.
  - Standard fit period for distribution is 1961–2010; historical data extend back to 1862 (via Historic Droughts digitisation).
  - Potential for future versions with alternative distributions or updated data sources if justified.

- Acknowledgments and references:
  - Collaborative outcome from DrIVER, Historic Droughts, and IMPETUS projects.
  - References include key works on SPI methodology, drought indices, and the datasets used for UK hydrological applications.