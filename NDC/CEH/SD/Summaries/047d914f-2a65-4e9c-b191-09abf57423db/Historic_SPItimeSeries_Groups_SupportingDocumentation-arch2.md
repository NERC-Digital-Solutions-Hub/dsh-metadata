# Standardised Precipitation Index time series for Integrated Hydrological Units Groups (1961-2012)

## Overview
- Time series of the Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) Groups, covering period 1862–2015 (with standard distribution period 1961–2010).
- SPI is calculated for accumulation periods of 1, 3, 6, 12, 18, and 24 months, with each duration computed for all twelve calendar months.
- The dataset supports drought monitoring and analysis within the CEH droughts portal by aggregating SPI across IHU Groups.
- SPI values are unitless “normal scores” (mean 0, standard deviation 1) and truncated to the range -5 to +5.

## Data scope and purpose
- Purpose: enable drought/wet-period analysis over specific UK hydrological areas by aggregating SPI across IHU Groups.
- SPI helps assess rarity and severity of meteorological drought and can indicate anomalously wet periods as well.
- The dataset is intended for monitoring environmental health and policy performance related to drought indicators.

## Data sources
- IHU Groups (Kral et al., 2015) as the spatial reference units.
- Met Office 5 km monthly rainfall grids, incorporating UKCP09 data (1910–2011), unpublished updates (2012–2015), and Historic Droughts project data (1862–1909).

## Methodology
- SPI computed as per McKee et al. (1993): uses the cumulative probability of precipitation for a given accumulation period.
- Distribution fitting: gamma distribution estimated with L-moments (instead of maximum likelihood) due to data characteristics; code based on the R SCI package with L-moments adaptation.
- Data transformation: precipitation time series are converted to standard normal scores (mean 0, sd 1).
- Truncation: SPI values are limited to -5 to +5.
- Distribution choice caveat: while gamma is widely used, UK-specific studies suggest other distributions (e.g., Pearson type 3 or Tweedie) may be more appropriate in some cases; current dataset uses gamma with notes on potential future updates.

## Data format and contents
- Format: CSV.
- Columns (9 total):
  - RID (row identifier)
  - POLYGONID (IHU Group ID; use for joining with shapefiles)
  - THEDATETIME (date and time)
  - Columns 4–9: SPI values for the six accumulation periods (1, 3, 6, 12, 18, 24 months), representing different temporal aggregations ending in each month.
- SPI values are unitless normal scores; No Data encoded as -9999.

## Temporal and data quality considerations
- Data span: 1862–2015; standard period for distribution: 1961–2010.
- For accumulation periods > 12 months, overlapping data are used, introducing potential autocorrelation in the underlying series.
- Serial correlation considerations: monthly SPIs derived from overlapping data may be autocorrelated; appropriate methods should account for this in trend analyses.

## Usage notes and caveats
- The SPI time series are designed for drought monitoring and for integration into drought portals; they are suitable for assessing short-, medium-, and long-term moisture patterns.
- Caution advised when applying standard frequency analysis due to possible autocorrelation from overlapping accumulation periods.
- Future updates may explore alternative distributions if justified by UK-specific validation.

## Acknowledgments and references
- Acknowledgments: Joint outputs from DrIVER, Historic Droughts, and IMPETUS projects (NERC funding).
- Key references include McKee et al. (1993), Stagge et al. (2015), Svensson et al. (2015, 2016), Barker et al. (2015), Gudmundsson & Stagge (2014), Hayes et al. (2011), and Kral et al. (2015).