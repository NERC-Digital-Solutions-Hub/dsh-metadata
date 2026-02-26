# Training and Accuracy Assessment Data for Maximum Likelihood Classifications of Centaurea nigra and Rubus fruticosus

## Overview
- Documents the data components used for pixel classification of two plant species (Centaurea nigra and Rubus fruticosus) at multiple spatial resolutions (3 cm and 7 cm) and the associated accuracy assessments.
- Distinguishes pixel categories (edge, pure, other) and outlines how training and accuracy datasets are organized as shapefiles.

## Definitions
- Edge pixels: Pixels gathered at the edge of floral unit clusters or in the center of small clusters where the pixel appears mixed with other features.
- Pure pixels: Pixels gathered deeper into the center of floral unit clusters, less likely to be mixed with other features.
- Other category: Regions of interest not belonging to the focal species (e.g., branches, soil, green vegetation).

## Training pixels
- Full training data sets used to calibrate maximum likelihood classifications; variants may remove or merge regions to allow manual threshold setting for pixel classification.
- Files (shapefiles with polygons representing regions of interest):
  - July_train_other
  - July_train_cent_pure
  - July_train_cent_edge
  - July_train_rubus_pure
  - July_train_rubus_edge

## Accuracy assessment pixels (3 cm classifications)
- Shapefiles containing polygons representing each of the accuracy-assessed pixels used for July 3 cm scale classifications:
  - July_acc_cent_pure_3cm
  - July_acc_cent_edge_3cm
  - July_acc_rubus_pure_3cm
  - July_acc_rubus_edge_3cm
  - July_acc_other_3cm

## Accuracy assessment pixels (7 cm classifications)
- Shapefiles containing polygons representing each of the accuracy-assessed pixels used for July 7 cm scale classifications:
  - July_acc_cent_7cm
  - July_acc_rubus_pure_7cm
  - July_acc_rubus_edge_7cm
  - July_acc_other_7cm