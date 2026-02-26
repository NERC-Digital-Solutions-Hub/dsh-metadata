# Mapping nectar-rich floral resources for pollinators: overview of data

- Purpose in context of monitoring frameworks: Provides a comprehensive data stack to map and assess nectar-rich floral resources for pollinators, supporting evaluation of policies and informing future decisions.

## Data assets and structure

- Core reference tables:
  - Floral_unit_data.csv (flora unit widths) with metadata in Floral_Unit_Metadata.rtf
  - Table_band_data.csv (3 cm and 7 cm imagery metadata, e.g., central wavelength and band width)
  - Table_flowering_species.csv (flowering plant species used as classification categories) with metadata in Flowering_species_metadata.rtf

- Seasonal data folders and contents (March, May, July):
  - Imagery folders contain remotely sensed TIFFs (e.g., March_3cm.tif, March_7cm.tif; May_3cm.tif, May_7cm.tif; July_3cm.tif, July_7cm.tif) plus band-related files (e.g., 28_03_2019_6_Band_3.tif, 14_05_2019_6_Band_3.tif, 04_07_2019_6_Band_3.tif) and accompanying image metadata (e.g., March_image_metadata.rtf, May_image_metadata.rtf, July_image_metadata.rtf).
  - Training and accuracy shapefile folders contain pixel-data used for classification training and accuracy assessments (e.g., Mar_train_*.shp; Mar_acc_*.shp; May_train_*.shp; May_acc_*.shp; July_train_*.shp; July_acc_*.shp) with metadata in corresponding *_meta.rtf files.
  - Classifications folders contain maximum likelihood classifications in TIFFs (e.g., March_3cm_classification1.tif, March_3cm_classification2.tif, March_7cm_classification.tif; May_3cm_classification1.tif …; July_3cm_classification1.tif …; July_7cm_classification1.tif …) with metadata in Mar_class_meta.rtf and Jul_class_meta.rtf.
  - Each season includes multiple classification rasters at different resolutions (3 cm and 7 cm) to support comparison and validation.

- Metadata availability:
  - Accompanying metadata files exist for imagery, classifications, and training/accuracy data (e.g., Floral_Unit_Metadata.rtf, Flowering_species_metadata.rtf, March_image_metadata.rtf, May_image_metadata.rtf, July_image_metadata.rtf, Mar_class_meta.rtf, Jul_class_meta.rtf, etc.).
  - Metadata details cover data provenance, band specifications, naming conventions, and classification attributes.

## Data governance, quality and accessibility

- Metadata emphasis: Dataset relies on detailed metadata to verify data suitability, provenance, and compatibility for integration into monitoring analyses.
- Data standards and openness: Supports the sharing of underlying data and results (through classifications, training/accuracy data, and imagery) while highlighting potential barriers related to metadata completeness and data transformation needs.
- Data lineage and transformation: Multiple resolutions and seasonal datasets require careful transformation and harmonization to enable consistent monitoring metrics across time and space.

## Relevance for monitoring frameworks

- Temporal and spectral coverage:
  - Seasonal imagery and classifications (March, May, July) enable tracking of changes in nectar-rich floral resources across key pollinator activity periods.
  - Multi-resolution data (3 cm and 7 cm) allows evaluation of spatial detail versus generalized patterns in floral resources.
- Taxa- and habitat-specific insights:
  - Species-level and habitat-classification categories (e.g., Prunus, Silene, Cratae, Cent, Rubus) support targeted assessments of resource availability for different pollinator communities.
- Data to support policy evaluation:
  - Training and accuracy datasets provide means to assess and improve classification methods used in monitoring floral resources.
  - The structured dataset supports reporting via maps, charts, and dashboards to inform policy decisions and future monitoring iterations.

## Practical considerations for implementation

- Data integration:
  - Harmonize imagery, training data, and classifications across March, May, and July for consistent monitoring outputs.
- Data governance steps:
  - Maintain and update metadata to ensure ongoing data quality, compatibility, and transparent data sharing.
- Operational barriers to anticipate:
  - Ensuring complete and up-to-date metadata, managing data formats and transformations, and coordinating data sharing across teams or agencies.