# Prunus spinosa Classification Training and Accuracy Assessment Data

- Definitions
  - Edge pixels: pixels gathered at the edge of floral unit clusters or in small clusters where mixed with other features.
  - Pure pixels: pixels deeper in floral unit clusters less likely to be mixed with other features.
  - Other category: regions not belonging to the focal Prunus spinosa species (e.g., branches, soil, green vegetation).

- Training pixels
  - Full training datasets used to calibrate classifications; variants may remove or merge regions of interest to enable manual threshold setting for category assignment.
  - Datasets:
    - Mar_train_other: 'Other' category training data for maximum likelihood classifications; used for both 3cm and 7cm classifications; provided as shapefile with polygons for ROI pixels.
    - Mar_train_prunus_pure: Prunus spinosa training data for maximum likelihood classifications; used for both 3cm and 7cm; provided as shapefile with polygons for pure ROI pixels.
    - Mar_train_prunus_edge: Prunus spinosa training data for maximum likelihood classifications; used for both 3cm and 7cm; provided as shapefile with polygons for edge ROI pixels.

- Accuracy assessment pixels 3cm classifications
  - Mar_acc_prunus_pure_3cm: shapefile with polygons representing Prunus spinosa 'pure' pixels used in the 3cm accuracy assessment.
  - Mar_acc_prunus_edge_3cm: shapefile with polygons representing Prunus spinosa 'edge' pixels used in the 3cm accuracy assessment.
  - Mar_acc_other_3cm: shapefile with polygons representing 'Other' category pixels used in the 3cm accuracy assessment.

- Accuracy assessment pixels 7cm classifications
  - Mar_acc_prunus_pure_7cm: shapefile with polygons representing Prunus spinosa 'pure' pixels used in the 7cm accuracy assessment.
  - Mar_acc_prunus_edge_7cm: shapefile with polygons representing Prunus spinosa 'edge' pixels used in the 7cm accuracy assessment.
  - Mar_acc_other_7cm: shapefile with polygons representing 'Other' category pixels used in the 7cm accuracy assessment.