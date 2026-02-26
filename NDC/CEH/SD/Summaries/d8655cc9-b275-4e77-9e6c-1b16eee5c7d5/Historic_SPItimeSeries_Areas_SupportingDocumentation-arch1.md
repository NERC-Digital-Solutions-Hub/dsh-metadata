# Supporting Information

## I. Brief Description of the dataset
- Time series of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) hydrometric areas (Kral et al., 2015).
- SPI is a drought index based on the probability of precipitation for a given accumulation period (1, 3, 6, 12, 18, 24 months) and calculated for each of the twelve calendar months.
- Standard fitting period for the gamma distribution: 1961-2010.
- Dataset covers 1862–2015 and is stored in CSV format.
- File structure: 9 columns (RID, POLYGONID, THEDATETIME, and 6 durations × 12 months = 72 SPI values). SPI values are normal scores (mean 0, SD 1), range limited to -5 to +5; -9999 indicates No Data.

## II. Motivation
- Intended for incorporation into the CEH droughts portal to study drought over specific IHUs by aggregating SPI.
- SPI provides a widely used, standardized measure of meteorological drought and wet periods, with time scales informing short- to long-term moisture conditions and potential impacts on soils, crops, streamflows, and reservoirs.

## III.1 Data Sources
- IHU hydrometric areas: coarsest spatial units within the UK hydrological framework.
- Met Office 5km monthly rainfall gridded data: combination of UKCP09 data (1910–2011), unpublished updates (2012–2015), and historic gridded data (1862–1909) from the Historic Droughts project.

## III.2 Method for deriving the SPI grids
- SPI calculated per accumulation period (1, 3, 6, 12, 18, 24 months) and per calendar month.
- For each location and duration, a gamma distribution is fitted to the historic precipitation series using L-moments (instead of maximum likelihood) to estimate parameters (via a modified R SCI package).
- Transformation to a standard normal distribution yields SPI values (unitsless).
- Truncation at absolute value 5; approximately 95% of SPIs lie within -2 to 2, and 68% within -1 to 1.
- Notes:
  - Gamma distribution widely used in Europe for SPI, though UK data show Shapiro-Wilk issues; alternative distributions (e.g., Pearson type 3, Tweedie) exist but are not used here.
  - For durations >12 months, overlapping data introduce autocorrelation; SPI series are not independent for frequency analysis.
  - Serial correlation considerations: new monthly SPIs constructed from overlapping data may be autocorrelated; account for this in trend analyses.

## IV. Format of the [SPI_IHU_HA] dataset
- CSV file containing 9 columns:
  - RID, POLYGONID, THEDATETIME, followed by 72 SPI values (6 durations × 12 months).
- SPI values are normal scores with no units, in the range [-5, 5], with -9999 as No Data.
- The POLYGONID column enables joining to the IHU hydrometric area shapefile.

## V. Acknowledgments
- Joint outcomes from DrIVER (NE/L010038/1), Historic Droughts (NE/L01016X/1), and IMPETUS (NE/L010267/1) projects.

## References (context)
- Foundational sources on SPI, methodology, distributions, and related UK datasets underpinning this compilation.