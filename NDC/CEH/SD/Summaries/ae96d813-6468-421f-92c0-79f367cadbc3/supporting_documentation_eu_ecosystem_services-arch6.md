# European-wide maps of modelled farmlevel ecosystem services, 2019

- Overview
  - Describes methods, data structure, quality control, assumptions, limitations, and data structure for three ecosystem services (ES) modelled at average per-farm level across Europe.
  - Outputs are Europe-wide, simulated per-farm ES values generated under the BESTMAP project methodology; final data are not yet fully validated due to data access limitations.
  - Outputs include simple quality checks and input data quality steps; methodology under peer review and may be superseded.

- Data structure and formats
  - Dataset comprises 3 GeoPackage files, each corresponding to an ES:
    - EU_2019_upscaling_carbon.gpkg (Carbon storage; tonnes C per ha)
    - EU_2019_upscaling_food.gpkg (Food production; Euros per year)
    - EU_2019_upscaling_nutrient_export.gpkg (Nutrient export; kg N per year)
  - Each file contains spatial layers with per-farm or per-area ES values; outputs are average per-farm values per NUTS3 region.

- Case study ecosystem service models (_CS_model_ descriptions)
  - Carbon sequestration
    - Baseline soil organic carbon (SOC) model using abiotic factors; adjustments for land use and AES applied.
  - Food production
    - WOFOST crop-model outputs (maize, sugar beet, wheat, sunflower, rapeseed, barley); yields averaged across climate scenarios; converted to standard EU economic output (€) per farm.
  - Nutrient export
    - InVEST NDR model to estimate nitrogen export; outputs linked to farm-level data; phosphorus not used in upscaling.
  - Final per-farm ES aims to be averaged at the NUTS3 region level across Europe.

- Generation method (two-stage upscaling)
  - Stage 1: Creation of transferable meta-models using case-study (CS) data
    - Data from five CS regions (Mulde, Germany; South Moravia, Czechia; Catalonia, Spain; Bačka, Serbia; Humber, UK) at farm level.
    - ES indicators: annual carbon sequestration (t ha⁻¹), nutrient export (kg N), food production (€).
    - Predictors: CS farm attributes, AES, economic data, and extensive environmental variables.
    - Data preparation: CS data merged with wide environmental datasets; to preserve privacy, environmental stats computed per homogeneous spatial mapping units (FSUs) rather than per farm; seasonal aggregations used where applicable.
  - Stage 2: Transferability assessment and upscaling
    - Meta-models tested for transferability across 18 other NUTS3 regions per ES, using 2021 Eurostat NUTS3 boundaries.
    - Representativeness and transferability evaluated via Minkowski distance in multivariate space and pred-R² metrics.

- Starting predictors and variable selection
  - Environmental predictors drawn from Europe-wide datasets (Table 3) and farm economic predictors (farm area, farm specialization, AES presence, economic size).
  - A large set of potential predictors was narrowed using variance inflation factor (VIF) to keep all predictors with VIF < 5.
  - Categorical predictors (farm specialization, AES presence) treated appropriately in model selection.

- Model fitting and selection
  - Meta-models fitted with the log-transformed ES as response.
  - Linear regression with stepwise AIC in forward and backward directions to obtain a parsimonious model.
  - Training/testing: 75% training, 25% testing; meta-models evaluated by R²; applied to full CS data after validation.

- Cross-region application and representativeness
  - Each meta-model (per ES per analysis region) applied to all other analysis regions to obtain pred-R² for cross-region performance.
  - Representativeness (Minkowski distance) calculated for ~1,500 NUTS3 regions using selected environmental and economic variables; economic data not included in distance due to Europe-wide availability limits.

- Transferability assessment (transferability diagrams)
  - Pred-R² plotted against Minkowski distance for each region pair; linear trend fitted; RMSE used to assess fit.
  - Predefined transferability criteria:
    - Predictive strength threshold: pred-R² ≥ 0.5 (based on expert judgement for ecological contexts).
    - Reliable linear trend: negative slope of the transferability line must be statistically significant (t-test).
  - Regions meeting criteria identified; transferability potential mapped across Europe.

- Output derivation and weighting
  - For regions meeting transferability criteria, region-specific meta-model coefficients used to predict ES for that NUTS3 region.
  - Caps applied to prevent outliers: predictions capped at 2× the maximum CS value; minimum capped at CS minimum.
  - Final per-farm ES values weighted by pred-R² (higher pred-R² increases influence).
  - Europe-wide economic data limitations meant some regions (notably Serbia and Balkans) could not be fully included in the final economic-based outputs.

- Data nature and units of results
  - Outputs represent the average per-farm ES for each NUTS3 region (not total regional ES).
  - Columns include: fid (row ID), NUTS_ID (region name), average_per_farm_ES (value).
  - Units:
    - Carbon: tonnes C per ha per average farm
    - Food production: Euros per year per average farm
    - Nitrogen export: kg N per year per average farm
  - Some regions may have NULL values if transferability criteria were not met.

- Quality control and limitations
  - CS ES validated against local region data; meta-models cross-validated (75/25 split); input variables reduced by iterative VIF.
  - Transferability criteria introduced to ensure reasonable cross-region applicability.
  - Final weighted averages capped to avoid extreme values; validation constrained by lack of comprehensive farm-level data across all NUTS3 regions.
  - Data gaps led to selective inclusion (e.g., Serbia excluded from final economic outputs; UK data proxying used).

- Assumptions and economic data considerations
  - Key assumption: pred-R² vs Minkowski distance relationship is linear; transferability threshold of 0.5 is adequate.
  - Assumed environmental factors drive transferability (data limitations prevented full inclusion of economic data in transferability assessments).
  - Europe-wide economic data constraints necessitated proxies (FADN-based synthetic data, UK weights, 2014–2017 averaging); some regions lacked complete economic data, affecting transferability.

- Limitations and data limitations
  - Final outputs rely on simulated data and limited validation; not all EU regions could be modeled due to data gaps (notably Serbia/Balkans for economic data).
  - Cropping differences (e.g., Catalonia’s crops) affected WOFOST applicability for food production scaling.
  - Only per-farm averages are reported; regional totals are not provided.

- Practical implications for data use (Data Support perspective)
  - Provides Europe-wide, per-farm ES estimates enabling cross-regional comparisons and policy-oriented analyses.
  - Demonstrates a data-centric approach to upscaling using meta-models, transferability testing, and representativeness metrics.
  - Highlights the importance of harmonized environmental and farm-level data, and the challenges when data are incomplete or regionally diverse.

- Data provenance and references
  - BESTMAP project basis; CS data drawn from five regional case studies; references include Cord et al. (2023) and related methodological sources on meta-modelling, environmental datasets, and ES modelling tools (InVEST, WOFOST, LUCAS, FADN, etc.).