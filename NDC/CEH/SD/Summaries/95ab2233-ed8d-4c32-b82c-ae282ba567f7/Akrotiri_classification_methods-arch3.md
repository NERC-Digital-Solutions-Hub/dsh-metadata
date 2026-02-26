# Akrotiri peninsula habitat map using remote sensing

## Objective and scope
- Baseline map of habitats and invasive species for future hydro-ecological monitoring.
- Aim to map main vegetation communities and identify Acacia and Casuarina; plan to use 2 m resolution WorldView imagery and seasonal differences between dates.
- Ground data collection planned to improve accuracy, including drone imagery for higher spatial detail, but COVID-19 restrictions curtailed field campaigns.

## Data sources and imagery
- Satellite imagery purchased from archives:
  - March 3, 2018: WorldView-3, 1.2 m multispectral (8 bands)
  - July 6, 2018: WorldView-2, 2.0 m multispectral (8 bands)
  - April 2018: East/West swaths with different viewing angles
- Anisotropic reflectance acknowledged due to different viewing angles; east and west images were classified separately.
- All imagery atmospherically corrected with ENVI FLAASH; resampled to a consistent 2 m, 16-band stack for integration.
- Ground reference data intended for training/validation collected in the field, plus archived non-native species shapefile data from 2015–2017.

## Field data, training, and reference data
- In-field training/validation data collected over 2.5 days with botanical expert; used via ODK (Open Data Kit).
- Initial field campaign limited by COVID; a second campaign planned for 2020 (drone data and SfM for 3D mapping) but canceled.
- ODK data losses occurred due to technical faults; supplementary reference points gathered from archived datasets (2015/2017) to bolster training.
- Reference data used to represent vegetation communities and cover types; base maps for orientation included Google Maps or Sentinel-2 false-color composites when WorldView data were unavailable.

## Processing workflow and classification approach
- Preprocessing:
  - Separate processing for east and west images due to anisotropy; final 2 m 16-band image stack produced.
- Feature-based (object-based) classification:
  - Image segmentation to create objects (segments).
  - Computation of spectral, spatial, and textural attributes for segments.
  - Interactive assignment of training samples to classes; multiple classes created.
  - Whole-image classification using supervised methods (KNN, SVM, PCA) with corresponding training samples.
  - Outputs exported as shapefiles or classified cover maps.
- Rationale: object-based approach leverages texture and spatial patterns in addition to spectral information, especially valuable at high spatial resolution.

## Classes and map content
- Generalized vegetation/cover types identified:
  - Bare, lake, temporary water
  - Salt marsh and rush salt meadow mosaics
  - Garrigue (shrubland), sparse vegetation, grass, mixed woodland
  - Eucalyptus, Acacia, Casuarina
- Specific mixed mosaics within salt marsh and rush salt meadow categories noted (e.g., chenopod, Suaeda, Tamarisk, reed-associated components).

## Validation and accuracy
- Validation strategy: compare with reference points; 50% of reference data typically used, but insufficient data collected during initial field campaign necessitated stratified, class-based random point selection reviewed over WorldView imagery.
- Accuracy assessment conducted via confusion matrix; overall accuracy reported as 64%.
- Limitations affecting accuracy:
  - Limited ground-truth data due to COVID-19 restrictions
  - Use of Google Maps for some validation steps potentially affecting accuracy
  - Notable confusion between certain classes (e.g., Bare Ground vs. Sparse Veg) acknowledged

## Results and interpretation
- Outcome: a baseline 2 m resolution habitat and invasive species map suitable for future hydro-ecological monitoring.
- The COVID-19 disruption reduced training and validation data, contributing to lower accuracy.
- The approach demonstrates feasibility of detecting main vegetation communities and invasive species with high-resolution remote sensing, albeit with limitations tied to ground-truth data availability and validation sources.

## Limitations, challenges, and governance implications
- Key challenges:
  - Data availability and access constraints, including timely procurement of imagery and ground data
  - Incomplete ground-truth data due to field-campaign cancellations
  - Anisotropic effects from multi-date imagery requiring separate processing
  - Incomplete metadata and data provenance complications affecting verification
- Governance considerations:
  - High reliance on purchased commercial imagery; data sharing and metadata standardization are critical for reproducibility
  - Ground-truth and training data management (ODK data integrity, archival references) are essential components of transparent monitoring outputs
  - Data quality management and validation strategies must account for potential disruptions (e.g., pandemics) that affect field activities

## Next steps and recommendations
- Reintroduce drone-based SfM data collection when feasible to improve sub-meter mapping of small patches and individual invasive trees.
- Expand and secure ground-truth datasets to strengthen training and validation; consider alternative validation sources to reduce dependence on external base maps.
- Improve metadata completeness and data governance to facilitate openness and reproducibility, while balancing data-sharing constraints.
- Reassess and refine classification workflow to mitigate misclassification between closely related classes (e.g., Bare vs. Sparse Veg) as more ground-truth becomes available. 
- Plan iterative updates of the map as new imagery and validation data become available to ensure up-to-date monitoring of hydro-ecological change.