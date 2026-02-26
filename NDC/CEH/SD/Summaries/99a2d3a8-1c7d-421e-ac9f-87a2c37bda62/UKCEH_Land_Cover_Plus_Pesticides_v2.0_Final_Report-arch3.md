# CEH Land Cover plus: Pesticides 2012-2017 (England, Scotland and Wales)

- Purpose and scope
  - Updated methodology and metadata for CEH Land Cover® Plus: Pesticides v2.0, covering England, Scotland and Wales at 1 km resolution.
  - Maps pesticide applications across 162 active ingredients, using average applications from 2012-2017.

- Key updates in v2.0
  - Extended coverage to Scotland (Scottish Pesticide Survey data contributed by SASA).
  - Revised modelling to remove a global intercept and align spatial extent across GB.
  - Temporal extension to 2012-2017 (including 2017 fodder and forage data for Scotland).
  - Added 36 active ingredients not in v1.0.

- Data sources and inputs
  - Pesticide Utilisation Survey (PUS) data for England, Wales, and Scotland (2012, 2013 fodder, 2014, 2016, 2017 fodder for Scotland).
  - Crops data from CEH Land Cover Plus: Crops to determine crop areas in each 1 km cell.
  - County/local authority boundaries and centroids for location mapping.
  - Organic farming scheme data to mask organic areas in England.

- Modelling approach
  - Annual application rates (kg per km² per crop) modelled as a function of crop type and county location using a lognormal distribution.
  - Spatial variation captured with a continuous Gaussian Markov Random Field via INLA (spatial smoothing across GB).
  - Years treated as independent replicates due to limited data; no explicit temporal trend modelling.
  - Predictions for 1 km squares combine spatially interpolated rates with crop area from LC Plus Crops to estimate total annual applications (kg/yr) per active ingredient.
  - Handling of crops with multiple LC Plus Crops estimates by averaging to avoid double counting.

- Uncertainty estimation
  - 100 draws from parameter distributions to create a distribution of estimates per 1 km square.
  - 95% uncertainty interval derived from 2.5% and 97.5% quantiles; uncertainty expressed as a percentage of the mean estimate.
  - Uncertainty reflects both variation in application rates and the proportion of land cropped.

- Outputs and metadata
  - Outputs at 1 km resolution with two layers per file:
    - Layer 1: estimated application (kg/yr) of each active ingredient.
    - Layer 2: uncertainty (percentage) associated with the estimated application.
  - Gaps may occur where crops are not present (no data for mountains or urban areas; some ingredients restricted to certain crops).

- Validation and quality assurance
  - Validation via regional total comparisons to PUS statistics and posterior predictive checks (RMSE).
  - 162 active ingredients included in final product; 9 models failed the RMSE comparison against null models and were removed.
  - Regional comparisons show varying agreement (better for some ingredients; poorer for others, e.g., certain Scottish data limitations).
  - A subset of 11 ingredients used for regional validation; results indicate general plausibility with expected discrepancies due to data scope (all crops vs. arable/fodder crops only).

- Differences from v1.0
  - Scotland is now included; added 36 ingredients.
  - Changes to modelling (removal of global intercept, consistent GB spatial extent) affect where higher estimates appear (notably seed potatoes in Scotland).
  - Some differences due to mapping seed potatoes to an “other” category in LC Plus Crops, influencing total estimates.

- Coverage and limitations
  - GB-wide product snapshot for average applications 2012-2017; temporal variation not modelled explicitly.
  - Highest reliability for ingredients with consistent year-to-year application; uncertainty higher where annual rates vary.
  - No independent national-scale validation data; regional totals compared to PUS statistics as a proxy.
  - Some data gaps for crops or regions reduce accuracy for certain ingredients (e.g., fruits/vegetables, protected crops).

- Usage, governance, and data access
  - Data can be cited as CEH Land Cover plus: Pesticides 2012-2017 (England, Scotland and Wales); available via the Environmental Information Data Centre (with potential licence fees).
  - Outputs support exposure assessment, risk mapping, and policy/science communication; include explicit uncertainty to inform decision-making.
  - Metadata includes file formats (TIF or shapefiles), two layers, and British National Grid reference system.

- Example outputs
  - Illustration using diflufenican shows 0–4 kg/yr per km² with higher central/eastern England and Scotland, lower in western areas; unexplained areas shown as white; uncertainty maps range broadly (from under 100% to nearly 500%).

- Citation and further information
  - Jarvis, S.G.; Redhead, J.W.; Henrys, P.A.; Risser, H.A.; Da Silva Osório, B.M.; Pywell, R.F. (2020). CEH Land Cover plus: Pesticides 2012-2017 (England, Scotland and Wales). NERC Environmental Information Data Centre. https://doi.org/10.5285/99a2d3a8-1c7d-421e-ac9f-87a2c37bda62. Data access via http://eidc.ceh.ac.uk/. License details may apply.