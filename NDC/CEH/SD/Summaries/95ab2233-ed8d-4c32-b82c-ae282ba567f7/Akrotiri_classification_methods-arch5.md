# Akrotiri peninsula habitat map using remote sensing

- Objective: Create a baseline, high-resolution map of habitats and invasive species on the Akrotiri peninsula to support future hydro-ecological change monitoring. The map aims to distinguish main vegetation communities and identify Acacia and Casuarina species, using a 2-meter resolution.

- Data sources and imagery:
  - Archived WorldView imagery:
    - 3 March 2018: WorldView-3, 1.2 m multispectral (8 bands)
    - 6 July 2018: WorldView-2, 2.0 m multispectral (8 bands)
    - April 2018: two images (east and west of the peninsula) from different swaths
  - Key processing decisions:
    - Different viewing angles cause anisotropic reflectance; east and west images classified separately
    - Atmospherically corrected with ENVI FLAASH
    - July and April imagery resampled to consistent 2 m resolution and combined into a single 2 m, 16-band image stack

- In situ reference data and field work:
  - Field data collection with ODK app to record reference areas representing vegetation communities; data included GPS points/polygons and photos
  - Field campaigns:
    - First campaign (2019): 2.5 days with botanical expert; used mobile base maps (WorldView planned but not materialized in time)
    - Planned second campaign (2020): drone imagery to improve mapping of small patches and individual invasive trees
    - COVID-19 disruptions halted the second campaign; limited additional ground data
  - Supplementary reference data:
    - 2015 and 2017 non-native plant species shapefile from the EIDC
  - Vegetation classes mapped at a generalized level, including bare, lake, temporary water, salt marsh, rush salt meadow, garrigue, sparse vegetation, grass, mixed woodland, Eucalyptus, Acacia

- Image classification and processing:
  - Pre-processing: masking non-interest areas (sea, urban, arable land) to reduce confusion
  - Classification approach: object-based (feature extraction) rather than pixel-based to leverage texture and spatial patterns
  - Workflow:
    - Image segmentation to create objects (segments)
    - Compute spectral, spatial, and textural attributes for segments
    - Create and label training samples for each class
    - Classify using supervised methods (KNN, SVM, or PCA) and train with the samples
    - Export results to shapefile or classified map
  - Outcome visualizations included a legend and example classification results

- Validation and accuracy:
  - Validation relied on a stratified sample due to limited ground truth data
  - Use of 50% reference data for validation; accuracy assessed with a confusion matrix
  - Overall accuracy achieved: 64%
  - Notable validation caveats:
    - Ground truth limited due to COVID; reliance on Google Maps for some validation introduced potential misclassifications
    - Significant confusion between Bare Ground and Sparse Veg, contributing to reduced accuracy
    - Omission and commission errors varied by class; some classes lacked sufficient reference data for robust assessment

- Key findings and outputs:
  - A 2 m resolution baseline map of habitats and invasive species suitable for future hydro-ecological monitoring
  - Invasive species targeted: Acacia and Casuarina
  - Recognized that ground data collection restrictions and imaging constraints limited classifier performance and validation robustness

- Governance, metadata, and data stewardship considerations:
  - Data provenance and sources:
    - Satellite imagery from WorldView (archived data) with explicit processing steps (atmospheric correction, resampling, 16-band stack)
    - In situ reference data collected via ODK, with field notes and photos; some data loss due to technical faults
    - Supplementary legacy data from EIDC (2015/2017) for non-native species
  - Data quality and documentation needs:
    - Detailed metadata required: sensor/satellite, acquisition dates, viewing angles, processing chain (ENVI FLAASH parameters), coordinate reference system, and spatial resolution
    - Documentation of training/validation dataset composition, geographic coverage, and class definitions
    - Clear lineage from raw imagery to final classified map and shapefiles
  - Data accessibility and updates:
    - Final products include shapefiles and a 2 m classified map; future updates depend on new field data (ideally including drone/SFM-derived imagery) and additional ground-truth collection
    - Plan to handle anisotropy by maintaining separate east/west classifications or harmonizing them in updates
  - Limitations and future improvements:
    - COVID-19 restrictions significantly limited ground truth data and the planned 2020 drone campaign
    - Need for more comprehensive reference data to improve accuracy and validation reliability
    - Potential improvements with drone-based high-resolution imagery (SfM) to better resolve small patches and individual invasive trees
    - Consider integrating older reference data (2015/2017) with current data for temporal consistency if appropriate

- Practical implications for data stewards:
  - Ensure robust metadata and data provenance for satellite and in situ data
  - Implement clear data governance around sharing, licensing, and updates, including the potential embargo or restricted access to ground-truth datasets
  - Maintain and quality-check the training and validation datasets to support reproducibility and future model improvements
  - Plan for iterative updates as new imagery and field data become available, preserving versioning and traceability of changes to the habitat/class definitions and classifications