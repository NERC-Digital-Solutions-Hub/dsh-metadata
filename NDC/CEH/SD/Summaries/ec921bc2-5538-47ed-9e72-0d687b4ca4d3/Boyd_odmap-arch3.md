# Overview, Data, Model Assessment and Prediction (ODMAP) document supporting the dataset 'UK maps of habitat suitability surfaces at 1km resolution for mammals, lichens, bryophytes, plants and invertebrates 2000-2015'

- Purpose and scope
  - Provides the methodological foundation for UK-wide 1km habitat suitability surfaces for 5073 species (bryophytes, lichens, vascular plants, mammals, reptiles, amphibians, insects, and non-insect invertebrates) for 2000-2015.
  - Outputs are continuous predictions of habitat suitability (0-1) intended for prediction, not extrapolation in time or space.

- Authorship and contact
  - Robin J. Boyd and Oliver Pescott. Contact: robboy@ceh.ac.uk

- Dataset and taxonomic coverage
  - Spatial extent: United Kingdom (including Northern Ireland) at 1km resolution.
  - Temporal extent: 2000-2015 (aggregated over this period).
  - Taxa: 5073 species across bryophytes, lichens, vascular plants, mammals, reptiles, amphibians, insects, and non-insect invertebrates.
  - Output format: one ensemble habitat-suitability ASCII file per species (named <species name>_ensemble.asc) plus a metadata.csv file with model_name, taxon_group, monads_with_records, scientific_name, etc.

- Metadata and data provenance
  - metadata.csv includes model_name (preferred identifier), taxon_group, monads_with_records (records per species), and scientific_name.
  - Data sources are presence-only records from multiple UK collaboration partners (structured surveys, atlas projects, citizen-science-like records).
  - Acknowledges geographic bias inherent in opportunistic data and documents filters applied to mitigate issues.

- Modeling objective and outputs
  - Objective: prediction-oriented SDMs, not explanatory; predictions are not intended to be comparable across species due to varying prevalence.
  - Outputs: relative habitat-suitability scores (0-1) per 1km cell, per species ensemble predictions.

- Data and predictor inputs
  - Biodiversity data: presence-only records de-duplicated to unique species/monad combinations; only species with ≥10 monads retained after filtering.
  - Predictors (25 total):
    - Climate: first six principal components of climate space derived from WorldClim-like bioclimatic variables (19 variables reduced via PCA to PC1–PC6; PC space explains ~96% of variance).
    - Land cover: 25 class-based covariates (e.g., broadleaved/coniferous woodland, arable, built-up areas, freshwater, etc.) expressed as monad-level percentages.
    - Elevation: average elevation.
  - Climate data processing: monthly min/max temperatures and precipitation from Met Office; 2000-2015 averages; PCAs with six components used as predictors.
  - Land cover processing: NI and GB maps reconciled onto a common grid; some classes aggregated for consistency.

- Modeling approach and algorithms
  - Algorithms: regularized GLMs (glmnet), Maxent, and Random Forests.
  - Pseudo-absences: generated using non-overlapping target-group method to address presence-only data biases (absences drawn where other species in the same taxonomic group were recorded but the focal species was not).
  - Pseudo-absences per species:
    - GLMs: 10,000 pseudo-absences
    - Maxent and Random Forests: pseudo-absences equal in number to presence data
  - Model fitting and cross-validation: five-fold cross-validation (each fold holds out 20% of presence and 20% of pseudo-absences).

- Model workflow and ensemble
  - For each species:
    1) De-duplicate to unique species/monad combinations.
    2) Generate target-group pseudo-absences.
    3) Fit five models per algorithm (five-fold CV).
    4) Compute AUC for each algorithm across folds; average to obtain a cross-validated skill per algorithm.
    5) Ensemble: compute a skill-weighted mean across the three algorithms (weights = cross-validated AUCs).
    6) Produce additional ensemble skill statistics.
    7) Optional expert assessment of ensemble predictions (up to 100 species per taxon group when available).
  - Model averaging: final predictions are a single ensemble set per species, weighted by algorithm performance (AUC).

- Validation, performance and uncertainty
  - Performance metric: Area Under the ROC Curve (AUC) computed from five-fold CV for each algorithm; used to weight ensemble contributions.
  - Additional metrics: median AUC across folds and algorithms reported on request.
  - Non-independence/ autocorrelation: no explicit correction for spatial or temporal autocorrelation in residuals.
  - Uncertainty quantification: 15 prediction sets (5 folds × 3 algorithms) averaged to form ensemble predictions; maps of coefficient of variation and standard deviation available on request.

- Plausibility checks and expert input
  - A subset of models (roughly 100 species per taxonomic group where possible) reviewed by domain experts via an interactive RShiny app.
  - App displays distribution of records, habitat-suitability maps, and species metadata; experts answered questions about data/model quality.
  - No aggregated expert-assessment results are published in the document; plans to analyse expert feedback in the future.

- Outputs, interpretation and accessibility
  - Outputs: relative habitat-suitability scores (0-1) per species; maps generated from the ensemble predictions.
  - Data accessibility: covariate data and code are publicly available; software and packages used are documented (R 4.0.1; glmnet, dismo, randomForest; soaR package on GitHub).
  - Reproducibility: workflow is described in detail; an R package (soaR) wraps modeling steps to facilitate replication; covariates and data sources are publicly accessible via specified links.

- Software, data, and reproducibility
  - Software: R 4.0.1; glmnet, dismo, randomForest; soaR (species occurrence analyses in R) for fitting models and managing tasks.
  - Code and data availability: soaR on GitHub; climate, land-cover, and other covariates are publicly available at designated CEH/UK metadata links; HadUK-Grid climate data referenced.
  - Data handling and governance: acknowledges metadata and data-sharing considerations; publicly sharing data is identified as a potential barrier, but model outputs and documentation are provided to support transparency and reproducibility.

- Key limitations and caveats
  - Use of presence-only data with potential geographic bias; filtering to 10+ monads may bias against rare species.
  - Absence of truly independent validation data; cross-validation within presence-only framework.
  - Spatial/temporal autocorrelation not explicitly corrected in residuals.
  - Predictions are not comparable across species due to differences in prevalence; results are intended for relative habitat suitability and monitoring purposes rather than direct cross-species comparisons of absolute suitability.

- References and methodological context
  - Cited methodological literature on pseudo-absences, SDMs, multicollinearity considerations, and model validation (Barbet-Massin et al., Phillips et al., etc.), plus software and data sources used (WorldClim-like climate, land-cover maps, HadUK-Grid, UK biodiversity datasets).