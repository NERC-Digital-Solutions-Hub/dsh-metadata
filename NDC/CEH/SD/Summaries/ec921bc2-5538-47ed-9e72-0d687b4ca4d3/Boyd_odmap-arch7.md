# Overview, Data, Model Assessment and Prediction (ODMAP) document supporting the dataset 'UK maps of habitat suitability surfaces at 1km resolution for mammals, lichens, bryophytes, plants and invertebrates 2000-2015'

## What the dataset contains
- 5073 species across bryophytes, lichens, vascular plants, mammals, reptiles, amphibians, insects and invertebrates.
- For each species, a single 1km resolution habitat suitability map (0-1) produced by an ensemble of species distribution models (SDMs).
- Output files: one ASCII (.asc) file per species named <species name>_ensemble.asc.
- Metadata: a metadata.csv with columns model_name, taxon_group, monads_with_records, scientific_name.
- Authors: Robin J. Boyd, Oliver Pescott. Contact: robboy@ceh.ac.uk.
- Location: United Kingdom (UK), 1km grid, 2000–2015 (aggregated over this period).

## Model objective and outputs
- Purpose: predict habitat suitability (not species prevalence or future extrapolation in time/space).
- Output: continuous habitat suitability scores (0–1); scores are not comparable across species due to differing prevalence.
- Output format intended for map-based visualization and spatial analysis in GIS workflows.

## Scope and scale
- Geography: UK (Great Britain and Northern Ireland).
- Spatial resolution: 1km OS grid.
- Temporal extent: data aggregated over 2000–2015.
- Taxonomic scope: 5073 species across multiple groups (e.g., bryophytes, lichens, vascular plants, various insects, moths, mammals, etc.).

## Data sources and data quality
- Biodiversity data: presence-only occurrence data from diverse sources (structured surveys, atlas projects, citizen science, etc.), leading to geographic sampling biases.
- Data sources include collaboration with national recording schemes and the Biological Records Centre (BRC); data subset corresponds to 2000–2015 used in UK biodiversity indicators.
- Filtering applied: retain only unique species/monad records; omit species with fewer than 10 monads; this reduces model fitting issues for rare species.
- Result: models constructed for 5073 species after data filtering.

## Model predictors and data processing
- Predictors used (25 total):
  - Climate: first six principal components of climate space derived from 19 WorldClim bioclimatic variables (via monthly HadUK-Grid data processed to biovars and PCA).
  - Land cover: 25 classes, expressed as percentage cover per monad; includes conversions/reclassifications (e.g., urban into built up areas, etc.).
  - Elevation: average elevation per monad.
- Climate processing: monthly minimum/maximum temperature and precipitation (2000–2015), then 19 bioclimatic variables, scaled/centered, PCA; PC1–PC6 used as predictors (96% variance explained).
- Land cover processing: NI data reprojected to British Grid and combined with GB; some classes aggregated for consistency.
- Variable pre-selection: broad predictor set used since the aim is prediction (not inference); multicollinearity is mitigated by using principal components and by algorithm robustness.

## Modelling approach and workflow
- SDM algorithms used: regularized GLMs (LASSO), Maxent, and Random Forests.
- Data preparation per species:
  - Degrade occurrence data to unique species/monad combinations.
  - Generate pseudo-absences using the non-overlapping target group method (pseudo-absences in locations where the focal species was not recorded but another in the same taxon group was recorded).
  - For GLMs: 10,000 pseudo-absences; for RF and MaxEnt: pseudo-absences equal in number to occurrence data.
- Model fitting and validation:
  - Five-fold cross-validation: each of five folds holds out 20% of occurrences and 20% of pseudo-absences.
  - Each algorithm trained five times (one per fold).
  - Performance metric: AUC for each fold; algorithm AUCs averaged to yield a cross-validated skill score per algorithm.
  - Ensemble prediction: predictions from the three algorithms are averaged using weights equal to their cross-validated AUCs (skill-weighted mean).
  - Additional ensemble statistics computed; non-independence corrections not applied to residuals.
- Model averaging and outputs:
  - A single ensemble prediction per species produced via model averaging.
  - Output is relative habitat suitability (0–1) for each 1km cell.

## Validation, plausibility checks, and uncertainty
- Plausibility checks: subset of models (typically up to 100 species per taxon) assessed by domain experts via an interactive RShiny app, evaluating data and model outputs; results not included in the released dataset but planned for future analysis.
- Output uncertainty:
  - Uncertainty quantified by averaging 15 prediction sets (5 folds × 3 algorithms).
  - Maps of coefficient of variation and standard deviation available on request.
  - Uncertainty not propagated into downstream analyses by default.

## Software, data and accessibility
- Software: analyses conducted in R (version 4.0.1); packages include glmnet (GLMs), dismo (Maxent), randomForest (RF); custom R package soaR (species occurrence analyses in R) available on GitHub.
- Code and workflows: soaR wraps standard packages to fit models, perform skill assessment, model averaging, discretization, etc. GitHub: https://github.com/robboyd/soaR
- Covariate data sources:
  - Land cover: UK-wide 1km maps (GB and NI) from CEH.
  - Climate: HadUK-Grid data processed to WorldClim-like variables.
- Data caveats: presence-only data with potential geographic bias; effort to mitigate biases via target-group pseudo-absences and cross-validation, but residual biases may remain.

## Outputs and practical use for GIS work
- Habitat suitability rasters (1km resolution) facilitate map-based visualization, spatial summaries, and spatial decision-making.
- Outputs are designed for prediction and mapping within the UK, suitable for integration into GIS analyses, policy briefing maps, or public-facing visualization.
- Metadata and outputs are organized to support traceability (species naming, taxon group, records count per monad).

## References (key methods and data sources)
- SDM and pseudo-absence methodology (target group approach), cross-validation and ensemble weighting, WorldClim and climate covariates, CEH land-cover data, HadUK-Grid climate data, R packages glmnet/dismo/randomForest, and related methodological literature cited in the document.