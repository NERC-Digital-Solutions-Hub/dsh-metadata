# Random Forest Classification and Regression Scripts

## Overview
- JavaScript scripts for running random forest (RF) classification and regression in Google Earth Engine (GEE).
- Demonstrates mapping peatland extent and predicted peat thickness, based on Hastie et al. (2022) work in lowland Peruvian Amazonia.
- References methods and data used in associated Nature Geoscience paper; includes guidance on citations.

## What the scripts do
- RF classification (RF_classification):
  - Imports a stack of remote sensing data and ground-truth polygons for training/testing.
  - Creates a 50/50 train/test split (modifiable via code).
  - Samples training pixels, trains RF, classifies the map into up to 5 classes.
  - Outputs the classified map, samples validation data, and a confusion matrix with producer’s and user’s accuracy.
  - Assesses driver variable importance using mean decrease in Gini (with noted limitations).
  - Applies a weighted kernel smoothing to reduce isolated patches and estimates class areas.
  - Exports the smoothed map.
- RF regression (RF_regression):
  - Imports training data and study-area extent.
  - Introduces a random column for 100-fold cross-validation; default train/test split is 80/20 (modifiable).
  - Uses the same remote sensing data stack; trains RF and runs k-fold CV.
  - Produces predicted thickness distributions per fold; computes median, mean, 5th and 95th percentiles.
  - Generates scatterplots of predicted vs observed peat thickness.
  - Exports results.

## Data inputs and structure
- Data stack includes: Landsat 7 bands (red, NIR, SWIR1, SWIR2), NDVI, NDWI; ALOS PALSAR HH/HV; elevation; slope; height above nearest drainage (HAND).
- Ground data: polygons for training/testing (path to polygons to import).
- Data structure: UTF-encoded plain text files.
- Authors emphasize aligning inputs with the example setups used in the referenced studies.

## Running the model code
- Requires a Google Earth Engine account and basic familiarity with the GEE Code Editor (JavaScript).
- User specifies paths to input polygons and can adjust train/test splits, class definitions, and RF parameters.

## Outputs and interpretation for GIS work
- Classification workflow outputs:
  - Classified map and smoothed map.
  - Confusion matrix with producer’s and user’s accuracy.
  - Variable importance ranking (with caveats on interpretation).
  - Estimated area by class.
- Regression workflow outputs:
  - Maps of peat thickness predictions with uncertainty (from CV across folds).
  - Summary statistics (median, mean, 5th/95th percentiles) and predicted vs observed scatterplots.
  - Exported thickness results.

## Considerations and caveats
- Variable importance in RF (mean decrease in Gini) has limitations; see referenced literature (Strobl et al. 2007).
- GEE may struggle with very large folds or high-resolution data; 100 folds are suggested but may be heavy.
- Data availability and resolution can affect model performance; users may need to add data as required.

## References and provenance
- Hastie, A. et al. (2022) Risks to carbon storage from land-use change revealed by peat thickness maps of Peru. Nature Geoscience.
- Rodríguez-Veiga, P. et al. (2020) Carbon stocks and fluxes in Kenyan forests and wooded grasslands derived from Earth observation and model-data fusion. Remote Sensing.
- Strobl, C. et al. (2007) Bias in random forest variable importance measures. BMC Bioinformatics.

## Author, project, and funding
- Authored by Dr Adam Hastie (adamhastie@hotmail.com).
- Project funded by UKRI-NERC, grant NE/R000751/1; P.I. Dr Ian Lawson.
- Contact and collaboration details provided within the scripts.