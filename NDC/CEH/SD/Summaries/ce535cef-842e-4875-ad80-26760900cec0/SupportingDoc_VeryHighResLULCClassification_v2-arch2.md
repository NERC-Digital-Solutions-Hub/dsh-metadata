# Land Cover/Use Classes

## Overview
- Classification of land cover/use in four areas of interest within the Corridor Ankeniheny-Zahamena (CAZ), Madagascar.
- Objective: produce standardized land cover outputs using very high-resolution imagery and an open-source processing workflow.
- Approach: supervised classification with a random forest model, using a consistent set of land cover classes and features derived from pan-sharpened SPOT 6 imagery.

## Land Cover / Use Classes
- 1 Closed Canopy Forest
- 2 Tree Fallow
- 3 Shrub Fallow
- 4 Bare
- 5 Water
- 6 Cloud/Shadow
- 7 Tany Maty (Dead land) — Only present in ZOI1, ZOI3, and ZOI4
- 8 Permanent Agriculture — Only present in ZOI4
- 0 NoData

## Data Transformation Methods
- SPOT 6 imagery used for classification across four zones (ZOI1–ZOI4), with:
  - ZOI1: Acquisition Date = 07/21/2013; Incidence Angle = 21°; Resolution = SPOT 6 (6m); Filename = ZOI1_LU_classification.tif
  - ZOI2: Acquisition Date = 07/21/2013; Incidence Angle = 21°; Resolution = SPOT 6 (6m); Filename = ZOI2_LU_classification.tif
  - ZOI3: Acquisition Date = 09/25/2013; Incidence Angle = 22.6°; Resolution = SPOT 6 (6m); Filename = ZOI3_LU_classification.tif
  - ZOI4: Acquisition Date = 05/23/2013; Incidence Angle = 21°; Resolution = SPOT 6 (6m); Filename = ZOI4_LU_classification.tif

## Analytical Methods
- Software ecosystem:
  - QGIS for imagery visualization and digitizing training data.
  - Monteverdi/OTB for pan-sharpening, image segmentation, and texture processing (able to handle very large images).
  - R for feature generation and classification (random forest).
- Preprocessing:
  - Pan-sharpening to create 4-band multispectral imagery at 1.5m resolution; resampling to align with panchromatic band.
  - Image segmentation following smoothing (mean-shift), segmentation, merging small segments, and creating vector coverage of segments.
- Texture and feature extraction:
  - Haralick texture extraction (two variants: Simple and Higher Order); 12 texture metrics retained.
  - Texture bands: Simple (bands 3,4,5,7,8) and Higher Order (bands 1,2,3,4,5,7,9).
  - Feature set comprises 17 input bands: four pan-sharpened SPOT 6 bands, twelve texture bands, and NDVI.
- Feature calculations:
  - For each segment, compute:
    - Mean, standard deviation (SD) for each band.
    - Mean, SD, and coefficient of variation after clipping 40% of pixels (removing 20% lowest and 20% highest DNs) to reduce outliers.
    - Median for each band.
  - Implemented via R script using zonal statistics defined by the segmented image.
- Training data:
  - Training segments created by digitizing and attributing polygons to include multiple segments of the same class within a single polygon feature.
- Classification approach:
  - Supervised classification using a random forest algorithm (randomForest package in R).

## Outputs and Workflow Goals
- Produce land cover maps for the four CAZ zones with standardized class definitions.
- Maintain reproducibility through an open-source workflow (QGIS, Monteverdi/OTB, R) and explicit preprocessing, feature extraction, and classification steps.
- Prepare data and features in a way that supports data sharing and reuse, aligning with the Analysts Monitoring the Environment aim of transparent, queryable environmental datasets.