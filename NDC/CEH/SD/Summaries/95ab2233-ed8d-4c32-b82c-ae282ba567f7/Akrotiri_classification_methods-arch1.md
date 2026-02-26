# Akrotiri peninsula habitat map using remote sensing

## Overview
- Objective: create a baseline map of habitats and invasive species to support future hydro-ecological monitoring.
- Scale and data: 2-meter resolution using archived high-spatial-resolution WorldView imagery; targeted mapping of main vegetation communities and invasive Acacia and Casuarina.
- Temporal approach: combine imagery from two dates (spring and early summer) to leverage seasonal greenness differences.
- Field plan: collect drone imagery in 2020 to improve mapping of very small patches (<1 m2) and individual trees, but field work was interrupted by COVID-19.

## Data and Imagery Used
- Satellite imagery
  - WorldView-3 (WV-3), 1.2 m multispectral, 3 March 2018
  - WorldView-2 (WV-2), 2.0 m multispectral, 6 July 2018
  - April 2018 imagery (east and west swaths) with different viewing angles
- Processing and correction
  - Atmospheric correction with ENVI FLAASH
  - East/west imagery classified separately due to anisotropic reflectance
  - Resampling to ensure consistent spatial resolution; combined into a single 2 m, 16-band image stack
- Ground reference and field data
  - In-field reference data collected with Open Data Kit (ODK) using GPS points or polygons plus photos
  - Botanical expert involvement (Oliver Pescott)
  - First field campaign yielded limited reference points; second campaign planned for 2020 but canceled
  - Supplementary reference data from archived 2015/2017 non-native species shapefile (EIDC)

## Field Data and Reference Data
- Training and validation data
  - Initial plan to collect many reference points; half of data lost due to ODK fault
  - Google Maps and Sentinel-2 false-color data used for validation when WorldView data not available
- Vegetation/class schema
  - Generalized to: bare, lake, temporary water, salt marsh, rush salt meadow, garrigue, sparse vegetation, grass, mixed woodland, Eucalyptus, Acacia
  - Salt marsh and rush salt marsh mosaics include sub-classes (e.g., Chenopod, Suaeda, Tamarisk, etc.)
- Limitations in ground truth
  - Some vegetation communities and individual Acacia/Casuarina plants too small or subtle for WorldView detection
  - Second field campaign planned to deploy drone-based SfM (3D) data to improve mapping, but canceled due to COVID-19

## Processing and Classification
- Data preparation
  - Masked non-interest areas (sea, urban, arable land) using existing data and manual masking
- Classification approach
  - Object-based (feature-based) classification using ENVI Example Based Feature Extraction
  - Steps: image segmentation, compute spectral/spatial/texture attributes, create training samples, classify with KNN, SVM, or PCA, export as shapefile or map
- Output
  - 2 m resolution habitat map with 16 spectral/texture bands
  - Classification legend linked to specific vegetation/cover types
- Validation process
  - Aimed for 50% of reference data for evaluation; insufficient data collected in the first campaign
  - Stratified random point selection reviewed by botanical expert Jodey Peyton
  - Accuracy metrics derived from confusion matrix

## Validation and Accuracy
- Overall accuracy: 64%
- Class-level insights (as reported in the confusion matrix)
  - Mixed results with some classes showing higher user accuracies and others poorly represented due to limited training data
  - Notable confusion between Bare Ground and Sparse Vegetation
  - Casuarina and some other classes had limited or no computed accuracies due to sparse reference data
- Factors affecting accuracy
  - Ground data limitations from COVID-19 restrictions
  - Validation reliant on Google Maps and non-ideal reference data
  - Anisotropic reflectance from multi-angle imagery requiring separate east/west processing

## Limitations and Challenges
- Data limitations
  - COVID-19 impeded ground-truth collection and drone data collection
  - Insufficient validation/reference data to achieve higher accuracy
- Technical and methodological
  - Anisotropic reflectance across viewing geometries necessitated separate east/west classifications
  - Reliance on older field data and external shapefiles to supplement training
  - Potential misclassification due to spectral similarity between some classes and limited high-resolution ground truth
- Scale and detection
  - Some vegetation patches and individual invasive trees too small for 2 m WorldView resolution
  - Ground-truth details and administrative boundaries were not always available at the needed scale

## Outcomes and Future Directions
- Deliverable: a baseline 2 m habitat and invasive species map for monitoring hydro-ecological change
- Current accuracy: 64%, with acknowledged improvements possible via drone-based data and 3D modeling (Structure from Motion) for finer-scale mapping
- Ongoing data management and availability
  - Reference data and training samples planned to be expanded and archived for discoverability
- Reference data used
  - Pescott, Peyton, Mountford, Onete, and Martinou (2017) non-native plant GIS data for Cyprus Sovereign Base Areas

## References
- Pescott, O.; Peyton, J.; Mountford, J.; Onete, M.; Martinou, A. (2017). Non-native plant species GIS data from Cyprus Sovereign Base Areas, October 2015 and March 2017. NERC Environmental Information Data Centre. https://doi.org/10.5285/7c84e06d-bb1a-4aac-b1d7-33c11310d8a0