# Mapping nectar-rich floral resources for pollinators: overview of data

## Overview
- A data collection intended to support map-based visualization of nectar-rich floral resources for pollinators.
- Organised around imagery (3 cm and 7 cm resolutions) across three timeframes (March, May, July), with accompanying training/accuracy data, classifications, and metadata.
- Includes floral resource descriptors and flowering plant species categories to support classification and mapping.

## Key data assets

- Floral resource definitions and taxonomy
  - Floral_unit_data.csv with floral unit widths; Floral_Unit_Metadata.rtf with accompanying metadata
  - Table_band_data.csv with 3 cm and 7 cm aerial imagery metadata (central wavelengths, band widths)
  - Table_flowering_species.csv listing flowering plant species used as classification categories; Flowering_species_metadata.rtf with metadata

- Imagery by timeframe
  - March imagery
    - March_3cm.tif, March_7cm.tif
    - 28_03_2019_6_Band_3.tif, 28_03_2019_6_Band_7_BIL.tif
    - March_image_metadata.rtf
  - May imagery
    - May_3cm.tif, May_7cm.tif
    - 14_05_2019_6_Band_3.tif, 14_05_2019_6_Band_7_BIL.tif
    - May_image_metadata.rtf
  - July imagery
    - July_3cm.tif, July_7cm.tif
    - 04_07_2019_6_Band_3.tif
    - July_image_metadata.rtf

- Training and accuracy datasets
  - March training and accuracy
    - Mar_train_other.shp, Mar_train_prunus_pure.shp, Mar_train_prunus_edge.shp
    - Mar_acc_prunus_pure_3cm.shp, Mar_acc_prunus_edge_3cm.shp, Mar_acc_other_3cm.shp
    - Mar_acc_prunus_pure_7cm.shp, Mar_acc_prunus_edge_7cm.shp, Mar_acc_other_7cm.shp
    - March_acc&train_meta.rtf
  - May training and accuracy
    - May_train_other.shp, May_train_silene_pure.shp, May_train_silene_edge.shp
    - May_train_cratae_pure.shp, May_train_cratae_edge.shp
    - May_acc_silene_3cm.shp, May_acc_cratae_pure_3cm.shp, May_acc_cratae_edge_3cm.shp
    - May_acc_other_3cm.shp
    - May_acc_Silene_7cm.shp, May_acc_Cratae_pure_7cm.shp, May_acc_Cratae_edge_7cm.shp
    - May_acc_other_7cm.shp
    - May_7cm_train_other.shp, May_7cm_train_cratae_pure.shp, May_7cm_train_cratae_edge.shp
    - May_7cm_train_silene_pure.shp, May_7cm_train_silene_edge.shp
    - May_acc&train_meta.rtf
  - July training and accuracy
    - July_train_other.shp, July_train_cent_pure.shp, July_train_cent_edge.shp
    - July_train_rubus_pure.shp, July_train_rubus_edge.shp
    - July_acc_cent_pure_3cm.shp, July_acc_cent_edge_3cm.shp
    - July_acc_rubus_pure_3cm.shp, July_acc_rubus_edge_3cm.shp
    - July_acc_other_3cm.shp
    - July_acc_cent_pure_7cm.shp, July_acc_cent_edge_7cm.shp
    - July_acc_rubus_pure_7cm.shp, July_acc_rubus_edge_7cm.shp
    - July_acc_other_7cm.shp
    - July_train_other.shp (duplicated naming in structure noted), July_7cm_train_*.shp
    - July_acc&train_meta.rtf
  - Classifications (maximum likelihood outputs)
    - March classifications: March_3cm_classification1.tif, March_3cm_classification2.tif, March_3cm_classification3.tif, March_3cm_classification4.tif, March_7cm_classification.tif
    - May classifications: May_3cm_classification1.tif, May_3cm_classification2.tif, May_3cm_classification3.tif, May_3cm_classification4.tif, May_7cm_classification.tif, May_7cm_class_trained_7cm.tif
    - July classifications: July_3cm_classification1.tif, July_3cm_classification2.tif, July_3cm_classification3.tif, July_3cm_classification4.tif, July_3cm_classification5.tif, July_3cm_classification6.tif, July_3cm_classification7.tif, July_3cm_classification8.tif, July_7cm_classification1.tif
    - Classification metadata: respective _class_meta.rtf or Jul_class_meta.rtf

- Documentation and metadata
  - Metadata files accompany each data block:
    - Floral_Unit_Metadata.rtf, Flowering_species_metadata.rtf
    - March_image_metadata.rtf, March_acc&train_meta.rtf, Mar_class_meta.rtf
    - May_image_metadata.rtf, May_acc&train_meta.rtf, May_class_metadata.rtf
    - July_image_metadata.rtf, July_acc&train_meta.rtf, Jul_class_meta.rtf

## How to use in GIS workflows

- Build map-based data products showing spatial distribution of nectar resources at 3 cm and 7 cm resolutions.
- Integrate floral unit widths, species classifications, and band metadata to classify and visualize nectar resources.
- Develop time-series or multi-temporal maps by comparing March, May, and July imagery and classifications.
- Use training and accuracy shapefiles to reproduce and validate maximum likelihood classifications; reference metadata for methodological context.
- Combine raster classifications with floral species categories to produce habitat-resource maps for pollinators.

## Data considerations for GIS specialists

- Data are multi-temporal (March, May, July) and multi-resolution (3 cm and 7 cm), with many shapefiles for training and accuracy assessments.
- Taxonomic categories and classification schemes are provided via Flowering_species.csv and related metadata; ensure consistency when integrating across months.
- Large, complex datasets require careful data management and preprocessing; consult the accompanying metadata files to interpret band properties and classification processes.
- Coordinate systems, alignment between rasters and vector shapefiles, and metadata completeness are important for reproducible analyses.

## End products and deliverables

- Raster classifications (3 cm and 7 cm) for each month, suitable for map products and analysis of nectar resource distribution.
- Training and accuracy shapefiles to support methodology transparency and model reproducibility.
- Metadata-driven documentation to facilitate interpretation and reuse of the data assets.