# Gathering ground-truth data

## Overview
- Description of a study on hedgerow and field margins near a Northamptonshire study farm.
- Ground-truth data collected for five nectar-rich flowering plant species within eight days of imagery acquisition in March, May, and July.
- Data are used to train and validate pixel-based classifications of flowering plants from high-resolution imagery.

## Study area and ground-truth data
- Study area: hedgerow and field margins around a designated study farm.
- Ground-truth for five nectar-rich species documented in Table_flowering_species.csv.
- For field-margin species (Centaurea nigra and Silene dioica):
  - Floral unit locations determined relative to known ground-control points using a DeWALT laser (±1.5 mm).
  - Predicted locations used to select training and validation pixels from imagery.
- Floral unit definitions:
  - Centaurea nigra: one floral capitulum per unit.
  - Silene dioica: floral unit defined as flowers within the same pixel space on a main stalk.
- For Prunus spinosa, Crataegus monogyna, and Rubus fruticosus:
  - Flowering units tended to form dense white/almost-white clusters; assumed as target species clusters in hedgerow sections.
- For each field-margin species, collected orientation and width data (Floral_unit_data.csv).

## Data collection and plant species
- Target species of interest: Prunus spinosa, Crataegus monogyna, Rubus fruticosus, Centaurea nigra, Silene dioica.
- Flowering patterns were not synchronous across species at the study site.

## Classification, training, and accuracy assessment
- Classification method:
  - Semi-automatic classification (SCP) plugin in QGIS (Congedo, 2016) used for maximum likelihood classifications.
  - Imagery: 3 cm resolution used to create training sets for March, May, and July.
  - Regions of interest (ROIs) created with a region-growing tool.
  - Categories: each flowering species of interest plus an 'other' class (soil, green vegetation, etc.).
- Pixel sampling and variability:
  - Addressed edge effects by including both 'pure' pixels (whitest/pinkest) and 'edge' pixels (on patch edges or mixed within small patches).
- Training and classification process:
  - Applied maximum likelihood classification to 3 cm imagery for each month.
  - Tested multiple training set variants (edge included vs excluded) and selected the variant with the highest overall accuracy for each month.
  - The chosen 3 cm training variant was then used to classify the corresponding 7 cm imagery for each month.
  - Additionally, a May 7 cm training set was created (May_7cm_class_trained_7cm.tif) and used to classify May 7 cm imagery.
- Accuracy assessment:
  - Conducted for each classification variant to determine overall, user’s, and producer’s accuracies.

## Data products and outputs
- Datasets referenced:
  - Table_flowering_species.csv (flowering species list)
  - Floral_unit_data.csv (orientation and width of floral units)
  - Training and accuracy assessment metadata (per month)
  - May_7cm_class_trained_7cm.tif (7 cm May classification trained with 3 cm data)
- Outputs include classified rasters for March, May, and July at 3 cm and 7 cm resolutions, along with the corresponding training datasets and accuracy results.
- The workflow emphasizes selecting the best-performing training variant for each month to maximize accuracy, and applying that variant to higher-resolution imagery.

## References and methodology foundations
- Carvell et al. (2007): definition and relevance of floral units for bee foraging in hedgerows.
- Congedo (2016): Semi-Automatic Classification Plugin methodology.
- QGIS (2020): Software framework and version used (QGIS 3.4.15-Madeira).