# Random Forest Classification and Regression Scripts

- Purpose: Provide example code to run random forest classification and regression in Google Earth Engine (GEE) for mapping peatland distribution and peat thickness in the lowland Peruvian Amazonia, based on Hastie et al. (2022). The scripts import a stack of remote sensing data, training polygons, and produce classified maps or peat thickness predictions with accompanying evaluation and outputs.
- Authors and funding: Dr Adam Hastie (adamhastie@hotmail.com); project funded by UKRI-NERC (NE/R000751/1) with PI Dr Ian Lawson.
- References to use: Hastie et al. (2022) Nature Geoscience; Rodríguez-Veiga et al. (2020) Remote Sensing; Strobl et al. (2007) on variable importance biases.

## Data and inputs

- Data stack inputs:
  - Landsat 7 bands: red, NIR, SWIR1, SWIR2
  - Indices: NDVI, NDWI
  - ALOS PALSAR HH and HV
  - Ancillary layers: elevation, slope, height above nearest drainage (HAND)
- Ground truth data: polygons used to train and test the model; user must specify the path to these polygons.
- Data structure: the scripts operate on a stack of remote sensing data and associated training/testing polygons; training/testing splits are configurable.
- Data governance and provenance notes: scripts document authorship, references, and intended data sources; outputs include classification/regression results and ancillary statistics.

## Methods and workflow

- RF Classification (classification script):
  - Build a multi-band data stack from remote sensing inputs.
  - Import ground polygons for training/testing; split data (example 50/50; modifiable).
  - Train a random forest classifier; classify the study area into predefined classes (example: 5 classes).
  - Evaluate with validation samples to produce confusion matrix and accuracy metrics (producer’s and user’s accuracy).
  - Assess variable importance via mean decrease in Gini (noting limitations).
  - Spatial smoothing with a weighted kernel; compute area per class; export the smoothed map.
- RF Regression (regression script):
  - Import training area and extent; create a random column (0–1) and generate 100 folds to assess model uncertainty; split data (example 80/20; modifiable).
  - Build the same data stack as the classification script.
  - Configure RF parameters; train with training data; perform k-fold cross-validation.
  - Extract predicted distributions from folds; compute median, mean, 5th and 95th percentile maps.
  - Produce diagnostic plots (scatterplots) of predicted vs observed peat thickness; export results.
- Outputs: classified maps or peat thickness maps, cross-validation metrics, variable importance, smoothed maps, and exportable results.

## Running environment and requirements

- Platform: Google Earth Engine (GEE) with JavaScript; code intended to be run in the GEE Code Editor.
- Prerequisites: GEE account and familiarity with running JavaScript in GEE.
- Notes on run-time and constraints: GEE may limit performance with large numbers of folds or high-resolution runs; 100 folds are used as an example but may be heavy.

## Data stewardship and governance considerations

- Documentation and provenance:
  - Clear authorship, contact details, project funding, and literature references are provided.
  - The scripts act as executable examples; users should maintain attribution when reusing results.
- Metadata and reproducibility:
  - The data inputs (bands, indices, SAR, elevation, HAND) and training polygons should be well-documented with variable names, sources, temporal coverage, and processing steps.
  - Output integrity relies on user-specified paths to input polygons and study extents; document these configurations for reproducibility.
- Data quality and QC:
  - Quality control is not explicitly defined in the scripts (Quality control: N/A); thus, implement site-specific QC, metadata checks, and validation beyond the built-in confusion matrix and CV outputs.
- Sharing, interoperability, and governance:
  - The code uses standard GEE data structures and is portable within GEE, but results depend on input data quality and the chosen model parameters.
  - When sharing results or workflows, include licensing, data sources, and any embargo or usage constraints on input data.

## Licensing, citations, and references

- Users should cite:
  - Hastie, A. et al. 2022. Nature Geoscience. “Risks to carbon storage from land-use change revealed by peat thickness maps of Peru.”
  - Rodríguez-Veiga, P. et al. 2020. Remote Sensing. “Carbon stocks and fluxes in Kenyan forests and wooded grasslands derived from Earth observation and model-data fusion.”
  - Strobl, C. et al. 2007. BMC Bioinformatics. “Bias in random forest variable importance measures.”
- Citations should accompany any reuse or redistribution of the scripts and derived maps.

## Summary of suitability for data stewards

- Provides a concrete, reproducible example of applying random forest methods to large, multi-source remote sensing datasets for land cover and peat thickness mapping.
- Emphasizes need for clear documentation of inputs, training data, model parameters, and outputs to support discoverability, reuse, and governance.
- Highlights potential governance gaps (QC, metadata) that Data Stewards would address when adopting or extending these scripts in organizational data ecosystems.