# Amplitude maps provide an indication of net ecosystem phenology since the satellite observations integrate the greenness variations across the plant individuals within each pixel

## What this document presents
- A map-based product of the average amplitude of annual vegetation greenness cycles derived from MODIS NDVI and EVI for Meso- and South America (2001–2013).
- The amplitude reflects how synchronized leaf phenology is among individuals and species within each pixel; areas with no significant annual greenness variation may still have diverse timing or constant canopy.

## Data sources and assets
- Input data:
  - MODIS MOD13A1 (Terra) 16-day vegetation indices, Global 500 m SIN grid, versions V006
  - Time series: 2000–2013 (NDVI and EVI at 500 m and 1000 m)
  - Source/availability: USGS LP DAAC, NASA EOSDIS
- Output data:
  - Maps of average amplitude (maximum minus minimum) of annual cycles
  - Resolutions: 0.5 km, 1 km, and 0.5 degree
  - Projection: Sinusoidal coordinate system
  - Legend codes: -3 water bodies, -2 not enough data, -1 not significant, 0–1 amplitude

## Methodology (how the data product was generated)
- Pre-processing and quality control:
  - Screen for good quality data; remove NDVI/EVI values < 0.01 and outliers (>3 SD from mean)
  - Require at least 100 observations and at least one observation per month
- Time-series analysis:
  - Linear detrending
  - Split cosine taper on the first and last 5% of the series
  - Lomb-Scargle Transform to handle irregular sampling
  - Three-point Hanning window smoothing to increase degrees of freedom
  - Identify annual cycles where the spectral peak exceeds 95% confidence
- Output derivation:
  - Amplitude is computed as the difference between the maximum and minimum of the detected annual cycle
- Validation approaches:
  - Compare amplitude grids with the independent IGBP land cover map (histograms by class)
  - Compare with published in situ canopy phenology observations (leaf flushing/falling, LAI, litter fall)

## Data provenance and acknowledgement
- Primary data source: MOD13A1 product from MODIS (DIDAN 2015)
- Other references: IGBP land cover dataset, related methodological sources on spectral analysis
- Acknowledgements to NASA EOSDIS LP DAAC and USGS EROS for data provision

## Relevance for data leaders ( Data Leaders perspective)
- Demonstrates end-to-end data product development from raw remote-sensing time series to a validated phenology metric.
- Illustrates rigorous data quality controls, metadata clarity, and reproducible methodology suitable for cross-regional analyses.
- Shows integration of data from multiple sources (satellite products) and explicit handling of data gaps and irregular sampling.
- Provides a reproducible workflow that can be applied to other regions, enabling better data stewardship, discoverability, and governance of phenology-related assets.