# Definitions

- This document defines pixel classifications and the accompanying training and accuracy data used for maximum likelihood classifications of plant species in May imagery, at 3 cm and 7 cm resolutions.
- Key categories:
  - Edge pixels: pixels at the edge of floral unit clusters or within small clusters that mix with other features.
  - Pure pixels: the whitest/pinkest pixels (depending on species), deeper in cluster centers, less likely to mix with other features.
  - Other: all regions not belonging to the focal species (e.g., branches, soil, green vegetation).

## Training pixels

- May_train_other: Training data for the 'Other' category, used for maximum likelihood classifications at both 3 cm and 7 cm.
- May_train_silene_pure: Silene dioica (red campion) 'pure' pixels for 3 cm and 7 cm classifications.
- May_train_silene_edge: Silene dioica 'edge' pixels for 3 cm and 7 cm classifications.
- May_train_cratae_pure: Crataegus monogyna (hawthorn) 'pure' pixels for 3 cm and 7 cm classifications.
- May_train_cratae_edge: Crataegus monogyna 'edge' pixels for 3 cm and 7 cm classifications.
- Training data are provided as shapefiles with polygons representing regions of interest used to establish thresholding for pixel classification.

## Accuracy assessment pixels – 3 cm classifications

- May_acc_silene_3cm: Silene dioica pixels used for accuracy assessment in the 3 cm classification variant.
- May_acc_cratae_pure_3cm: Crataegus monogyna 'pure' pixels used for 3 cm accuracy assessment.
- May_acc_cratae_edge_3cm: Crataegus monogyna 'edge' pixels used for 3 cm accuracy assessment.
- May_acc_other_3cm: 'Other' category pixels used for 3 cm accuracy assessment.

## Accuracy assessment pixels – 7 cm classifications

- May_acc_Silene_7cm: Silene dioica pixels used for accuracy assessment in the 7 cm classification variant.
- May_acc_Cratae_pure_7cm: Crataegus monogyna 'pure' pixels used for 7 cm accuracy assessment.
- May_acc_Cratae_edge_7cm: Crataegus monogyna 'edge' pixels used for 7 cm accuracy assessment.
- May_acc_other_7cm: 'Other' category pixels used for 7 cm accuracy assessment.

## 7 cm training data

- May_7cm_train_other: 'Other' category training data for 7 cm classifications.
- May_7cm_train_cratae_pure: Crataegus monogyna 'pure' pixels for 7 cm training.
- May_7cm_train_cratae_edge: Crataegus monogyna 'edge' pixels for 7 cm training.
- May_7cm_train_silene_pure: Silene dioica 'pure' pixels for 7 cm training.
- May_7cm_train_silene_edge: Silene dioica 'edge' pixels for 7 cm training.
- May_7cm_train_acc_other: 'Other' pixels used for accuracy assessment when training at 7 cm.

## Notes on training data and methodology

- For May, a classification using 7 cm training data was performed; only the 'Other' category pixels changed slightly between 3 cm and 7 cm trainings; Silene dioica and Crataegus monogyna accuracy assessment pixels remained the same as for the 7 cm classification trained with 3 cm data.