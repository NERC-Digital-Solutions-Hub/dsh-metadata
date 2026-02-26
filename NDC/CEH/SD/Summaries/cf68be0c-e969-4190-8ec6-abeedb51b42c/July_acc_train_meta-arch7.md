# Definitions

- Edge pixels: Pixels at the edge of floral unit clusters or at the centre of small clusters where the pixel appears mixed with other features.
- Pure pixels: Pixels deeper inside floral unit clusters less likely to be mixed with other features.
- Other category: Pixels representing regions of interest not belonging to the focal flowering plant species (e.g., branches, soil, green vegetation).

## Training pixels

- Full training data sets used to determine threshold values for pixel classification.
- Regions of interest may be removed or merged when applying different training set variants.
- Datasets (shapefiles) used to create regions of interest:
  - July_train_other: 'Other' category training data for maximum likelihood classifications (used for both 3cm and 7cm classifications).
  - July_train_cent_pure: Centaurea nigra 'pure' pixels for maximum likelihood classifications (used for both 3cm and 7cm classifications).
  - July_train_cent_edge: Centaurea nigra 'edge' pixels for maximum likelihood classifications (used for both 3cm and 7cm classifications).
  - July_train_rubus_pure: Rubus fruticosus 'pure' pixels for maximum likelihood classifications (used for both 3cm and 7cm classifications).
  - July_train_rubus_edge: Rubus fruticosus 'edge' pixels for maximum likelihood classifications (used for both 3cm and 7cm classifications).

## Accuracy assessment pixels 3cm classifications

- Shapefiles containing polygons for accuracy assessment of 3cm classifications:
  - July_acc_cent_pure_3cm: Centaurea nigra 'pure' pixels used in accuracy assessment for 3cm variants.
  - July_acc_cent_edge_3cm: Centaurea nigra 'edge' pixels used in accuracy assessment for 3cm variants.
  - July_acc_rubus_pure_3cm: Rubus fruticosus 'pure' pixels used in accuracy assessment for 3cm variants.
  - July_acc_rubus_edge_3cm: Rubus fruticosus 'edge' pixels used in accuracy assessment for 3cm variants.
  - July_acc_other_3cm: 'Other' category pixels used in accuracy assessment for 3cm variants.

## Accuracy assessment pixels 7cm classifications

- Shapefiles containing polygons for accuracy assessment of 7cm classifications:
  - July_acc_cent_7cm: Centaurea nigra pixels used in accuracy assessment for the July 7cm classification.
  - July_acc_rubus_pure_7cm: Rubus fruticosus 'pure' pixels used in accuracy assessment for the July 7cm classification.
  - July_acc_rubus_edge_7cm: Rubus fruticosus 'edge' pixels used in accuracy assessment for the July 7cm classification.
  - July_acc_other_7cm: 'Other' category pixels used in accuracy assessment for the July 7cm classification.

## Notes on usage

- All listed datasets are shapefiles representing polygons for training or accuracy assessment of maximum likelihood classifications.
- The training data were used to train both the 3cm and 7cm classification schemes.
- These resources support QA and refinement of GIS-based, map-focused data products for identifying and mapping the target plant species and associated land-cover features.