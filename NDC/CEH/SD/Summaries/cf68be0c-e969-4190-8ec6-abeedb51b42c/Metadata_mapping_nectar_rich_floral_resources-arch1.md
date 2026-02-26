# Mapping nectar-rich floral resources for pollinators: overview of data

## Overview
- A comprehensive dataset designed to map nectar-rich floral resources for pollinators using remotely sensed imagery across three timepoints (March, May, July) and different spatial resolutions (3 cm and 7 cm).
- Includes imagery, ground-truth training data, accuracy assessments, and final classifications to support analyses of floral resource distribution and potential correlations with pollinator habitats.
- Data are organized by month with accompanying metadata to document imagery properties, classifications, and training/accuracy procedures.
- Floral resources are categorized by species/groups (e.g., Silene, Cratae, Rubus, Prunus) with dedicated training and assessment shapefiles.

## Core data files and metadata
- Floral_unit_data.csv: file detailing floral unit widths. Accompanying metadata in Floral_Unit_Metadata.rtf.
- Table_band_data.csv: metadata for 3 cm and 7 cm aerial imagery, including central wavelength and band width.
- Table_flowering_species.csv: list of flowering plant species used as classification categories. Metadata in Flowering_species_metadata.rtf.

## Monthly datasets

### March
- Imagery
  - March_3cm.tif
  - 28_03_2019_6_Band_3.tif
  - March_7cm.tif
  - 28_03_2019_6_Band_7_BIL.tif
  - March_image_metadata.rtf (metadata)
- Training and accuracy
  - Mar_train_other.shp
  - Mar_train_prunus_pure.shp
  - Mar_train_prunus_edge.shp
  - Mar_acc_prunus_pure_3cm.shp
  - Mar_acc_prunus_edge_3cm.shp
  - Mar_acc_other_3cm.shp
  - Mar_acc_prunus_pure_7cm.shp
  - Mar_acc_prunus_edge_7cm.shp
  - Mar_acc_other_7cm.shp
  - March_acc&train_meta.rtf (metadata)
- Classifications
  - March_3cm_classification1.tif
  - March_3cm_classification2.tif
  - March_7cm_classification.tif
  - Mar_class_meta.rtf (metadata)

### May
- Imagery
  - May_3cm.tif
  - 14_05_2019_6_Band_3.tif
  - May_7cm.tif
  - 14_05_2019_6_Band_7_BIL.tif
  - May_image_metadata.rtf (metadata)
- Training and accuracy
  - May_train_other.shp
  - May_train_silene_pure.shp
  - May_train_silene_edge.shp
  - May_train_cratae_pure.shp
  - May_train_cratae_edge.shp
  - May_acc_silene_3cm.shp
  - May_acc_cratae_pure_3cm.shp
  - May_acc_cratae_edge_3cm.shp
  - May_acc_other_3cm.shp
  - May_acc_Silene_7cm.shp
  - May_acc_Cratae_pure_7cm.shp
  - May_acc_Cratae_edge_7cm.shp
  - May_acc_other_7cm.shp
  - May_7cm_train_other.shp
  - May_7cm_train_cratae_pure.shp
  - May_7cm_train_cratae_edge.shp
  - May_7cm_train_silene_pure.shp
  - May_7cm_train_silene_edge.shp
  - May_7cm_train_acc_other.shp
  - May_acc&train_meta.rtf (metadata)
- Classifications
  - May_3cm_classification1.tif
  - May_3cm_classification2.tif
  - May_3cm_classification3.tif
  - May_3cm_classification4.tif
  - May_7cm_classification.tif
  - May_7cm_class_trained_7cm.tif
  - May_class_metadata.rtf (metadata)

### July
- Imagery
  - July_3cm.tif
  - 04_07_2019_6_Band_3.tif
  - July_7cm.tif
  - July_image_metadata.rtf (metadata)
- Training and accuracy
  - July_train_other.shp
  - July_train_cent_pure.shp
  - July_train_cent_edge.shp
  - July_train_rubus_pure.shp
  - July_train_rubus_edge.shp
  - July_acc_cent_pure_3cm.shp
  - July_acc_cent_edge_3cm.shp
  - July_acc_rubus_pure_3cm.shp
  - July_acc_rubus_edge_3cm.shp
  - July_acc_other_3cm.shp
  - July_acc_cent_pure_7cm.shp
  - July_acc_rubus_pure_7cm.shp
  - July_acc_rubus_edge_7cm.shp
  - July_acc_other_7cm.shp
- Classifications
  - July_3cm_classification1.tif
  - July_3cm_classification2.tif
  - July_3cm_classification3.tif
  - July_3cm_classification4.tif
  - July_3cm_classification5.tif
  - July_3cm_classification6.tif
  - July_3cm_classification7.tif
  - July_3cm_classification8.tif
  - July_7cm_classification1.tif
  - Jul_class_meta.rtf (metadata)

## Classification and metadata organization
- All imagery is stored as georeferenced TIFFs at 3 cm or 7 cm spatial resolution.
- For each month, there are separate training shapefiles (used to build classifiers), accuracy shapefiles (to assess performance), and final classification rasters.
- Metadata accompanies imagery and classification workflows to document sensor details, processing steps, and accuracy/classification metadata (RTF files such as March_acc&train_meta.rtf, May_class_metadata.rtf, Jul_class_meta.rtf, etc.).

## Species and floral resource focus
- Flowering species are defined as classification categories within Table_flowering_species.csv, with metadata outlining category definitions.
- Training and accuracy datasets include species/group labels such as Prunus, Silene, Cratae, Rubus, and generic “other” categories to support robust classification of nectar-rich floral resources.