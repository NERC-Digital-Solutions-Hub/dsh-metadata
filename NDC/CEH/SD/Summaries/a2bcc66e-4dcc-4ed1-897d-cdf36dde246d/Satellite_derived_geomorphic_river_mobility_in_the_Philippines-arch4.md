# Supporting documentation for 'Satellite-derived geomorphic river mobility for ten catchments in the Philippines, 1988-2019'

## Overview
- A dataset with satellite-derived geomorphic river mobility across ten Philippine catchments (1988–2019), using locational probabilities to map how often a river channel occupies a given location.
- Quantifies mobility over ~600 km2 of riverbed; aims to inform resilience to river-related hazards in dynamic landscapes.
- Includes example code and outputs to reproduce analyses: Google Earth Engine (GEE) code, MATLAB code for locational probabilities, MATLAB code for longitudinal analyses, and processed locational probability outputs for the catchments.
- Funded by the Natural Environment Research Council (NERC) and DOST-PCIEERD-Newton Fund (NE/S003312/1).
- The methodology and dataset are described in Boothroyd et al. (2025) in Nature Communications.

## Data assets included
- Example GEE code to run satellite imagery analyses (two versions: Landsat Collection 1 and Collection 2).
- Example MATLAB code and data to generate locational probabilities.
- Example MATLAB code and data to produce longitudinal analyses.
- Processed locational probability outputs for the ten catchments (GeoTIFFs and related files).
- Binary active channel masks derived from Landsat imagery, with quality checks and cleaning steps.
- README and data-structure documentation detailing file organization and subfolder contents (e.g., Abulug_Example and processed outputs).

## Methods: data sources and processing
- Data source: Atmospheric-corrected Landsat imagery (Landsat 5, 7, 8; including Landsat 9 in Collection 2) spanning 1988–2019.
- Spatial scope: ten catchments in the Philippines; trunk channel defined with a 3 km buffer to capture the active channel.
- Time windows: sixteen two-year windows (e.g., 1988–1989, 1990–1991, etc.) chosen to maximize cloud-free observations.
- Cloud masking: CFmask applied to mask clouds and cloud shadows; only cloud-free pixels retained; bicubic resampling to smooth channels.
- Active channel classification: NDVI and MNDWI indices used; thresholding with relationships between NDVI and MNDWI; for this study, MNDWI ≥ -0.4 and NDVI ≤ 0.2 to identify the active channel; pixel values were rescaled to [0,1].
- Time-window aggregation: per time window, a 10th percentile value is used to summarize the collection into a single image, reflecting the active channel extent across time windows.
- Binary masking: per time window, binary masks created and intersected (Boolean AND) to produce final active channel masks; masks exported as GeoTIFFs.
- Code versions: (i) original GEE code for Landsat Collection 1 (1989–2019) and (ii) updated code migrated to Landsat Collection 2 for ongoing data (including Landsat 9).
- Reproducibility emphasis: steps and code provided to allow others to apply Graf’s approach to other rivers.

## Quality control and data cleaning
- Artefact removal in MATLAB to clean binary masks: remove small disconnected regions (<500 pixels), apply morphological closing (disk radius 2) to smooth edges, then remove large isolated regions (<2500 pixels).
- Visual sense-check in GIS; manual edits to remove features not part of the main trunk channel.
- Data availability variability: some time-windows are data-poor due to nonuniform Landsat imagery availability across locations and years, particularly on Mindanao (e.g., Agusan and Mindanao catchments).

## Locational probability concept and outputs
- Locational probability (lp) per pixel summarizes channel occupancy over time:
  - p = sum(Wn * Fn) across time-windows, where Fn is 1 if the pixel is in the active channel in window n, else 0.
  - Wn = 1.0 / x, with x = total number of time-windows for the catchment; equal weighting across windows (each window represents a bankfull-event condition).
  - lp ranges from 0 (never occupied) to 1 (always occupied); low lp indicates mobility, high lp indicates stability.
- Outputs and metadata:
  - Spatial reference: EPSG:32651 (WGS 84 / UTM zone 51N).
  - Resolution: ~10 m x 10 m.
  - Quality control: visually consistent with Landsat and Google Earth imagery.
  - Data structure includes multiple README files and categorized folders detailing code and processing outputs (e.g., Abulug_Example, Processed_Locational_Probabilities).

## Data structure and access details
- Documentation includes: general dataset overview and subfolder-specific readme files (e.g., GEE code, processing steps, and longitudinal plotting scripts).
- Examples of outputs named per catchment (e.g., Abulug_Locational_Probability.tif, Abra_Locational_Probability.tif) and time-series probability images for each catchment.
- The dataset is designed for reuse, with step-by-step descriptions to support replication and application to other river systems.

## Significance, usage, and considerations for Data Leaders
- Enables assessment of river channel dynamics and mobility to inform hazard resilience planning.
- Demonstrates a reproducible workflow with open tools (GEE and MATLAB) and shareable data products.
- Provides a framework for assessing data availability, quality, and gaps across a network of catchments, and for coordinating data gathering and analysis efforts.
- Supports cross-catchment comparisons and integration with wider data communities to strengthen data-informed decision-making in river management and policy.