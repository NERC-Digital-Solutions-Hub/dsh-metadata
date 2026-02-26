# Dataset Documentation for Gridded estimates of Ellenberg N, R, F, and L indicators for Great Britain 1990 and 2015-2019

## Overview
- Presents gridded estimates of Ellenberg N, R, F, and L indicators (nutrient content, acidity, moisture, light) for Great Britain.
- Derived from an integrated model combining three vegetation datasets: Countryside Survey (CS), Natural England Long Term Monitoring Network (LTMN), and the National Plant Monitoring Scheme (NPMS).
- Time periods: 2015-2019 (integrated across all three datasets) and 1990 (CS only).
- Outputs include 1 km grid predictions and accompanying uncertainty maps; also provides changes from 1990 to 2015-2019.

## Data Sources and Processing
- Datasets used: CS, LTMN, NPMS; CS provides representative GB coverage, LTMN and NPMS have less uniform coverage.
- Plots and time frames:
  - 2015-2019: 2,375 plots (CS 445, LTMN 1,287, NPMS 643).
  - 1990: 2,282 CS plots.
- Plot types:
  - CS: randomly located 2m x 2m X plots.
  - LTMN: 2m x 2m VC plots on stratified grid.
  - NPMS: 5m x 5m squares on a fixed grid (Inventory surveys only).
- Indicator construction:
  - Uses vascular plants only; computes plot-average and cover-weighted Ellenberg indicators.
  - Cover values converted to Domin scale; midpoints used for weighting.
  - Bryophytes excluded due to cross-scheme recording differences.
  - Taxon matching via vegtaxon R package.
- Covariates considered (to explain spatial patterns): broad habitat (BAP), nitrogen and sulphur deposition (CBED 10-year mean), annual precipitation, maximum July temperature, minimum January temperature.
- Auxiliary data:
  - Deposition data from CBED; climate data from HadUKGrid; habitat mapping linked to BAP classes.
  - LCM (Land Cover Map) used for dominant class in predictions.

## Modelling Approach
- Hierarchical model structure:
  - Fixed effects: covariates (m terms).
  - Random effects: plot within site within scheme.
  - Spatial components: shared spatial effect across all datasets plus NPMS-uptake-specific spatial effect.
  - NPMS uptake modeled with a dataset-specific spatial term (NPMS only) and a dummy indicator.
- Handling dataset differences:
  - Weighting to account for uneven scheme coverage; NPMS uptake modeled directly to capture complex patterns.
  - LTMN location bias mitigated by downweighting based on National Nature Reserve (NNR) overlap.
  - CS treated as the most representative and heavily weighted dataset.
- Key model form (conceptual):
  Ellenberg ~ covariates + (1/scheme/site/plot) + s(East, North) + s(East, North, NPMS only)
- Stationarity assumption for 2015-2019; year effects within 2015-2019 not explicitly modeled.

## Predictions, Validation, and Uncertainty
- Predictions:
  - 1 km grid cells across GB for 1990 and 2015-2019; uses corresponding Land Cover Map (LCM) dominant class per period.
  - Separate uncertainty maps (standard error) provided for each indicator.
- Validation:
  - RMSE assessed primarily on CS data (highest weighting and best spatial representation).
  - Findings: non-cover weighted indicators generally predict better than cover-weighted ones; cover-weighted indicators show higher uncertainty due to cross-dataset recording variation.
- Uncertainty and regional notes:
  - Higher uncertainty in northern Scotland; treat estimates there with caution.
- Change calculation:
  - Change = 2015-2019 value minus 1990 value.
  - Uncertainty for change is SE(change) = sqrt(SE1990^2 + SE2015-19^2); covariance not accounted.

## Data Structure and Access
- File format: three sets of 2-band TIFF files per indicator.
- Naming:
  - [variable]_90.tif: 1990 predicted means (band 1) and standard error (band 2).
  - [variable]_15-19.tif: 2015-2019 predicted means (band 1) and standard error (band 2).
  - [variable]_difference.tif: differences (band 1) and SE (band 2).
- Indicators:
  - EBERGN, EBERGR, EBERGF, EBERGL; with separate non-cover weighted (_site) and cover-weighted (_cwt) variants.
- Availability and licensing:
  - Open Government Licence.
  - Citations required: Jarvis et al. 2022; NERC EDS, UK-SCAPE.
  - Scripts to reproduce modeling available on request; GitHub repository: NERC-CEH/T1.1-indicatormaps.
  - Input data sources publicly available; CS plots data available on request; NPMS weights provided separately.

## Reuse, Limitations, and Considerations for Data Leaders
- Strengths for data leadership:
  - Demonstrates integration of multiple data sources with varying coverage to produce consistent spatial indicators.
  - Incorporates covariates and spatial modelling to explain broad patterns and improve transferability.
  - Produces explicit uncertainty maps and change estimates to support decision-making.
  - Clear data documentation, licensing, and provenance; reproducible workflow (scripts available).
- Limitations and caveats:
  - Potential residual biases due to non-representative scheme coverage (LTMN, NPMS) despite weighting and NPMS uptake modelling.
  In 1990, maps rely solely on CS data; cross-time comparability depends on data consistency.
  Cover-weighted indicators are more variable across schemes; non-cover-weighted indicators are preferred for general use.
  Uncertainty is higher in some regions (e.g., northern Scotland) and should be considered in interpretation.
- Usage guidance:
  - Prefer non-cover weighted values for broad analyses; refer to uncertainty maps when applying results to decision-making.
  - Update plans anticipated as new data become available; acknowledge potential residual differences from a single unbiased dataset.