# Dataset Documentation for Gridded estimates of Ellenberg N, R, F, and L indicators for Great Britain 1990 and 2015-2019

## Aim and Context
- Provides integrated, gridded estimates of Ellenberg N, R, F, and L indicators for Great Britain.
- Combines three vegetation datasets (Countryside Survey, Long Term Monitoring Network, National Plant Monitoring Scheme) to produce consistent spatial maps for 2015-2019, with 1990 maps derived from Countryside Survey data only.
- Enables monitoring of environmental conditions and policy performance over time using standardized outputs.

## Data Sources
- Countryside Survey (CS): random 2m x 2m plots (X plots); representative GB coverage.
- Natural England Long Term Monitoring Network (LTMN): 2m x 2m plots (VC plots); stratified grid; not fully representative of GB.
- National Plant Monitoring Scheme (NPMS): 5m x 5m plots; fixed grid; community scientists; potential sampling biases.
- 1990 maps rely solely on CS data due to data availability.
- Only vascular plants used for indicator calculation; bryophytes excluded due to recording differences.
- Taxon matching supported by vegtaxon R package.

## Indicator Computation
- Indicators: Ellenberg N (EBERGN), Ellenberg R (EBERGR), Ellenberg F (EBERGF), Ellenberg L (EBERGL).
- Calculations: both plot-average and cover-weighted Ellenberg values; cover values converted to the Domin scale with midpoints used for weighting.
- Covariates considered: broad habitat (Biodiversity Action Plan classification), nitrogen and sulphur deposition (CBED model), annual precipitation, maximum July temperature, minimum January temperature.
- Climate and deposition data derived as 10-year means for the year of survey; habitat at plot level.

## Modelling Approach
- Model framework accounts for data structure: plots nested within sites, nested within schemes (CS, LTMN, NPMS).
- Additive model components:
  - Covariate effects (f_p(X_p)).
  - Random effects for plot/site/scheme (α_i j k).
  - Spatial effects: a shared spatial term across all datasets (s(East, North)) plus an NPMS-specific spatial term (s(East, North, NPMS only)).
- Weighting and uptake adjustments:
  - Observation weights (W) applied to the likelihood to address dataset biases (notably down-weighting LTMN and adjusting NPMS uptake through a NPMS-only spatial term).
  - NPMS uptake directly modeled via a dataset-specific spatial term; LTMN and NPMS sampling non-representativeness acknowledged.
- Specific equations described but conceptually: Ellenberg ~ covariates + random effects + shared spatial smooth + NPMS-only spatial smooth.
- Stationarity assumed within 2015-2019 data; year-to-year variability not explicitly estimated.

## Predictions, Outputs, and Uncertainty
- Predictions generated on a 1 km grid across Great Britain for both time periods.
- Time periods and inputs:
  - 2015-2019: using climate/deposition inputs and 2015 Land Cover Map dominant class.
  - 1990: using climate/deposition inputs and 1990 Land Cover Map dominant class.
- Outputs include separate uncertainty maps (standard errors) for each indicator.
- Predictions provided as non-cover weighted (preferred) and cover-weighted variants; non-cover weighted generally more reliable.

## Quality Control and Validation
- Model fit assessed using RMSE, primarily based on CS data (highest weighting and GB-wide representation).
- Reported RMSE values indicate generally good predictive performance (RMSE often below 1 unit for individual indicators); cover-weighted indicators show higher RMSE due to differences in cover recording across schemes.
- Recommendation: use non-cover weighted indicator maps unless cover weighting is specifically required.
- Uncertainty is higher in parts of northern Scotland; outputs should be interpreted with caution in high-uncertainty regions.

## Calculation of Change (1990 vs 2015-2019)
- Change = predicted 2015-2019 value minus predicted 1990 value.
- Uncertainty of change approximated by SE = sqrt(SE_1990^2 + SE_2015-2019^2); covariance not accounted for, so this is a relative uncertainty estimate.

## Data Structure and Access
- Data delivered as three sets of 2-band TIFF files per indicator:
  - [variable]_90.tif: 1990 mean (band 1) and prediction standard error (band 2).
  - [variable]_15-19.tif: 2015-2019 mean (band 1) and prediction standard error (band 2).
  - [variable]_difference.tif: predicted difference (band 1) and SE of difference (band 2).
- Variables include EBERGN, EBERGR, EBERGF, EBERGL, with both '_site' (non-cover weighted) and '_cwt' (cover weighted) variants, totaling 24 files.
- Data are Open Government Licence; citations required when used.
- Reproducibility:
  - Scripts to replicate modelling process available on GitHub (request access; contact susjar@ceh.ac.uk).
  - Input data sources publicly available; plot location data available on request.

## Reproducibility and Data Availability
- Acknowledgements to contributors and funders.
- Data and methodological details enable replication and updating as new data become available.

## Additional References and Resources
- Linked datasets and methods for deposition, climate, and land-cover data; NPMS weights; NNR map; related foundational papers cited.