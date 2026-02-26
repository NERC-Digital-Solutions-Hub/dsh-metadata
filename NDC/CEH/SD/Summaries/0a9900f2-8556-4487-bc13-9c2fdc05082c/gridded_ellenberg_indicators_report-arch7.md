# Dataset Documentation for Gridded estimates of Ellenberg N, R, F, and L indicators for Great Britain 1990 and 2015-2019

## Overview
- Integrated model combines Countryside Survey (CS), Natural England's Long Term Monitoring Network (LTMN), and National Plant Monitoring Scheme (NPMS) data to map four Ellenberg indicators (N, R, F, L) across Great Britain.
- Aims to provide consistent spatial patterns by merging datasets with different coverage and protocols.
- Produces 1km-resolution gridded predictions for 2015-2019 (dominant Land Cover Map target classes) and 1990 (CS-only, for comparison).

## Data sources and indicators
- Datasets: CS, LTMN, NPMS (vegetation plots/quadrats; mixed spatial coverage).
- Indicators: Ellenberg N (nitrogen), R (moisture/acidity proxy), F (moisture/light), L (light availability).
- Focus: vascular plant information; bryophytes excluded due to recording differences.
- Data processing uses taxon matching (vegtaxon R package).

## Data collation and processing
- Time periods: 2015-2019 (2,375 plots: CS 445; LTMN 1,287; NPMS 643) and 1990 (2,282 CS plots).
- Plot types considered:
  - CS: randomly located 2m x 2m X plots.
  - LTMN: 2m x 2m VC plots on stratified grid.
  - NPMS: 5m x 5m squares on a grid (Inventory surveys only).
- Indicator calculations:
  - Both plot-average and cover-weighted Ellenberg values.
  - Cover reduced to Domin scale with midpoints used for weighted indicators.
- Covariates prepared to explain spatial patterns:
  - Habitat (Biodiversity Action Plan Broad Habitat classifications).
  - Nitrogen and sulphur deposition (CBED model; 5km means over preceding 10 years).
  - Climate variables (HadUKGrid; mean of preceding 10 years for 1km squares).
- Data standardized to enable cross-dataset comparability.

## Modelling approach
- Hierarchical, spatially explicit model:
  - Fixed effects for covariates.
  - Random effects: plot within site within scheme.
  - Shared spatial term across datasets.
  - NPMS-specific spatial term (to capture uptake/coverage patterns).
- Down-weighting and biases:
  - LTMN and NPMS down-weighted relative to CS due to coverage biases.
  - NPMS uptake modeled directly with a dataset-specific spatial term.
  - LTMN locations down-weighted using National Nature Reserve (NNR) presence/absence layer to reflect non-representative coverage.
- Model form (conceptual):
  - E(y) = covariates + (1 / scheme/site/plot) + s(East, North) + s(East, North, NPMS only)
- Stationarity assumed for 2015-2019; year-to-year variation within this period not estimated.

## Predictions and outputs
- Predictions generated on a 1km GB grid using:
  - Same climate and deposition inputs across periods.
  - Dominant Land Cover Map target class for each period (2015 LCM; 1990 LCM).
- Outputs:
  - Predicted mean indicator values for 1990 and 2015-2019 (non-cover weighted and cover-weighted versions).
  - Uncertainty maps (standard errors) accompany each prediction.
  - Difference maps: change between 2015-2019 and 1990.
- Format and structure:
  - Three sets of 2-band GeoTIFF files per indicator:
    - [variable]_90.tif: mean and SE for 1990.
    - [variable]_15-19.tif: mean and SE for 2015-2019.
    - [variable]_difference.tif: difference and SE between periods.
  - Suffixes:
    - _site: non-cover weighted maps.
    - _cwt: cover weighted maps.
  - Total: 24 files (4 indicators x 2 weighting schemes x 3 periods).

## Model validation and quality control
- Evaluation metric: RMSE.
- CS data drive performance (highest weighting, best spatial representation); used for validation in both periods.
- Findings:
  - General RMSE < 1 unit for most non-cover weighted indicators.
  - Cover-weighted indicators show higher RMSE due to cross-dataset variability in cover recording.
- Recommendations:
  - Prefer non-cover weighted values unless cover weighting is required.
  - Use accompanying uncertainty (standard error) maps for spatial caution, especially in northern Scotland.
- Limitations:
  - Potential subtle dataset-specific differences not fully captured by the model.
  - The approach provides best-use maps given available data; updates anticipated as new data become available.

## Change calculation
- Change = 2015-2019 predicted value minus 1990 predicted value.
- Uncertainty around change approximated by combining individual period SEs (SE_change ≈ sqrt(SE_1990^2 + SE_2015-19^2)); covariance not accounted for.

## Data structure and access
- File naming convention:
  - [variable]_[period].tif with two bands (mean, SE).
  - [variable]_difference.tif with mean difference and SE.
- Variables correspond to EBERGN, EBERGR, EBERGF, EBERGL, each with _site and _cwt variants.
- Data licensing: Open Government Licence.
- Citation: Jarvis et al. (2022) NERC EDS Environmental Information Data Centre.
- Reproducibility: modelling scripts available on request; public data sources listed (plot data, LCM, climate, deposition, NPMS weights, NNR map).

## Practical notes for GIS specialists
- Resolution and scope:
  - 1km grid across GB; suitable for broad spatial patterns and policy-scale analyses.
  - Not intended for detailed local-level, fine-scale guidance.
- Interpretation:
  - Non-cover weighted maps generally more reliable across datasets; cover-weighted maps show higher uncertainty.
  - Uncertainty maps highlight regions with higher prediction uncertainty (e.g., northern Scotland).
- Data usage considerations:
  - Data are combined from multiple schemes with differing designs; maps reflect a harmonised approach to integrate heterogeneous sources.
  - Expect potential residual biases due to dataset design even after weighting; plan to update with new data as available.