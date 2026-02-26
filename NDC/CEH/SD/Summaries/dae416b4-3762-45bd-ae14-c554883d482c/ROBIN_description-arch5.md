# Amplitude maps provide an indication of net ecosystem phenology since the satellite observations integrate the greenness variations across the plant individuals within each pixel

## Overview
- Purpose: Create a map of the average amplitude of annual greenness cycles derived from MODIS NDVI and EVI data (2000–2013) for Mesoamerica and South America, using a Lomb-Scargle spectral analysis to quantify leaf phenology.
- Interpretation: Amplitude reflects how synchronized leaf life cycles are among plants within each pixel; areas with no statistically significant annual variation may still host diverse, synchronized events or constant canopies.
- Data sources: 13-year MODIS time-series (2001–2013) of NDVI/EVI from MOD13A1 products (500 m and 1000 m) provided by MODIS/Terra; data and metadata supplied by USGS/NASA LP DAAC; surface reflectance and vegetation indices from MOD13A1 (DIDAN et al., 2015).
- Outputs: Robust amplitude maps (average amplitude = max minus min of annual cycles) derived from power spectral estimates; quality-screened time series underpin the analyses.
- Preprocessing and quality: Time-series screened for quality flags; NDVI/EVI < 0.01 and outliers (>3 standard deviations from the mean) removed; require at least 100 observations with at least one per month; linear detrending; split cosine taper on the first/last 5% of series.

## Methodology
- Spectral analysis: Lomb-Scargle Transform used to handle irregularly spaced data; periodograms smoothed with a three-point Hanning window to increase degrees of freedom.
- Annual cycle detection: A pixel is deemed to have a detectable annual cycle if the spectral peak exceeds a 95% confidence level.
- Output measure: The maps show the average amplitude of the annual cycle as derived from the spectral estimates.

## Evaluation
- External validation: Compare amplitude grids with the independent IGBP land cover map (histograms of amplitude values within land cover classes).
- In situ validation: Compare amplitude values with published site observations describing canopy leaf life cycles (leaf flushing/falling, LAI, litter fall, etc.).

## Coverage and Data Products
- Region: Mesoamerica and South America.
- Projection: Sinusoidal coordinate system (as described in the dataset metadata).
- Resolutions: 0.5 km, 1 km, and 0.5 degree.
- Legend (interpretation in maps):
  - -3: water bodies
  - -2: not enough data
  - -1: not significant
  - 0–1: amplitude of phenological signal
- Data sources and references: MODIS MOD13A1 (MODIS/Terra Vegetation Indices, 16-Day L3 Global 500m SIN Grid, V006); IGBP land cover data (Loveland & Belward, 1997; Friedl et al., 2010); related methodological references (Weedon 2003; Sulla-Menashe et al. 2010s).

## Access and Reuse
- Data accessibility: MOD13A1 products retrieved from NASA EarthData LP DAAC (NASA EOSDIS); acknowledging the LP DAAC/USGS and NASA data providers.

## Governance and Stewardship Considerations for Data Stewards
- Data provenance: Clear lineage from MODIS MOD13A1 inputs to the amplitude product; proper attribution to Didan (2015) and related data/products.
- Metadata and documentation: Maintain comprehensive documentation of data sources, preprocessing steps (quality screening, detrending, taper), and spectral analysis parameters (Lomb-Scargle settings, smoothing, significance threshold).
- Quality assurance: Preserve the screening criteria (quality flags, thresholds, minimum observations) to ensure reproducibility and traceability.
- Reproducibility: Document and version-control the processing workflow (time window 2001–2013, 16-day composites, amplitude calculation).
- Interoperability: Ensure consistent projection (Sinusoidal) and resolutions (0.5 km, 1 km, 0.5 degree) to enable integration with other datasets and analyses.
- Updates and versioning: Note the temporal extent and data product version (MOD13A1 V006) and any future updates or reprocessing.
- Usage and licensing: Adhere to data use policies for MODIS/LP DAAC data; provide proper citations (MODIS product, associated metadata, and methodological references).