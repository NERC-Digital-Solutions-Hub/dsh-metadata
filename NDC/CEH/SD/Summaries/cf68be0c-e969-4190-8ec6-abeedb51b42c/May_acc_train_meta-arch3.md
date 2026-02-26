# Definitions and Training/Accuracy Assessment Data for May 3cm and 7cm Maximum Likelihood Classifications

## Overview
- Defines pixel categories and lists the training and accuracy assessment shapefiles used for May classifications at 3cm and 7cm resolutions.
- Focuses on three plant feature classes: Silene dioica (red campion), Crataegus monogyna (hawthorn), and an 'Other' category (non-target features).
- Describes two training regimes (3cm and 7cm) and their associated accuracy assessments to support transparent monitoring workflows.

## Key Concepts
- Edge pixels: Pixels at the edge of floral unit clusters or within small clusters, mixed with other features.
- Pure pixels: Whitest/pinkest pixels (species-dependent), typically toward the cluster centers, less mixed with other features.
- Other category: Regions of interest outside the focal species (e.g., branches, soil, green vegetation).

## Training pixels (3cm and 7cm classifications)
- May_train_other: 'Other' category training data for maximum likelihood classifications; used to train both 3cm and 7cm classifications. Shapefile with polygons for 'other' pixels.
- May_train_silene_pure: Silene dioica (pure) training data for maximum likelihood classifications; used for both 3cm and 7cm. Shapefile with polygons for 'pure' Silene dioica pixels.
- May_train_silene_edge: Silene dioica (edge) training data; used for both 3cm and 7cm. Shapefile with polygons for 'edge' Silene dioica pixels.
- May_train_cratae_pure: Crataegus monogyna (hawthorn) (pure) training data; used for both 3cm and 7cm. Shapefile with polygons for 'pure' Crataegus monogyna pixels.
- May_train_cratae_edge: Crataegus monogyna (hawthorn) (edge) training data; used for both 3cm and 7cm. Shapefile with polygons for 'edge' Crataegus monogyna pixels.

## Accuracy assessment pixels (3cm classifications)
- May_acc_silene_3cm: Shapefile polygons representing Silene dioica pixels used in accuracy assessment for the 3cm classifications.
- May_acc_cratae_pure_3cm: Shapefile polygons representing Crataegus monogyna 'pure' pixels used in 3cm accuracy assessment.
- May_acc_cratae_edge_3cm: Shapefile polygons representing Crataegus monogyna 'edge' pixels used in 3cm accuracy assessment.
- May_acc_other_3cm: Shapefile polygons representing 'Other' category pixels used in 3cm accuracy assessment.

## Accuracy assessment pixels (7cm classifications)
- May_acc_Silene_7cm: Shapefile polygons for Silene dioica pixels used in 7cm accuracy assessment.
- May_acc_Cratae_pure_7cm: Shapefile polygons for Crataegus monogyna 'pure' pixels used in 7cm accuracy assessment.
- May_acc_Cratae_edge_7cm: Shapefile polygons for Crataegus monogyna 'edge' pixels used in 7cm accuracy assessment.
- May_acc_other_7cm: Shapefile polygons for 'Other' category pixels used in 7cm accuracy assessment.

## 7cm training data
- May_7cm_train_other: 7cm training data for the 'Other' category used to classify May 7cm imagery; polygons represent 'other' pixels used to create regions of interest.
- May_7cm_train_cratae_pure: 7cm Crataegus monogyna 'pure' pixel training data for May 7cm imagery; polygons for 'pure' Crataegus monogyna.
- May_7cm_train_cratae_edge: 7cm Crataegus monogyna 'edge' pixel training data for May 7cm imagery; polygons for 'edge' Crataegus monogyna.
- May_7cm_train_silene_pure: 7cm Silene dioica 'pure' training data for May 7cm imagery; polygons for 'pure' Silene dioica.
- May_7cm_train_silene_edge: 7cm Silene dioica 'edge' training data for May 7cm imagery; polygons for 'edge' Silene dioica.
- May_7cm_train_acc_other: Shapefile containing polygons for 'Other' category pixels used within the accuracy assessment for the May 7cm classification trained with 7cm data (note: small changes reported in this dataset relative to other 7cm training sets).

## Notes on changes and consistency
- When using May 7cm training data, only the 'Other' category training pixels changed slightly; the Silene dioica and Crataegus monogyna accuracy assessment pixels remained the same as those for the 7cm classification trained with 3cm data.
- The documentation emphasizes reproducibility through explicit shapefile datasets for training and accuracy assessment across both 3cm and 7cm contexts.