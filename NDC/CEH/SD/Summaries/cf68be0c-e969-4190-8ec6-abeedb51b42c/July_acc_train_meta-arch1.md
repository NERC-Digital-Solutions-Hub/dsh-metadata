# Definitions

- Edge pixels — Pixels gathered at the edge of floral unit clusters or in the center of small clusters where the pixel appears mixed with other features.
- Pure pixels — Pixels gathered deeper into the center of floral unit clusters, less likely to be mixed with other features.
- Other category — The classification category containing regions of interest not belonging to the focal flowering plant species (e.g., branches, soil, green vegetation).

# Training pixels

- Training sets are the full sets of training data used to manually select threshold values for pixel classification in which regions of interest may be removed or merged when applying different training set variants.
- July_train_other — 'Other' category training data for maximum likelihood classifications; used to train both the 3cm and 7cm classifications. Provided as a shapefile with polygons representing the corresponding 'other' pixels.
- July_train_cent_pure — Centaurea nigra (common knapweed) pure training data for maximum likelihood classifications; used to train both the 3cm and 7cm classifications. Provided as a shapefile with polygons representing the corresponding 'pure' Centaurea nigra pixels.
- July_train_cent_edge — Centaurea nigra edge training data for maximum likelihood classifications; used to train both the 3cm and 7cm classifications. Provided as a shapefile with polygons representing the corresponding 'edge' Centaurea nigra pixels.
- July_train_rubus_pure — Rubus fruticosus (bramble) pure training data for maximum likelihood classifications; used to train both the 3cm and 7cm classifications. Provided as a shapefile with polygons representing the corresponding 'pure' Rubus fruticosus pixels.
- July_train_rubus_edge — Rubus fruticosus edge training data for maximum likelihood classifications; used to train both the 3cm and 7cm classifications. Provided as a shapefile with polygons representing the corresponding 'edge' Rubus fruticosus pixels.

# Accuracy assessment pixels 3cm classifications

- July_acc_cent_pure_3cm — Shapefile containing polygons representing Centaurea nigra 'pure' pixels used within the accuracy assessment for each 3cm classification variant for July.
- July_acc_cent_edge_3cm — Shapefile containing polygons representing Centaurea nigra 'edge' pixels used within the accuracy assessment for each 3cm classification variant for July.
- July_acc_rubus_pure_3cm — Shapefile containing polygons representing Rubus fruticosus 'pure' pixels used within the accuracy assessment for each 3cm classification variant for July.
- July_acc_rubus_edge_3cm — Shapefile containing polygons representing Rubus fruticosus 'edge' pixels used within the accuracy assessment for each 3cm classification variant for July.
- July_acc_other_3cm — Shapefile containing polygons representing 'other' category pixels used within the accuracy assessment for each 3cm classification variant for July.

# Accuracy assessment pixels 7cm classifications

- July_acc_cent_7cm — Shapefile containing Centaurea nigra pixels used within the accuracy assessment for the July 7cm classification.
- July_acc_rubus_pure_7cm — Shapefile containing Rubus fruticosus 'pure' pixels used within the accuracy assessment for the July 7cm classification.
- July_acc_rubus_edge_7cm — Shapefile containing Rubus fruticosus 'edge' pixels used within the accuracy assessment for the July 7cm classification.
- July_acc_other_7cm — Shapefile containing 'other' category pixels used within the accuracy assessment for the July 7cm classification.