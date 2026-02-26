# Dataset Documentation

- The CEH Land Cover Plus: Pesticides v2.0 provides 1 km resolution maps of average pesticide applications (kg active ingredient per year) across England, Wales and Scotland for 162 active ingredients, covering 2012–2017 (yearly data collapsed to a 2012–2017 average).
- Scotland extension: v2.0 includes Scotland using Scottish Pesticide Survey data, enabling GB-wide coverage.
- Modelling improvements: removed a global intercept, refined GB extent, and updated spatial extent; active ingredients mapped over the same spatial domain with higher uncertainty in areas where ingredients are regionally limited.
- Added data: 36 active ingredients not present in v1.0; temporal coverage extended with 2017 fodder and forage data for Scotland (extending to 2012–2017).

- Background and uses: Builds on CEH Land Cover Plus Crops (which uses Sentinel-1/2 data to identify crop types) to enable high-resolution mapping of agricultural practices, in particular pesticide applications when combined with crop data and national survey data.
- Data sources: 
  - Pesticide Utilisation Surveys (PUS) for GB (England, Wales, Scotland) providing annual kg of active ingredient per crop per county/LA; data summarized to crops and areas (ha) and application rates (kg/ha).
  - CEH Land Cover Plus: Crops provides crop-type maps and crop areas at 1 km resolution.
  - Regions and boundaries: English ceremonial counties, Welsh preserved counties, Scottish local authorities; centroids used to geolocate records.
- Output scope: 1 km resolution maps for 162 active ingredients across GB, plus accompanying uncertainty maps.

- Product specification:
  - Output units: kg of active ingredient applied per year per 1 km square; uncertainty maps show relative confidence.
  - Two data layers per file: (1) application – estimated annual kg/yr per active ingredient; (2) uncertainty – percentage uncertainty relative to the mean.
  - Temporal snapshot: 2012–2017 average (reflecting crop coverage from 2015–2017).

- Methodology:
  - Data collation: as combine PUS (2012, 2013 fodder, 2014, 2016, 2017 fodder for Scotland) with crop area data; remove unspecified actives and non-pesticide uses; crop area and county/LA boundaries attached to records.
  - Annual application rates: computed as total active ingredient applied per crop per county/LA divided by crop area; fewer than 10 observations for an ingredient removed from modelling.
  - Spatial assignment: county/LA boundaries mapped to 1 km cells using centroids; crops in each 1 km cell from LC Plus Crops.
  - Modelling: lognormal model of rate (kg/km2 per crop) as a function of crop and location; spatial field modeled with Gaussian Markov Random Field via INLA to interpolate across GB; same spatial pattern assumed across crops.
  - Year treatment: different years treated as independent replicates; limited data means no explicit temporal trend modelling.
  - Predictions: for each 1 km cell, estimate rates per crop, then multiply by average crop area in the cell (2015–2017) to obtain total application; average rates across crops to avoid double counting where crops map to multiple LC Plus Crops classes.
  - Organic masking: England’s Organic Farming Scheme areas masked (not currently done for Wales/Scotland in v2.0).

- Uncertainty:
  - 100 draws from parameter distributions (intercept, crop, spatial term) used to generate 1 km cell estimates; 95% CI derived from 2.5% and 97.5% quantiles.
  - Uncertainty reflects both variation in application rates and variation in the cropped land proportion treated; maps produced for each active ingredient.

- Validation and limitations:
  - Validation approaches: regional totals compared to PUS statistics; posterior predictive checks for RMSE against null models.
  - Compared results for a subset of 11 ingredients; differences vary by region and ingredient; overall RMSE-based validation shows most models outperform simple nulls, with 9 of 171 models failing the strict RMSE test and 93 of 162 passing the crop-space spatial variation test.
  - Acknowledges lack of independent national-scale validation data; PUS data themselves are estimates with uncertainty.
  - Limitations:
    - No explicit temporal modelling; results are an average across 2012–2017 with temporal variability captured only in model uncertainty.
    - England masking for organics; Wales/Scotland not masked in this version.
    - Some regional differences in Scotland/England/Wales due to data density and crop distribution.
    - Some ingredients particularly associated with specific crops (e.g., seed potatoes) may have differences in v2.0 because of data mapping to “other” crops in LC Plus Crops.

- Differences between v1.0 and v2.0:
  - GB coverage extended to Scotland; inclusion of 36 new actives.
  - Minor changes in estimation patterns, especially for potatoes/seed potatoes; Scotland-specific application patterns can differ due to data sources and mapping decisions.

- Outputs and data access:
  - Example: outputs illustrate diflufenican with predicted ranges and uncertainty; higher applications in central/eastern GB; white areas indicate unavailable estimates (mountainous/urban).
  - Data format: TIF or shapefile; each file contains two layers (application and uncertainty), both at 1 km resolution with British National Grid CRS.
  - Processing note: areas with no crops yield no data; absence of data in mountains/urban areas and ingredients limited to crops not grown in a cell.
  - Citation and access: Jarvis, S.G.; Redhead, J.W.; Henrys, P.A.; Risser, H.A.; Da Silva Osório, B.M.; Pywell, R.F. (2020). CEH Land Cover plus: Pesticides 2012-2017 (England, Scotland and Wales). NERC Environmental Information Data Centre. https://doi.org/10.5285/99a2d3a8-1c7d-421e-ac9f-87a2c37bda62. Data accessible via the Environmental Information Data Centre (eidc.ceh.ac.uk); licence fees may apply for some users.

- Appendices and supplementary aspects:
  - Appendix 1: regional comparisons for 11 active ingredients; highlights where model estimates align or diverge from PUS data.
  - Appendix 2: table of null-model tests for model validation (test 1 across space and crops; test 2 across space with crop variation); 162 active ingredients included in final product; some ingredients fail test 2 but remain in product with caution advised.
  - Acknowledgements: collaboration with Fera, SASA, CEH contributors.

- Practical takeaway for analysts:
  - Provides GB-wide, 1 km pesticide application maps for 162 ingredients (2012–2017 average) integrated with crop data; includes spatially explicit uncertainty maps to inform risk assessment and policy analyses.
  - Suitable for exploring exposure risk, environmental modelling, or targeting interventions, with explicit notes on uncertainty, data limitations, and validation context.