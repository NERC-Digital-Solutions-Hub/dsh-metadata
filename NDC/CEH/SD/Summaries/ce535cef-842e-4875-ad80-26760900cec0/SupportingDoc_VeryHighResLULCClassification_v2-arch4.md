# Land Cover/Use Classes

- Land cover/use categories and class numbers:
  - Closed Canopy Forest (Class 1)
  - Tree Fallow (Class 2)
  - Shrub Fallow (Class 3)
  - Bare (Class 4)
  - Water (Class 5)
  - Cloud/Shadow (Class 6)
  - Tany Maty (Dead land) (Class 7) — present only in ZOI1, ZOI3, ZOI4
  - Permanent Agriculture (Class 8) — present only in ZOI4
  - NoData (Class 0)

- Data Transformation Methods
  - Satellite imagery: SPOT 6 used for all classifications; four zones of interest (ZOI1–ZOI4) with 6 m resolution; acquisition dates and file names provided.
  - Pan-sharpening: SPOT 6 multispectral bands resampled to 1.5 m using pan-sharpening; four bands per zone; filenames recorded (e.g., ZOI1_LU_classification.tif).
  - Preprocessing steps include: resampling to common resolution, pan-sharpening to 4-band multispectral images, and image segmentation setup.

- Analytical Methods
  - Study area: four areas of interest within the Corridor Ankeniheny-Zahamena (CAZ), Madagascar.
  - Software stack (open source):
    - QGIS for visualization, digitizing training data, and overall workflow management.
    - Monteverdi/OTB for accessing processing tools, pan-sharpening, image segmentation, and texture processing.
    - R for feature extraction, statistics, and classification.
  - Image processing workflow:
    - Pan-sharpening to create 4-band multispectral images at the panchromatic resolution.
    - Image segmentation using a mean-shift approach, followed by merging small segments into larger ones, and creating a vector coverage of segments.
    - Texture extraction using Haralick metrics (Simple and Higher Order versions) to generate texture layers from the panchromatic image.
    - Feature generation:
      - 17 input bands: 4 pan-sharpened SPOT 6 bands, 12 texture bands, and NDVI.
      - For each segment, computation of features via an R script:
        - Mean and standard deviation per band.
        - Mean, standard deviation, and coefficient of variation after clipping 40% of outliers (remove 20% from low end and 20% from high end).
        - Median per band.
  - Variable selection and model:
    - The 12 most significant texture variables were selected based on random forest results.
    - Training data: segments labeled by digitizing and attributing polygons with multiple segments per class within a single polygon.
    - Classification: supervised approach using the randomForest package in R.

- Data Governance and Reproducibility
  - Explicit, documented processing steps and metadata (acquisition dates, incidence angles, resolutions, and file names) support discoverability and auditability.
  - Workflow relies on open-source tools and script-based feature extraction and classification, aiding reproducibility and potential reuse by other teams.

- Implications for Data Leaders
  - End-to-end data lifecycle: from raw SPOT 6 imagery to labeled land-cover classifications, with explicit preprocessing, feature engineering, and supervised learning steps.
  - Data quality and standards: clear class definitions and metadata enable consistent usage across partners; texture features and segmentation parameters are explicitly described, supporting quality control.
  - Collaboration and co-ownership: open-source tooling and clearly delineated steps facilitate cross-team collaboration and potential extension to other regions.
  - Data discoverability and stewardship: documented data products (classification outputs and training data structure) and accessible codebase support governance, metadata management, and future updates.
  - Capacity and skills: requires multi-disciplinary expertise (remote sensing, GIS, statistics, and R programming) and careful management of data provenance and versioning for ongoing data products.