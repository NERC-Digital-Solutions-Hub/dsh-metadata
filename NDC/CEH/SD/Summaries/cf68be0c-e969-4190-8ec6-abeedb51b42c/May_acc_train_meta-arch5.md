# Definitions

- This document defines pixel categories, training data, and accuracy assessment data used for maximum likelihood classifications at different spatial resolutions (3 cm and 7 cm) for May imagery involving Silene dioica and Crataegus monogyna.
- Data are provided as shapefiles where each polygon represents regions of interest (ROIs) used to create training or assessment datasets.

## Pixel categories

- Edge pixels: Pixels at the edge of floral unit clusters or within small clusters where mixed features are present.
- Pure pixels: The whitest/pinkest pixels (depending on species) located deeper in floral unit clusters, with minimal mixing.
- Other category: All regions not belonging to the focal flowering plant species (e.g., branches, soil, green vegetation).

## Training pixels (full sets)

- May_train_other: Training data for the 'Other' category used to help define non-target regions for maximum likelihood classifications (used for both 3 cm and 7 cm).
- May_train_silene_pure: Silene dioica 'pure' pixel training data used for both 3 cm and 7 cm classifications.
- May_train_silene_edge: Silene dioica 'edge' pixel training data used for both 3 cm and 7 cm classifications.
- May_train_cratae_pure: Crataegus monogyna 'pure' pixel training data used for both 3 cm and 7 cm classifications.
- May_train_cratae_edge: Crataegus monogyna 'edge' pixel training data used for both 3 cm and 7 cm classifications.

## Accuracy assessment pixels (3 cm classifications)

- May_acc_silene_3cm: Shapefile polygons representing Silene dioica pixels used in accuracy assessment for the 3 cm classification variant.
- May_acc_cratae_pure_3cm: Shapefile polygons representing Crataegus monogyna 'pure' pixels used in 3 cm accuracy assessment.
- May_acc_cratae_edge_3cm: Shapefile polygons representing Crataegus monogyna 'edge' pixels used in 3 cm accuracy assessment.
- May_acc_other_3cm: Shapefile polygons representing 'Other' category pixels used in 3 cm accuracy assessment.

## Accuracy assessment pixels (7 cm classifications)

- May_acc_Silene_7cm: Polygons used for Silene dioica accuracy assessment in the 7 cm classification.
- May_acc_Cratae_pure_7cm: Polygons used for Crataegus monogyna 'pure' accuracy assessment in the 7 cm classification.
- May_acc_Cratae_edge_7cm: Polygons used for Crataegus monogyna 'edge' accuracy assessment in the 7 cm classification.
- May_acc_other_7cm: Polygons used for the 'Other' category accuracy assessment in the 7 cm classification.

## 7 cm training data

- For May, a classification was also performed using a training set trained with May 7 cm data. The training pixels for this 7 cm-trained set are listed below; only the 'Other' category training data changed slightly between the 7 cm and 3 cm training runs.
- May_7cm_train_other: 'Other' category training data for the 7 cm-trained model.
- May_7cm_train_cratae_pure: Crataegus monogyna 'pure' pixel training data for the 7 cm-trained model.
- May_7cm_train_cratae_edge: Crataegus monogyna 'edge' pixel training data for the 7 cm-trained model.
- May_7cm_train_silene_pure: Silene dioica 'pure' pixel training data for the 7 cm-trained model.
- May_7cm_train_silene_edge: Silene dioica 'edge' pixel training data for the 7 cm-trained model.
- May_7cm_train_acc_other: 'Other' category pixels used in accuracy assessment for the 7 cm-trained model (noting that the May 7 cm training dataset’s 'Other' training data changed slightly from the 3 cm version).

## Notes on purpose and structure

- The datasets are organized to support training and evaluation of maximum likelihood classifications at two resolutions (3 cm and 7 cm).
- Shapefiles provide polygonal ROIs for reproducible training and accuracy assessment.
- The 7 cm training set extends the 3 cm framework, with targeted updates to the 'Other' training data and corresponding impact on accuracy assessments.