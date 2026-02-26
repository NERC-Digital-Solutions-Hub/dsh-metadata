# Supporting information for CEH Land Cover plus: Pesticides 2012-2016 (England and Wales)

## Overview
- Provides methodology and metadata for CEH Land Cover plus: Pesticides 2012-2016 (England and Wales), mapping pesticide applications at 1 km resolution.
- Combines CEH Land Cover Plus: Crops with Pesticide Utilisation Survey (PUS) data to map average annual applications across 129 active ingredients.
- Data intended for high-resolution analysis of cropping and pesticide use to support exposure risk modelling, management interventions, and policy assessments.
- Outputs include uncertainty estimates alongside application rates.

## Data Access and Citation
- Access via Environmental Information Data Centre: https://doi.org/10.5285/a72f8ce8-561f-4f3a-8866-5da620c0c9fe
- Citation required: Jarvis et al. (2019), CEH Land Cover plus: Pesticides 2012-2016 (England and Wales), NERC Environmental Information Data Centre.
- Licence fees may apply for some users and applications.

## Data Product and Format
- 129 two-band raster TIFF files (one per active ingredient).
- Coordinate system: British National Grid.
- Resolution: 1 km x 1 km.
- Bands:
  - Band 1: Application (kg per year per 1 km square)
  - Band 2: Uncertainty (percent uncertainty for the estimated application)
- Spatial coverage: England and Wales; areas without data appear where crops are absent or outside ingredient extent.
- Data availability caveats:
  - Some cells (mountain tops, urban areas) have no estimates due to no relevant crops.
  - Some active ingredients are excluded if they do not cover at least 95% of England and Wales.
  - Wales-specific predictions may be uncertain or excluded for certain ingredients due to Welsh data limitations.
  - England organic areas masked (via Organic Farming Scheme); Wales masking not implemented in this version.

## Methodology and Data Lineage
- Data sources:
  - PUS data for 2012, 2014, 2016 (arable) and 2013 (fodder/forage).
  - Crop area data from CEH Land Cover Plus: Crops.
  - County centroids from Ministry of Housing, Communities and Local Government.
- Processing steps:
  - Clean PUS data to remove non-pesticide uses and unspecified actives; compile annual kg applications per crop per county.
  - Compute annual application rates (kg per km² of crop grown) per active ingredient.
  - Model rates as a lognormal function of crop type and county location, with a continuous spatial field (Gaussian Markov Random Field) estimated via INLA to capture spatial smoothing.
  - Combine crop-area information from LC Plus: Crops to derive 1 km-square total applications by summing crop-specific rates times crop area.
  - Aggregate to 1 km squares; treat years as independent replicates due to limited year data.
- Predictions:
  - Use average cropping patterns from LC Plus Crops (2015–2017) to predict average total applications (2012–2016).
  - For crops with multiple rate estimates, average rates to avoid double counting.
  - Organic areas in England masked; Wales masking not yet implemented in this version.
- Uncertainty:
  - 100 draws from the posterior parameter distributions to create a distribution of estimates per 1 km cell.
  - 95% confidence intervals (2.5th–97.5th percentiles) used to derive relative uncertainty (Uncertainty = 100 × (CI width) / mean).
  - Uncertainty reflects both rate variability and crop-coverage variability.

## Validation and Quality Assurance
- Validation approaches:
  - Regional totals: compare summed regional estimates to PUS regional totals (averaged 2012–2016); notes about potential underestimation for non-arable crops.
  - Posterior predictive checks: RMSE compared to null models (no spatial variation) and crop-varying models.
- Outcomes:
  - 12 of 157 models failed the null-model RMSE test and were removed.
  - 86 of remaining 145 models passed the spatial-variation RMSE test.
  - Some ingredients excluded due to insufficient extent (less than 95% coverage) or poor RMSE performance.
- Appendix documentation provides detailed regional comparisons across English regions and Wales.

## Data Quality, Limitations, and Governance
- Limitations:
  - No independent national-scale validation dataset; regional checks rely on PUS totals.
  - Wales data sometimes excluded from modelling due to limited Welsh observations, increasing uncertainty for Wales.
  - The product uses an averaged cropping pattern over several years, so explicit temporal variation is not modeled.
  - Estimates may be biased for crops not mainly arable or fodder/forage and for ingredients with sparse observations.
  - 1 km estimates depend on crop presence and treatment proportions; missing crops in a cell reduce data availability.
- Extent and coverage decisions:
  - Only ingredients with at least 95% extent across England and Wales included in the final product.
  - Some ingredients excluded or with extrapolated Wales data; Appendix lists per-ingredient outcomes.
- Future improvements anticipated:
  - Additional years of fodder/forage data to reduce temporal uncertainty.
  - Potential Wales masking enhancements and refined spatial patterns per crop as data allow.

## Usage and Citational Guidance
- Intended uses include spatial analysis of pesticide applications, exposure assessment, and policy-relevant modelling in England and Wales.
- Users should account for spatially varying uncertainty, especially in regions with limited data or Wales-specific modelling gaps.
- Acknowledge data provenance (PUS, LC Plus Crops) and consult the accompanying methodology and uncertainty maps when interpreting results.

## Acknowledgements and References
- Acknowledges contributions from Fera and CEH data access teams.
- References include PUS, INLA, and related methodological works cited in the document.