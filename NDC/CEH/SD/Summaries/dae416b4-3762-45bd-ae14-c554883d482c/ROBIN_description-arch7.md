# Amplitude maps provide an indication of net ecosystem phenology since the satellite observations integrate the greenness variations across the plant individuals within each pixel.

## Overview
- Maps depict the average amplitude of annual greenness cycles derived from MODIS NDVI and EVI time series (2001–2013).
- Amplitude reflects how synchronised leaf life cycles are among individuals within a pixel.
- Areas with low apparent annual variation may still have defined phenology due to varied timing among individuals or constant canopy turnover.
- The product uses a robust spectral method to identify annual cycles and applies quality controls to ensure reliable results.

## Data sources and study area
- Input: 13-year, 16-day MODIS vegetation index time series (NDVI and EVI) at 500 m and 1000 m resolutions.
- Data provider: MODIS MOD13A1 product (Terra), MODIS data supplied via USGS LP DAAC.
- Region: Mesoamerica and South America.
- Spatial details: outputs in a Sinusoidal projection with resolutions of 0.5 km, 1 km, and 0.5 degree.

## Methodology and processing
- Pixel-level quality screening:
  - Exclude non-flagged poor quality data, NDVI/EVI < 0.01, and outliers (>3 standard deviations from the mean).
  - Retain pixels with at least 100 observations and at least one observation per month.
- Time-series pre-processing:
  - Linear detrending.
  - Split cosine taper on the first and last 5% of the series to reduce spectral leakage.
- Spectral analysis:
  - Lomb-Scargle Transform for irregularly spaced data.
  - Periodograms smoothed with a three-point Hanning window (eight degrees of freedom).
  - Annual cycles detected if the spectral peak exceeds 95% confidence.
- Output metric:
  - Amplitude = difference between maximum and minimum of the detected annual cycle.
  - The produced maps reflect the average amplitude derived from the spectral estimates.

## Output product and interpretation
- Primary product: map of average amplitude of annual vegetation greenness cycles.
- Legend:
  - -3: water bodies
  - -2: not enough data
  - -1: not significant
  - 0–1: amplitude of the phenological signal
- Output aids GIS-based visualization and spatial analysis of phenology patterns and synchronization across landscapes.

## Evaluation and validation
- Two validation approaches:
  - Comparison with independent IGBP land cover map to assess amplitude distributions across cover classes.
  - Comparison with published in situ observations describing canopy phenology, LAI, leaf flushing/falling, and litter fall.
- These validations support interpretation of amplitude as a robust indicator of annual phenology in the studied region.

## Access and attribution
- Data sources and references:
  - MODIS MOD13A1 product (Didan et al., 2015) and related MODIS land cover datasets (Loveland & Belward, Friedl et al.).
- Acknowledgement to NASA LP DAAC and USGS EROS Center for data provisioning.