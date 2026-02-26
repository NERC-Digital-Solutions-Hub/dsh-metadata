# Random Forest Classification and Regression Scripts

- Purpose and scope
  - Demonstrates how to run random forest classification and regression in Google Earth Engine (GEE) using JavaScript.
  - Based on methods used to map peatland extent and peat thickness in lowland Peruvian Amazonia, referencing Hastie et al. (2022).
  - Classification example outputs a landcover map (5 classes in the example) and associated accuracy metrics; regression example maps peat thickness and quantifies uncertainty.

- Data and inputs
  - Stack of remote sensing data: six Landsat 7 bands (red, NIR, SWIR1, SWIR2), NDVI, NDWI; ALOS PALSAR HH and HV; elevation; slope; height above nearest drainage (HAND).
  - Ground data: polygons used to train and test the model; user must specify the path to these polygons.
  - Data structure: UTF-encoded plain text files; code imports training/testing polygons to create training pixels from the data stack.

- Modeling approach
  - Classification
    - Splits data into training and testing sets (example 50/50; adjustable via code).
    - Trains a random forest classifier; allows modification of model parameters.
    - Produces a classified map and samples validation data to generate a confusion matrix.
    - Outputs producer’s and user’s accuracies; evaluates variable importance via mean decrease in Gini (noting limitations).
    - Applies a weighted kernel to smooth the map and estimates class area; exports the final map.
  - Regression
    - Creates a data stack similar to classification and uses a random forest regressor.
    - Generates a random column to enable k-fold cross-validation (default 100 folds; adjustable; be mindful of GEE limits for large folds).
    - Splits data (example 80/20; adjustable), trains the model, runs cross-validation, and extracts predictions for each fold.
    - Computes percentile maps (median, mean, 5th and 95th percentiles) and produces scatterplots of predicted vs observed peat thickness.
    - Exports the results and maps.

- Outputs and outputs format
  - Classification: classified landcover map, confusion matrix, accuracy metrics, variable importance, smoothed map, and area per class; export of the final map.
  - Regression: predicted peat thickness maps with uncertainty percentiles, scatterplots, and exported results.
  - All workflows rely on the GEE JavaScript environment and produce map outputs suitable for interpretation and policy-relevant reporting.

- Running the code
  - Prerequisites: Google Earth Engine account and familiarity with the GEE code editor (JavaScript).
  - User actions: specify paths to training polygons, adjust parameters (class count, train/test split, RF settings, smoothing, folds), and run to generate outputs.
  - Detailed in-code comments provide guidance for customization.

- Data quality and caveats
  - Quality control note: not explicitly provided (N/A).
  - Variable importance interpretation for RF can be limited; reference Strobl et al. (2007) for caveats on Gini-based importance measures.
  - GEE performance considerations: high fold counts may be computationally intensive; plan folds accordingly.

- References and provenance
  - Hastie, A. et al. (2022). Risks to carbon storage from land-use change revealed by peat thickness maps of Peru. Nature Geoscience.
  - Rodríguez-Veiga, P. et al. (2020). Carbon stocks and fluxes in Kenyan forests and wooded grasslands derived from Earth observation and model-data fusion. Remote Sensing.
  - Strobl, C. et al. (2007). Bias in random forest variable importance measures: Illustrations, sources and a solution. BMC Bioinformatics.

- Author and funding
  - Authored by Dr Adam Hastie (adamhastie@hotmail.com).
  - Funded by UKRI-NERC, grant NE/R000751/1; P.I. Dr Ian Lawson (itl2@st-andrews.ac.uk).