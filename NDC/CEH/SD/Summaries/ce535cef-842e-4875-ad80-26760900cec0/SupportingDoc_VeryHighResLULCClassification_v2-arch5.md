# Land Cover/Use Classes

- Overview
  - Defines land cover/use classes with class numbers:
    - 1 Closed Canopy Forest
    - 2 Tree Fallow
    - 3 Shrub Fallow
    - 4 Bare
    - 5 Water
    - 6 Cloud/Shadow
    - 7 Tany Maty (Dead land) [present only in ZOI1, ZOI3, ZOI4]
    - 8 Permanent Agriculture [present only in ZOI4]
    - 0 NoData
  - The classification was produced for four areas of interest in the Corridor Ankeniheny-Zahamena (CAZ), Madagascar.

- Data Inputs
  - SPOT 6 imagery used for all classifications at 6 m resolution.
  - Four zones of interest (ZOI1–ZOI4) with acquisition dates:
    - ZOI1: 2013-07-21
    - ZOI2: 2013-07-21
    - ZOI3: 2013-09-25
    - ZOI4: 2013-05-23
  - Incidence angles around 21–22.6°, filenames for each zone (e.g., ZOI1_LU_classification.tif).
  - Included classes beyond NoData: Closed Canopy Forest, Tree Fallow, Shrub Fallow, Bare, Water, Cloud/Shadow, Tany Maty, Permanent Agriculture.

- Data Transformation and Preprocessing
  - Pan-sharpening and resampling to SPOT 6 6 m resolution to produce a four-band multispectral image per zone.
  - Image preprocessing steps:
    - Superimpose/resample multispectral data to match panchromatic resolution.
    - Pan-sharpen to create 4-band multispectral imagery.
  - Image segmentation workflow (per zone):
    - Smooth with mean-shift filter.
    - Segment the smoothed image to create segments.
    - Merge small segments using a threshold.
    - Create vector polygon coverage from the segmented image.
  - Texture analysis:
    - Haralick texture extraction (Simple and Higher Order) using Monteverdi/OTB.
    - Selected 12 texture metrics; combined with spectral bands for modeling.
  - Input features for modeling:
    - 17 bands in total: 4 pan-sharpened SPOT 6 bands + 12 texture bands + NDVI.

- Feature Engineering and Data Preparation
  - For each segment, compute predictor variables using an R script:
    - Mean, standard deviation, and coefficient of variation per band (after clipping 40% of pixels to reduce outliers: removing 20% from low end and 20% from high end).
    - Median per band.
  - Training data creation:
    - Digitize and attribute polygons to include several segments of the same class within a single polygon feature.

- Modeling and Classification
  - Classification approach:
    - Supervised classification using the randomForest algorithm in R.
  - Model details:
    - Features derived from 17 bands (4 SPOT bands, 12 texture bands, NDVI).
    - Selection of the 12 most significant variables from the random forest results.
  - Output:
    - Classified land cover/use rasters for each zone (ZOI1–ZOI4).

- Software and Reproducibility
  - Open-source tools used:
    - QGIS for visualization and digitizing training data.
    - Monteverdi/OTB for pan-sharpening, segmentation, and texture processing.
    - R for feature calculation, statistical summarization, and random forest classification.
  - Workflow is documented with explicit parameters and scripts (R scripts for feature extraction and classification).

- Metadata and Data Governance Considerations for Data Stewards
  - Clear, zone-specific metadata:
    - Acquisition dates, incidence angles, resolutions, and filenames per zone.
    - Class definitions and presence notes (e.g., certain classes only in specific ZOIs).
  - Data provenance and reproducibility:
    - Step-by-step preprocessing, feature extraction, and modeling processes are documented.
    - Use of open-source software and explicit feature calculations support traceability and reuse.
  - Data interoperability and sharing:
    - Output classifications are organized by zone and named consistently (e.g., ZOI1_LU_classification.tif).
    - Alignment of class definitions across zones facilitates cross-dataset analysis.
  - Quality and governance considerations:
    - Metadata about data availability (e.g., zone-specific class presence) informs disclosure and usage constraints.
    - The approach emphasizes standardization of inputs, features, and model parameters to support quality assurance and future updates.

- Practical Implications for Data Stewardship
  - Ensures transparent, reproducible methodology for land cover classification in CAZ.
  - Supports data users with clearly defined classes, zone-specific notes, and processed product files.
  - Highlights the need for ongoing data updates and versioning to reflect new imagery or revised training data.