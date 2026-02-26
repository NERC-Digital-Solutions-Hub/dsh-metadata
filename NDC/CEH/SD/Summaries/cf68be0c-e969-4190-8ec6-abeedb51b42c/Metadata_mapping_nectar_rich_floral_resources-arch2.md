# Mapping nectar-rich floral resources for pollinators: overview of data

## Purpose and scope
- Provides an overview of data used to map nectar-rich floral resources for pollinators.
- Supports environmental monitoring by standardising data inputs, classifications, and outputs (maps, charts).

## Core data components
- Floral_unit_data.csv with floral unit widths; accompanying Floral_Unit_Metadata.rtf.
- Table_band_data.csv containing metadata for 3 cm and 7 cm aerial imagery (central wavelength, band width).
- Table_flowering_species.csv listing flowering plant species of interest; accompanying Flowering_species_metadata.rtf.

## Imagery, classifications, and training data by month

- March
  - Imagery: March_3cm.tif, March_7cm.tif, and 28_03_2019_6_Band_3.tif / 28_03_2019_6_Band_7_BIL.tif.
  - Training and accuracy: Mar_train_other.shp, Mar_train_prunus_pure.shp, Mar_train_prunus_edge.shp; accuracy shapefiles for prunus_pure_3cm, prunus_edge_3cm, other_3cm, and corresponding 7 cm variants.
  - Classifications: March_3cm_classification1.tif, March_3cm_classification2.tif, March_7cm_classification.tif.

- May
  - Imagery: May_3cm.tif, 14_05_2019_6_Band_3.tif, May_7cm.tif, 14_05_2019_6_Band_7_BIL.tif.
  - Training and accuracy: May_train_other.shp, May_train_silene_pure.shp, May_train_silene_edge.shp, May_train_cratae_pure.shp, May_train_cratae_edge.shp; accuracy shapefiles for silene_3cm, cratae_pure_3cm, cratae_edge_3cm, other_3cm, and corresponding 7 cm variants; May_7cm_train_* shapefiles.
  - Classifications: May_3cm_classification1.tif, May_3cm_classification2.tif, May_3cm_classification3.tif, May_3cm_classification4.tif, May_7cm_classification.tif, May_7cm_class_trained_7cm.tif.

- July
  - Imagery: July_3cm.tif, 04_07_2019_6_Band_3.tif, July_7cm.tif.
  - Training and accuracy: July_train_other.shp, July_train_cent_pure.shp, July_train_cent_edge.shp, July_train_rubus_pure.shp, July_train_rubus_edge.shp; accuracy shapefiles for cent_pure_3cm, cent_edge_3cm, rubus_pure_3cm, rubus_edge_3cm, other_3cm, and corresponding 7 cm variants.
  - Classifications: July_3cm_classification1.tif through July_3cm_classification8.tif, July_7cm_classification1.tif (and associated metadata Jul_class_meta.rtf).

## Metadata and governance
- Metadata files accompany imagery and classifications across months (e.g., March_image_metadata.rtf, May_class_metadata.rtf, July_image_metadata.rtf, Jul_class_meta.rtf).
- Training and accuracy meta files provided (e.g., March_acc&train_meta.rtf, May_acc&train_meta.rtf, July_acc&train_meta.rtf) to document dataset preparation and validation processes.

## Data organization and monitoring relevance
- Data are organized by month and by data type (imagery, training/accuracy shapefiles, classifications), with standardised naming to support reproducible analyses.
- Outputs support consistent monitoring of environmental health and pollinator resources through mapped classifications and accuracy assessments.
- Includes a mix of raster classifications (maximum likelihood) and vector training data, stored with explicit provenance through metadata files.

## Access and reuse considerations
- Designed to enable others to access underlying data used to generate final outputs, aligning with data-sharing practices for environmental monitoring datasets.