# Supporting information for CEH Land Cover plus: Pesticides 2012-2016 (England and Wales)

- Purpose and scope
  - Presents methodology and metadata for CEH Land Cover® plus: Pesticides 2012-2016 (England and Wales), a high-resolution product mapping pesticide applications across England and Wales at 1 km resolution.
  - Combines CEH Land Cover® Plus: Crops with Pesticide Utilisation Survey (PUS) data to map average annual pesticide applications for 129 active ingredients (kg active ingredient per year).

- Data sources and inputs
  - PUS data for England and Wales from 2012, 2013 (fodder and forage only), 2014, and 2016; includes foliar/granular and seed treatments.
  - Crop and area data from CEH Land Cover® Plus: Crops (2015–2017 averages) to derive crop presence and area in each 1 km cell.
  - County/ceremonial county centroids for spatial modelling; organic farming areas masked in England using Organic Farming Scheme data (Natural England Open Data); Wales masking not implemented in this version.
  - Access and citation: data available via Environmental Information Data Centre; cite Jarvis et al. (2019).

- Product specifications
  - Output format: 1 km x 1 km rasters (TIFF), one file per active ingredient (129 ingredients in final product).
  - Bands per file:
    - Band 1: Estimated application in kg/yr (kg/yr) for the active ingredient.
    - Band 2: Uncertainty (percentage) associated with the estimated application.
  - Coverage notes: some 1 km cells have no data due to absence of treated crops; estimates outside the ingredient’s extent are not produced. Regions outside 95% coverage (notably Cornwall for some ingredients) are omitted for those ingredients.

- Modelling approach and methodology
  - Annual application rates (kg/km² of crop grown) modelled as a function of crop type and county location using a Lognormal model.
  - Spatial component: continuous spatial field (Gaussian Markov Random Field) estimated with INLA to interpolate between county centroids, smoothing across county boundaries.
  - Temporal treatment: model uses data treated as independent replicates across 2012, 2013, 2014, and 2016; explicit temporal trends are not estimated due to limited years of data.
  - Crop information: crop-specific rates are assumed to be consistent across England and Wales; some ingredients required Welsh data exclusion for model convergence.
  - Data inclusion: from initial 157 ingredients, those with <20 observations or failing to produce outputs were excluded; national-level modeling uses England and Wales data together, with Wales exclusion for some ingredients increasing uncertainty there.
  - Predictions: for each 1 km cell, predict ingredient-specific rates for all crops present (from LC Plus Crops), then multiply rates by crop area to obtain total application per cell; for ingredients mapped to multiple LC Plus Crops classes within a cell, rate estimates are averaged to avoid double counting.
  - Uncertainty propagation: draw 100 parameter-value realizations from the model’s posterior distributions to generate distributions of cell-level estimates; 2.5th and 97.5th percentiles used to form 95% interval and relative uncertainty (as a percentage of the mean).

- Uncertainty and interpretation
  - Uncertainty maps accompany each active ingredient map, reflecting parameter distribution and spatial variation.
  - Relative uncertainty is calculated as (97.5th quantile – 2.5th quantile) / mean × 100; ranges observed include substantial uncertainty, particularly where application rates vary over time or land area treated varies widely.
  - Uncertainty is expected to decrease in future versions as more data become available.

- Validation and quality assessment
  - No independent national validation dataset is available; validation relies on regional totals and posterior predictive checks.
  - Regional comparison: summed estimated regional totals compared with published PUS totals (averaged 2012–2016); generally reasonable magnitudes, with some regional discrepancies (notably Wales and some ingredients).
  - Model performance tests (RMSE): compared against a null model of no spatial variation and against a crop-based variation model; 12 of 157 models failed the null-model test and were excluded; 86 of remaining 145 models passed the spatial-variation test.
  - Coverage constraint: 16 ingredients removed due to not achieving at least 95% geographic extent across England and Wales; final product comprises 129 ingredients.
  - Appendix provides detailed regional comparisons and per-ingredient validation results.

- Outputs and example interpretation
  - Example: tebuconazole shows estimated 2012–2016 applications ranging from 0 to >10 kg/yr per km², higher in eastern England and lower in western areas; uncertainty is often lower where higher applications are measured.
  - Uncertainty patterns reflect temporal variation and the proportion of cropped land treated; high uncertainty tends to accompany ingredients with variable application rates or limited crop coverage.

- Accessibility, licensing, and usage notes
  - Data and supporting information available via the Environmental Information Data Centre; license fees may apply for some users and applications.
  - Documentation includes extensive methodological detail, validation results, and appendices summarizing regional comparisons and null-model tests.
  - The product supports policy evaluation, environmental health monitoring, exposure modelling, and scenario analysis by providing high-resolution spatial patterns of pesticide applications and associated uncertainties.

- Key caveats and limitations
  - Wales: models built without Welsh data for certain ingredients, leading to higher uncertainty in predictions for Wales.
  - Areas without crops treated or outside ingredient extents show no data; some regions (e.g., mountains, urban areas) are white in outputs.
  - Organic areas in England are masked; not masked in Wales in this version.
  - Temporal trends are not explicitly modelled due to limited year coverage; uncertainty captures year-to-year variation rather than a temporal trajectory.
  - Independent national validation data are unavailable; regional checks are used to assess plausibility.