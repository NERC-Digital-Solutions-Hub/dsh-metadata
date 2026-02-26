# Definitions

- Edge pixel: Pixels gathered at the edge of floral unit clusters or in the centre of small clusters where the pixel appears mixed with other features.
- Pure pixel: Pixels deeper into the centre of floral unit clusters, less likely to be mixed with other features.
- Other category: Regions of interest containing non-target features (e.g., branches, soil, green vegetation), not the focal Prunus spinosa.

- Training pixels
  - Mar_train_other: ‘Other’ category training data for maximum likelihood classifications; used to train both 3cm and 7cm classifications. Provided as a shapefile with polygons representing ‘Other’ pixels for regions of interest.
  - Mar_train_prunus_pure: Prunus spinosa ‘pure’ training data for maximum likelihood classifications; used for both 3cm and 7cm classifications. Provided as a shapefile with polygons representing ‘pure’ pixels.
  - Mar_train_prunus_edge: Prunus spinosa training data for maximum likelihood classifications; used for both 3cm and 7cm classifications. Provided as a shapefile with polygons representing ‘edge’ pixels.

- Accuracy assessment pixels 3cm classifications
  - Mar_acc_prunus_pure_3cm: Shapefile polygons representing Prunus spinosa ‘pure’ pixels used in accuracy assessment for the 3cm classification variant.
  - Mar_acc_prunus_edge_3cm: Shapefile polygons representing Prunus spinosa ‘edge’ pixels used in accuracy assessment for the 3cm classification variant.
  - Mar_acc_other_3cm: Shapefile polygons representing ‘Other’ pixels used in accuracy assessment for the 3cm classification variant.

- Accuracy assessment pixels 7cm classifications
  - Mar_acc_prunus_pure_7cm: Shapefile polygons representing Prunus spinosa ‘pure’ pixels used in accuracy assessment for the 7cm classification variant.
  - Mar_acc_prunus_edge_7cm: Shapefile polygons representing Prunus spinosa ‘edge’ pixels used in accuracy assessment for the 7cm classification variant.
  - Mar_acc_other_7cm: Shapefile polygons representing ‘Other’ pixels used in accuracy assessment for the 7cm classification variant.

- Overview of use
  - Datasets are designed to train and validate maximum likelihood classifications of Prunus spinosa at 3cm and 7cm resolutions, using defined pixel categories and region-of-interest polygons.
  - Training data establish thresholds and region definitions; accuracy assessment data provide pixel-level validation for each classification variant.