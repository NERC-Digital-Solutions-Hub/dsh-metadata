# Dataset Documentation

- Overview of CEH Land Cover® Plus: Pesticides v2.0
  - Updates pesticide application mapping across England, Wales, and Scotland at 1 km resolution for 162 active ingredients.
  - Builds on CEH Land Cover® Plus: Pesticides by expanding to Scotland and extending temporal coverage (2012–2017).

## Key updates from v1.0
- Scotland coverage extended using Scottish Pesticide Survey data from SASA.
- Modelling revision: remove global intercept, harmonise spatial extent across GB; potential high uncertainty in areas with limited ingredient use.
- Temporal extension to 2012–2017, including 2017 fodder and forage data for Scotland.
- Addition of 36 active ingredients not previously mapped.

## Product scope and outputs
- Output format and resolution
  - 1 km resolution; units: kilograms of active ingredient per year (kg/yr).
  - For each 1 km square: pesticide application rates per crop × crop area in the square.
- Coverage and ingredients
  - 162 active ingredients (herbicides, insecticides, molluscicides, fungicides).
- Uncertainty
  - Uncertainty maps produced alongside each ingredient map; expresses uncertainty relative to total estimated application.
- Temporal framing
  - Snapshot of average applications for 2012–2017, using average crop coverage from 2015–2017 (LC Plus Crops 2015–2017).
  - Temporal variation not explicitly modelled; uncertainty captures some year-to-year variability.
- Data formats
  - Output files (TIF or shapefile) with two layers: (1) application (kg/yr) and (2) uncertainty (%).
  - Spatial reference: British National Grid; 1 km resolution.
- Map coverage caveats
  - Areas with no data where crops do not exist; mountains/urban areas may be missing for certain ingredients.
  - England masking for organic areas via Organic Farming Scheme; Wales/Scotland not masked in this version.

## Data sources and inputs
- Pesticide Utilisation Survey (PUS) data
  - England & Wales: 2012, 2013 (fodder/forage only), 2014, 2016, and 2017 (fodder/forage in Scotland).
  - Scotland: 2012, 2014, 2016 (arable); 2013, 2017 (fodder/forage).
- Crop area and land cover
  - CEH Land Cover Plus: Crops (LC Plus: Crops) data for crops in GB.
- Boundaries and locations
  - English/Welsh boundaries; Scottish Local Authority boundaries provided by SASA.
  - County centroids calculated for spatial modelling.
- Data processing constraints
  - Excluded active ingredients with fewer than 10 observations; 171 progressed to modelling, 162 included in final product.

## Methodology
- Data collation
  - Cleaning to remove unspecified actives and non-pesticide uses.
  - Annual application totals calculated by crop and county/LA; area-based rates computed (kg/yr per crop per county/LA).
- Modelling approach
  - Annual rates modelled as lognormal function of crop type and county location.
  - Spatial variation modeled with a Gaussian Markov Random Field via INLA (Integrated Nested Laplace Approximations).
  - Spatial pattern assumed consistent across crops; cross-crop spatial heterogeneity not separately estimated due to data limits.
  - Years treated as independent replicates; temporal trends not estimated due to limited data points.
- Predictions
  - Combine crop-area data from LC Plus Crops with spatially smoothed crop-specific rates to estimate 1 km x 1 km total applications per ingredient.
  - For crops with multiple LC Plus Crops class estimates, average the rate to avoid double counting.
  - Organic areas masked in England; not masked in Wales/Scotland in this version.
- Uncertainty estimation
  - 100 draws from parameter distributions to generate a distribution of estimates per 1 km cell.
  - 95% CI computed from 2.5% and 97.5% quantiles; uncertainty expressed as percentage of the mean estimate.
  - Uncertainty reflects both rate variation and crop-treated proportions within cells.

## Validation and limitations
- Validation approaches
  - Regional totals compared against PUS statistics; posterior predictive checks (RMSE compared to null models).
  - 11 active ingredients subjected to regional comparisons across English regions, Wales, and Scotland; results summarized in Appendix 1.
  - 162 models evaluated; 9 failed the RMSE test against the spatially varying model and were excluded from the product.
- Limitations
  - No national independent validation data; comparisons rely on regional totals from PUS.
  - Some ingredients show larger discrepancies due to data sparsity (e.g., Scotland data gaps for certain actives).
  - Temporal variability is not explicitly modelled; uncertainty partly captures year-to-year variation.
  - Seed potatoes and “other” LC Plus Crops classifications can influence patterns in v2.0, especially in Scotland.

## Differences with v1.0
- Scotland coverage added; Scotland data integrated into GB product.
- Spatial extent harmonised; same GB extent for all ingredients.
- Temporal coverage extended to 2012–2017; 2017 fodder/forage data included for Scotland.
- 36 new active ingredients added.
- Minor shifts in patterns for potatoes/seed potatoes due to differences in crop categorisation (e.g., “other” category in LC Plus Crops).

## Access, citation, and licensing
- Citation: Jarvis, S.G.; Redhead, J.W.; Henrys, P.A.; Risser, H.A.; Da Silva Osório, B.M.; Pywell, R.F. (2020). CEH Land Cover plus: Pesticides 2012-2017 (England, Scotland and Wales). NERC Environmental Information Data Centre. https://doi.org/10.5285/99a2d3a8-1c7d-421e-ac9f-87a2c37bda62.
- Data access: Environmental Information Data Centre (eidc.ceh.ac.uk); licence fees may apply for some users and applications.
- Notes: Outputs are designed for GIS use in map-based analyses of pesticide applications and associated uncertainties.

## Practical notes for GIS specialists
- Use the application layer to map estimated kg/yr of active ingredients per 1 km cell; use the accompanying uncertainty layer to assess confidence in estimates.
- Integrate LC Plus: Crops data to contextualize where crops drive predicted applications within each cell.
- Be mindful of missing data areas (mountainous/urban) and organic-masked areas in England when interpreting results.
- Compare regional totals with PUS-derived statistics for sanity checks; acknowledge limitations due to data sparsity in some regions or crop groups.
- For cross-version analyses, account for differences in crop categorisation (e.g., seed potatoes) that may affect apparent spatial patterns.