# Amplitude maps provide an indication of net ecosystem phenology

- Purpose: Present amplitude maps that indicate net ecosystem phenology by summarizing the annual greenness cycles across plant individuals within each pixel. The average amplitude reflects how synchronized leaf life cycles are among individuals; areas with low apparent annual variation may still host well-defined phenology at the individual level or maintain a constant canopy through leaf turnover.

- Key concepts:
  - Amplitude corresponds to the maximum minus minimum of annual greenness cycles derived from satellite data.
  - Areas with synchronized leaf phenology show detectable annual cycles in vegetation indices (VIs).

## Data and inputs

- Data source: MODIS vegetation indices (NDVI and EVI) time series from 2000–2013 (2001–2013 used for analysis), 16-day resolution.
- Specific products: MOD13A1 (MODIS/Terra Vegetation Indices 16-Day L3 Global 500m SIN Grid V006).
- Study region: Meso- and South America.
- Spatial resolutions available: 0.5 km, 1 km, and 0.5 degree.
- Pre-processing:
  - Quality screening: exclude data not flagged as good quality, NDVI/EVI < 0.01, and outliers >3 standard deviations from the mean.
  - Inclusion criteria: at least 100 observations (out of up to 320) and at least one observation per month.

## Methodology

- Time-series analysis approach:
  - Spectral analysis using Lomb-Scargle Transform to handle irregularly spaced data.
  - Pre-processing: linear detrending and a split cosine taper on the first and last 5% of the series to reduce spectral leakage.
  - Smoothing: three-point Hanning window to increase degrees of freedom.
  - Annual cycle detection: a spectral peak must exceed 95% confidence to be considered significant.
- Output metric:
  - Amplitude is derived from the power spectrum as the average maximum-minus-minimum of the detected annual cycles.
- Validation and interpretation:
  - Evaluation against independent data:
    - Comparison with the IGBP land cover map (histograms of amplitude by land-cover class).
    - Comparison with published in situ observations describing canopy leaf life cycles (LAI, leaf flushing/falling, litter fall).
  - Significance assessment ensures that only robust annual signals contribute to the amplitude maps.

## Outputs and legend

- Generated outputs:
  - Amplitude maps of annual vegetation greenness cycles for NDVI and EVI across the study region.
- Legend interpretation:
  - -3: water bodies
  - -2: not enough data
  - -1: not significant
  - 0–1: amplitude of phenological signal
- Projection and metadata:
  - Coordinate system: Sinusoidal projection.
  - Acknowledges data lineage and sources (MODIS MOD13A1; IGBP references).

## Interpretation and potential uses

- What amplitude tells us:
  - Higher amplitude suggests a higher degree of synchronization in leaf phenology among individuals within a pixel.
  - Low amplitude may indicate asynchronous phenology or consistent canopy with diverse leaf ages.
- Practical applications:
  - Assess regional phenology patterns and their relation to land cover, climate, or management regimes.
  - Support ecological and environmental decision-making by providing a data-driven view of phenological timing and plant turnover at the pixel level.

## Data sources and acknowledgments

- Primary data: MODIS MOD13A1 (MODIS Terra Vegetation Indices 16-Day) products, 500 m resolution.
- Data providers: NASA EOSDIS LP DAAC; USGS EROS Center.
- Data retrieval and references cited for methodology and land-cover validation.