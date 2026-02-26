# Historic Droughts Inventory of drought references for Historic Standardised Precipitation Index time series for IHU hydrometric areas (1862-2015) - version 2

## Brief description of the dataset
- Time series of Standardised Precipitation Index (SPI) for the Integrated Hydrological Units (IHU) hydrometric areas, covering 1862–2015.
- SPI calculated for accumulation periods of 1, 3, 6, 9, 12, 18, and 24 months, for each calendar month.
- SPI values are “normal scores” (mean 0, sd 1), truncated at -5 to +5; values of -9999 indicate no data.
- Underlying data: 1961–2010 standard period for gamma distribution fitting; dataset extends beyond this period (1862–2015).

## Context of the dataset
- Produced as part of two projects: DrIVER (Drought Impacts: Vulnerability thresholds in monitoring and Early warning Research) and Historic Droughts (part of the UK Drought and Water Scarcity Programme).
- Historic Droughts Inventory serves as a knowledge base of past drought characteristics, drivers, impacts, and responses, aimed at providing a common reference for policy makers, water suppliers, agriculture, and industry.
- Inventory comprises:
  - Hydro-meteorological timelines of rainfall, river flows, and groundwater.
  - References to past droughts from the 19th century to today (newspaper reports, legislation, agricultural media, oral histories), with consistent formatting and links to full sources.
- Structure draws on EDII (European Drought Impact Inventory) formats adapted for broader drought references.

## Motivation
- Aims to support incorporation into the CEH droughts portal and to enable multi-sectoral understanding of drought by aggregating SPI across IHU areas.
- SPI enables assessment of drought severity and rarity at various time scales and is endorsed as a primary drought monitoring tool by international guidance (e.g., Lincoln Declaration).

## Data sources
- IHU hydrometric areas (UK hydrological reference units).
- Met Office 5 km monthly rainfall grids, including data from:
  - UKCP09 (1910–1959, 2001–2011)
  - Derived monthly grids from daily data (1960–2000)
  - Unpublished updates (2012–2015)
  - Historic droughts data rescues (1862–1909)
- Historic rainfall and temperature data digitisation/gridding by the Met Office as part of the Historic Droughts project.

## Method for deriving the SPI grids
- SPI calculated following McKee et al. (1993) by fitting a gamma distribution to each time series of accumulation-period precipitation.
- For each location, SPI is computed for 7 accumulation periods (1, 3, 6, 9, 12, 18, 24 months) and for 12 calendar months (84 time series per location).
- Parameter estimation via L-moments (instead of maximum likelihood) due to fitting issues; uses the R SCI package with L-moments.
- Transformation to a normal distribution to yield SPI values; truncation at +/-5 to manage extremes.
- Notes on methodology:
  - Gamma distribution is widely used; alternative distributions (e.g., Pearson Type III, Tweedie) may be considered in future if justified.
  - For longer accumulation periods, data are overlapping, introducing autocorrelation; serial correlation should be accounted for in trend analyses.
  - The standard fitting period is 1961–2010; dataset extends back to 1862 using historic digitised data.
- Format considerations:
  - Data stored as CSV with temporal aggregations of SPI; appears as 10 columns (RID, POLYGONID, THEDATETIME, plus SPI aggregations).

## Format of the dataset
- CSV file with 10 columns:
  - RID (row identifier)
  - POLYGONID (IHU hydrometric area ID)
  - THEDATETIME (date/time)
  - Columns 4–10: SPI values for the seven accumulation periods (across 12 months)
- SPI values are normal scores (mean 0, sd 1); range is -5 to +5; -9999 denotes No Data.

## Acknowledgements
- Joint outcomes from DrIVER, Historic Droughts, and IMPETUS projects.
- Funders include the Natural Environment Research Council (NERC) and related Belmont Forum initiatives.

## References (selected)
- Foundational SPI and drought index literature (e.g., McKee et al., 1993; Hayes et al., 2011; Barker et al., 2015; Stagge et al., 2015).
- Data and methodology tools (e.g., Gudmundsson & Stagge, 2014; Kral et al., 2015; Keller et al., 2015).
- Related UK drought inventories and hydrological units (IHU) documentation.