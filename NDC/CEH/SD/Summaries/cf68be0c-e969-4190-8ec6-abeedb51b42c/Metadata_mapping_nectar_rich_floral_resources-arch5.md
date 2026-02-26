# Mapping nectar-rich floral resources for pollinators: overview of data

## Overview
- A dataset collection mapping nectar-rich floral resources for pollinators, including floral unit measurements, imagery metadata, flowering species classifications, and extensive training/accuracy data for remote sensing classifications.
- Core data files: Floral_unit_data.csv, Table_band_data.csv, Table_flowering_species.csv.
- Imagery and classification data organized by collection periods (March, May, July) across multiple resolutions (3 cm and 7 cm) with accompanying metadata.
- All data are accompanied by metadata files (RTF) to document provenance, formats, and methods, supporting discoverability and reuse.

## Data assets and structure

- Floral and band metadata
  - Floral_unit_data.csv with Floral_Unit_Metadata.rtf.
  - Table_band_data.csv with 3 cm and 7 cm imagery metadata (central wavelength and band width).
  - Table_flowering_species.csv with Flowering_species_metadata.rtf.

- March data
  - Imagery: March_3cm.tif, March_7cm.tif, 28_03_2019_6_Band_3.tif, 28_03_2019_6_Band_7_BIL.tif (with March_image_metadata.rtf).
  - Training and accuracy: Mar_train_other.shp, Mar_train_prunus_pure.shp, Mar_train_prunus_edge.shp, Mar_acc_prunus_pure_3cm.shp, Mar_acc_prunus_edge_3cm.shp, Mar_acc_other_3cm.shp, Mar_acc_prunus_pure_7cm.shp, Mar_acc_prunus_edge_7cm.shp, Mar_acc_other_7cm.shp (with March_acc&train_meta.rtf).
  - Classifications: March_3cm_classification1.tif, March_3cm_classification2.tif, March_7cm_classification.tif (with Mar_class_meta.rtf).

- May data
  - Imagery: May_3cm.tif, 14_05_2019_6_Band_3.tif, May_7cm.tif, 14_05_2019_6_Band_7_BIL.tif (with May_image_metadata.rtf).
  - Training and accuracy: May_train_other.shp, May_train_silene_pure.shp, May_train_silene_edge.shp, May_train_cratae_pure.shp, May_train_cratae_edge.shp, May_acc_silene_3cm.shp, May_acc_cratae_pure_3cm.shp, May_acc_cratae_edge_3cm.shp, May_acc_other_3cm.shp, May_acc_Silene_7cm.shp, May_acc_Cratae_pure_7cm.shp, May_acc_Cratae_edge_7cm.shp, May_acc_other_7cm.shp, May_7cm_train_other.shp, May_7cm_train_cratae_pure.shp, May_7cm_train_cratae_edge.shp, May_7cm_train_silene_pure.shp, May_7cm_train_silene_edge.shp, May_7cm_train_acc_other.shp (with May_acc&train_meta.rtf).
  - Classifications: May_3cm_classification1.tif, May_3cm_classification2.tif, May_3cm_classification3.tif, May_3cm_classification4.tif, May_7cm_classification.tif, May_7cm_class_trained_7cm.tif (with May_class_metadata.rtf).

- July data
  - Imagery: July_3cm.tif, 04_07_2019_6_Band_3.tif, July_7cm.tif (with July_image_metadata.rtf).
  - Training and accuracy: July_train_other.shp, July_train_cent_pure.shp, July_train_cent_edge.shp, July_train_rubus_pure.shp, July_train_rubus_edge.shp, July_acc_cent_pure_3cm.shp, July_acc_cent_edge_3cm.shp, July_acc_rubus_pure_3cm.shp, July_acc_rubus_edge_3cm.shp, July_acc_other_3cm.shp, July_acc_cent_pure_7cm.shp, July_acc_rubus_pure_7cm.shp, July_acc_rubus_edge_7cm.shp, July_acc_other_7cm.shp (with July_acc&train_meta.rtf).
  - Classifications: July_3cm_classification1.tif, July_3cm_classification2.tif, July_3cm_classification3.tif, July_3cm_classification4.tif, July_3cm_classification5.tif, July_3cm_classification6.tif, July_3cm_classification7.tif, July_3cm_classification8.tif, July_7cm_classification1.tif (with Jul_class_meta.rtf).

## Data formats and metadata

- Formats: TIFF rasters for imagery and shapefiles for training/accuracy; metadata provided in accompanying .rtf files.
- Metadata coverage includes: dataset provenance, sensor/imagery details, band information, species/classification schemes, and method documentation for training and accuracy assessments.

## Purpose and use

- Designed to enable mapping and analysis of nectar-rich floral resources for pollinators using remotely sensed imagery.
- Provides end-to-end data for classification workflows (training samples, accuracy assessments, and final classifications) across multiple dates and resolutions.
- Metadata supports discovery, interpretation, and reuse by data stewards, researchers, and practitioners.

## Data governance and stewardship implications

- Large, multi-format dataset requiring robust data management, including consistent naming, storage, and metadata documentation.
- Per-month organization (March, May, July) with multiple data products (imagery, training/accuracy shapefiles, classifications) and accompanying RTFs to ensure traceability.
- Data stewards should monitor metadata completeness, manage storage for large rasters and shapefiles, and maintain linkage between imagery, training data, classifications, and their metadata to support reproducibility and updates.