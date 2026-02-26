Supporting information for CEH Land Cover plus: Pesticides 2012-2016 (England and Wales)

- Overview
  - A new product mapping pesticide applications across England and Wales at 1km resolution, released in 2019.
  - Combines CEH Land Cover Plus: Crops with Pesticide Utilisation Survey (PUS) data to map average annual pesticide applications for 129 active ingredients.
  - Snapshot covers 2012–2016 (average), enabling spatial analysis of cropping practices and associated pesticide use.
  - Intended for monitoring environmental health and informing policy, with outputs suitable for exposure, runoff, and wildlife impact studies when combined with other data.

- Data sources and access
  - PUS data: 2012, 2013 (fodder/forage only), 2014, 2016. Includes annual applications by crop and county.
  - Crop area data: CEH Land Cover Plus: Crops (LC plus Crops) for 2015–2017 (used to derive crop areas in each 1km cell).
  - Spatial framework: county centroids derived from ceremonial county boundaries.
  - Organic areas masked in England (Organic Farming Scheme); not masked in Wales in this version.
  - Data access: Environmental Information Data Centre (EIDC); citation required if used; licence fees may apply for some uses.

- Product specifications
  - Spatial resolution and units: 1km x 1km rasters in British National Grid; units are kg active ingredient per year (kg/km2/yr).
  - Contents: 129 active ingredients, each with two-band TIFF
    - Band 1: Application — estimated annual kg of active ingredient in the 1km square.
    - Band 2: Uncertainty — percentage uncertainty for the estimated application.
  - Coverage notes: some 1km cells have no data where crops do not occur or where the active ingredient is not used; some ingredients excluded if <95% extent of England and Wales.
  - Example outputs: illustrate spatial patterns (e.g., tebuconazole higher in eastern England; white areas for mountains/urban where estimation is not possible).

- Methodology (how outputs are produced)
  - Data collation: clean PUS data (remove non-pesticide actives, undefineds, etc.); aggregate to annual kg per crop per county.
  - Cropping data integration: combine crop-area information with pesticide rates.
  - Modelling approach:
    - Annual application rates (kg/km2 of crop) modelled as a lognormal function of crop type and county location.
    - Spatial dependence captured with a continuous spatial field (Gaussian Markov Random Field) estimated via INLA; interpolates between county centroids.
    - Assumes a common spatial pattern across crops; full crop-specific spatial patterns not modelled due to data limits.
    - Years treated as independent replicates (3 arable years, 1 fodder year); temporal trends not explicitly modelled.
  - Prediction and calculation:
    - Predict per-crop application rates across the 1km grid using cropped area from LC plus Crops.
    - Total 1km cell application = sum over crops (rate per crop × crop area in cell).
    - For crops with multiple rate estimates (e.g., field beans), average estimates to avoid double counting.
  - Uncertainty estimation:
    - 100 draws from the posterior parameter distributions (intercept, crop effect, spatial term) to produce 100 alternative estimates per cell.
    - 95% CI per cell from 2.5th to 97.5th percentile; uncertainty mapped as a percentage relative to the mean estimate.
    - Uncertainty reflects both rate variation and land area treated, plus cropping variability.

- Validation and quality
  - Validation approaches:
    - Regional totals comparison with PUS website figures (averaged 2012–2016; accounts for arable crops only, not all crops).
    - posterior predictive checks; RMSE compared against null models (no spatial variation; or crop-specific, space-varying models).
  - Outcomes:
    - 12 of 157 models failed the null-model RMSE test and were excluded.
    - 86 of remaining 145 models passed the spatial-variation RMSE test.
    - 16 active ingredients removed due to insufficient extent (<95% area covered).
  - Data limitations:
    - No national independent validation dataset; comparisons rely on regional totals and PUS statistics.
    - Wales data are less robust due to sparse Welsh observations; some ingredients extrapolated with high uncertainty.
    - Some ingredients excluded or with high uncertainty; results note higher uncertainty for ingredients with spatial or temporal variability.
  - Acknowledgement of Welsh data caveat: “Models are built without Welsh data; high uncertainty in predictions for Wales” (noted in product description).

- Data products and usage considerations
  - Data availability: 129 raster files (TIFF), two bands each; stored and accessible via EIDC.
  - Use cases: spatially explicit estimates of pesticide applications to support exposure modelling, runoff modelling, wildlife impact analyses, and policy assessment.
  - Key caveats for analysts:
    - Averages 2012–2016; not explicit temporal trends; variability across years reflected in uncertainty maps.
    - Not all crops or all crop types are represented equally; some ingredients may be underrepresented in certain regions.
    - England masks for organic areas reduce exposure estimates in those zones; Wales masking is not fully implemented in this version.
    - Uncertainty maps vary by ingredient and cell; interpretation should weight uncertainty, especially in areas with limited crop data or sparse observations.
  - Data integration potential: designed to be used with complementary data (e.g., crop types, land cover, water quality) to enhance environmental monitoring and policy evaluation; underlying data sources are accessible for transparency and reuse.

- Citation and references
  - Jarvis, S.G.; Henrys, P.A.; Redhead, J.W.; Da Silva Osório, B.M.; Pywell, R.F. (2019). CEH Land Cover plus: Pesticides 2012-2016 (England and Wales). NERC Environmental Information Data Centre. doi: 10.5285/a72f8ce8-561f-4f3a-8866-5da620c0c9fe
  - Supporting information and detailed methodology available via the same DOI; related publications on data sources and modelling approaches are cited in the document.