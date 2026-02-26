# Supporting Information

## Brief Description of the dataset
- 5km gridded Standardised Precipitation Index (SPI) data for the United Kingdom.
- SPI calculated for accumulation periods of 1, 3, 6, 9, 12, 18, and 24 months, each for 12 calendar months.
- Standard period used to fit the gamma distribution: 1961–2010.
- Coverage: 1862–2015.
- Format: NetCDF4, projected on the British National Grid.
- SPI values are normal scores with mean 0 and standard deviation 1, unitless, typically within -2 to +2 (range limited to -5 to +5).

## Motivation
- Derived within the Historic droughts project to develop cross-disciplinary understanding of past UK droughts and improve drought management tools.
- SPI is a widely used drought index for defining/monitoring drought and assessing periods of anomalously wet events.
- Enables spatial analysis of drought propagation, identification of severely affected areas, and examination of short- to long-term moisture trends across multiple time scales.

## Data Sources
- Met Office 5km monthly rainfall gridded data, incorporating:
  - UKCP09 data for 1910–1959 and 2001–2011
  - Monthly rainfall grids from Met Office daily grids (1960–2000)
  - Unpublished updates by the Met Office (2012–2015)
  - Restored data for 1862–1909 (historic period)

## Method for deriving the SPI grids
- SPI computed as defined by McKee et al. (1993) using the cumulative precipitation over each accumulation period ending in a given month.
- For each location, 84 time series: 7 durations × 12 months.
- Gamma distribution fitted to each series using L-moments (via a modified R SCI package) to estimate parameters; standardization to a normal distribution (mean 0, SD 1).
- Values truncated to the range -5 to +5 due to tail uncertainties.
- Noted caveats:
  - Gamma distribution may not be optimal for the UK; alternatives (e.g., Pearson type 3, Tweedie) exist and could be used in future versions.
  - Accumulations >12 months involve overlapping data, introducing autocorrelation; this affects independence assumptions for frequency analyses.
  - Serial correlation may arise if constructing concatenated SPI series over months; account for this in trend analyses.

## Format of the SPI dataset
- Stored in NetCDF4 format, following CEH gridded dataset conventions.
- Structure: two-dimensional UK grids with twelve monthly grids per year; one yearly file per accumulation period.
- Projection: British National Grid.
- Data: normal scores (unitless), range limited to -5 to +5.

## Acknowledgments
- Joint outcomes from the DrIVER project, Historic Droughts project, and IMPETUS project.
- Grants: NE/L010038/1 (DrIVER), NE/L01016X/1 (Historic Droughts), NE/L010267/1 (IMPETUS).

## References
- Barker et al. 2015; Gudmundsson & Stagge 2014; Hayes et al. 2011; Keller et al. 2015; McKee et al. 1993; National Drought Mitigation Center 2015; Stagge et al. 2015; Svensson et al. 2017; Tanguy et al. 2015; Tanguy et al. 2014.