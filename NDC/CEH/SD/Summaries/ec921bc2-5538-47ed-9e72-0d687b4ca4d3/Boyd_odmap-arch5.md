# Overview, Data, Model Assessment and Prediction (ODMAP) document supporting the dataset 'UK maps of habitat suitability surfaces at 1km resolution for mammals, lichens, bryophytes, plants and invertebrates 2000-2015'

## Purpose and scope
- Documents the methods and outputs for 1km habitat suitability surfaces for 5073 UK species (mammals, lichens, bryophytes, plants, invertebrates) across 2000-2015.
- Provides guidance on data structure, modeling workflow, predictors, validation, and output interpretation to support reuse and discovery.

## File naming and metadata
- Files: one .asc file per species named <species name>_ensemble.asc, representing ensemble model predictions.
- Metadata: metadata.csv with columns:
  - model_name: species model identifier (prefer persistent taxon identifiers)
  - taxon_group: higher taxonomic grouping
  - monads_with_records: number of 1km grid cells with records
  - scientific_name: Latin name of species
- Authorship: Robin J. Boyd, Oliver Pescott; contact robboy@ceh.ac.uk

## Model objective and scope
- Objective: prediction-focused habitat suitability; not suitable for time/space extrapolation.
- Output: continuous habitat suitability scores in [0, 1]; not comparable across species due to prevalence differences.
- Taxa covered: 5073 species across bryophytes, lichens, vascular plants, mammals, reptiles, amphibians, insects and non-insect invertebrates.
- Geography: United Kingdom (UK); extent 2000-2015; 1km UK grid.

## Data sources and biodiversity data quality
- Data type: presence-only occurrence data from multiple sources (structured surveys, atlas projects, citizen science, etc.), harmonised through UK recording schemes.
- Data filtering: removed species with fewer than 10 monads; retained unique species/monad records to reduce redundancy.
- Acknowledged biases: geographic sampling bias due to opportunistic data; cross-referencing with UK biodiversity indicators and UK Species Inventory for taxonomic resolution.

## Predictors and data processing
- Predictors: climate, land cover, and elevation.
  - Climate: first six principal components of climate space derived from WorldClim-like bioclimatic variables (19 bioclim vars reduced to PCs explaining 96% of climate space variance).
  - Land cover: 25 variables including broad categories (e.g., arable, woodland, built-up areas) and aggregated classes (e.g., urban, dwarf shrub heath, freshwater).
  - Elevation: average elevation per monad.
- Predictor preparation: climate maps averaged 2000-2015, processed via biovars() and PCA; land cover reprojected/aggregated to UK grid; covariates scaled/centered where appropriate.

## Modeling approach and workflow
- Algorithms: regularized GLMs (glmnet), MaxEnt, Random Forests.
- Pseudo-absences: generated using non-overlapping target-group method (akin to selecting pseudo-absences where other group members were recorded).
  - GLMs: 10,000 pseudo-absences per species.
  - MaxEnt and Random Forest: equal number of pseudo-absences as presence records.
- Data partitioning: five-fold cross-validation (each fold holds out 20% of presence and 20% of pseudo-absences).
- Model training: for each species, five models per algorithm with 20% held-out data; cross-validated AUC computed per fold and per algorithm.
- Model ensemble: ensemble predictions are a skill-weighted mean across the three algorithms, weights equal to cross-validated AUCs.
- Model averaging: ensemble of the three algorithms using cross-validated performance as weights; 15 prediction sets (5 folds × 3 algorithms) for uncertainty assessment.
- Non-independence: no spatial or temporal autocorrelation correction applied to residuals.

## Model settings and reproducibility
- Software: analyses in R 4.0.1; glmnet (GLMs), dismo (MaxEnt), randomForest (RF); custom soaR package for workflow; source code available on GitHub (https://github.com/robboyd/soaR).
- Default settings: 500 trees in RF; RF node splits use sqrt(number of predictors); MaxEnt features scale with data size; GLMs regularization via LASSO (cv.glmnet used for full-model prediction).
- Covariate processing notes: climate variables condensed to six PCs; multicollinearity considerations acknowledged, with prediction-focused rationale.

## Output, interpretation, and uncertainty
- Prediction output: relative habitat suitability scores in 0–1; not prevalence-adjusted, hence not comparable across species.
- Uncertainty: 15 ensemble sets (five folds × three algorithms) used to reflect algorithmic and parameter uncertainty; maps of coefficient of variation and standard deviation available on request.
- Plausibility checks: subset of models expert-assessed via an interactive RShiny app; typical evaluation covers record distribution maps and habitat suitability ranges; about 100 species per taxon group are typically reviewed when available.

## Quality assurance and limitations
- Data quality: presence-only data with potential geographic bias; stringent filtering reduces sparse data issues but may bias against rare species.
- Limitations: no explicit correction for spatial/temporal autocorrelation; predictions are relative and species-specific; some predictor variables are broad aggregates which can affect fine-scale interpretation.
- Output considerations: users should not interpret ensemble scores as absolute habitat suitability or species prevalence without additional contextual consideration.

## Access to data and related resources
- Covariate data sources:
  - Land cover maps for GB and Northern Ireland (CEH)
  - HadUK-Grid climate data (Met Office)
- Additional technical resources:
  - soaR R package on GitHub for model fitting and assessment
  - R packages: glmnet, dismo, randomForest
- Availability of ancillary outputs: uncertainty maps and variability statistics available upon request.

## References and supporting literature
- Key methodological references for pseudo-absences, SDMs, and model evaluation cited in the document (Barbet-Massin et al., 2012; Phillips et al., 2008, 2009; Breiman; Hijmans; Outhwaite et al.; etc.), plus software and data sources (R, WorldClim principles, UK land cover datasets).

## Contact and governance
- Data stewardship and governance considerations reflected in authorship attribution and open-access code/data practices; contact provided for further inquiries and data requests.