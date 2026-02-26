# Definitions, Training Pixels, and Accuracy Assessment Pixels

- Purpose of the document
  - Defines pixel categories and catalogs training and accuracy assessment datasets used for maximum likelihood classifications of plant species, across two spatial resolutions (3 cm and 7 cm) in July data.

- Pixel category definitions
  - Edge: Pixels at the edge of floral unit clusters or near small clusters where features mix with others.
  - Pure: Pixels toward the center of clusters, less likely to be mixed with other features.
  - Other: Pixels containing non-target features (e.g., branches, soil, green vegetation).

- Training pixels (datasets used to inform classification thresholds and ROI creation)
  - July_train_other: Training data for the 'Other' category, used to train both 3 cm and 7 cm classifications (shapefile with polygons for 'Other' pixels).
  - July_train_cent_pure: Centaurea nigra 'pure' pixels for both 3 cm and 7 cm classifications (shapefile with polygons).
  - July_train_cent_edge: Centaurea nigra 'edge' pixels for both 3 cm and 7 cm classifications (shapefile with polygons).
  - July_train_rubus_pure: Rubus fruticosus 'pure' pixels for both 3 cm and 7 cm classifications (shapefile with polygons).
  - July_train_rubus_edge: Rubus fruticosus 'edge' pixels for both 3 cm and 7 cm classifications (shapefile with polygons).

- Accuracy assessment pixels for 3 cm classifications
  - July_acc_cent_pure_3cm: Centaurea nigra 'pure' pixels used for accuracy assessment (shapefile with polygons).
  - July_acc_cent_edge_3cm: Centaurea nigra 'edge' pixels used for accuracy assessment (shapefile with polygons).
  - July_acc_rubus_pure_3cm: Rubus fruticosus 'pure' pixels used for accuracy assessment (shapefile with polygons).
  - July_acc_rubus_edge_3cm: Rubus fruticosus 'edge' pixels used for accuracy assessment (shapefile with polygons).
  - July_acc_other_3cm: 'Other' category pixels used for accuracy assessment (shapefile with polygons).

- Accuracy assessment pixels for 7 cm classifications
  - July_acc_cent_7cm: Centaurea nigra pixels used for accuracy assessment (shapefile with polygons).
  - July_acc_rubus_pure_7cm: Rubus fruticosus 'pure' pixels used for accuracy assessment (shapefile with polygons).
  - July_acc_rubus_edge_7cm: Rubus fruticosus 'edge' pixels used for accuracy assessment (shapefile with polygons).
  - July_acc_other_7cm: 'Other' category pixels used for accuracy assessment (shapefile with polygons).