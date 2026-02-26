# Dataset Documentation

- Overview
  - CEH Land Cover® Plus: Pesticides v2.0 maps pesticide applications across England, Wales and Scotland at 1km resolution.
  - Extends coverage to Scotland and includes 36 new active ingredients.
  - Uses Pesticide Utilisation Survey (PUS) data and CEH Land Cover Plus: Crops as inputs; provides uncertainty maps for each active ingredient.

- Key updates from v1.0
  - Scotland now included, enabled by SASA data.
  - Modelling revised: removal of a global intercept; uniform spatial extent across GB; uncertainty may be high in areas with limited data.
  - Temporal coverage extended to 2012–2017 with 2017 fodder and forage data for Scotland.
  - 36 active ingredients added to the mapping.

- Product specification
  - Output: 1km resolution; units are kg of active ingredient applied per year.
  - Coverage: 162 active ingredients (herbicides, insecticides, molluscicides, fungicides, etc.).
  - Uncertainty: accompanying uncertainty maps per ingredient; uncertainty expressed as a percentage relative to the mean.
  - Temporal snapshot: average applications across 2012–2017, based on LC Plus Crops for 2015–2017 crop coverage.
  - Notes: some areas (mountainous/urban) and crops not grown may have no data; organic areas in England masked; not masked in Wales/Scotland in this version.

- Methodology in brief
  - Data sources:
    - PUS data for England/Wales (2012, 2013 fodder, 2014, 2016; 2017 fodder in Scotland)
    - Crop area data from CEH Land Cover Plus: Crops
  - Spatial assignment:
    - Records linked to county/LA centroids; boundaries defined by Lieutenancies Act 1997 (England/Wales) and Scottish Local Authorities (Scotland).
  - Modelling:
    - Annual application rates (kg per km² per crop) modelled as lognormal functions of crop type and county location.
    - Spatial variation captured with a Gaussian Markov Random Field (INLA); assumed common spatial pattern across crops.
    - Years treated as independent replicates due to limited data for temporal trends.
  - Predictions:
    - Apply 1km crop-area data (2015–2017 average) to predicted rates to estimate total annual applications per 1km cell.
    - For crops with multiple LC Plus Crops estimates, average the rates to avoid double counting.
  - Uncertainty:
    - 100 draws from parameter distributions generate a distribution of estimates per 1km cell.
    - 2.5% and 97.5% quantiles yield a 95% interval; uncertainty scaled to mean to produce a relative percentage.
  - Additional filters:
    - Organic areas masked in England; not yet in Wales/Scotland.

- Validation and quality
  - No independent national-scale validation data available; regional totals compared to PUS statistics as a consistency check.
  - Posterior predictive checks and RMSE used to assess model performance; 9 of 171 models removed after tests; 162 models retained (including 36 new ingredients).
  - Validation highlights:
    - Regional comparisons show varying agreement by ingredient/region; some under- or over-estimates reflect data limitations (e.g., crops not modeled or ingredients mainly used on non-arable crops).
  - Limitations:
    - PUS data are themselves estimates; no national independent validation data currently available.
    - Some ingredients exhibit weak spatial variation or limited Scotland data, increasing uncertainty.

- Differences between v1.0 and v2.0
  - Broadly similar patterns; notable changes for potatoes-related applications (seed potatoes) and Scotland-specific mappings.
  - Scotland-specific mapping of seed potatoes influences total estimates due to reclassification in Land Cover Plus Crops.

- Usage and access
  - Citation: Jarvis, S.G.; Redhead, J.W.; Henrys, P.A.; Risser, H.A.; Da Silva Osório, B.M.; Pywell, R.F. (2020). CEH Land Cover plus: Pesticides 2012-2017 (England, Scotland and Wales). NERC Environmental Information Data Centre. doi:10.5285/99a2d3a8-1c7d-421e-ac9f-87a2c37bda62.
  - Data access: Environmental Information Data Centre (eidc.ceh.ac.uk); licence fees may apply for some users.

- Outputs and interpretation
  - Example outputs provided (e.g., diflufenican) show spatial variation in estimated applications (kg/yr per km²) and corresponding uncertainty.
  - Uncertainty maps illustrate higher relative uncertainty where data are sparse or where cropland treatment varies considerably year-to-year.
  - Areas without data correspond to non-cropped or data-deficient regions (mountains, urban areas).

- Acknowledgements
  - Acknowledges data access and contributions from Fera, SASA, CEH, and related partners.