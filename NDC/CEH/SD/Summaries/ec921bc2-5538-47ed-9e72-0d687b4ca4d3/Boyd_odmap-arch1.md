# Overview, Data, Model Assessment and Prediction (ODMAP) document supporting the dataset 'UK maps of habitat suitability surfaces at 1km resolution for mammals, lichens, bryophytes, plants and invertebrates 2000-2015'

## Purpose and scope
- Provides the methodology and outputs for UK habitat suitability surfaces at 1km resolution for 5073 species (across bryophytes, lichens, vascular plants, mammals, reptiles, amphibians, insects, and invertebrates) over 2000-2015.
- Aims to predict habitat suitability (0-1) using ensemble species distribution models (SDMs); predictions are for current-time/space prediction only and are not intended for temporal or spatial extrapolation.

## Data and metadata
- Data type: presence-only species occurrence data from diverse sources (structured surveys, atlas projects, citizen science).
- Filtering: unique species/1km grid cells retained; species with fewer than 10 monads omitted.
- Result: models for 5073 species; metadata in metadata.csv with columns: model_name, taxon_group, monads_with_records, scientific_name.
- Authorship and contact: Robin J. Boyd, Oliver Pescott.

## Model objective and taxon/location
- Location: United Kingdom (UK).
- Scale: 1km grid, UK extent (8.5°W to 2°E; 49.96°N to 58.64°N).
- Temporal extent: 2000-2015, aggregated over this period.
- Output: relative habitat suitability scores (0-1); not directly comparable among species due to prevalence differences.

## Predictor variables and data processing
- Predictors: 25 variables comprising climate space (first six principal components of climate space derived from 19 WorldClim bioclimatic variables), land cover (percentage cover per monad for various classes), and elevation.
- Climate processing: monthly min/max temperature and precipitation from Met Office HadUK-Grid (2000-2015); generated 19 bioclimatic variables; PCA to six components explaining 96% of climate-space variance; all predictors scaled/centered.
- Land cover processing: GB and NI maps merged; some classes aggregated (e.g., suburban/urban to built up areas; heather to dwarf shrub heath; water classes consolidated).
- Data sources: HadUK-Grid climate data, UK land cover maps (CEH), all publicly available; covariate data freely accessible.

## Conceptual model and assumptions
- No explicit species-environment hypotheses; focus on prediction rather than interpretation.
- Assumptions include: species are at equilibrium with environment; sampling bias can be mitigated; occurrence data are independent; predictors measured without error; niche conservatism over space/time.
- Multicollinearity treated as non-problematic for the prediction goal; principal components used to address climate variable correlation.

## Modeling approaches and workflow
- SDM algorithms: regularized generalized linear models (GLMs, via glmnet), Maxent, and Random Forests.
- Pseudo-absences: generated using non-overlapping target group method (same taxonomic group, locations without focal species).
- Data partitioning: five-fold cross-validation (each fold holds out 20% of presence data and 20% of pseudo-absences).
- Model settings:
  - Random Forest: 500 trees; mtry = sqrt(number of predictors).
  - Maxent: number of features grows with records, up to 80 features; regularization parameter tuned externally.
  - GLMs: LASSO-penalized; cross-validated error via cv.glmnet (full dataset used for prediction).
- Model evaluation: AUC for each algorithm over five folds; cross-validated AUC used as algorithm weights in ensemble.

## Model averaging and outputs
- Ensemble approach: weighted average of the three algorithms, weights equal to each algorithm’s cross-validated AUC.
- Non-independence correction: no spatial or temporal autocorrelation adjustments in residuals.
- Output format: continuous 0-1 habitat suitability surfaces per species.
- Uncertainty: averages across 15 prediction sets (5 folds × 3 algorithms); maps of coefficient of variation and standard deviation available on request.

## Plausibility checks and expert assessment
- Subset evaluation: approximately 100 species per taxon group underwent expert assessment via an interactive RShiny app.
- Experts evaluated data quality and model predictions; results are planned for future analysis to understand drivers of good models (no results provided in this document).

## Software, code and data availability
- Implementation: in R (version 4.0.1).
- Packages: glmnet (GLMs), dismo (Maxent), randomForest (Random Forests).
- Custom tooling: soaR R package (species occurrence analyses in R) to fit models, assess skill, perform model averaging, discretization, etc.; available on GitHub (https://github.com/robboyd/soaR).
- Data access: covariate data are publicly available; climate data from Met Office HadUK-Grid; land cover maps from CEH; metadata file included with the dataset (metadata.csv).

## Key caveats and limitations
- Data are presence-only with potential geographic and taxonomic biases; applied target-group pseudo-absences to mitigate sampling bias but biases may persist.
- Predictions are not comparable across species due to differences in prevalence.
- No explicit correction for spatial/temporal autocorrelation in residuals.
- Model outputs reflect current conditions (2000-2015) and are not intended for forecasting beyond the training period.

## References (selected)
- Barbet-Massin et al. 2012; Phillips et al. 2009, 2008; Outhwaite et al. 2019; Morton et al.; Hollis et al. 2018; Hijmans et al. 2017; Friedman et al. 2010; Breiman et al. 2018; De Marco & Nóbrega 2018; Pocock et al. 2015.