# Akrotiri peninsula habitat map using remote sensing

- Objective: Create a baseline, high-resolution map of habitats and invasive species on the Akrotiri peninsula to support future hydro-ecological monitoring, leveraging multi-date remote sensing to differentiate vegetation communities and detect Acacia and Casuarina.
- Outputs: A 2-meter resolution habitat/invasive species map derived from WorldView imagery, with major vegetation/cover types defined and labeled (including Acacia and Casuarina).

## Data inputs and sources

- Satellite imagery
  - 3 March 2018: WorldView-3, 1.2 m multispectral (8 bands)
  - 6 July 2018: WorldView-2, 2.0 m multispectral (8 bands)
  - April 2018: Two images (east and west), different viewing angles
- Preprocessing
  - Atmospheric correction with ENVI FLAASH
  - East/West and July imagery resampled to 2 m and combined into a single 2 m, 16-band image stack
- In situ reference data
  - Field collection with botanist over 2.5 days using Open Data Kit (ODK) to record GPS points/polygons and photos
  - Additional reference data from October 2015 and March 2017 (non-native species shapefile from EIDC)
- Planned data upgrades
  - Drone imagery (SfM) in 2020 to improve small patches (<1 m2) and detect individual Acacia/Casuarina, but cancelled due to COVID-19

## Data acquisition constraints and governance

- Field campaigns disrupted by COVID-19, severely limiting training and validation data
- Some reference points were lost due to an ODK fault
- WorldView data materialized late; reliance on Google Maps for validation introduced potential inaccuracies
- anisotropic reflectance effects addressed by classifying east and west images separately

## Methods and processing

- Classification approach
  - Object-based (feature-based) classification to exploit spectral, spatial, and textural attributes
  - Image processing steps:
    - Image segmentation to form objects
    - Compute spectral, spatial, and textural attributes for segments
    - Create and assign training samples to classes
    - Classify using KNN, SVM, or PCA (supervised)
    - Export results to shapefile or classified map
- Target classes
  - Bare, lake, temporary water, salt marsh, rush salt meadow, garrigue, sparse vegetation, grass
  - Mixed woodland, Eucalyptus, Acacia, Casuarina
  - Special mosaics within salt marsh/rush salt meadow composites
- Masking
  - Excluded non-interest areas (sea, urban, arable) to reduce confusion
- Validation approach
  - Due to limited field data, used stratified random points and visual interpretation against WorldView imagery
  - Confusion matrix calculation to estimate accuracy

## Validation results and outputs

- Overall accuracy: 64%
- Key notes
  - Validation constrained by limited ground truth data; some misclassifications likely inflated by use of Google Maps for validation reference
  - Notable confusion between Bare Ground and Sparse Veg; some classes (e.g., Casuarina) had limited validation signals
  - The dataset’s accuracy is expected to improve with augmented ground truth and drone-derived high-resolution data

## Findings and implications for data strategy

- Achievements
  - Delivered a baseline, multi-date, high-resolution habitat/invasive species map for hydro-ecological monitoring
  - Demonstrated an object-based workflow suitable for high-resolution imagery to capture texture and spatial patterns
- Data quality and gaps
  - Ground truth data was constrained by field access and technical issues, affecting training/validation quality
  - Some vegetation types and individual invasive trees (Acacia/Casuarina) were challenging to detect with WorldView alone
- Data management considerations
  - Importance of robust, loss-preventive field data collection (ODK workflows, backups)
  - Need for consistent reference data and improved validation methods beyond Google Maps
  - Documentation of sensor angles, cross-date alignment, and processing steps critical for reproducibility
- Next steps to enhance data value
  - Reintroduce drone-based SfM imagery for ultra-high resolution mapping of small patches and individual trees
  - Expand reference data collection (in-field points and polygons) across all vegetation communities
  - Integrate legacy non-native species data with current maps for improved change detection
  - Increase validation sample size and incorporate independent validation data to better quantify accuracy

## Key takeaways for Data Leaders

- Plan for multi-temporal data acquisition to capture seasonal differences and improve class separability
- Support object-based classification workflows when using high-resolution imagery to leverage texture and patterns
- Prioritize robust, in-field reference data collection and secure data pipelines to prevent loss of critical training points
- Establish clear metadata and provenance (sensor specs, viewing angles, processing steps, versioning) to enable reproducibility and future reuse
- Build a data governance approach that anticipates disruptions (e.g., pandemics) with contingency plans for ground truth collection and validation
- Recognize limitations of remote sensing alone; combine with high-resolution drone data and archival datasets to improve detection of small patches and invasive species

## References

- Pescott, O.; Peyton, J.; Mountford, J.; Onete, M.; Martinou, A. (2017). Non-native plant species GIS data from Cyprus Sovereign Base Areas, October 2015 and March 2017. NERC Environmental Information Data Centre. https://doi.org/10.5285/7c84e06d-bb1a-4aac-b1d7-33c11310d8a0