# Definitions: 'Edge' pixels - Those pixels gathered at the edge of floral unit clusters or in the centre of small clusters but where the pixel appears to be mixed with other features.

- Overview
  - Defines three pixel categories used for classification training and accuracy assessment: Edge, Pure, and Other.
  - Documents the training and accuracy datasets used for maximum likelihood classifications at two resolutions (3 cm and 7 cm).

- Training pixels
  - Mar_train_other: Other category training data for maximum likelihood classifications; used to train both the 3 cm and 7 cm classifications. Provided as a shapefile with polygons representing the corresponding 'other' pixels.
  - Mar_train_prunus_pure: Prunus spinosa (blackthorn) pure pixels used to train both 3 cm and 7 cm classifications. Provided as a shapefile with polygons for the corresponding 'pure' pixels.
  - Mar_train_prunus_edge: Prunus spinosa edge pixels used to train both 3 cm and 7 cm classifications. Provided as a shapefile with polygons for the corresponding 'edge' pixels.
  - Note: The training data were created by varying the regions of interest (removing or merging areas) to manually select threshold values that determine pixel allocation to classification categories.

- Accuracy assessment pixels (3 cm classifications)
  - Mar_acc_prunus_pure_3cm: Shapefile polygons representing Prunus spinosa 'pure' pixels used in accuracy assessment for the 3 cm classification.
  - Mar_acc_prunus_edge_3cm: Shapefile polygons representing Prunus spinosa 'edge' pixels used in accuracy assessment for the 3 cm classification.
  - Mar_acc_other_3cm: Shapefile polygons representing 'other' pixels used in accuracy assessment for the 3 cm classification.

- Accuracy assessment pixels (7 cm classifications)
  - Mar_acc_prunus_pure_7cm: Shapefile polygons representing Prunus spinosa 'pure' pixels used in accuracy assessment for the 7 cm classification.
  - Mar_acc_prunus_edge_7cm: Shapefile polygons representing Prunus spinosa 'edge' pixels used in accuracy assessment for the 7 cm classification.
  - Mar_acc_other_7cm: Shapefile polygons representing 'other' pixels used in accuracy assessment for the 7 cm classification.

- Classification context
  - The datasets support maximum likelihood classifications at two resolutions: 3 cm and 7 cm.
  - Training data were used to train both classification variants; accuracy assessments are provided separately for each variant.

- Data governance and stewardship implications
  - All datasets are provided as shapefiles containing polygons that delineate the respective pixel categories (edge, pure, other).
  - Essential metadata to accompany these datasets should include: category definitions, spatial extent, coordinate reference system, number of polygons, and lineage (which training/accuracy dataset, and for which classification variant).
  - Enables reproducibility of classifications and assessment of pixel-level accuracy across resolutions.