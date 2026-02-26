# Amplitude maps provide an indication of net ecosystem phenology from MODIS NDVI and EVI time series in Meso- and South America

## Overview
- Presents a robust map of the average amplitude of annual vegetation greenness cycles derived from MODIS NDVI and EVI data (2000–2013, analyzed 2001–2013).
- Amplitude reflects how synchronised leaf phenology is across plant individuals within a pixel.
- Explains interpretation: high amplitude suggests well-defined annual leaf phenology; low amplitude may indicate diverse timing, mixed strategies, or constant canopy.

## Data sources
- Input time-series: MODIS vegetation indices (NDVI and EVI) at 500 m and 1000 m resolution.
- Source product: MOD13A1 (MODIS/Terra Vegetation Indices 16-Day L3 Global 500 m SIN Grid V006).
- Temporal coverage: 13-year series used for spectral analysis.
- Data provenance: USGS LP DAAC.

## Pre-processing and quality control
- Per-pixel screening for quality: exclude non-good quality data, NDVI/EVI < 0.01, and outliers beyond ±3 standard deviations.
- Inclusion criteria: at least 100 observations and at least one observation per month.
- Time-series pre-processing: linear detrending; split cosine taper on the first and last 5% of the series.

## Analysis
- Spectral method: Lomb-Scargle Transform to handle irregularly spaced data.
- Spectral smoothing: three-point Hanning window to increase degrees of freedom.
- Annual cycle detection: a peak must exceed the 95% confidence level to be considered significant.
- Output metric: average amplitude = (maximum − minimum) of the detected annual cycle.

## Outputs and interpretation
- Generated maps of mean annual-cycle amplitude for NDVI and EVI.
- Legend interpretation:
  - -3: water bodies
  - -2: not enough data
  - -1: not significant
  - 0–1: amplitude of phenological signal
- Purpose: provide a robust, interpretable indicator of leaf phenology strength and timing across landscapes.

## Validation and evaluation
- Two evaluation approaches:
  - Comparison with independent IGBP land cover maps via histogram distributions of amplitude within land cover classes.
  - Comparison with published in situ observations describing canopy leaf life cycles, LAI, and litter fall.

## Coverage and resolutions
- Geographic focus: Mesoamerica and South America.
- Resolutions available: 0.5 km, 1 km, and 0.5 degree.

## Data products and accessibility
- Output derived from a long time-series MODIS product; methodology details provided for reproducibility and potential re-use in similar phenology studies.
- Inputs and references include key datasets and methodological sources (MOD13A1, IGBP land cover, and related spectral analysis literature).

## Acknowledgements
- MODIS MOD13A1 data retrieved via NASA LP DAAC (EarthData); acknowledgement of data providers and project contributors.