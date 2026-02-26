# Random Forest Classification and Regression Scripts

## Overview
- This document provides JavaScript scripts for performing random forest (RF) classification and regression in Google Earth Engine (GEE).
- Purpose: illustrate how to map peatland distribution and predict peat thickness using a multi-source remote sensing data stack.
- Based on Hastie et al. (2022) for peatland studies in the Lowland Peruvian Amazonia; includes citations to related work.

## Data inputs and structure
- Data stack includes:
  - Landsat 7 bands: red, NIR, SWIR1, SWIR2
  - Indices: NDVI, NDWI
  - ALOS PALSAR HH and HV polarizations
  - Elevation, slope, and height above nearest drainage (HAND)
- Training and testing data provided as ground polygons; user must specify the path to these polygons.
- Data files described as UTF-encoded plain text; code comments provide guidance.

## RF Classification workflow
- Load data stack and ground polygons; create feature stack.
- Split data into training and testing sets (example uses 50/50 split; adjustable via code).
- Sample training pixels from the stack to train the RF model.
- RF outputs a classified map with a predefined number of classes (example uses 5).
- Validate with a confusion matrix; compute producer's and user’s accuracy.
- Assess variable importance using the greatest mean decrease in Gini (noting limitations of this metric).
- Apply smoothing with a weighted kernel to remove isolated patches.
- Compute and export the predicted area for each class.
- Output: classified map, accuracy metrics, variable importance, smoothed map, class areas.

## RF Regression workflow
- Similar stacking of data; introduce a random column to enable k-fold cross-validation.
- Data split (example: 80/20 training/testing; adjustable).
- Use RF to model peat thickness; conduct k-fold cross-validation (default example uses 100 folds; GEE may limit feasibility for large runs).
- Generate predicted thickness distributions across folds; derive summary maps: median, mean, 5th percentile, 95th percentile.
- Create scatterplots of predicted vs observed thickness.
- Export results and associated maps.

## Running the model code
- Prerequisites:
  - Google Earth Engine account
  - Familiarity with the Google Earth Engine Code Editor and JavaScript
- Steps:
  - Import the provided scripts
  - Specify the path to ground polygons
  - Adjust RF parameters as needed for classification or regression
  - Run to generate maps, validation metrics, and exports
- Notes: detailed comments are embedded within the code files to guide customization.

## Outputs and deliverables
- Classification: land cover/peatland extent map, accuracy metrics (confusion matrix, producer’s and user’s accuracies)
- Feature importance: variable importance measures (mean decrease in Gini)
- Spatial refinement: smoothed classification map
- Area metrics: predicted area per class
- Regression: peat thickness distribution maps, uncertainty maps (via percentile maps), scatterplots (predicted vs observed)
- Exports: maps and results ready for dissemination or inclusion in reporting

## Data governance and transparency considerations
- Code emphasizes reproducibility and transparency via explicit data inputs, model parameters, and outputs.
- In-text references and citations accompany the workflow to support methodological choices.
- The scripts acknowledge potential methodological caveats (e.g., limitations of Gini-based variable importance, GEE fold limits).

## References
- Hastie, A. et al. (2022) Risks to carbon storage from land-use change revealed by peat thickness maps of Peru. Nature Geoscience.
- Rodríguez-Veiga, P. et al. (2020) Carbon stocks and fluxes in Kenyan forests and wooded grasslands derived from Earth observation and model-data fusion. Remote Sensing.
- Strobl, C., et al. (2007) Bias in random forest variable importance measures: Illustrations, sources and a solution. BMC Bioinformatics.

## Project context
- Project funded by UKRI-NERC, grant NE/R000751/1; Principal Investigator: Dr Ian Lawson.