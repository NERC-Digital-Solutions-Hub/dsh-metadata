# Random Forest Classification and Regression Scripts

## Overview
- Provides JavaScript code for Google Earth Engine (GEE) to perform random forest classification and regression.
- Demonstrates mapping peatland extent and peat thickness in lowland Peruvian Amazonia, following methods from Hastie et al. (2022).
- Outputs include classified landcover maps and peat thickness predictions, with validation and product exports.

## Data inputs and structure
- Data stack includes:
  - Landsat 7 bands: red, NIR, SWIR1, SWIR2
  - Indices: NDVI, NDWI
  - ALOS PALSAR HH and HV polarisations
  - Elevation, slope, and height above nearest drainage (HAND)
- Ground-truth polygons used for training and testing; user must specify paths to these polygons.
- Data structure noted as UTF-encoded plain text files.
- No quality control (N/A) footnoted in the documentation.

## Classification (RF_classification)
- Goal: classify the map into predefined landcover/peatland classes (example uses 5 classes).
- Process:
  - Import data stack and ground polygons, split data into training and testing (example 50/50 split; adjustable).
  - Sample training pixels from the stack to train a random forest model.
  - Classify the map and display results in GEE.
  - Validate using a sampling of validation data to produce a confusion matrix; compute producer’s and user’s accuracy.
  - Assess variable importance via greatest mean decrease in Gini (with caveats and known limitations).
  - Smooth the classified map with a weighted kernel to remove isolated patches.
  - Calculate the predicted area for each class.
  - Export the smoothed (final) map.
- Key configurable aspects: number of classes, split ratio, and RF parameters.

## Regression (RF_regression)
- Goal: map peat thickness distribution and quantify uncertainty.
- Process:
  - Import training data and study extent; create a random column and perform 100 folds for uncertainty assessment.
  - Split data into training/testing (example 80/20; adjustable).
  - Build the same remote sensing data stack as in classification.
  - Run the RF model with defined parameters; perform k-fold cross-validation.
  - Derive predicted distributions across folds; compute median, mean, 5th percentile, and 95th percentile maps.
  - Create scatterplots of predicted vs observed peat thickness; export results.
- Notes:
  - Be mindful of GEE limits when using large numbers of folds (>1,000 may be problematic depending on extent/resolution).
  - Additional data can be incorporated as needed.

## Running the models
- Requirements:
  - Google Earth Engine account and familiarity with the GEE code editor (JavaScript).
- Inputs:
  - Path to training/testing polygons; ensure data is accessible in GEE.
- Outputs:
  - Classification: classified map, smoothed map, class area estimates, accuracy metrics.
  - Regression: peat thickness distribution maps, uncertainty maps, scatterplots, and exported results.

## Outputs and interpretation
- Classification outputs include accuracy metrics (producer’s and user’s accuracy) and a confusion matrix.
- Feature importance indicates which drivers (variables) most influence classification (with acknowledged limitations of Gini-based measures).
- Regression outputs provide central tendency (median/mean) and uncertainty (5th/95th percentiles) maps, plus diagnostic plots.
- All final products are exportable for downstream use and sharing.

## Limitations and considerations
- Quality control is not implemented (N/A).
- Variable importance measures (mean decrease in Gini) have known biases; interpret with caution.
- Large 100-fold cross-validation can be computationally intensive in GEE.

## References and attribution
- Hastie, A. et al. (2022) Risks to carbon storage from land-use change revealed by peat thickness maps of Peru. Nature Geoscience.
- Rodríguez-Veiga, P. et al. (2020) Carbon stocks and fluxes in Kenyan forests and wooded grasslands derived from Earth observation and model-data fusion. Remote Sensing.
- Strobl, C. et al. (2007) Bias in random forest variable importance measures: illustrations, sources and a solution. BMC Bioinformatics.

## Author, project, and funding
- Author: Dr Adam Hastie (adamhastie@hotmail.com)
- Project/funding: UKRI-NERC, grant NE/R000751/1; P.I. Dr Ian Lawson (itl2@st-andrews.ac.uk)
- Notes: Detailed comments available within the code files.