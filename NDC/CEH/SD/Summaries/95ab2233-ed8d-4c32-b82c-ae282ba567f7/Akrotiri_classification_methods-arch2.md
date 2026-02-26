# Akrotiri peninsula habitat map using remote sensing

## Objective
- Produce a baseline map of habitats and invasive species on the Akrotiri peninsula to enable future hydro-ecological monitoring.
- Aim for high thematic/spatial detail using suitable remote sensing data; map main vegetation communities and identify Acacia and Casuarina.
- Use multi-date imagery to exploit seasonal greenness differences; plan to add drone data later for fine-scale mapping (c. <1 m^2 patches) and individual trees.

## Data used

- Satellite imagery
  - WorldView-3 (WV-3): 1.2 m multispectral, March 3, 2018
  - WorldView-2 (WV-2): 2.0 m multispectral, July 6, 2018
  - July imagery covered the whole peninsular; April imagery split east/west with different viewing angles (anisotropic reflectance)
- Pre-processing
  - Atmospherically corrected with ENVI FLAASH
  - East and West images resampled for consistent 2 m resolution and merged into a single 2 m, 16-band image stack
- In situ reference data
  - Field campaign in 2019 with botanist Oliver Pescott; collected via Open Data Kit (ODK)
  - A second field campaign planned for 2020 but canceled due to COVID-19
  - Supplementary reference data from October 2015 and March 2017 on non-native species (EIDC)
- Classes and mapping focus
  - Main vegetation/cover types: bare, lake, temporary water, salt marsh, rush salt meadow, garrigue, sparse vegetation, grass, mixed woodland, Eucalyptus, Acacia
  - Salt marsh mosaics and rush salt meadow components explicitly recognised
- Validation data
  - Ground-truth points largely limited due to field access restrictions; validation used stratified random points plus interpretation with WorldView imagery and, where needed, Google/Sentinel basemaps

## Methodology

- Data preparation
  - Address anisotropic reflectance by classifying east and west imagery separately
  - Combine July and April data into a single 16-band stack
  - Mask non-interest areas (sea, urban, arable) to reduce processing and confusion
- Classification approach
  - Object-based (feature extraction) classification using ENVI
  - Image segmentation to create “objects,” then compute spectral, spatial, and textural attributes
  - Create and label training samples for each class
  - Classify with supervised methods (KNN, SVM, PCA)
  - Output as shapefile or classified cover map
- Validation
  - Limited reference data; used stratified random points assessed via confusion matrix
  - Overall accuracy reported as 64%
  - Per-class user and producer accuracies provided in the validation set; some values not fully resolved due to data limitations
- Validation constraints
  - Incomplete ground truth data from first field campaign; difficulties validating with Google/Sentinel basemaps
  - Second field campaign did not occur due to COVID-19

## Field data & training challenges

- COVID-19 restricted ground data collection, limiting training and validation datasets.
- Some vegetation communities and individual Acacia/Casuarina plants not detectable at WorldView resolution.
- Drone/SfM data planned for higher resolution mapping but canceled; would have improved detection of small patches and woody individuals.

## Results

- A baseline habitat and invasive species map at 2 m resolution was produced
- Classification outputs included Acacia and Casuarina as mapped classes
- Overall accuracy of 64% acknowledged; some misclassifications likely due to limited training data and validation constraints
- Validation indicated notable confusion between Bare ground and Sparse vegetation, among others, influenced by validation method (use of basemaps)

## Implications for monitoring and data governance

- Provides a baseline dataset for ongoing hydro-ecological monitoring and change detection
- Demonstrates the value and limitations of high-resolution imagery under real-world field constraints (COVID, limited ground truth)
- Highlights potential improvements through:
  - Additional ground truth collection (field campaigns, drone surveys)
  - Integration of drone-derived 3D data (SfM) to improve patch-level and canopy-level mapping
  - Enhanced data sharing and reuse, leveraging external datasets (e.g., EIDC) to bolster training/validation
- Notes anisotropy issues due to multiple viewing angles, suggesting careful pre-processing in future work

## Key references

- Pescott, O.; Peyton, J.; Mountford, J.; Onete, M.; Martinou, A. (2017). Non-native plant species GIS data from Cyprus Sovereign Base Areas, October 2015 and March 2017. NERC Environmental Information Data Centre. https://doi.org/10.5285/7c84e06d-bb1a-4aac-b1d733c11310d8a0