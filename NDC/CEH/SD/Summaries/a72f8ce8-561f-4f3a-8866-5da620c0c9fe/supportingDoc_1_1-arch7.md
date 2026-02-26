# Supporting information for CEH Land Cover plus: Pesticides 2012-2016 (England and Wales)

- Purpose and scope
  - New product mapping pesticide applications across England and Wales at 1 km resolution.
  - Combines CEH Land Cover® Plus: Crops with PUS data to map average annual pesticide applications for 129 active ingredients.
  - Aims to support exposure risk assessment, runoff modelling, targeting interventions, and wildlife impact studies.
  - Snapshot covers 2012–2016 averages; temporal variation across years is reflected in uncertainty, not explicit seasonality.

- Data sources and inputs
  - Pesticide Utilisation Survey (PUS) data for 2012, 2013 (fodder/forage only), 2014, 2016.
  - Crop area data from CEH Land Cover® Plus: Crops (average across 2015–2017 years).
  - County location data from ceremonial county centroids (MHCLG).
  - Organic areas in England masked using Organic Farming Scheme data; Wales masking not applied in this version.
  - Geospatial framework uses British National Grid (1 km grid).

- Data product and format
  - 129 two-band raster TIFF files (one per active ingredient), 1 km × 1 km resolution.
  - Bands:
    - Band 1: Application — estimated yearly application in kg/year per 1 km² for the ingredient.
    - Band 2: Uncertainty — percentage uncertainty for the estimated application.
  - Areas with no data occur where crops are not grown or outside the ingredient’s extent (mountain/urban areas, or limited crop ranges).
  - Some ingredients are excluded if coverage across England and Wales is less than 95%.

- Modelling approach (how estimates are generated)
  - Annual application rates (kg/km² of crop grown) modelled as a lognormal function of crop type and county location.
  - Spatial effect modelled with a continuous Gaussian Markov Random Field using INLA to interpolate across counties.
  - Assumes a common spatial pattern across crops; data treated as independent replicates for different years.
  - Predictions per 1 km cell: multiply crop-specific rates by crop areas in that cell (from LC Plus Crops) and sum across crops.
  - Some ingredients excluded if Welsh data are required for robust estimates; extrapolations for Wales are high-uncertainty for these cases.

- Uncertainty assessment
  - 100 parameter draws per ingredient to generate a distribution of estimates per 1 km cell.
  - 95% interval derived from 2.5th and 97.5th percentiles; uncertainty is expressed as a relative percentage of the mean estimate.
  - Uncertainty captures both rate variation and the proportion of land treated; expected to be higher where temporal variation or crop-area variation is large.

- Validation and quality assurance
  - Regional totals compared with PUS regional totals (averaged 2012–2016) as a rough check.
  - Posterior predictive checks and RMSE comparisons against null and crop-varying models.
  - 12 active ingredients failed null-model RMSE test and were removed; 59 ingredients failed a spatial variation test but remain in product with caution.
  - 157 ingredients progressed to modelling; 16 removed due to insufficient extent; final product includes 129 ingredients.
  - Appendix data provide detailed regional comparisons for some ingredients (e.g., Glyphosate, Azoxystrobin, Tebuconazole).

- Outputs and example interpretation
  - Example: tebuconazole maps show 0–over 10 kg/yr per km², with higher applications in eastern England; white areas indicate no data (mountain/urban or crops absent).
  - Uncertainty maps accompany application maps; higher uncertainty where data are sparse or vary more between years.
  - Uncertainty tends to be lower for ingredients with more consistent annual usage and crop coverage.

- Access, licensing, and citation
  - Data available via Environmental Information Data Centre (EIDC).
  - Citation required: Jarvis et al. (2019), CEH Land Cover plus: Pesticides 2012-2016 (England and Wales).
  - Licensing fees may apply for some users/applications.

- Limitations and caveats for GIS users
  - Wales data for some ingredients are extrapolated or less certain; not all ingredients cover Wales robustly.
  - No independent national-scale validation dataset; regional totals serve as the validation basis.
  - Temporal trends are not explicitly modelled; the product reflects a 2012–2016 average with year-to-year variation captured in uncertainty.
  - Organic areas masked only in England; future versions aim to extend masking to Wales.
  - Some ingredients are excluded due to insufficient extent (<95% coverage).