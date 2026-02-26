# 5km gridded Standardised Precipitation Index (SPI) data for the United Kingdom

## I. Brief Description of the dataset
- 5km gridded SPI data for the United Kingdom, a drought index based on the probability of precipitation for a given accumulation period.
- SPI calculated for accumulation periods: 1, 3, 6, 9, 12, 18, 24 months; each period calculated for all 12 calendar months.
- Standard gamma distribution fitted over 1961-2010; covers 1862-2015; stored in NetCDF4 format.
- Data are on the British National Grid and represent SPI normal scores (mean 0, sd 1) with no units, truncated to the range -5 to +5.
- Version notes:
  - Version 2 uses Met Office 5km rainfall grids (including historic data) rather than CEH-GEAR, with monthly data from 1960-2000 updated 2012-2015; includes a 9-month accumulation added in this version.
  - This dataset differs from the earlier SPIgamma61-10 dataset primarily in the underlying rainfall data and temporal/spatial extent.

## II. Motivation
- Derived under the Historic droughts project to understand past UK droughts and develop tools for future drought management.
- SPI is widely used to define and monitor meteorological drought and to quantify drought rarity or detect unusually wet periods.
- Gridded SPI enables spatial analysis, tracking drought propagation, and identifying heavily affected areas.
- The multiple accumulation periods provide different insights:
  - 1-month SPI relates to short-term soil moisture and crop stress.
  - 3-month SPI captures short- to medium-term moisture conditions.
  - 6–9 month SPI indicates medium-term trends and may relate to flows and reservoirs.
  - 12-month SPI reflects long-term precipitation patterns tied to streams and reservoirs.
  - 18–24 month SPI reflects even longer-term patterns and groundwater considerations.

## III.1 Data Sources
- Met Office 5km monthly rainfall gridded data, combining:
  - UKCP09 data (1910-1959; 2001-2011)
  - Monthly rainfall grids from Met Office daily grids (1960-2000)
  - Unpublished Met Office updates (2012-2015)
  - Historic Droughts project rescues (1862-1909)

## III.2 Method for deriving the SPI grids
- SPI calculation follows McKee et al. (1993): for each location, compute precipitation accumulations for 7 durations across 12 months (84 time series).
- Fit a gamma distribution to each time series using L-moments (via a modified R SCI package) to estimate parameters; transform to normal scores (mean 0, sd 1).
- SPI values are truncated at ±5 due to distribution tails.
- Note on distributions:
  - While gamma distribution is widely used and accepted, recent work suggests other distributions (e.g., Pearson type 3, Tweedie) may fit UK data better; future versions may adopt alternative distributions.
- Overlap considerations:
  - For >12-month periods, the underlying data overlap across years, introducing potential autocorrelation.
  - Serial correlation may affect trend analyses; users should account for this in analyses using concatenated SPIs.

## IV. Format of the SPI dataset
- NetCDF4 format, CEH gridded conventions.
- Two-dimensional UK grids with 12 monthly grids per year; one file per accumulation period.
- Projection: British National Grid.
- SPI values are normal scores with no units, expected range approximately -5 to +5.

## V. Acknowledgments
- Joint outcomes from DrIVER, Historic Droughts, and IMPETUS projects.
- Funders: Natural Environment Research Council (NE/L010038/1; Belmont Forum), Historic Droughts (NE/L01016X/1), and IMPETUS (NE/L010267/1).

### References
- Barker, L.J., et al. (2015). A preliminary assessment of meteorological and hydrological drought indicators for UK catchments.
- Gudmundsson, L. & Stagge, J. H. (2014). Package 'SCI': Standardized Climate Indices.
- Hayes, M., et al. (2011). The Lincoln Declaration on Drought Indices.
- Keller, V. D. J., et al. (2015). CEH-GEAR: 1km resolution rainfall estimates for the UK.
- McKee, T. B., et al. (1993). The Relationship of Drought Frequency and Duration to Time Scales.
- National Drought Mitigation Center (2015). Interpretation of SPI Maps.
- Stagge, J. H., et al. (2015). Candidate Distributions for Drought Indices.
- Svensson, C., et al. (2017). Statistical distributions for monthly drought indices.
- Tanguy, M., et al. (2015). SPIgamma61-10 dataset for Great Britain.
- Tanguy, M., et al. (2014). Gridded estimates of rainfall for the UK (CEH-GEAR).