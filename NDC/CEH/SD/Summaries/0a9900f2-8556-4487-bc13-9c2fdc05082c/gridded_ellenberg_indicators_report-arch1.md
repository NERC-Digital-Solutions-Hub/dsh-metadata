# Dataset Documentation for Gridded estimates of Ellenberg N, R, F, and L indicators for Great Britain 1990 and 2015-2019

- Integrates three vegetation datasets (Countryside Survey, Natural England Long Term Monitoring Network, National Plant Monitoring Scheme) to produce spatial maps of Ellenberg indicators N, R, F, and L for Great Britain.
- Time coverage: 1990 (CS only) and 2015-2019 (integrated model).

## Background and purpose
- Aims to provide consistent spatial estimates of four vegetation indicators by combining datasets with different coverage and designs.
- Enables use of data with limited or uneven spatial coverage (LTMN, NPMS) by integrating with CS, which has representative GB coverage.
- Indicators describe environmental conditions: N (nutrient content), R (soil reaction acidity), F (moisture/wetness), L (light availability).

## Data sources and processing
- Data sources (2015-2019): CS (445 plots), LTMN (1,287 plots), NPMS (643 plots); 1990: CS only (2,282 plots).
- Plot types and scales:
  - CS: 2m x 2m randomly located X plots.
  - LTMN: 2m x 2m VC plots on a stratified grid.
  - NPMS: 5m x 5m squares on a grid (Inventory surveys when used).
- Indicators calculated:
  - Plot-average and cover-weighted Ellenberg values for vegetation plots.
  - Cover values converted to Domin scale; midpoints used for cover-weighted indicators.
  - Bryophyte indicators excluded due to inter-scheme recording differences.
- Covariates considered to explain spatial patterns: broad habitat (mapped to Biodiversity Action Plan habitats), nitrogen and sulfur deposition (CBED, 1km grid, mean over preceding 10 years), annual precipitation, maximum July temperature, minimum January temperature (HadUKGrid, 1km, mean over preceding 10 years).
- Taxon matching performed with vegtaxon R package; data structured to enable cross-scheme integration.

## Modelling approach
- Goal: estimate a shared spatial pattern across datasets while accounting for non-representative scheme coverage.
- Model components:
  - Covariate effects (fixed effects).
  - Random effects for plot within site within scheme.
  - Spatially explicit shared effect across all datasets.
  - NPMS-specific spatial term (to capture uptake/coverage differences).
- Formal model concept (paraphrased): Ellenberg indicators are modeled as a function of covariates, random effects, and smooth spatial terms, with an additional NPMS-specific spatial term.
- Weighting and sampling considerations:
  - NPMS squares weighted to habitats of interest; incorporated as observation weights in the likelihood.
  - LTMN site placement biased by nature reserve locations; downweighting applied using an NNR presence layer.
  - NPMS uptake estimated directly from NPMS data via a dedicated spatial term (dummy variable) to capture complex uptake patterns.
- Time structure: year effects within 2015-2019 treated as non-estimated; stationarity assumed within that period.

## Predictions and outputs
- Predictions produced for both time periods on a 1 km grid across GB, using the same climate, deposition, and Land Cover Map inputs and the dominant 1 km land cover class for each period.
- 1990 predictions rely on the 1990 Land Cover Map; 2015-2019 predictions use the 2015 LCM.
- Separate uncertainty maps (standard errors) accompany each indicator map.
- Data products include 24 two-band TIFF files:
  - [variable]_90.tif: 1990 mean and SE (non-cover or cover-weighted variants).
  - [variable]_15-19.tif: 2015-2019 mean and SE.
  - [variable]_difference.tif: difference mean and SE between 1990 and 2015-2019.
  - Variables: EBERGN, EBERGR, EBERGF, EBERGL with suffixes _site (non-cover weighted) or _cwt (cover weighted).

## Quality control and validation
- Model fit assessed primarily against CS data (highest weighting, best spatial representation, available in both periods).
- Validation indicates generally good performance (RMSE typically < 1 unit for non-cover weighted indicators); cover-weighted indicators show higher RMSE due to greater inter-dataset variation in recording.
- Recommendation: use non-cover weighted indicator values unless cover-weighted values are specifically required.
- Uncertainty maps highlight higher uncertainty in northern Scotland and other regions; use these maps to guide interpretation.

## Data structure and access
- Data format: 24 two-band TIFF files per indicator (mean and standard error, per time period and per weighting scheme).
- Data availability: Open Government Licence.
- Citation: Jarvis et al. (2022) dataset; DOI provided; accompanying methodology and scripts available on request or via GitHub.
- Reproducibility: Scripts to replicate the modelling process available on request; input data are publicly available with location constraints for Countryside Survey plot data.

## Change calculation
- Change between 1990 and 2015-2019 computed as the difference between predicted values for 2015-2019 and 1990.
- Uncertainty around change estimated via propagation of standard errors (SE_2015-2019 and SE_1990), noting that covariance is not accounted for.

## Data availability and acknowledgments
- Data and methodology underpinning the gridded indicators are backed by NERC/UK-SCAPE support; NPMS and CS data acknowledgments and data sources listed.
- Users must cite the dataset and refer to data sources and licensing when using the maps.