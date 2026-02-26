# Supporting documentation for 'Satellite-derived geomorphic river mobility for ten catchments in the Philippines, 1988-2019'

## Overview
- Dataset provides satellite-derived information on geomorphic river mobility for ten catchments in the Philippines.
- Uses locational probability to map the proportion of time a river channel occupies a given location, quantified for ~600 km2 of riverbed.
- Aims to support prediction and resilience planning for river-related hazards in dynamic landscapes.
- Includes example Google Earth Engine (GEE) and MATLAB codes to replicate analyses, and outputs for each catchment.

## Data Content
- (1) Example GEE codes to run satellite imagery analyses.
- (2) Example MATLAB codes and data to generate locational probabilities.
- (3) Example MATLAB codes and data to produce longitudinal analyses.
- (4) Processed locational probability outputs for the ten catchments.
- Data and methods are documented in Boothroyd et al. (2025) Nature Communications.

## Methods and Workflow
- Extraction of binary active channel masks from Landsat imagery using GEE.
- Active channel defined as bankfull extent including wetted channel and unvegetated alluvial deposits; trunk channel buffered by 3 km to define ROI.
- Time-windows: two-year periods from 1988 to 2019 (16 windows) chosen to maximize cloud-free observations.
- Image collection: all available atmospherically corrected Landsat 5, 7, and 8 data within each window; CFmask used for cloud/shadow masking; bicubic resampling per image.
- Classification: active channel identified with NDVI and MNDWI; thresholding and an intersection approach (MNDWI ≥ -0.4 and NDVI ≤ 0.2) with rescaled values to [0,1].
- Output per window: single image via 10th percentile reducer to summarize varying image counts; binary masks produced by AND operation; exported as GeoTIFFs to Google Drive.
- Code versions: (i) original code for Landsat Collection 1 (1989–2019) and (ii) updated code for Landsat Collection 2 (including Landsat 9) to ensure reproducibility with current data.

## Data Processing and Cleaning
- Artefact removal in MATLAB to clean binary masks:
  - Remove small disconnected areas < 500 pixels.
  - Apply one iteration of morphological closing with a 2-pixel disk.
  - Remove large isolated features < 2500 pixels away from trunk channel.
- Final masks reviewed in GIS; manual editing to remove non-channel features adjacent to tributaries.
- Note on data availability: some time-windows are data-poor due to variable Landsat data availability and cloud cover, especially in Mindanao (e.g., Agusan and Mindanao catchments).

## Locational Probability Calculation
- Locational probability (lp) for each pixel computed from binary active channel masks across time-windows:
  - p = sum(Wn * Fn) for all n, where Fn is 1 if pixel is occupied in time-window n, else 0.
  - Weights Wn = 1.0 / x, with x the total number of time-windows for the catchment (equal weighting across windows).
- lp ranges from 0 (never occupied) to 1 (always occupied).
- Interpretation: low lp indicates high mobility; high lp indicates channel stability.

## Spatial Reference and Resolution
- Spatial reference: EPSG:32651 - WGS 84 / UTM zone 51N.
- Spatial resolution: approximately 10 m × 10 m.
- Quality control: classified active river channels showed good visual agreement with Landsat and Google Earth imagery.

## Data Structure and Access
- Data structure details provided via README files in the dataset:
  - General overview and subfolder-specific READMEs (e.g., Abulug examples).
  - Processed locational probabilities and associated MATLAB code.
  - Example files include Abulug_Locational_Probability.tif and related outputs for all ten catchments.
- Outputs include locational probability rasters and associated processing scripts, organized per catchment.

## Reproducibility and Code Versions
- Two GEE code versions provided:
  - GEE_Code_Abulug_Deprecated.txt (original)
  - GEE_Code_Abulug_Migrated.txt (updated for Collection 2)
- Emphasis on reproducibility and applicability to other rivers using newer Landsat data.

## Limitations and Considerations
- Data gaps due to variable satellite imagery availability and cloud cover.
- Some catchments require manual GIS review to ensure masks remain representative of the trunk channel.
- The data reflect historical to near-present conditions (1988–2019) within the Philippines’ dynamic river systems.

## References
- Boothroyd, R.J., Williams, R.D., Hoey, T.B., et al. (2025). Big data show idiosyncratic patterns and rates of geomorphic river mobility. Nature Communications.
- Related methodological references cited in the document (e.g., on locational probabilities, NDVI/MNDWI thresholds, Landsat data availability, and morphodynamic analyses).