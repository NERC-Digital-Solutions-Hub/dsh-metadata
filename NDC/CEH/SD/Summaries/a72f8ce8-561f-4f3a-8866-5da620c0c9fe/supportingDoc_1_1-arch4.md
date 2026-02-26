# Supporting information for CEH Land Cover plus: Pesticides 2012-2016 (England and Wales)

## Overview
- Provides methodology, metadata, and data product details for CEH Land Cover Plus: Pesticides 2012-2016 (England and Wales).
- Delivers high-resolution (1 km) maps of average pesticide applications across England and Wales for 129 active ingredients, covering 2012–2016 (average values).
- Combines CEH Land Cover Plus: Crops with Pesticide Utilisation Survey (PUS) data to map annual pesticide applications and associated uncertainty.
- Intended for research, policy, and environmental management uses, including exposure risk and runoff modelling.

## Data Product: Format, Scope, and Access
- Format: 2-band raster TIFFs at 1 km x 1 km, British National Grid.
  - Band 1: Application in kg/yr of each active ingredient.
  - Band 2: Uncertainty as a percentage for each 1 km cell.
- Coverage: England and Wales; 129 active ingredients included (some excluded due to insufficient extent or data quality).
- Data extent notes:
  - Areas with no data where the ingredient is not applied to crops, mountains, urban areas, or outside the ingredient’s extent.
  - Some ingredients have Wales extrapolations with high uncertainty; generally, Wales data included but with caveats.
- Data availability:
  - Access via Environmental Information Data Centre.
  - Citation required: Jarvis et al. (2019).
  - Licence fees may apply for some users/applications.

## Data Sources and Provenance
- Primary data sources:
  - Pesticide Utilisation Surveys (PUS): 2012, 2013 (fodder/forage only), 2014, 2016.
  - Crop area and type data from CEH Land Cover Plus: Crops (LC Plus Crops) for 2015–2017.
  - County centroid locations from MHCLG ceremonial county boundaries.
  - Organic farming areas used to mask England (Organic Farming Scheme).
- Data assembly:
  - Annual application amounts per crop by county/year; convert to rates (kg per km^2 per crop).
  - For each 1 km cell, combine crop-area data with crop-specific application rates to estimate total per-cell application.

## Methodology: Modelling and Computation
- Modelling approach:
  - For each active ingredient, model annual application rate (kg/km^2) as a function of crop type and county location using a lognormal distribution.
  - Spatial component modeled with a continuous Gaussian Markov Random Field via INLA to interpolate across counties; assumes a common spatial pattern across crops.
  - Years treated as independent replicates; temporal dynamics not explicitly modeled due to limited data.
- Prediction pipeline:
  - Use Land Cover Plus: Crops to provide per-1 km square crop composition.
  - Multiply estimated per-crop rates by cropped area in each cell to obtain total per-cell application.
  - For crops with multiple estimates within a cell, average estimates to avoid double counting.
- Uncertainty estimation:
  - Draw 100 samples from the posterior distributions of model parameters to create 100 predicted maps per ingredient.
  - 2.5% and 97.5% quantiles used to form 95% prediction intervals for each 1 km cell.
  - Uncertainty expressed as a percentage of the mean estimate to enable cross-ingredient comparison.
- Extent and inclusion:
  - 157 active ingredients progressed to modelling; 129 included in final product after extent and validation checks.
  - Some ingredients excluded if coverage < 95% of England and Wales or if Wales data were too uncertain.

## Validation and Quality Assurance
- Validation strategies:
  - Regional totals: compare estimated regional totals to PUS-derived regional totals (2012–2016 average) for England and Wales; acknowledges that some crops (soft fruits, vegetables, protected/ornamental crops) are underrepresented in the model.
  - RMSE comparisons against null models (no spatial variation) and crop-varying models to assess spatial structure capture.
- Key findings:
  - 12 of 157 models failed the null-model RMSE test and were removed.
  - 86 of the remaining 145 models passed the spatial-variation RMSE test; the rest indicate limited or no detectable spatial variation.
  - Validation results vary by region and ingredient; some ingredients show close agreement with PUS totals (e.g., Glyphosate in the South East), others show larger discrepancies.
- Documentation of limitations:
  - No national independent validation dataset; regional totals used as a proxy check.
  - Maps exclude certain crops, regions, or years due to data limitations; extrapolations for Wales exist for some ingredients with higher uncertainty.

## Data Access, Usage, and Citation
- Access: Environmental Information Data Centre (EIDC).
- Citation: Jarvis, S.G.; Henrys, P.A.; Redhead, J.W.; Da Silva Osório, B.M.; Pywell, R.F. (2019). CEH Land Cover plus: Pesticides 2012-2016 (England and Wales). NERC Environmental Information Data Centre. DOI provided in the documentation.
- Licensing: Some licence fees may apply; check with data access provider.
- Documentation availability: Supporting information and appendices available online for deeper methodological and validation details.

## Outputs, Interpretation, and Examples
- Outputs include per-ingredient 1 km raster maps with both estimated application and associated uncertainty.
- Example (tebuconazole):
  - Estimated application 0–>10 kg/yr per km^2, with higher values in eastern England.
  - Uncertainty maps show variability, with higher uncertainty where data are sparse or where crop coverage varies.
- Practical interpretation notes:
  - Uncertainty reflects both variation in application rates and the proportion of cropped land treated.
  - Confidence intervals illustrate where predictions are most reliable; areas with data gaps or extrapolations have higher relative uncertainty.

## Limitations, caveats, and Future Improvements
- Temporal dynamics:
  - Averaged across 2012–2016; explicit year-to-year variation not modeled.
- Wales data:
  - Some active ingredients rely on Welsh data; for a subset, Wales predictions are extrapolated with high uncertainty.
- Extent-based exclusions:
  - Ingredients with less than 95% geographic extent are excluded; may omit relevant pesticides with localized use.
- Data scope:
  - Estimates pertain to crops in LC Plus Crops (arable and fodder/forage crops); soft fruits, vegetables, orchards, and protected crops may be underrepresented.
- Future enhancements:
  - Incorporate additional years to reduce temporal uncertainty.
  - Improve Welsh data coverage and mask out organic areas comprehensively in both England and Wales.
  - Explore crop-specific spatial patterns to better capture differences across crops.
  - Expand validation with independent national data as it becomes available.

## Practical Takeaways for Data Leaders
- Robust, high-resolution pesticide application data product for policy and research, with explicit uncertainty quantification and clear methodological documentation.
- Valuable for exposure modelling, environmental risk assessments, and targeted management, while acknowledging regional limitations and data gaps.
- Useful case study in integrating multiple data sources (survey data, land cover, crop maps) into a coherent, spatially explicit environmental dataset with transparent validation and uncertainty reporting.
- Highlights the importance of data extent criteria, transparent handling of absent data, and clear licensing/citation requirements for data reuse.