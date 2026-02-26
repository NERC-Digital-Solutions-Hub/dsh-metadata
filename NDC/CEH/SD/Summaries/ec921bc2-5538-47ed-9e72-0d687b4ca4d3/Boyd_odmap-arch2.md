# ODMAP document supporting dataset 'UK maps of habitat suitability surfaces at 1km resolution for mammals, lichens, bryophytes, plants and invertebrates 2000-2015'

## Purpose and scope
- Provides a reproducible workflow and outputs for predicting habitat suitability (0-1) for 5073 UK species across 2000–2015.
- Predictions are for monitoring environmental health and policy performance; models are designed for prediction (not extrapolation in time/space) and outputs are ensemble-based.
- Habitat suitability scores are not directly comparable across species due to differences in prevalence.

## Dataset and metadata
- One .asc file per species (5073 total), named <species name>_ensemble.asc.
- metadata.csv with columns: model_name, taxon_group, monads_with_records, scientific_name.
- Authorship: Robin J. Boyd, Oliver Pescott. Contact: robboy@ceh.ac.uk.

## Model objective and scope
- Models predict habitat suitability, not species likelihoods; outputs are continuous 0–1 measures.
- The study covers the United Kingdom (UK) at 1 km resolution, 8.5 W–2 E, 49.96 N–58.64 N, aggregated over 2000–2015.

## Data sources and taxonomic scope
- Taxa include bryophytes, lichens, vascular plants, mammals, reptiles, amphibians, insects, and other invertebrates.
- Presence-only data compiled from multiple sources (structured surveys, atlas projects, citizen-science and opportunistic records) via a partnership between the Biological Records Centre and national recording schemes.
- Data quality filters: retain only unique species/monad records; omit species recorded in fewer than 10 monads; enables model fitting for 5073 species.

## Predictor variables and data processing
- Predictors: climate, land cover, and elevation.
- Climate: first six principal components of climate space, derived from monthly min/max temperatures and precipitation, processed into WorldClim-like bioclimatic variables (19 variables reduced to 6 PCs explaining ~96% of climate space variance).
- Land cover: 25 variables, derived from UK land cover maps; includes re-projection steps for NI and GB, plus some aggregation (e.g., built-up areas, dwarf shrub heath, freshwater).
- Elevation: average elevation per monad.
- Data processing: climate maps (2000–2015) aggregated annually, then PCs computed; land cover maps harmonized across GB and NI; covariates scaled/centered as needed.

## Model algorithms and workflow
- SDM algorithms: regularized GLMs (glmnet), Maxent, and Random Forests.
- Pseudo-absences: generated using non-overlapping target group method to mitigate sampling bias (absence data drawn where focal species not recorded but a related taxon in the same group was recorded).
- Training and validation: five-fold cross-validation; each algorithm fitted five times with 20% held out per fold; 10,000 pseudo-absences for GLMs; pseudo-absences equal in number to occurrences for Maxent and RF.
- Model averaging: ensemble predictions are a skill-weighted mean of the three algorithms, weights based on cross-validated AUC per algorithm.

## Model settings and design choices
- Random Forest: 500 trees; at each split, a random subset of predictors (sqrt of total predictors).
- Maxent: number of features grows with data; up to 80 features; regularization tuned on a multi-region dataset.
- GLMs: LASSO regularization via cv.glmnet; cross-validation used for model selection, but full-data model used for prediction.
- Multicollinearity: 25 predictors used; principal components used for climate space; SDMs are chosen for prediction robustness rather than coefficient interpretation.

## Model evaluation and outputs
- Skill measured with AUC, calculated across five folds for each algorithm; ensemble weights are based on these cross-validated AUCs.
- Additional ensemble statistics computed; median AUC across folds and algorithms available on request.
- Output: relative habitat suitability scores (0–1) per species; not comparable across species due to prevalence differences.
- Non-independence: no explicit spatial or temporal autocorrelation correction in residuals.

## Uncertainty and plausibility checks
- Uncertainty: averaged predictions from 15 sets (5 folds × 3 algorithms); maps of coefficient of variation and standard deviation available on request.
- Plausibility checks: subset of models (roughly 100 species per taxon) assessed by experts via an interactive RShiny app; results not included in the release but planned for future evaluation to refine model quality.

## Software, code and data availability
- Analyses conducted in R 4.0.1; packages: glmnet (GLMs), dismo (Maxent), randomForest (RF).
- Custom package: soaR (species occurrence analyses in R) for model fitting, assessment, averaging, discretization, etc.; available on GitHub: https://github.com/robboyd/soaR.
- Covariate data sources: land cover maps for GB and NI (CEH catalogue links) and HadUK-Grid climate data (Met Office).

## Access, storage and reuse considerations
- Data are produced as 1 km resolution ASCII rasters with accompanying metadata; model outputs are relative, non-comparable across species.
- Underlying data include presence-only records with known geographic biases; target-group pseudo-absences mitigate some biases, but users should interpret results with these limitations in mind.
- Expert assessments are being used to inform plausibility, with future plans to integrate their insights.

## References
- Key methodological and data references provided (Barbet-Massin et al. 2012; Breiman et al. 2001, 2018; Cerasoli et al. 2017; Feng et al. 2019; Fick & Hijmans 2017; Friedman et al. 2010; Hijmans et al. 2017; Hollis et al. 2018; Morton et al. 2011, 2014; Outhwaite et al. 2019; Phillips et al. 2008, 2009; Pocock et al. 2015; R Core Team 2019).