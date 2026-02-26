# Gathering ground-truth data

## Overview
- Study area: hedgerow and field margins around a field in Northamptonshire.
- Imagery timeline: March, May, and July.
- Ground-truth focus: five nectar-rich flowering plant species (data in Table_flowering_species.csv).

## Ground-truth data collection and floral units
- Field margin species (Centaurea nigra and Silene dioica):
  - Floral unit locations determined relative to ground-control points using a DeWALT laser (±1.5 mm).
  - Floral unit definitions:
    - C. nigra: one capitulum.
    - S. dioica: flowers on the same main stalk within the same pixel considered one floral unit.
  - For each focal species, collected orientation and width of floral units; data stored in Floral_unit_data.csv.
- Hedgerow species (Prunus spinosa, Crataegus monogyna, Rubus fruticosus):
  - Flowering not synchronous; floral units form dense white clusters.
  - Dense white clusters in hedgerows used as the flowering unit for data acquisition months.

## Data acquisition and imagery
- Ground-truth locations for training and validation: registered to imagery using ground-control points.
- Training and validation pixels: selected from patches corresponding to floral units within imagery.

## Classification approach and workflow
- Software and methods:
  - Semi-automatic classification (SCP) plugin in QGIS 3.4.15 (Congedo 2016) for maximum likelihood classifications.
  - Regions of interest (ROIs) created via region-growing tool.
  - Classes: each flowering plant species of interest + an 'other' category.
- Pixel sampling strategy:
  - Included both 'pure' (spectrally representative) and 'edge' (spectrally mixed) seed pixels to capture variability.
  - Edge pixels may border non-target features (soil, green vegetation).
- Training and classification process:
  - Train on 3 cm imagery for March, May, and July.
  - Test alternative training variants (edge included vs excluded) and select the variant with the highest overall accuracy for 3 cm data.
  - Use the selected 3 cm training variant to classify the 7 cm imagery for each month.
  - May used a separate training set created from 7 cm data (May_training_7cm) to classify the May 7 cm image.

## Accuracy assessment and validation
- For each month, perform accuracy assessments to derive:
  - Overall accuracy
  - User's accuracy
  - Producer's accuracy
- The chosen 3 cm training variant per month informs the subsequent 7 cm classification.

## Data sources and references
- Carvell et al. (2007) on flowering unit definitions.
- Congedo (2016) Semi-Automatic Classification Plugin.
- QGIS (2020) Geographic Information System, version 3.4.15-Madeira.

## Notes on spectral treatment
- Edge vs. pure pixel considerations address spectral variability within clusters.
- Edge pixels may introduce spectral mixing; strategies include selective seed pixel variants to improve classifier performance.