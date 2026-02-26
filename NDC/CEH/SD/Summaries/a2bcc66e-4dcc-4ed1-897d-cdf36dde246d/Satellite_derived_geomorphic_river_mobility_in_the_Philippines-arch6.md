# Supporting documentation for 'Satellite-derived geomorphic river mobility for ten catchments in the Philippines, 1988-2019'

- A dataset and accompanying documentation describing satellite-derived geomorphic river mobility for ten catchments in the Philippines, using locational probability to map how often a river channel occupies a location within ~600 km2 of riverbed.
- Outputs designed to support resilience planning for river-related hazards in dynamic landscapes.
- Provides example code and data in Google Earth Engine (GEE) and MATLAB to reproduce analyses and generate locational probabilities and longitudinal analyses.
- Funded by the Natural Environment Research Council (NERC) and DOST-PCIEERD Newton Fund; linked to a Nature Communications (2025) paper.

## Data content and structure

- Datasets included:
  - Example GEE code to run satellite imagery analyses (Landsat-based).
  - Example MATLAB code and data to generate locational probabilities.
  - Example MATLAB code and data to produce longitudinal analyses.
  - Processed locational probability outputs for the ten catchments.
- Outputs are organized with detailed README documentation and subfolders (e.g., Abulug example) describing data structures and processing steps.
- Data products include binary active channel masks and locational probability rasters for each catchment.
- Spatial reference and resolution:
  - EPSG:32651 (WGS 84 / UTM zone 51N)
  - ~10 m × 10 m spatial resolution

## Methods and workflow (data processing pipeline)

- Active channel extraction:
  - Use Google Earth Engine to define trunk channel and apply a 3 km buffer.
  - Analyze atmospherically corrected Landsat 5, 7, 8 imagery in two-year time-windows from 1988–2019 (16 windows in total).
  - Cloud masking with CFmask; retain cloud-free pixels; bicubic resampling.
  - Active channel classification using NDVI and MNDWI with thresholds (MNDWI ≥ -0.4 and NDVI ≤ 0.2); rescale to [0,1].
  - Reduce each time-window’s image collection to a single image using the 10th percentile to capture active-channel extents.
  - Convert per-window results to binary masks and intersect to produce binary active channel masks; export as GeoTIFFs.
- Code versions:
  - Original GEE code for Landsat Collection 1 (1989–2019).
  - Updated code migrated to Landsat Collection 2 (including Landsat 9) for reproducibility with current data.
- Cleaning and quality control (MATLAB):
  - Remove artefacts by discarding small disconnected areas (<500 pixels).
  - Morphological closing to smooth edges (disk radius of 2 pixels).
  - Remove large, isolated features away from the trunk channel (<2500 pixels).
  - Manual GIS sense-check and editing to ensure masks align with the main trunk channel.
  - Note: some time-windows are data-poor due to Landsat availability or cloud cover, especially around Mindanao.
- Locational probability calculation:
  - For each pixel, p = sum(Wn Fn) across time-windows, where Fn is 1 if occupied, 0 otherwise.
  - Equal weighting Wn = 1/x, with x = number of time-windows for the catchment.
  - Locational probability lp ∈ [0,1], indicating channel occupancy frequency; low values indicate mobility, high values indicate stability.

## Data quality, limitations, and validation

- Quality checks show good visual agreement between classified active channels and satellite/aerial imagery.
- Data limitations:
  - Variable data availability across time-windows and catchments leads to some time-windows being data-poor.
  - Geographic pattern: catchments on Mindanao (e.g., Agusan, Mindanao) have fewer usable images.
- Output artifacts are addressed through standard image processing (removal of misclassifications, morphological operations, and manual editing).

## How to use and reuse

- Primary products:
  - Binary active channel masks per time-window.
  - Locational probability rasters showing river mobility dynamics for the ten catchments.
  - Longitudinal analyses outputs using the processed locational probabilities.
- Reproducibility:
  - Two GEE code versions ensure compatibility with both Landsat Collection 1 and 2 datasets.
  - MATLAB processing scripts enable QC, masking, and generation of longitudinal data.
  - Documentation and README files describe data structures and usage.
- Potential applications:
  - Explore river mobility patterns for hazard assessment and infrastructure resilience.
  - Apply Graf-style locational probability methodology to other rivers using newer imagery.
  - Self-serve exploration of outputs via the provided scripts and rasters.

## Files, data structure, and access notes

- Documentation files:
  - README.txt: general overview of all data sets.
  - README_01_GEE_Code.txt: data structure details for GEE code in Abulug_Example/01_GEE_CODE.
  - README_02_Process_Locational_Probabilities_from_GEE_Binary_Images.txt: data structure for probability processing.
  - README_03_Process_Locational_Probabilities_using_TopoToolbox_SWATHobj.txt: data structure for longitudinal analyses.
- Example data/products:
  - Abulug_Example/01_GEE_CODE (GEE scripts, deprecated/migrated versions).
  - Abulug_Example/02_Process_Locational_Probabilities_from_GEE_Binary_Images (MATLAB processing scripts and outputs).
  - Abulug_Example/03_Process_Locational_Probabilities_using_TopoToolbox_SWATHobj (longitudinal plotting and related data).
  - Processed_Locational_Probabilities (final probability rasters like Abulug_Locational_Probability.tif and others for ten catchments).
- Example outputs include per-catchment locational probability rasters and related metadata (e.g., Abulug_Locational_Probability.tif, Abulug_1988.tif, etc.).

## Relevance to Data Support goals

- Demonstrates end-to-end data work: data sourcing from satellite imagery, processing to derive meaningful data products (binary masks and locational probabilities), quality control, and packaging with reproducible code.
- Enables self-serve data exploration across topics by providing both data products and the code necessary to reproduce analyses or adapt methods to other regions.
- Highlights practical challenges in data integration across time, formats, and cloud-impacted imagery, offering concrete approaches to cleaning, QC, and documenting data lineage.