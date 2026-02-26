# SPI_IHU_HA

## Brief overview
- A dataset of Standardised Precipitation Index (SPI) time series for Integrated Hydrological Units (IHU) hydrometric areas (IHU_HA).
- SPI calculated for accumulation periods: 1, 3, 6, 12, 18, 24 months, with every accumulation period evaluated for each of the twelve calendar months.
- Time span: 1862 to 2015 (fitting period 1961–2010).
- Stored in CSV format; outputs are normal scores (mean 0, sd 1) with no units, truncated to ±5; -9999 indicates No Data.

## Purpose and use
- Designed for incorporation into the CEH droughts portal to study drought within specific IHU hydrometric areas.
- SPI provides a drought/ wetter signal at multiple timescales, enabling assessment of short-, medium-, and long-term moisture conditions and their relation to streamflows, reservoirs, and groundwater.

## Data sources
- IHU hydrometric areas (Kral et al. 2015): the spatial framework (coarsest IHU units for hydrological analysis).
- Met Office 5km monthly rainfall grids: UKCP09 data (1910–2011), unpublished updates (2012–2015), and rescued data for 1862–1909 (Historic Droughts project).

## Methodology
- SPI computation follows McKee et al. (1993): based on the cumulative probability of precipitation for each location and duration.
- Gamma distribution fitted to each time series using L-moments (via modified R SCI package) instead of maximum likelihood.
- Transformation to a standard normal distribution to obtain SPI values.
- Truncation of extreme SPI values at ±5.
- 72 time series per location (6 durations × 12 months) derived; fit uses the standard period 1961–2010.
- Note: overlapping data for durations >12 months introduces autocorrelation; SPIs themselves may be autocorrelated when concatenated monthly, affecting trend analyses.

## SPI grids format and content
- CSV format with 9 columns:
  - RID: row identifier
  - POLYGONID: IHU hydrometric area ID
  - THEDATETIME: date and time
  - Columns 4–9: SPI values for the six accumulation periods (1, 3, 6, 12, 18, 24 months) across the time period covered (monthly end-points)
- SPI values are unitless normal scores (mean 0, sd 1), range effectively within -5 to +5; -9999 indicates No Data.

## Data quality, limitations, and interpretation
- While gamma distribution is commonly used for SPI, UK-specific studies suggest other distributions may fit better; gamma is still broadly used for consistency and comparability.
- Serial correlation due to data overlapping across long accumulation periods; treat monthly SPIs for trend analysis with adjustments for autocorrelation.
- The dataset explicitly notes limitations around independence assumptions in frequency analyses due to overlapping records.

## Data access and provenance
- This release is part of the Historic Droughts project.
- Underpins drought monitoring and analysis within CEH initiatives; builds on digitised historic rainfall data to extend temporal coverage back to 1862.
- Acknowledges support from multiple NERC projects: DrIVER, Historic Droughts, and IMPETUS (funding NE/L010038/1, NE/L01016X/1, NE/L010267/1).

## Acknowledgments and references
- References include work on SPI distributions and drought indicators (McKee et al., 1993; Hayes et al.; Barker et al.; Stagge et al.; Gudmundsson & Stagge).
- Data and methodology rely on CEH-GEAR enhancements and Met Office rainfall grids; evolving approaches discussed for future updates with alternative distributions.