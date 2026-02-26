# Random Forest Classification and Regression Scripts

## 1. Purpose
- Provide JavaScript examples to run random forest (RF) classification and regression in Google Earth Engine (GEE).
- Demonstrate mapping peatland distribution and predicted peat thickness, based on methods used in Hastie et al. (2022) Nature Geoscience.
- Link to related work and offer guidance on model building, validation, and exporting results.

## 2. What the scripts do
- RF_classification:
  - Imports a data stack including Landsat 7 bands (red, NIR, SWIR1, SWIR2), NDVI, NDWI; ALOS PALSAR HH/HV; elevation; slope; HAND.
  - Imports ground-truth polygons for training/testing.
  - Splits data into training/testing (default 50/50).
  - Samples remote sensing data to create training pixels and trains a RF model.
  - Classifies the study area into 5 classes (example) and displays the map in GEE.
  - Validates with a confusion matrix; reports producer’s and user’s accuracy.
  - Assesses variable importance via mean decrease in Gini (noting limitations).
  - Applies a weighted kernel smoothing to reduce isolated patches.
  - Calculates and exports the predicted area per class.
- RF_regression:
  - Similar workflow for peat thickness; imports training data and study extent.
  - Creates a random column to enable 100-fold cross-validation; splits data (default 80/20).
  - Builds the same data stack and RF model; runs cross-validation.
  - Extracts predictions from folds to generate distribution maps; computes median, mean, 5th and 95th percentiles.
  - Produces scatterplots of predicted vs observed peat thickness and exports results.

## 3. Data inputs and structure
- Data stack includes: Landsat 7 bands, NDVI, NDWI, ALOS PALSAR HH/HV, elevation, slope, HAND.
- Ground-truth polygons are required to train/test; user must specify polygon paths in the code.
- Data files are UTF-encoded plain text.
- Authors provide guidance and references within the code comments.

## 4. Running the model code
- Requires a Google Earth Engine account and familiarity with the GEE Code Editor (JavaScript).
- The classification example typically uses a 5-class output.
- Users should adjust training/testing splits, model parameters, and input data as needed.

## 5. Model parameters and interpretation
- Classification:
  - 50/50 train/test split by default; adjustable in code.
  - Variable importance shown via mean decrease in Gini (with acknowledged limitations).
- Regression:
  - 100 folds with a random column to assess uncertainty; folds may be constrained by GEE performance.
  - Cross-validation yields median, mean, 5th percentile, and 95th percentile predictions.

## 6. Outputs
- Classification:
  - Classified land-cover/peatland map.
  - Confusion matrix with producer’s and user’s accuracy.
  - Variable importance ranking.
  - Smoothed map and area estimates per class.
  - Exported (smoothed) map.
- Regression:
  - Predicted peat thickness maps with uncertainty percentiles.
  - Scatterplots of predicted vs observed thickness.
  - Exported results.

## 7. Notes, caveats, and considerations
- Detailed comments are embedded in the code for guidance.
- Feature importance (Gini) has known biases and limitations.
- GEE performance may constrain the number of folds or data volume (especially for >1,000 folds).
- Additional data can be incorporated beyond the example stack as needed.

## 8. References
- Hastie, A. et al. (2022) Risks to carbon storage from land-use change revealed by peat thickness maps of Peru. Nature Geoscience 15: 369-374. https://doi.org/10.1038/s41561-022-00923-4
- Rodríguez-Veiga, P. et al. (2020) Carbon stocks and fluxes in Kenyan forests and wooded grasslands derived from Earth observation and model-data fusion. Remote Sensing 12: 2380. https://doi.org/10.3390/rs12152380
- Strobl, C. et al. (2007) Bias in random forest variable importance measures: Illustrations, sources and a solution. BMC Bioinformatics 8:25. https://doi.org/10.1186/1471-2105-8-25

## 9. Author and funding
- Author/Contact: Dr Adam Hastie (adamhastie@hotmail.com)
- Project and funding: UKRI-NERC, grant NE/R000751/1; P.I. Dr Ian Lawson (itl2@st-andrews.ac.uk)