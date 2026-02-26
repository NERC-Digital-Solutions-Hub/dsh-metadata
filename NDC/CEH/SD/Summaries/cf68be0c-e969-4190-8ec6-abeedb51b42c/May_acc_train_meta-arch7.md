# Definitions

- Edge pixels: Pixels at the edge of floral unit clusters or centers of small clusters that appear mixed with other features.
- Pure pixels: Whitest/pinkest (species-dependent) pixels located toward the center of floral unit clusters, less likely to be mixed with other features.
- Other category: Regions not belonging to the focal flowering plant species (e.g., branches, soil, green vegetation).

- Training pixels: Full training datasets used to create threshold-based region decisions for maximum likelihood classifications. Training variants may remove or merge regions to allow manual thresholding.
  - May_train_other: ‘Other’ category training data for maximum likelihood classifications (used for both 3cm and 7cm classifications). Shapefile with polygons for the corresponding ‘other’ pixels.
  - May_train_silene_pure: Silene dioica ‘pure’ training data (used for both 3cm and 7cm). Shapefile with polygons.
  - May_train_silene_edge: Silene dioica ‘edge’ training data (used for both 3cm and 7cm). Shapefile with polygons.
  - May_train_cratae_pure: Crataegus monogyna ‘pure’ training data (used for both 3cm and 7cm). Shapefile with polygons.
  - May_train_cratae_edge: Crataegus monogyna ‘edge’ training data (used for both 3cm and 7cm). Shapefile with polygons.

- Accuracy assessment pixels (3cm classifications):
  - May_acc_silene_3cm: Silene dioica pixels used for accuracy assessment of 3cm classifications.
  - May_acc_cratae_pure_3cm: Crataegus monogyna ‘pure’ pixels for 3cm accuracy assessment.
  - May_acc_cratae_edge_3cm: Crataegus monogyna ‘edge’ pixels for 3cm accuracy assessment.
  - May_acc_other_3cm: ‘Other’ category pixels for 3cm accuracy assessment.

- Accuracy assessment pixels (7cm classifications):
  - May_acc_Silene_7cm: Silene dioica pixels for 7cm accuracy assessment.
  - May_acc_Cratae_pure_7cm: Crataegus monogyna ‘pure’ pixels for 7cm accuracy assessment.
  - May_acc_Cratae_edge_7cm: Crataegus monogyna ‘edge’ pixels for 7cm accuracy assessment.
  - May_acc_other_7cm: ‘Other’ category pixels for 7cm accuracy assessment.

- 7cm training data (May):
  - May_7cm_train_other: 7cm training data for the ‘Other’ category used to classify May imagery at 7cm.
  - May_7cm_train_cratae_pure: 7cm Crataegus monogyna ‘pure’ training data.
  - May_7cm_train_cratae_edge: 7cm Crataegus monogyna ‘edge’ training data.
  - May_7cm_train_silene_pure: 7cm Silene dioica ‘pure’ training data.
  - May_7cm_train_silene_edge: 7cm Silene dioica ‘edge’ training data.
  - May_7cm_train_acc_other: 7cm training data for the accuracy assessment of the ‘Other’ category.

- Notes:
  - For May, a classification was also conducted using a training set derived from May 7cm data. When using the 7cm-trained data, only the ‘other’ pixel training data changed slightly (May_7cm_train_acc_other). The Silene dioica and Crataegus monogyna accuracy assessment pixels remained the same as for the 7cm classification trained with 3cm data (May_acc_Silene_7cm, May_acc_Cratae_pure_7cm, May_acc_Cratae_edge_7cm).