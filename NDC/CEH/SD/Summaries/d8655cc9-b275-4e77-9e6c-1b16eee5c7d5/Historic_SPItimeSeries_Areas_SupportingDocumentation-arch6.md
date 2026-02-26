# Supporting Information

## I. Brief Description of the dataset
- Time series of Standardised Precipitation Index (SPI) for the Integrated Hydrological Units (IHU) hydrometric areas.
- SPI calculated for accumulation periods: 1, 3, 6, 12, 18, and 24 months, each for the twelve calendar months.
- Standard fitting period: 1961–2010; dataset covers 1862–2015.
- Data format: CSV.
- SPI values are normal scores (mean 0, standard deviation 1), unitless; values range effectively within -5 to +5; -9999 denotes No Data.

## II. Motivation
- Developed to be incorporated into the CEH droughts portal by aggregating SPI over IHU hydrometric areas, enabling drought analysis for specific regions.
- SPI is a widely used drought indicator, enabling assessment of drought rarity or unusually wet periods at various time scales, and is recommended by drought-related authorities (e.g., WMO).

## III.1 Data Sources
- IHU hydrometric areas (Kral et al., 2015) as the geographical reference units.
- Met Office 5 km monthly rainfall gridded data:
  - UKCP09 data (1910–2011)
  - Unpublished updates (2012–2015)
  - Historic Droughts project data (1862–1909)
- Historic digitisation and gridding of rainfall and temperature data to enable long historical spans.

## III.2 Method for deriving the SPI grids
- SPI computed as defined by McKee et al. (1993) from cumulative precipitation for each accumulation period.
- For each location (grid cell), 72 time series are produced (6 durations × 12 months).
- For each time series, a gamma distribution is fitted using L-moments to estimate parameters (via the R SCI package, modified to use L-moments).
- SPI is transformed to a normal distribution with mean 0 and SD 1 (normal scores). Values are truncated at -5 and +5.
- Although gamma is widely used, notes acknowledge potential inadequacy for UK data; alternatives (e.g., Pearson type 3, Tweedie) could be considered in future.
- For accumulation periods >12 months, the underlying annual series overlap, creating potential autocorrelation; this should be accounted for in trend analyses.
- The standard fitting period remains 1961–2010.

## IV. Format of the [SPI_IHU_HA] dataset
- Stored in CSV format with 9 columns:
  - RID (row identifier)
  - POLYGONID (IHU hydrometric area ID)
  - THEDATETIME (date/time)
  - Columns 4–9: six SPI aggregations (one per accumulation period)
- SPI values are unitless normal scores (mean 0, SD 1), limited to [-5, 5]; -9999 indicates No Data.

## V. Acknowledgments
- Joint outcome from the DrIVER, Historic Droughts, and IMPETUS projects:
  - DrIVER: NE/L010038/1
  - Historic Droughts: NE/L01016X/1
  - IMPETUS: NE/L010267/1

## References
- Barker et al. (2015)
- Gudmundsson & Stagge (2014)
- Hayes et al. (2011)
- Keller et al. (2015)
- Kral et al. (2015)
- McKee et al. (1993)
- National Drought Mitigation Center (2015)
- Stagge et al. (2015)
- Tanguy et al. (2015)
- Tanguy et al. (2014)