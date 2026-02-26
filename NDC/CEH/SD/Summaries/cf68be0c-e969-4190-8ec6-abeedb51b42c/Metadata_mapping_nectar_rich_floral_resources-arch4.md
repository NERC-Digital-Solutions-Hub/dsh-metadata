# Mapping nectar-rich floral resources for pollinators: overview of data

## Overview
- A data collection intended to map nectar-rich floral resources for pollinators.
- Organised around imagery (3 cm and 7 cm resolutions) across three time periods (March, May, July), with corresponding training, accuracy assessments, and classifications.
- Includes both raw imagery and derived products, plus metadata to support discoverability and reuse.

## Core data tables and metadata
- Floral_unit_data.csv — file with floral unit widths; metadata in Floral_Unit_Metadata.rtf
- Table_band_data.csv — 3 cm and 7 cm aerial imagery metadata (central wavelength and band width)
- Table_flowering_species.csv — list of flowering plant species of interest and their classification categories; metadata in Flowering_species_metadata.rtf

## Imagery by month
- March imagery
  - March_3cm.tif, March_7cm.tif
  - 28_03_2019_6_Band_3.tif, 28_03_2019_6_Band_7_BIL.tif
  - Metadata: March_image_metadata.rtf
- May imagery
  - May_3cm.tif, 14_05_2019_6_Band_3.tif
  - May_7cm.tif, 14_05_2019_6_Band_7_BIL.tif
  - Metadata: May_image_metadata.rtf
- July imagery
  - July_3cm.tif, 04_07_2019_6_Band_3.tif
  - July_7cm.tif
  - Metadata: July_image_metadata.rtf

## Training and accuracy datasets
- March training and accuracy
  - Training: Mar_train_other.shp, Mar_train_prunus_pure.shp, Mar_train_prunus_edge.shp
  - Accuracy: Mar_acc_prunus_pure_3cm.shp, Mar_acc_prunus_edge_3cm.shp, Mar_acc_other_3cm.shp
  - 7 cm equivalents: Mar_acc_prunus_pure_7cm.shp, Mar_acc_prunus_edge_7cm.shp, Mar_acc_other_7cm.shp
  - Metadata: March_acc&train_meta.rtf
- May training and accuracy
  - Training: May_train_other.shp, May_train_silene_pure.shp, May_train_silene_edge.shp, May_train_cratae_pure.shp, May_train_cratae_edge.shp
  - Accuracy: May_acc_silene_3cm.shp, May_acc_cratae_pure_3cm.shp, May_acc_cratae_edge_3cm.shp, May_acc_other_3cm.shp
  - 7 cm equivalents: May_acc_Silene_7cm.shp, May_acc_Cratae_pure_7cm.shp, May_acc_Cratae_edge_7cm.shp, May_acc_other_7cm.shp
  - Additional 7 cm training: May_7cm_train_other.shp, May_7cm_train_cratae_pure.shp, May_7cm_train_cratae_edge.shp, May_7cm_train_silene_pure.shp, May_7cm_train_silene_edge.shp, May_7cm_train_acc_other.shp
  - Metadata: May_acc&train_meta.rtf
- July training and accuracy
  - Training: July_train_other.shp, July_train_cent_pure.shp, July_train_cent_edge.shp, July_train_rubus_pure.shp, July_train_rubus_edge.shp
  - Accuracy: July_acc_cent_pure_3cm.shp, July_acc_cent_edge_3cm.shp, July_acc_rubus_pure_3cm.shp, July_acc_rubus_edge_3cm.shp, July_acc_other_3cm.shp
    and July_acc_cent_pure_7cm.shp, July_acc_cent_edge_7cm.shp, July_acc_rubus_pure_7cm.shp, July_acc_rubus_edge_7cm.shp, July_acc_other_7cm.shp
  - Classifications: July_3cm_classification1.tif, July_3cm_classification2.tif, July_3cm_classification3.tif, July_3cm_classification4.tif, July_3cm_classification5.tif, July_3cm_classification6.tif, July_3cm_classification7.tif, July_3cm_classification8.tif, July_7cm_classification1.tif
  - Metadata: Jul_class_meta.rtf

## Classifications
- March classifications
  - March_3cm_classification1.tif, March_3cm_classification2.tif, March_7cm_classification.tif
  - Metadata: Mar_class_meta.rtf
- May classifications
  - May_3cm_classification1.tif, May_3cm_classification2.tif, May_3cm_classification3.tif, May_3cm_classification4.tif
  - May_7cm_classification.tif, May_7cm_class_trained_7cm.tif
  - Metadata: May_class_metadata.rtf
- July classifications
  - July_3cm_classification1.tif, July_3cm_classification2.tif, July_3cm_classification3.tif, July_3cm_classification4.tif, July_3cm_classification5.tif, July_3cm_classification6.tif, July_3cm_classification7.tif, July_3cm_classification8.tif
  - July_7cm_classification1.tif
  - Metadata: Jul_class_meta.rtf

## Metadata and provenance
- Metadata files accompany all data components, including:
  - Floral_Unit_Metadata.rtf
  - Flowering_species_metadata.rtf
  - March_image_metadata.rtf, May_image_metadata.rtf, July_image_metadata.rtf
  - March_acc&train_meta.rtf, May_acc&train_meta.rtf, July_acc&train_meta.rtf
  - Mar_class_meta.rtf, May_class_metadata.rtf, Jul_class_meta.rtf

## Data leadership considerations
- The collection provides end-to-end data assets for mapping nectar-rich floral resources, including base tables, multi-temporal imagery at two resolutions, supervised classification outputs, and full training/accuracy datasets.
- Clear, month-based structure supports reproducibility, validation, and iterative improvement of data products.
- Rich metadata across imagery, classifications, and training/accuracy components enhances discoverability, provenance, and governance for organisational data strategies.