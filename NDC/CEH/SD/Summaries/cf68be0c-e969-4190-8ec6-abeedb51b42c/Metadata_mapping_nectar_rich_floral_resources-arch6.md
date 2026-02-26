# Mapping nectar-rich floral resources for pollinators: overview of data

## Overview
- A structured data bundle intended to map nectar-rich floral resources for pollinators using remotely sensed imagery and classification outputs.
- Data are organized by imagery months (March, May, July), with corresponding training/accuracy shapefiles, maximum likelihood classifications, and metadata.
- Includes supporting tables for floral units, imagery band metadata, and flowering species classifications to enable data exploration and product creation.

## Data assets

- Floral resources and species metadata
  - Floral_unit_data.csv (flowering unit widths) with accompanying Floral_Unit_Metadata.rtf
  - Table_band_data.csv (3 cm and 7 cm imagery metadata: central wavelength, band width)
  - Table_flowering_species.csv (flowering plant species and classification categories) with Flowering_species_metadata.rtf

- Imagery and metadata by month
  - March imagery
    - March_3cm.tif, 28_03_2019_6_Band_3.tif, March_7cm.tif, 28_03_2019_6_Band_7_BIL.tif
    - March_image_metadata.rtf
  - May imagery
    - May_3cm.tif, 14_05_2019_6_Band_3.tif, May_7cm.tif, 14_05_2019_6_Band_7_BIL.tif
    - May_image_metadata.rtf
  - July imagery
    - July_3cm.tif, 04_07_2019_6_Band_3.tif, July_7cm.tif
    - July_image_metadata.rtf

- Training, accuracy, and classifications by month
  - March
    - Training shapefiles: Mar_train_other.shp, Mar_train_prunus_pure.shp, Mar_train_prunus_edge.shp
    - Accuracy shapefiles: Mar_acc_prunus_pure_3cm.shp, Mar_acc_prunus_edge_3cm.shp, Mar_acc_other_3cm.shp, Mar_acc_prunus_pure_7cm.shp, Mar_acc_prunus_edge_7cm.shp, Mar_acc_other_7cm.shp
    - Classifications: March_3cm_classification1.tif, March_3cm_classification2.tif, March_7cm_classification.tif
    - Metadata: March_acc&train_meta.rtf, Mar_class_meta.rtf
  - May
    - Training shapefiles: May_train_other.shp, May_train_silene_pure.shp, May_train_silene_edge.shp, May_train_cratae_pure.shp, May_train_cratae_edge.shp
    - Accuracy shapefiles: May_acc_silene_3cm.shp, May_acc_cratae_pure_3cm.shp, May_acc_cratae_edge_3cm.shp, May_acc_other_3cm.shp, May_acc_Silene_7cm.shp, May_acc_Cratae_pure_7cm.shp, May_acc_Cratae_edge_7cm.shp, May_acc_other_7cm.shp, May_7cm_train_other.shp, May_7cm_train_cratae_pure.shp, May_7cm_train_cratae_edge.shp, May_7cm_train_silene_pure.shp, May_7cm_train_silene_edge.shp, May_7cm_train_acc_other.shp
    - Classifications: May_3cm_classification1.tif, May_3cm_classification2.tif, May_3cm_classification3.tif, May_3cm_classification4.tif, May_7cm_classification.tif, May_7cm_class_trained_7cm.tif
    - Metadata: May_acc&train_meta.rtf, May_class_metadata.rtf
  - July
    - Training shapefiles: July_train_other.shp, July_train_cent_pure.shp, July_train_cent_edge.shp, July_train_rubus_pure.shp, July_train_rubus_edge.shp
    - Accuracy shapefiles: July_acc_cent_pure_3cm.shp, July_acc_cent_edge_3cm.shp, July_acc_rubus_pure_3cm.shp, July_acc_rubus_edge_3cm.shp, July_acc_other_3cm.shp, July_acc_cent_pure_7cm.shp, July_acc_rubus_pure_7cm.shp, July_acc_rubus_edge_7cm.shp, July_acc_other_7cm.shp
    - Classifications: July_3cm_classification1.tif, July_3cm_classification2.tif, July_3cm_classification3.tif, July_3cm_classification4.tif, July_3cm_classification5.tif, July_3cm_classification6.tif, July_3cm_classification7.tif, July_3cm_classification8.tif, July_7cm_classification1.tif
    - Metadata: Jul_class_meta.rtf

## How the data are organized and what they enable
- Multi-temporal and multi-resolution structure (3 cm and 7 cm imagery) to support detailed mapping of floral resources.
- Classifications and training data support supervised/maximum likelihood classification workflows for identifying nectar-producing floral resources.
- Accompanying metadata files (RTFs) provide context on imagery bands, classification schemes, and training/validation details.
- Supporting tables (Floral units, imagery band metadata, and flowering species) enable cross-dataset interpretation and compatibility with analysis workflows.

## Potential uses for data support and insights
- Build self-serve dashboards or data products showing spatial distribution and temporal change in nectar-rich resources for pollinators.
- Compare classification outputs across months (March, May, July) and resolutions (3 cm vs 7 cm) to assess detection sensitivity and resource availability.
- Combine with species classifications to analyze habitat-specific floral resources and potential pollinator foraging patterns.
- Validate and refine classification models using the provided training and accuracy shapefiles, and extend analyses to new areas or time periods.
- Promote outputs and capture feedback by sharing placeholder prototypes or early maps for stakeholder input.

## Access and documentation notes
- Metadata files (RTFs) accompany imagery, training/accuracy data, and classifications to aid interpretation and reuse.
- The dataset includes explicit mappings between imagery data, classification outputs, and training/validation sets to support reproducibility and data product development.