# Land Cover/Use Classes

## Purpose and scope
- Document describing land cover/use classification for four areas of interest in the Corridor Ankeniheny-Zahamena (CAZ), Madagascar.
- Classes defined for classification: Closed Canopy Forest (1), Tree Fallow (2), Shrub Fallow (3), Bare (4), Water (5), Cloud/Shadow (6), Tany Maty (Dead land) (7; present only in ZOI1, ZOI3, ZOI4), Permanent Agriculture (8; present only in ZOI4), NoData (0).
- Approach is a supervised classification intended to support environmental monitoring and decision-making.

## Land Cover/Use Classes
- Class 1: Closed Canopy Forest
- Class 2: Tree Fallow
- Class 3: Shrub Fallow
- Class 4: Bare
- Class 5: Water
- Class 6: Cloud/Shadow
- Class 7: Tany Maty (Dead land) — present in ZOI1, ZOI3, ZOI4
- Class 8: Permanent Agriculture — present in ZOI4
- Class 0: NoData

## Data transformation methods
- Imagery: SPOT 6 used for classification; four zones of interest (ZOI1–ZOI4) with 6 m resolution.
- Zone-specific metadata:
  - ZOI1: Acquisition 07/21/2013; Incidence Angle 21°; Filename ZOI1_LU_classification.tif
  - ZOI2: Acquisition 07/21/2013; Incidence Angle 21°; Filename ZOI2_LU_classification.tif
  - ZOI3: Acquisition 09/25/2013; Incidence Angle 22.6°; Filename ZOI3_LU_classification.tif
  - ZOI4: Acquisition 05/23/2013; Incidence Angle 21°; Filename ZOI4_LU_classification.tif
- Data handling notes: pan-sharpening and resolution matching; data prepared for segmentation and feature extraction.

## Analytical methods and processing workflow
- Tools: Open-source software including QGIS, Monteverdi/OTB, and R.
- Preprocessing steps:
  - Pan-sharpening to create 4-band multispectral imagery at 6 m resolution.
  - Image segmentation to partition imagery into meaningful segments.
- Texture analysis:
  - Haralick texture extraction using Monteverdi/OTB; two variants used: Simple and Higher Order.
  - Subset selection: 12 most significant texture variables retained for modelling.
  - Texture metrics derived from selected bands: simple texture bands (bands 3,4,5,7,8) and higher-order texture bands (bands 1,2,3,4,5,7,9).
- Feature generation:
  - Input bands for feature calculation: 4 pan-sharpened SPOT 6 bands, 12 texture bands, and an NDVI band (total 17 bands).
  - Features computed per segment using R:
    - Mean and standard deviation per band.
    - Mean, standard deviation, and coefficient of variation after clipping/removing outliers (removing 40% of pixels via 20% trimming and 20% of highest DN values).
    - Median per band.
  - Zonal statistics defined by segments to derive predictor variables for each segment.
- Training data and modelling:
  - Segments created and labeled by digitizing polygons; segments within a single polygon may belong to the same class.
  - Supervised classification using a random forest algorithm (R, randomForest package).
- Output classification:
  - Land cover/use maps produced for each zone, with file names similar to ZOI1_LU_classification.tif, etc., at 6 m resolution.

## Outputs and implications for monitoring
- Produces high-resolution land cover/use maps for the CAZ zones.
- Class labels and raster outputs enable monitoring of deforestation, agricultural expansion, and land degradation patterns.
- Methodology emphasizes reproducibility and transparency through open-source tools and explicit feature and preprocessing steps.

## Data governance and openness (relevance to monitoring frameworks)
- Uses open-source software (QGIS, Monteverdi/OTB, R) to enhance transparency and reproducibility.
- Detailed documentation of preprocessing, segmentation, texture extraction, feature calculation, and modeling supports auditing and future updates.
- Outputs are classificatory rasters with explicit zone-specific provenance (filenames and acquisition details), aiding traceability and data management for monitoring programs.