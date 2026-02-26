# European-wide maps of modelled farmlevel ecosystem services, 2019.

- Purpose: Describe methods, data structure, quality controls, assumptions, and limitations for Europe-wide per-farm ecosystem service (ES) maps (carbon storage, food production, nutrient export) generated from case studies using a novel upscaling meta-model approach.
- Project context: Outputs originate from the BESTMAP project; final Europe-wide data are simulated and not fully validated; simple quality checks were performed; methodology under peer review.

## Data structure and formats

- Data format: 3 GeoPackage files, each corresponding to an ES.
  - EU_2019_upscaling_carbon.gpkg – ES: Carbon storage; unit: tonnes C per ha.
  - EU_2019_upscaling_food.gpkg – ES: Standard economic output; unit: Euros per year.
  - EU_2019_upscaling_nutrient_export.gpkg – ES: Nutrient exported (nitrogen); unit: kg N per year.
- Output structure: Each ES file contains per-farm–level results aggregated to NUTS3 regions; final per-farm European values with region identifiers.
- Output fields: fid (row ID), NUTS_ID (NUTS3 region name), average_per_farm_ES (region-wide average per farm); some regions may be NULL if criteria are not met.
- Units summary:
  - Carbon: tonnes C per ha per average farm
  - Food: Euros per year per average farm
  - Nitrogen export: kg N per year per average farm

## Case study ecosystem service models (CS)

- ES models (briefly):
  - Carbon sequestration: Baseline soil organic carbon (SOC) modeled from abiotic factors; adjustments for land use and AES applied.
  - Food production: WOFOST crop-model outputs for six crops (with Spain case variations); yields converted to standard economic output.
  - Nutrient export: InVEST Nutrient Delivery Ratio (NDR) model; outputs converted to farm-level nutrient export (only nitrogen used).
- Case study regions (CS) across Europe: Mulde (Germany), South Moravia (Czechia), Catalonia (Spain), Bačka (Serbia), Humber (UK).
- Data scope: CS farm-level values plus farm attributes, AES, and economic data; used to build meta-models for upscaling.
- CS outputs feed the Europe-wide upscaling but are not themselves the Europe-wide data.

## Generation method: transferable meta-models

- Overall approach: Two-stage process creating meta-models (statistical emulators) from CS data, then assessing transferability across regions.
- Meta-model concept: Fragmented meta-models (multiple sub-models for higher spatial detail and transferability) using linear regression on log ES values.
- Regionalization: NUTS3 regions used as analysis units; 19 NUTS3 regions retained after filtering for data sufficiency.
- Starting predictors: Europe-wide environmental variables plus farm economic data (farm area, farm specialization, AES presence, economic size).
- Data preparation: Environmental data summarized to Farm Spatial Mapping Units (FSUs) via FADN-based zoning; zonal statistics provide means, SDs, and relative proportions.
- Variable selection and predictors:
  - Initial predictor list per ES (environmental + economic variables).
  - Multicollinearity reduced via variance inflation factor (VIF < 5); remove variables with high correlation and low ES relevance.
  - Categorical predictors (Farm specialization, AES) treated appropriately in selection.
- Model fitting and selection:
  - Response: ES (logged) to improve fit.
  - Linear regression with stepwise AIC (forward/backward) to obtain parsimonious models.
  - 75% training / 25% testing with cross-validation; model accuracy assessed by R².
- Cross-region application:
  - Meta-models applied to all 18 other analysis regions to obtain pred-R² for inter-region transferability assessment.
  - Representativeness and transferability are central to upscaling decisions.

## Representativeness and transferability

- Representativeness metric: Minkowski distance in multivariate space among NUTS3 regions using selected predictors (environmental and CS-relevant variables); economic data excluded from distance due to incomplete Europe-wide coverage.
- Transferability diagrams: Plot pred-R² (transfer accuracy) versus Minkowski distance; fit linear trend lines and compute RMSE.
- Transferability criteria (a priori):
  - Predictive strength: pred-R² threshold of 0.5 to indicate adequate transferability.
  - Linearity criterion: negative, statistically significant trend in the transferability diagram.
- Transferability mapping:
  - Regions with Minkowski distance below the threshold are considered transferable with higher confidence.
  - Binary assessment (transferable vs not) across diagrams; sum across CS regions yields overall transferability potential per region.
- Output derivation:
  - For regions meeting transfer criteria, meta-model coefficients are used to predict the ES for that NUTS3 region.
  - Values capped at 2x max observed CS value; minimum capped to min observed CS value.
  - Final per-farm Europe-wide ES values weighted by pred-R² (model reliability) to obtain a composite regional estimate.
- Economic data limitation:
  - Europe-wide economic data were often unavailable; Serbia and Balkans were excluded from final ES outputs when meta-models required economic inputs, though environmental data-based transferability could still be assessed.

## Outputs, quality controls, and limitations

- Quality control measures:
  - CS ES validations against local data (case studies).
  - Meta-models cross-validated (75/25 split) with further testing on full CS data.
  - Iterative VIF reduction to mitigate multicollinearity.
  - Transferability criteria to ensure reasonable cross-region applicability.
  - Cap and floor rules to prevent extreme values; acknowledges limited external validation data.
- Practical limitations:
  - Final Europe-wide validation data are not available; results are scenario-based simulations.
  - Differences in CS data (e.g., Catalonia with large farm counts and crop types not supported by WOFOST) affect upscaling consistency.
  - Economic data gaps led to regional exclusions or proxy-based substitutions (FADN-based synthesis, UK proxies).
  - Outputs reflect average per-farm values, not total ES sums for regions.
  - Serbia and Balkans frequently excluded from final outputs due to missing economic inputs, though transferability analysis could still incorporate environmental similarity.

## Assumptions

- Transferability: Linear relationship between pred-R² and Minkowski distance; transferability threshold of 0.5 is appropriate.
- Only environmental factors drive transferability in the main assessment (data limitations limit inclusion of economic variables).
- Regional representativeness captured sufficiently by chosen environmental and economic predictors for meta-models.

## Practical takeaways for GIS work

- Data layers are stored as GeoPackages with per-farm–level upscaled values aggregated to NUTS3; useful for map-based analyses and policy dialogues.
- The approach provides a reproducible workflow to upscale CS ES models to Europe-wide scales while explicitly testing transferability across regions.
- Output supports policy-oriented visualizations of per-farm ES across Europe, with explicit notes on regions where transferability is strong or weak.
- Users should be aware of data limitations, especially in regions lacking Europe-wide economic data and in crops or regions not well represented in CS data.