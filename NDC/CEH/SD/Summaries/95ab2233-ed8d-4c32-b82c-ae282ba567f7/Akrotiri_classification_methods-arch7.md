# Akrotiri peninsula habitat map using remote sensing

## Objective
- Produce a baseline map of habitats and invasive species to enable future hydro-ecological monitoring.
- Map main vegetation cover types and identify invasive Acacia and Casuarina trees.
- Achieve meaningful detail by leveraging high-resolution remote sensing data and seasonal imagery.

## Data sources and imagery
- Satellite imagery
  - WorldView-3 (WV-3): 1.2 m multispectral (8 bands), captured 3 March 2018
  - WorldView-2 (WV-2): 2.0 m multispectral (8 bands), captured 6 July 2018
- Image characteristics and processing
  - July 2018 imagery covered the whole peninsular; April 2018 imagery split east/west swaths with different viewing angles
  - Anisotropic reflectance required separate east/west processing
  - Atmospherically corrected with ENVI FLAASH
  - East and West, and July/April images were resampled to a consistent 2 m resolution and combined into a single 2 m, 16-band image stack
- In situ reference data and fieldwork
  - Field data collected with Open Data Kit (ODK) for training/validation
  - First field campaign (2019) involved 2.5 days with botanical expert; data issues included partial data loss due to technical faults
  - A planned second field campaign in 2020 (including drone data collection) aimed to improve detection of small patches and individual Acacia/Casuarina trees
  - COVID-19 cancelled the second campaign; additional reference data: archival non-native plant species data from October 2015 and March 2017

## Field data and training samples
- Training and validation points sought to be spatially random across vegetation communities
- Ground truth opportunities were limited by COVID-19, impacting classifier calibration and validation

## Vegetation and cover classes
- Main classes used in the thematic map:
  - Bare
  - Lake
  - Temporary water
  - Salt marsh
  - Rush salt meadow
  - Garrigue
  - Sparse vegetation
  - Grass
  - Mixed woodland
  - Eucalyptus
  - Acacia
  - Casuarina
  - Masked (background/noise)
- Salt marsh and rush salt meadow: mosaics of multiple sub-communities listed (e.g., Chenopod, Suaeda, Tamarisk, Elymus, etc.)

## Image classification approach
- Object-based image analysis (OBIA) using ENVI Example Based Feature Extraction
  - Benefits: leverages spectral, spatial, and textural attributes; more effective than pixel-based classification at high resolution
  - Workflow:
    - Image segmentation to form objects (segments)
    - Compute spectral, spatial, and textural attributes for segments
    - Create and label training samples for each class
    - Classify the entire image with supervised methods (KNN, SVM, or PCA) using training samples
    - Export results as shapefiles or classified maps
- Pre-classification masking
  - Areas outside interest (sea, urban/built-up fabric, arable land) masked to reduce confusion

## Validation and accuracy
- Validation approach
  - Ideally 50% of reference data used for validation via confusion matrix
  - Limited reference data from the first field campaign required stratified random point selection and expert interpretation for validation
- Results
  - Overall accuracy reported: 64%
  - Per-class accuracy and error metrics described in the confusion matrix (values partially obscured in the text)
  - Notable issue: large potential validation bias due to using Google Maps for validation and misclassification between Bare ground and Sparse Veg
- Implications
  - COVID-19 restrictions reduced training/validation data, contributing to lower accuracy
  - Some vegetation communities and single Acacia/Casuarina plants may not be detectable with WorldView alone

## End-to-end summary and limitations
- Outcome: Baseline 2 m resolution habitat and invasive species map produced from WorldView data
- Limitations due to pandemic
  - Ground truth collection severely constrained
  - Second field campaign and drone-based SfM data could have substantially improved mapping of small patches and woody individuals
- Accuracy interpretation
  - 64% overall accuracy likely conservative given validation approach; some misclassifications may arise from validation data sources and anisotropic imagery
- Future directions
  - Use drone data and SfM-derived 3D landscape information to refine small patches and woody species detection
  - Expand reference data and improve validation practices to increase classifier robustness
  - Consider additional data sources or later imagery to enhance temporal monitoring and change detection

## References
- Pescott, O.; Peyton, J.; Mountford, J.; Onete, M.; Martinou, A. (2017). Non-native plant species GIS data from Cyprus Sovereign Base Areas, October 2015 and March 2017. NERC Environmental Information Data Centre. https://doi.org/10.5285/7c84e06d-bb1a-4aac-b1d7-33c11310d8a0