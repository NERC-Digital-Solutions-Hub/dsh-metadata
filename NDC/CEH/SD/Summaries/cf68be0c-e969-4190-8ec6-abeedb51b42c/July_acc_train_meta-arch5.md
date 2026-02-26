# Definitions, Training pixels, and Accuracy assessment pixels for maximum likelihood classifications (3cm and 7cm)

## Overview
- This document defines pixel categories and documents the training and accuracy assessment datasets used for maximum likelihood classifications at 3cm and 7cm resolutions.
- Datasets are provided as shapefiles containing polygons that represent regions of interest used for training and accuracy assessment.

## Definitions
- Edge pixels: Pixels gathered at the edge of floral unit clusters or in the centre of small clusters where the pixel appears mixed with other features.
- Pure pixels: Pixels gathered deeper into the centre of floral unit clusters, less likely to be mixed with other features.
- Other category: Regions of interest not belonging to the focal flowering plant species (e.g., branches, soil, green vegetation, etc.).

## Training pixels
- July_train_other: 'Other' category training data for maximum likelihood classifications; used to train both the 3cm and 7cm classifications. Provided as a shapefile with polygons representing the 'other' category pixels.
- July_train_cent_pure: Centaurea nigra (common knapweed) training data for maximum likelihood classifications; used for both 3cm and 7cm classifications. Shapefile with polygons for 'pure' Centaurea nigra pixels.
- July_train_cent_edge: Centaurea nigra training data for maximum likelihood classifications; used for both 3cm and 7cm classifications. Shapefile with polygons for 'edge' Centaurea nigra pixels.
- July_train_rubus_pure: Rubus fruticosus (bramble) training data for maximum likelihood classifications; used for both 3cm and 7cm classifications. Shapefile with polygons for 'pure' Rubus fruticosus pixels.
- July_train_rubus_edge: Rubus fruticosus training data for maximum likelihood classifications; used for both 3cm and 7cm classifications. Shapefile with polygons for 'edge' Rubus fruticosus pixels.

## Accuracy assessment pixels (3cm classifications)
- July_acc_cent_pure_3cm: Shapefile containing polygons for Centaurea nigra 'pure' pixels used in the accuracy assessment for the July 3cm classification variant.
- July_acc_cent_edge_3cm: Shapefile containing polygons for Centaurea nigra 'edge' pixels used in the accuracy assessment for the July 3cm classification variant.
- July_acc_rubus_pure_3cm: Shapefile containing polygons for Rubus fruticosus 'pure' pixels used in the accuracy assessment for the July 3cm classification variant.
- July_acc_rubus_edge_3cm: Shapefile containing polygons for Rubus fruticosus 'edge' pixels used in the accuracy assessment for the July 3cm classification variant.
- July_acc_other_3cm: Shapefile containing polygons for the 'other' category pixels used in the accuracy assessment for the July 3cm classification variant.

## Accuracy assessment pixels (7cm classifications)
- July_acc_cent_7cm: Shapefile containing Centaurea nigra pixels used in the accuracy assessment for the July 7cm classification variant.
- July_acc_rubus_pure_7cm: Shapefile containing Rubus fruticosus 'pure' pixels used in the accuracy assessment for the July 7cm classification variant.
- July_acc_rubus_edge_7cm: Shapefile containing Rubus fruticosus 'edge' pixels used in the accuracy assessment for the July 7cm classification variant.
- July_acc_other_7cm: Shapefile containing 'other' category pixels used in the accuracy assessment for the July 7cm classification variant.