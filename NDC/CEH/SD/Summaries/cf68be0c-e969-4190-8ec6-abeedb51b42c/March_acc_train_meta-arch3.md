# Definitions and Training/Accuracy Assessment Datasets for Prunus spinosa Classification

## Overview
- Defines pixel categories and lists the training and accuracy assessment datasets used for maximum likelihood classification of Prunus spinosa at two spatial scales (3 cm and 7 cm).

## Key definitions
- Edge pixels: Pixels at the edge of floral unit clusters or mixed with other features.
- Pure pixels: Pixels deeper in clusters, less likely to be mixed with other features.
- Other: Regions not comprising the focal species (e.g., branches, soil, green vegetation).

## Training pixels
- Purpose: Full training sets used to apply different variants by removing or merging regions of interest and to manually set classification thresholds.
- Datasets (shapefiles, polygons representing ROIs):
  - Mar_train_other: ‘Other’ category training data for maximum likelihood classifications; used to train both 3 cm and 7 cm classifications.
  - Mar_train_prunus_pure: Prunus spinosa (blackthorn) training data; used for both 3 cm and 7 cm classifications.
  - Mar_train_prunus_edge: Prunus spinosa training data for edges; used for both 3 cm and 7 cm classifications.

## Accuracy assessment datasets (3 cm classifications)
- Shapefiles containing polygons representing validation pixels for accuracy assessment:
  - Mar_acc_prunus_pure_3cm: Prunus spinosa 'pure' pixels for 3 cm accuracy assessment.
  - Mar_acc_prunus_edge_3cm: Prunus spinosa 'edge' pixels for 3 cm accuracy assessment.
  - Mar_acc_other_3cm: 'Other' category pixels for 3 cm accuracy assessment.

## Accuracy assessment datasets (7 cm classifications)
- Shapefiles containing polygons representing validation pixels for accuracy assessment:
  - Mar_acc_prunus_pure_7cm: Prunus spinosa 'pure' pixels for 7 cm accuracy assessment.
  - Mar_acc_prunus_edge_7cm: Prunus spinosa 'edge' pixels for 7 cm accuracy assessment.
  - Mar_acc_other_7cm: 'Other' category pixels for 7 cm accuracy assessment.

## Methodological notes
- All training and accuracy datasets are used to support maximum likelihood classifications and to create regions of interest for threshold setting and validation.
- Datasets are provided as shapefiles with polygons corresponding to the categorized pixel regions.