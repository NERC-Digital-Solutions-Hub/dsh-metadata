# ODMAP document supporting the dataset 'UK maps of habitat suitability surfaces at 1km resolution for mammals, lichens, bryophytes, plants and invertebrates 2000-2015'

## Purpose and scope
- Presents methods and outputs for generating UK-wide 1km habitat suitability surfaces (0-1) for 5073 species across bryophytes, lichens, vascular plants, mammals, reptiles, amphibians, insects, and invertebrates for 2000-2015.
- Emphasizes prediction with ensemble models and explicit output as relative suitability (not comparable across species due to prevalence not accounted for).

## Data products and file structure
- One .asc habitat file per species: <species name>_ensemble.asc (5073 files).
- Metadata: metadata.csv with model_name, taxon_group, monads_with_records, scientific_name.
- Authorship: Robin J. Boyd, Oliver Pescott; contact robboy@ceh.ac.uk.

## Study design: scope and location
- Location: United Kingdom (UK: GB + Northern Ireland).
- Scale: 1km resolution (Ordnance Survey grid); spatial extent 8.5W–2E, 49.96N–58.64N.
- Temporal extent: 2000-2015 (data aggregated over this period).

## Biodiversity data and availability
- Data are presence-only, sourced from diverse programs (structured surveys, atlas projects, citizen science, etc.) via BRC and UK recording schemes.
- Pre-filtering: unique species/monad records retained; species with fewer than 10 monads omitted to enable model fitting.
- Result: 5073 species modeled; data are opportunistic with potential geographic bias.

## Modelling approach
- Taxa coverage across bryophytes, lichens, vascular plants, mammals, etc.
- Algorithms used: regularized GLMs (glmnet), Maxent, and Random Forests.
- Ensemble approach: predictions weighted by cross-validated AUC scores (skill-weighted ensemble).

## Predictors and data preparation
- Predictors include climate, land cover, and elevation.
- Climate: first six principal components of climate space derived from WorldClim-like 19 bioclimatic variables, using HadUK-Grid data processed to 1km, scaled/centered.
- Land cover: UK CEH 2007 maps, harmonized between GB and NI with some aggregation (e.g., suburban/urban to built up areas; heather to dwarf shrub heath; water bodies combined into freshwater).
- Elevation: average elevation as a predictor.
- Predictor count: 25 variables (to support prediction; not intended for causal inference).

## Modelling specifics and assumptions
- Conceptual model: prediction-focused; no explicit hypotheses about species-environment relationships.
- Assumptions: species are at equilibrium with environment; sampling bias mitigated via target-group pseudo-absences; independence of observations; predictors measured without error; niche conservatism over space/time.
- Pseudo-absences: generated using non-overlapping target-group method (same taxon group, locations where focal species not recorded).
- Data partitioning: five-fold cross-validation (each fold holds out 20% of presence and 20% of pseudo-absences per species).

## Model settings and workflow
- Model settings: default settings for glmnet (LASSO), dismo (Maxent), and randomForest; RF = 500 trees; RF uses 5-variable splits; Maxent features scale with data, up to full features; regularization tuned with cross-region dataset.
- Workflow steps per species:
  1) Degrade occurrences to unique species/monad combos.
  2) Generate pseudo-absences via target-group method.
  3) Fit five models per algorithm with 5-fold cross-validation.
  4) Compute AUC per fold; average per algorithm.
  5) Ensemble predictions: weighted average across algorithms using their AUC scores.
  6) Compute additional skill statistics for ensemble.
  7) Expert plausibility assessment for a subset (up to 100 species per taxon, or all if fewer).

## Output and interpretation
- Output: relative habitat suitability scores in 0-1 scale; not directly comparable across species due to prevalence differences.
- Output products: ensemble raster per species; accompanying metadata and potential uncertainty summaries on request.
- Uncertainty: algorithmic and parameter uncertainty quantified by averaging 15 prediction sets (5 folds × 3 algorithms); coefficient of variation and standard deviation available on request.

## Validation and expert review
- Plausibility checks: subset of models evaluated by experts via an interactive RShiny app showing species records, habitat suitability, and data provenance.
- Outcome: qualitative feedback collected; plans to analyse determinants of good models in future; no public release of expert assessments.

## Software, data, and reproducibility
- Analyses conducted in R (version 4.0.1); key packages: glmnet (GLMs), dismo (Maxent), randomForest (RF).
- Custom package: soaR (species occurrence analyses in R) to fit models and support tasks (skill assessment, model averaging, discretization); hosted on GitHub: https://github.com/robboyd/soaR.
- Covariate data sources: land cover (GB and NI maps), climate data (HadUK-Grid-derived; HadUK-Grid sources cited); climate processing and 6 PC climate space explained.
- Data access: covariates freely available via CEH catalogues; climate data from Met Office HadUK-Grid.

## Limitations and considerations for use
- Presence-only data with potential geographic bias; models reflect sampling distribution as well as species-habitat associations.
- Not intended for extrapolation in space or time; predictions are for 2000-2015 with current covariates.
- No spatial or temporal residual autocorrelation correction applied.
- Prevalence not accounted for in predictions; cross-species comparability limited to relative habitat suitability within a species.

## References and supporting material
- Key methodological references for pseudo-absences, SDMs, and evaluation.
- Data provenance and processing citations for climate and land-cover products.
- Documentation of the soaR package and R-based workflow.