# Definitions

## What this document defines
- Edge pixels: Pixels at the edge of floral unit clusters or within small clusters where mixing with other features occurs.
- Pure pixels: Whitest/pinkest pixels (species-dependent), typically deeper in floral unit clusters with less mixing.
- Other category: Regions of interest not belonging to the focal plant species (e.g., branches, soil, green vegetation).

## Training data
- Full training datasets used to derive thresholding for classifications; some regions may be merged or removed when applying different training set variants.
- May_train_other: ‘Other’ category training data (max likelihood classifications) used for both 3cm and 7cm classifications (presented as shapefiles with polygons for ‘other’ pixels).
- May_train_silene_pure: Silene dioica (red campion) training data for both 3cm and 7cm classifications (polygons in shapefiles).
- May_train_silene_edge: Silene dioica edge training data for both 3cm and 7cm classifications (polygons in shapefiles).
- May_train_cratae_pure: Crataegus monogyna (hawthorn) training data for both 3cm and 7cm classifications (polygons in shapefiles).
- May_train_cratae_edge: Crataegus monogyna edge training data for both 3cm and 7cm classifications (polygons in shapefiles).

## Accuracy assessment data (3cm classifications)
- May_acc_silene_3cm: Silene dioica pixels used for accuracy assessment for 3cm classification.
- May_acc_cratae_pure_3cm: Crataegus monogyna ‘pure’ pixels used for accuracy assessment for 3cm.
- May_acc_cratae_edge_3cm: Crataegus monogyna edge pixels used for accuracy assessment for 3cm.
- May_acc_other_3cm: ‘Other’ category pixels used for accuracy assessment for 3cm.

## Accuracy assessment data (7cm classifications)
- May_acc_Silene_7cm: Silene dioica pixels used for accuracy assessment for 7cm.
- May_acc_Cratae_pure_7cm: Crataegus monogyna ‘pure’ pixels used for accuracy assessment for 7cm.
- May_acc_Cratae_edge_7cm: Crataegus monogyna edge pixels used for accuracy assessment for 7cm.
- May_acc_other_7cm: ‘Other’ category pixels used for accuracy assessment for 7cm.

## 7cm training data details
- May_7cm_train_other: 7cm training data for the ‘other’ category; only these pixels changed slightly when using 7cm training data.
- May_7cm_train_cratae_pure: 7cm Crataegus monogyna ‘pure’ pixel training data for 7cm classification.
- May_7cm_train_cratae_edge: 7cm Crataegus monogyna edge pixel training data for 7cm.
- May_7cm_train_silene_pure: 7cm Silene dioica ‘pure’ pixel training data for 7cm.
- May_7cm_train_silene_edge: 7cm Silene dioica edge pixel training data for 7cm.
- May_7cm_train_acc_other: Accuracy assessment data corresponding to the 7cm training set for the ‘other’ category (used to create regions of interest).

## Notes on data usage
- For May, classification was conducted with a training set that used May 7cm data; as a result, the 7cm classification’s accuracy for Silene dioica and Crataegus monogyna remained the same as when trained with 3cm data, while only the ‘other’ category pixels slightly changed for May_7cm_train_acc_other.