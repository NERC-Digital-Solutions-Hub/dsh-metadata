# Definitions

- Edge pixels: Pixels gathered at the edge of floral unit clusters or in the center of small clusters where the pixel appears mixed with other features.
- Pure pixels: Pixels gathered deeper into the center of floral unit clusters, less likely to be mixed with other features.
- Other category: The classification category containing regions of interest that are not the focal flowering plant species (e.g., branches, soil, green vegetation, etc.).

## Training pixels (for maximum likelihood classifications)

- Mar_train_other: ‘Other’ category training data used to train both the 3 cm and 7 cm classifications. Provided as a shapefile with polygons representing the corresponding ‘other’ pixels used to create regions of interest.
- Mar_train_prunus_pure: Prunus spinosa (blackthorn) training data used to train both the 3 cm and 7 cm classifications. Provided as a shapefile with polygons representing the corresponding ‘pure’ pixels.
- Mar_train_prunus_edge: Prunus spinosa training data used to train both the 3 cm and 7 cm classifications. Provided as a shapefile with polygons representing the corresponding ‘edge’ pixels.
  
## Accuracy assessment pixels (3 cm classifications)

- Mar_acc_prunus_pure_3cm: Shapefile of polygons representing each of the Prunus spinosa 'pure' pixels used in the accuracy assessment for the 3 cm classification variant.
- Mar_acc_prunus_edge_3cm: Shapefile of polygons representing each of the Prunus spinosa 'edge' pixels used in the accuracy assessment for the 3 cm classification variant.
- Mar_acc_other_3cm: Shapefile of polygons representing each of the 'other' category pixels used in the accuracy assessment for the 3 cm classification variant.

## Accuracy assessment pixels (7 cm classifications)

- Mar_acc_prunus_pure_7cm: Shapefile of polygons representing each of the Prunus spinosa 'pure' pixels used in the accuracy assessment for the 7 cm classification.
- Mar_acc_prunus_edge_7cm: Shapefile of polygons representing each of the Prunus spinosa 'edge' pixels used in the accuracy assessment for the 7 cm classification.
- Mar_acc_other_7cm: Shapefile of polygons representing each of the 'other' category pixels used in the accuracy assessment for the 7 cm classification.

## Notes

- All training and accuracy assessment datasets are provided as shapefiles with polygon geometries.
- The training data are used to develop both 3 cm and 7 cm maximum likelihood classifications for Prunus spinosa (blackthorn) presence.
- The accuracy assessment datasets are organized separately for 3 cm and 7 cm classifications to evaluate the classifier performance on pure, edge, and other categories.