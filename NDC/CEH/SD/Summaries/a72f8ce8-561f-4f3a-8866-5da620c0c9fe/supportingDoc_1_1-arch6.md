# Supporting information for CEH Land Cover plus: Pesticides 2012-2016 (England and Wales)

## Overview
- A high-resolution product mapping pesticide applications across England and Wales at 1 km resolution, released in 2019.
- Combines CEH Land Cover Plus: Crops with PUS data to map average annual pesticide applications for 129 active ingredients.
- Data and outputs support spatial analysis of pesticide use, exposure risk, and environmental/public-health research.

## Data sources
- Pesticide Utilisation Survey (PUS): annual total applications (kg) per crop, county, year (2012, 2013 fodder/forage, 2014, 2016); includes foliar/granular and seed treatments.
- Crop area data: area grown per crop per county per year.
- Spatial reference: county centroids from ceremonial county boundaries; crops data from CEH Land Cover Plus: Crops.
- Organic areas in England masked using Environmental Stewardship data; Wales masking not implemented in this version.

## Product specification
- Output: raster data for 129 active ingredients, 1 km x 1 km, British National Grid (units: kg active ingredient per year).
- Each raster has two bands:
  - Band 1: Estimated application (kg/yr) per 1 km² for the active ingredient.
  - Band 2: Uncertainty (%), relative uncertainty based on parameter distributions.
- Temporal scope: average across 2012–2016 (not explicit year-to-year variation in the main product).
- Coverage: active ingredients must have ≥95% extent of England and Wales to be included; some ingredients excluded or incomplete in Wales (extents noted).
- Data limitations: missing data in mountains/urban areas where crops do not occur; some 1 km cells may be excluded if not relevant to a given ingredient.

## Methodology in brief
- Data collation: clean PUS data (remove unspecified actives, non-pesticide usage, non-pesticide controls); compute annual total applications per crop per county; calculate annual rates (kg/yr per km² of crop).
- Modelling: model annual application rates (lognormal) as a function of crop and county location, with a continuous spatial field (Gaussian Markov Random Field via INLA) to interpolate across counties; assume a common spatial pattern across crops.
- Prediction: combine crop-specific rates with 1 km² crop-area data from LC Plus Crops to estimate total application per cell; sum across crops within each 1 km cell.
- Uncertainty: generate 100 draws from parameter distributions to create a distribution of estimates per cell; compute 2.5% and 97.5% quantiles, scale by mean to express as a relative uncertainty (%).
- Temporal aspect: data treated as independent replicates across years; no explicit temporal trend due to limited years of data.

## Data outputs and formats
- 129 two-band TIFF rasters (UK National Grid, 1 km resolution).
- Band 1: Application (kg/yr) per active ingredient per cell.
- Band 2: Uncertainty (%) per cell.
- Data coverage notes: white areas indicate cells without data (no relevant crops or outside ingredient extent); some areas excluded due to 95% extent rule.

## Uncertainty and validation
- Uncertainty maps accompany each active ingredient, reflecting both rate and crop-coverage variability, plus spatial model uncertainty.
- Validation approaches:
  - Regional totals comparison: estimated regional totals vs. PUS site totals (averaged 2012–2016); acknowledges differences due to crop types included.
  - Posterior predictive checks with RMSE: compared against null models; 12 models failed null-model test and were removed; 86 of remaining 145 models passed a spatial-variation RMSE test.
- Extent filtering: 16 active ingredients removed for insufficient spatial extent; 12 removed due to RMSE criteria; results in 129 ingredients in final product.
- Wales data: some ingredients rely on Welsh data; for a subset of ingredients Wales is excluded to obtain model outputs with higher certainty.

## Data access and licensing
- Data access via Environmental Information Data Centre (EIDC): https://doi.org/10.5285/a72f8ce8-561f-4f3a-8866-5da620c0c9fe
- Citation required: Jarvis, S.G.; Henrys, P.A.; Redhead, J.W.; Da Silva Osório, B.M.; Pywell, R.F. (2019). CEH Land Cover plus: Pesticides 2012-2016 (England and Wales). NERC Environmental Information Data Centre. https://doi.org/10.5285/a72f8ce8-561f-4f3a-8866-5da620c0c9fe
- Licence fees may apply for some users/applications.
- Note: The document includes extensive appendices with Tables (Appendix 1 and 2) detailing regional comparisons and model test outcomes.

## Limitations and caveats
- Wales: some ingredients lack robust Wales data; uncertainty is higher in those extents.
- Temporal dynamics: product provides a snapshot (average 2012–2016); does not model year-to-year temporal variation explicitly.
- Crop-coverage dependency: accuracy depends on crop-area data and inclusion of crops; some crops or regions (e.g., soft fruits, vegetables) may be underrepresented.
- Validation data: no independent national-scale pesticide-application data; validation relies on regional totals and predictive checks against available PUS statistics.

## Example outputs
- Te buconazole (fungicide) example illustrates spatial patterns:
  - Higher applications in eastern England, lower in western regions.
  - White regions correspond to mountains/urban areas (no data).
  - Uncertainty ranges show higher relative uncertainty where data are sparser or variability is greater.

## Practical takeaways for Data Support
- This product exemplifies integrating multi-source data (PUS, crop maps) with spatial modelling to produce high-resolution, user-accessible data products.
- It demonstrates handling data gaps, extent filtering, and uncertainty quantification across a large geographic area and many variables.
- Suitable for data support tasks like preparing data products for end users, communicating uncertainty, and guiding future data collection to reduce gaps (notably in Wales and certain ingredients).