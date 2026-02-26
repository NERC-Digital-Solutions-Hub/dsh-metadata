# Definitions

- Core terms
  - Edge pixels: Pixels at the edge of floral unit clusters or centers of small clusters that appear mixed with other features.
  - Pure pixels: Pixels toward the center of floral unit clusters that are less likely to be mixed with other features.
  - Other category: Regions of interest not belonging to the focal species (e.g., branches, soil, green vegetation).

- Training pixels (full training sets used to derive classification thresholds)
  - July_train_other: 'Other' category training data for maximum likelihood classifications; used for both 3cm and 7cm classifications; provided as shapefiles with polygons representing ROI pixels.
  - July_train_cent_pure: Centaurea nigra ('pure') training data for maximum likelihood classifications; used for both 3cm and 7cm; shapefiles with polygons representing ROI.
  - July_train_cent_edge: Centaurea nigra ('edge') training data for maximum likelihood classifications; used for both 3cm and 7cm; shapefiles with polygons representing ROI.
  - July_train_rubus_pure: Rubus fruticosus ('pure') training data for maximum likelihood classifications; used for both 3cm and 7cm; shapefiles with polygons representing ROI.
  - July_train_rubus_edge: Rubus fruticosus ('edge') training data for maximum likelihood classifications; used for both 3cm and 7cm; shapefiles with polygons representing ROI.

- Accuracy assessment pixels (used to evaluate classification performance)
  - 3cm classifications
    - July_acc_cent_pure_3cm: Centaurea nigra 'pure' pixels used in accuracy assessment; shapefile of polygons.
    - July_acc_cent_edge_3cm: Centaurea nigra 'edge' pixels used in accuracy assessment; shapefile of polygons.
    - July_acc_rubus_pure_3cm: Rubus fruticosus 'pure' pixels used in accuracy assessment; shapefile of polygons.
    - July_acc_rubus_edge_3cm: Rubus fruticosus 'edge' pixels used in accuracy assessment; shapefile of polygons.
    - July_acc_other_3cm: 'Other' category pixels used in accuracy assessment; shapefile of polygons.

  - 7cm classifications
    - July_acc_cent_7cm: Centaurea nigra pixels used in accuracy assessment; shapefile of polygons.
    - July_acc_rubus_pure_7cm: Rubus fruticosus 'pure' pixels used in accuracy assessment; shapefile of polygons.
    - July_acc_rubus_edge_7cm: Rubus fruticosus 'edge' pixels used in accuracy assessment; shapefile of polygons.
    - July_acc_other_7cm: 'Other' category pixels used in accuracy assessment; shapefile of polygons.

- Format and purpose
  - All datasets are provided as shapefiles containing polygons that delineate regions of interest (ROIs) for training or accuracy assessment.
  - Purpose: to train maximum likelihood classifications distinguishing Centaurea nigra and Rubus fruticosus from other features, using organized edge/pure/other categories, and to assess classification accuracy across 3cm and 7cm classifications.