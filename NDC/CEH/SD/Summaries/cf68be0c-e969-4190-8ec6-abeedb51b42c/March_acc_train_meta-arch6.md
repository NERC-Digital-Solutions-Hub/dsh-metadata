# Definitions and Data Sets for Pixel Classification of Prunus spinosa (Mar)

## Key Definitions
- Edge pixels: Pixels gathered at the edge of floral unit clusters or near the center of small clusters where mixing with other features occurs.
- Pure pixels: Pixels gathered deeper into the centre of floral unit clusters, less likely to be mixed with other features.
- Other category: Pixels representing regions not the focal flowering plant species (e.g., branches, soil, green vegetation).

## Training Pixels
- Purpose: Full training data sets; when applying different training set variants, some regions may be removed or merged to allow manual thresholding for pixel allocation to categories; used to train classifications.
- Mar_train_other: 'Other' category training data for maximum likelihood classifications; used to train both 3 cm and 7 cm classifications; provided as a shapefile with polygons for the corresponding 'other' pixels.
- Mar_train_prunus_pure: Prunus spinosa ('pure') training data for maximum likelihood classifications; shapefile with polygons for the corresponding 'pure' pixels.
- Mar_train_prunus_edge: Prunus spinosa ('edge') training data for maximum likelihood classifications; shapefile with polygons for the corresponding 'edge' pixels.

## Accuracy Assessment Pixels – 3 cm Classifications
- Mar_acc_prunus_pure_3cm: Shapefile polygons representing each of the corresponding Prunus spinosa 'pure' pixels used in accuracy assessment for the 3 cm classification variant.
- Mar_acc_prunus_edge_3cm: Shapefile polygons representing each of the corresponding Prunus spinosa 'edge' pixels used in accuracy assessment for the 3 cm classification variant.
- Mar_acc_other_3cm: Shapefile polygons representing each of the corresponding 'other' category pixels used in accuracy assessment for the 3 cm classification variant.

## Accuracy Assessment Pixels – 7 cm Classifications
- Mar_acc_prunus_pure_7cm: Shapefile polygons representing each of the corresponding Prunus spinosa 'pure' pixels used in accuracy assessment for the 7 cm classification variant.
- Mar_acc_prunus_edge_7cm: Shapefile polygons representing each of the corresponding Prunus spinosa 'edge' pixels used in accuracy assessment for the 7 cm classification variant.
- Mar_acc_other_7cm: Shapefile polygons representing each of the corresponding 'other' category pixels used in accuracy assessment for the 7 cm classification variant.