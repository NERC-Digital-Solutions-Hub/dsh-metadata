# Random Forest Classification and Regression Scripts

## Overview
- JavaScript scripts designed to run random forest (RF) classification and RF regression in Google Earth Engine (GEE).
- Demonstrates methods used to map peatland distribution and estimate peat thickness in lowland Peruvian Amazonia, drawing on Hastie et al. (2022).
- Includes guidance on data inputs, model training, validation, variable importance, map smoothing, and exporting results.
- References key related works and provides code-level notes to help implementers.

## What the scripts do

- RF Classification
  - Imports multi-source remote sensing data to create a feature stack (six Landsat bands/indices: red, NIR, SWIR1, SWIR2; NDVI; NDWI; plus ALOS PALSAR HH/HV, elevation, slope, HAND).
  - Imports user-provided ground-truth polygons for training/testing.
  - Splits data (example: 50/50) into training and testing sets.
  - Trains a random forest classifier with configurable parameters.
  - Classifies the area into predefined land-cover classes (example uses 5 classes) and displays the result in GEE.
  - Samples validation data to produce a confusion matrix and calculates producer’s and user’s accuracies.
  - Assesses variable importance via mean decrease in Gini (with caveats about limitations).
  - Applies a weighted kernel smoothing to reduce isolated patches.
  - Computes and exports the predicted area per class.

- RF Regression
  - Imports training data and study-area extent.
  - Creates a random column and uses it to generate folds for cross-validation (example uses 100 folds; 80/20 train-test split is common in the example but adjustable).
  - Builds the same remote-sensing data stack as the classification script.
  - Trains RF regression, runs k-fold cross-validation, and extracts predicted distributions for each fold.
  - Produces summary maps: median, mean, 5th and 95th percentile estimates of peat thickness.
  - Generates scatterplots of predicted vs observed peat thickness and exports results.

## Data inputs and structure

- Data inputs come from a stack of remote-sensing measurements and terrain attributes.
- Ground-truth training data are user-supplied polygons (path must be specified in the code).
- Data structure noted as UTF-encoded plain text files for any associated metadata or outputs.
- Requires Google Earth Engine account and familiarity with the GEE Code Editor (JavaScript).

## Modeling approach and outputs

- Classification outputs
  - Classified peatland/land-cover map with user-defined class count (example: 5 classes).
  - Accuracy metrics: producer’s and user’s accuracies from a confusion matrix.
  - Variable importance: importance scores (mean decrease in Gini) to identify driving variables.
  - Final products: smoothed classification map and class-area estimates, ready for export.

- Regression outputs
  - Peat thickness predictions with uncertainty (median, mean, 5th and 95th percentiles across folds).
  - Validation visuals: predicted vs observed peat thickness scatterplots.
  - Final products: thickness maps and exported results.

## Running the models and prerequisites

- Requires a Google Earth Engine account and knowledge of JavaScript in the GEE Code Editor.
- For classification: provide path to training/testing polygons; adjust train-test split as needed.
- For regression: can configure the number of folds (default example uses 100) and train-test split (e.g., 80/20); note GEE performance limitations with very large fold counts.
- Data and code can be adapted with additional inputs as required.

## Governance, quality, and reuse considerations for Data Leaders

- End-to-end data pipeline demonstrates how to integrate multi-source remote sensing data with ground-truth data to produce actionable maps and thickness estimates.
- Emphasizes:
  - Data provenance: explicit data stack sources, ground-truth polygons, and references to the underlying study (Hastie et al. 2022).
  - Reproducibility: configurable parameters, explicit cross-validation/uncertainty assessment, and exportable results.
  - Quality assessment: classification accuracy metrics, confusion matrix, and caution regarding variable-importance interpretation (Gini-based measures).
  - Metadata and discoverability: notes on data structure (UTF-encoded text) and the need to document inputs, parameters, and outputs for reuse.
  - Collaboration and impact: aligns with multi-data-source approaches used to assess carbon-related risks and land-use impacts, enabling broader community use and adaptation.
- Practical considerations:
  - Variable importance measures have known biases; users should consult cited limitations (e.g., Strobl et al., 2007).
  - Smoothing and area calculations influence interpretation; transparency about thresholds and methodology is advised.
  - Cross-validation strategy (folds, splits) affects uncertainty estimates; balance computational feasibility with robustness.

## References and provenance

- Hastie, A. et al. (2022). Risks to carbon storage from land-use change revealed by peat thickness maps of Peru. Nature Geoscience, 15:369-374.
- Rodríguez-Veiga, P. et al. (2020). Carbon stocks and fluxes in Kenyan forests and wooded grasslands derived from Earth observation and model-data fusion. Remote Sensing, 12:2380.
- Strobl, C. et al. (2007). Bias in random forest variable importance measures: Illustrations, sources and a solution. BMC Bioinformatics, 8:25.