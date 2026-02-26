# Definitions

- Edge pixels - Pixels gathered at the edge of floral unit clusters or in the centre of small clusters where the pixel appears mixed with other features.
- Pure pixels - Whitest/pinkest pixels (depending on species), usually gathered further into the centre of floral unit clusters and less likely to be mixed with other features.
- Other category - The classification category containing regions of interest not belonging to the focal flowering plant species (e.g., branches, soil, green vegetation).

# Training pixels

- May_train_other - Other category training data for maximum likelihood classifications. Used to train both the 3cm and 7cm classifications. Provided as a shapefile with polygons representing the corresponding 'other' pixels used to create regions of interest.
- May_train_silene_pure - Silene dioica (red campion) training data for maximum likelihood classifications. Used to train both the 3cm and 7cm classifications. Shapefile with polygons representing the 'pure' Silene dioica pixels.
- May_train_silene_edge - Silene dioica training data for maximum likelihood classifications. Used to train both the 3cm and 7cm classifications. Shapefile with polygons representing the 'edge' Silene dioica pixels.
- May_train_cratae_pure - Crataegus monogyna (hawthorn) training data for maximum likelihood classifications. Used to train both the 3cm and 7cm classifications. Shapefile with polygons representing the 'pure' Crataegus monogyna pixels.
- May_train_cratae_edge - Crataegus monogyna training data for maximum likelihood classifications. Used to train both the 3cm and 7cm classifications. Shapefile with polygons representing the 'edge' Crataegus monogyna pixels.

# Accuracy assessment pixels 3cm classifications

- May_acc_silene_3cm - Shapefile containing polygons representing Silene dioica pixels used in the accuracy assessment for the 3cm classification variants.
- May_acc_cratae_pure_3cm - Shapefile containing polygons representing Crataegus monogyna 'pure' pixels used in the accuracy assessment for the 3cm classification variants.
- May_acc_cratae_edge_3cm - Shapefile containing polygons representing Crataegus monogyna 'edge' pixels used in the accuracy assessment for the 3cm classification variants.
- May_acc_other_3cm - Shapefile containing polygons representing 'other' category pixels used in the accuracy assessment for the 3cm classification variants.

# Accuracy assessment pixels 7cm classifications

- May_acc_Silene_7cm - Shapefile containing polygons representing Silene dioica pixels used in the accuracy assessment for the May 7cm classification.
- May_acc_Cratae_pure_7cm - Shapefile containing polygons representing Crataegus monogyna 'pure' pixels used in the accuracy assessment for the May 7cm classification.
- May_acc_Cratae_edge_7cm - Shapefile containing polygons representing Crataegus monogyna 'edge' pixels used in the accuracy assessment for the May 7cm classification.
- May_acc_other_7cm - Shapefile containing polygons representing 'other' category pixels used in the accuracy assessment for the May 7cm classification.

# 7cm training data

- May_acc_Cratae_pure_7cm - Accuracy assessment data for Crataegus monogyna 'pure' pixels using May 7cm training data (same as 7cm classification trained with 3cm data for this category).
- May_acc_Cratae_edge_7cm - Accuracy assessment data for Crataegus monogyna 'edge' pixels using May 7cm training data (same as 7cm classification trained with 3cm data for this category).
- May_7cm_train_other - 7cm training data for the 'other' category used in May 7cm classification.
- May_7cm_train_cratae_pure - 7cm training data for Crataegus monogyna 'pure' pixels used to classify May 7cm imagery.
- May_7cm_train_cratae_edge - 7cm training data for Crataegus monogyna 'edge' pixels used to classify May 7cm imagery.
- May_7cm_train_silene_pure - 7cm training data for Silene dioica 'pure' pixels used to classify May 7cm imagery.
- May_7cm_train_silene_edge - 7cm training data for Silene dioica 'edge' pixels used to classify May 7cm imagery.
- May_7cm_train_acc_other - 7cm training data (accuracy assessment) for the 'other' category used to classify May 7cm imagery.

# Notes on training data equivalence across scales

- For May, a classification was also carried out using a training set built from May 7cm data.
- In this 7cm-trained setup, only the 'other' category pixels changed slightly; the Silene dioica and Crataegus monogyna accuracy assessment pixels remained the same as for the 7cm classification trained with 3cm data.