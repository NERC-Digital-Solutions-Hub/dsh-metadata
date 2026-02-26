# Overview, Data, Model Assessment and Prediction (ODMAP) document supporting the dataset 'UK maps of habitat suitability surfaces at 1km resolution for mammals, lichens, bryophytes, plants and invertebrates 2000-2015'

## Purpose and scope
- Describes the dataset and modelling workflow used to produce UK-wide 1km habitat suitability surfaces (0-1) for 5073 species across Bryophytes, Lichens, Vascular Plants, Mammals, Insects, and other invertebrates.
- Emphasises prediction rather than explanation; outputs are relative habitat suitability and not directly comparable across species due to prevalence differences.
- Scale: UK extent (GB and NI) at 1km resolution, 2000-2015 aggregated in time.

## Data and structure
- File naming: one .asc ensemble file per species named <species name>_ensemble.asc.
- Metadata: metadata.csv with columns including model_name, taxon_group, monads_with_records, scientific_name.
- Authorship and contact: Robin J. Boyd, Oliver Pescott; contact robboy@ceh.ac.uk.
- Output: relative habitat suitability scores (0-1); not comparable across species; ensemble predictions produced by model averaging.

## Taxa, location and data coverage
- Taxa: bryophytes, lichens, vascular plants, mammals, moths, hoverflies, dragonflies, butterflies, etc. (5073 species total).
- Location: United Kingdom (GB + NI).
- Biodiversity data: presence-only occurrence records aggregated from multiple sources (structured surveys, atlas projects, citizen science); potential geographic bias acknowledged.
- Data filtering: records degraded to unique species/monad (1km) combinations; species with fewer than 10 monads omitted to ensure model feasibility.

## Predictors and data processing
- Predictors: climate, land cover, and elevation.
  - Climate: first six principal components of climate space derived from WorldClim-like bioclimatic variables (PC1–PC6 explaining 96% of climate space variance).
  - Land cover: 25 predictors including various forest, grassland, urban, wetland, and water classes; data harmonised between Great Britain and Northern Ireland with some class aggregations.
  - Elevation: average elevation per monad.
- Data preparation: climate maps (2000-2015) averaged monthly values, PCA performed, scaled/centered, and used as predictors. Land cover maps reprojected and aggregated where appropriate.
- Variable selection: broad approach (25 predictors) chosen because the aim is prediction, not inference; multicollinearity considered manageable given ensemble methods and use of principal components.

## Modelling approach and algorithms
- Algorithms: regularized GLMs (glmnet), Maxent, and Random Forests.
- Pseudo-absences: generated per species using non-overlapping target group method (same taxonomic group; presence-only data).
  - GLMs: 10,000 pseudo-absences.
  - Maxent and Random Forests: equal number of pseudo-absences as occurrences.
- Model settings: standard defaults with specific tunings (GLMs with LASSO; RF with 500 trees; Maxent features grow with data up to a cap).
- Cross-validation: five-fold cross-validation (each fold uses 20% of presence and 20% of pseudo-absences); models trained five times per algorithm.
- Model averaging: ensemble predictions are a skill-weighted mean across algorithms, where weights are the cross-validated AUC scores per algorithm.

## Validation, plausibility checks, and uncertainty
- Skill assessment: cross-validated AUC for each algorithm; ensemble weights based on these AUCs; median AUC across folds and algorithms reported on request.
- Expert plausibility checks: subset of models (approximately 100 species per taxon group when possible) reviewed via an interactive RShiny app by domain experts; app visualises occurrence records, habitat suitability, and data provenance; feedback intended to inform future improvements.
- Non-independence: no explicit correction for spatial or temporal autocorrelation in residuals.
- Uncertainty: outputs include 15 prediction sets (5 folds × 3 algorithms) to capture algorithmic and parameter uncertainty; coefficient of variation and standard deviation maps available on request; explicit propagation into downstream analyses not performed.

## Outputs and interpretation
- Prediction outputs: relative habitat suitability scores in the 0-1 range; not comparable across species due to prevalence differences.
- Spatial resolution and extent: 1km grid cells across the UK (GB + NI) over 2000-2015.
- Output storage: ensemble predictions per species as .asc files; accompanying metadata describes modelling details.
- Access to methods and code: analyses conducted in R (version 4.0.1); SOA R package (soaR) used to fit models and manage tasks; code and package available on GitHub (https://github.com/robboyd/soaR).
- Data and covariates: covariate data are publicly available (specific land cover and climate data sources linked in document); climate data modified for use (details in predictor variables section).

## Reproducibility, software, and data accessibility
- Software stack: R 4.0.1; glmnet for GLMs; dismo for Maxent; randomForest for RF; soaR package to automate modelling workflow.
- Reproducibility: detailed workflow steps (data degradation, pseudo-absences, cross-validation, ensemble weighting) enable replication; cross-validation and ensemble methodology explicitly described.
- Data provenance: presence-only biodiversity data compiled via Biological Records Centre and UK recording schemes; data filtered and aligned to UK Species Inventory; sample bias acknowledged and mitigated via target-group pseudo-absences.

## References and further resources
- Key methodological references for pseudo-absences, model averaging, SDMs, and data sources are listed (Barbet-Massin et al. 2012; Phillips et al. 2008, 2009; Outhwaite et al. 2019; WorldClim variables; HadUK-Grid; UK Land Cover maps; R packages and authors).
- Links to data sources and the soaR package repository provided for users seeking to reproduce or extend analyses.