# Satellite-derived geomorphic river mobility for ten catchments in the Philippines, 1988-2019

## Overview
- A dataset of satellite-derived geomorphic river mobility across ten catchments in the Philippines.
- Uses locational probability to map the proportion of time a river channel occupies each location, quantified over 600 km2 of riverbed.
- Aims to support prediction and resilience planning for river-related hazards in dynamic landscapes.
- Includes example code (Google Earth Engine and MATLAB) and processed outputs for each catchment.
- Funded by Natural Environment Research Council (NERC) and DOST-PCIEERD Newton Fund.

## Data and outputs
- Datasets and code collections:
  - Example Google Earth Engine (GEE) codes to run satellite imagery analyses.
  - Example MATLAB codes and data to generate locational probabilities.
  - Example MATLAB codes and data to produce longitudinal analyses.
  - Processed locational probability outputs for the ten catchments.
- Ten catchments include Abulug, Abra, Agusan, Amburayan, Cagayan, Chico, Ilog, Laoag, Mindanao, Pampanga.
- Outputs exported as GeoTIFFs to Google Drive.

## Methods: imagery and active-channel extraction
- Source: Landsat imagery (Collection 1, migrated to Collection 2 for updates; Landsat 9 included in Collection 2 as of 2022).
- Time framing: 16 two-year time-windows covering 1988–2019 (e.g., 1988–1989, 1990–1991, etc.) to maximize cloud-free data.
- Active channel definition: trunk channel buffered by 3 km to encompass the active channel and nearby deposits.
- Cloud masking: CFmask applied to mask clouds and shadows; bicubic resampling to smooth channel representation.
- Spectral indices for classification:
  - NDVI and MNDWI used to distinguish active channel.
  - Active channel classification: MNDWI ≥ -0.4 and NDVI ≤ 0.2.
  - Pixel values rescaled to [0, 1] and time-window collections reduced to a single image via the 10th percentile.
- Binary masks: final active channel masks produced as binary presence/absence images; intersection of NDVI and MNDWI masks (logical AND) used to create final masks.

## Locational probabilities and interpretation
- Locational probability (lp) calculation:
  - lp per pixel = sum over time-windows of Fn weighted by Wn, where Fn is 1 if the pixel is occupied in window n, 0 otherwise.
  - Weights Wn = 1/x, where x is the total number of time-windows for the catchment (equal weighting across windows).
  - lp ranges from 0 (never occupied) to 1 (always occupied).
- Interpretation:
  - 0 < lp < 0.25 = low occupancy (high mobility).
  - 0.75 < lp < 1 = high occupancy (stable channel).
- Spatial resolution and reference: ~10 m x 10 m; EPSG:32651 (WGS 84 / UTM zone 51N).

## Data cleaning, quality control, and limitations
- Cleaning steps in MATLAB:
  - Remove disconnected artefacts with < 500 pixels.
  - Morphological closing (disk radius of 2 pixels) to smooth edges.
  - Remove large, isolated features with < 2500 pixels away from the trunk channel.
  - Manual GIS sense-check and editing to ensure correct trunk-channel delineation.
- Data quality and gaps:
  - Some time-windows data-poor due to variable Landsat availability and cloud cover.
  - Greater data gaps on Mindanao (e.g., Agusan, Mindanao catchments) due to cloud obscuration and acquisition limitations.
- Data provenance and consistency:
  - Quality controlled by visual agreement with Landsat and Google Earth imagery.
  - Variability in cloud cover and sensor availability acknowledged.

## Data structure and accessibility
- Directory structure and readme files describe data organization:
  - General overview in README.txt.
  - Subfolders (e.g., Abulug_Example/01_GEE_CODE) with detailed data structure notes.
  - README_02_Process_Locational_Probabilities_from_GEE_Binary_Images.txt for processing steps.
  - README_03_Process_Locational_Probabilities_using_TopoToolbox_SWATHobj for longitudinal analyses.
- Outputs include:
  - Abulug_Locational_Probability.tif and similar for each catchment.
  - Processed Locational Probability outputs for the ten catchments (e.g., Abra_Locational_Probability.tif, Mindanao_Locational_Probability.tif).
  - Associated MATLAB and TopoToolbox scripts for plotting and analysis.

## Reproducibility and code versions
- Two GEE code versions provided:
  - Original code for Landsat Collection 1 imagery.
  - Updated code migrated to Landsat Collection 2 (supports Landsat 9) for future reproducibility.
- Emphasis on reproducibility to enable application to other rivers and time periods.

## Related work and references
- Context and validation discussed in the accompanying research:
  - Boothroyd et al. (2025) Nature Communications: Big data reveal idiosyncratic patterns and rates of geomorphic river mobility.
  - Prior methodological references on remote-sensing-based river morphology, cloud impact, and locational probability concepts are cited for validation and rationale.