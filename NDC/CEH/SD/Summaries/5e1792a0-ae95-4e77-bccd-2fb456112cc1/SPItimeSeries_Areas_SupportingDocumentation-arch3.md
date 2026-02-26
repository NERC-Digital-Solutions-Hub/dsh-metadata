# Standardised Precipitation Index time series for IHU hydrometric areas (1961-2012)

## Overview
- Time series dataset of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) hydrometric areas in the UK.
- SPI calculated for six accumulation periods (1, 3, 6, 12, 18, 24 months) across 12 calendar months, yielding 72 series per IHU area.
- Data spans 1961–2012, with a standard fitting period of 1961–2010.
- Stored in CSV format; values are the SPI normal scores (mean 0, std dev 1) truncated to [-5, 5]; -9999 indicates missing data.

## Data sources and scope
- IHU hydrometric areas: core spatial units used for hydrological purposes.
- CEH-GEAR: gridded, areal rainfall estimates used to derive area-averaged rainfall for each IHU area.
- Purpose: support a drought monitoring portal and enable analysis of drought frequency, duration, and intensity across areas and time.

## Methodology
- SPI computation follows McKee et al. (1993): based on the cumulative probability of precipitation for each accumulation period ending in a given month.
- For each IHU area: 72 time series (6 durations × 12 months) are derived.
- Distribution fitting: gamma distribution fitted to historic precipitation accumulations using L-moments (preferred when maximum likelihood is unstable); parameters estimated with a modified R SCI package.
- Transformation: data converted to standard normal scores; resulting SPIs are unitless.
- Extremes: SPI values truncated at ±5.
- Limitations noted: gamma distribution, while widely used in Europe, may not always be the best fit (other distributions like Pearson type 3 or Tweedie may be more adequate in some UK cases).

## Data format and schema
- File format: CSV.
- Key columns:
  - RID: row identifier
  - POLYGONID: IHU hydrometric area identifier (for joining with shapefiles)
  - THEDATETIME: date (end of the accumulation period)
  - Columns 4–9: SPI values for the six accumulation periods (1, 3, 6, 12, 18, 24 months)
- SPI values are unitless normal scores (mean 0, stdev 1); range limited to -5 to +5; -9999 denotes No Data.

## Data quality, limitations, and considerations
- Serial and spatial dependencies:
  - For accumulation periods > 12 months, underlying precipitation series involve overlapping data, introducing potential autocorrelation.
  - Concatenated monthly SPIs are also likely autocorrelated if used for trend analysis; appropriate statistical methods should account for this.
- Data and metadata considerations:
  - Metadata sufficiency is acknowledged; transformation and standardization steps are explicitly described.
  - Some work suggests reconsidering the gamma distribution for UK data; future versions may adopt alternative distributions if justified.
- Temporal and data coverage notes:
  - Although CEH-GEAR spans 1890–2012, SPI calculations begin in 1961 due to higher uncertainty in rainfall data prior to 1961.
  - The standard fitting period remains 1961–2010; dataset provides 1961–2012 coverage.

## Usage and interpretation guidance
- Suitable for drought monitoring, distinguishing short- to long-term moisture deficits and wet spells at various time scales.
- Different accumulation periods provide insights into:
  - 1-month SPI: short-term soil moisture and crop stress
  - 3-month SPI: seasonal moisture
  - 6-month SPI: medium-term trends; potential link to streamflows and reservoirs
  - 12-, 18-, 24-month SPIs: longer-term precipitation patterns and their hydrological implications
- When performing trend or frequency analyses, account for autocorrelation due to overlapping data and potential non-independence.

## Data governance and reproducibility notes
- Data are derived from established rainfall datasets (CEH-GEAR) and standardized processing (L-moments with a gamma fit) to ensure reproducibility.
- The methodology and data processing steps are documented; potential future updates may explore alternative distributions and updated rainfall inputs.
- Data are designed to be joinable with IHU shapefiles via POLYGONID, facilitating spatial analyses and visualization.

## References
- Barker, L.J., et al. (2015). A preliminary assessment of meteorological and hydrological drought indicators for UK catchments.
- Gudmundsson, L. & Stagge, J. H. (2014). SCI: Standardized Climate Indices package.
- Hayes, M. et al. (2011). The Lincoln Declaration on Drought Indices.
- Keller, V. D. J., et al. (2015). CEH-GEAR: 1km resolution rainfall estimates for the UK.
- Kral, F., Fry, M., Dixon, H. (2015). Integrated Hydrological Units of the United Kingdom: Hydrometric Areas without Coastline.
- McKee, T.B., Doesken, N.J., Kleist, J. (1993). The Relationship of Drought Frequency and Duration to Time Scales.
- National Drought Mitigation Center (2015). SPI interpretation guidelines.
- Stagge, J. H. et al. (2015). Candidate distributions for climatological drought indices.
- Svensson, C. et al. (2015). Ongoing work on drought indicators.
- Tanguy, M., et al. (2014). CEH-GEAR: daily and monthly areal rainfall for the UK.