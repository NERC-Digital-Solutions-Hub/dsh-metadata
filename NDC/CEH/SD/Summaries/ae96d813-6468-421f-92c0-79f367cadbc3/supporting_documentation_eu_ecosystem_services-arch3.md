# European-wide maps of modelled farmlevel ecosystem services, 2019

- Purpose: Describe methods, data, and outputs for upscaling three ecosystem services (carbon storage, food production, nutrient export) to average per-farm values across Europe, enabling scrutiny of policy decisions and informing future monitoring.

- Ecosystem services modeled
  - Carbon storage: soil and vegetation SOC per farm area
  - Food production: standard economic output per farm
  - Nutrient export: nitrogen exported per farm (used; phosphorus not utilized in final upscaling)

- Case-study basis and upscaling approach
  - Five case-study regions (CS): Mulde (Germany), South Moravia (Czechia), Catalonia (Spain), Bačka (Serbia), Humber (UK)
  - CS data provided at farm level, including AES (agri-environment schemes) and economic data
  - Final Europe-wide outputs are simulated via a two-stage meta-modelling approach (CS data → transferable meta-models)

- Data structure and formats
  - Three GeoPackage files corresponding to each ecosystem service
  - Each file contains per-km2 data with units:
    - Carbon: tonnes C per ha
    - Food: Euros per year
    - Nutrient export: kg N per year
  - Output fields include fid, NUTS3 region name, and average_per_farm_ES (with NULL where not meeting thresholds)

- Meta-modeling and generation method
  - Meta-models (emulators) approximate CS models, enabling faster upscaling
  - Fragmented meta-modelling: multiple regional sub-models (per NUTS3) vs. a single global model
  - Starting predictors: environmental variables (soil, climate, topography, land cover, hydrology) plus farm economics (area, AES presence, farm specialization, economic size)
  - Variable selection and reduction:
    - Initial predictor set informed by CS models and expert input
    - Multicollinearity addressed via Variance Inflation Factor (VIF) with a cutoff of VIF < 5
  - Model fitting:
    - Linear regression on log-transformed ES values
    - Stepwise AIC for model simplification (forward/backward)
    - 75% training / 25% testing with cross-validation; accuracy assessed by R^2
  - Transferability concept:
    - Meta-models applied across all 19 NUTS3 analysis regions to evaluate cross-region performance (pred-R^2)
    - Representativeness via Minkowski distance (multi-variate similarity) between regions
    - Transferability diagrams plot pred-R^2 against Minkowski distance; linear trends evaluated and used to gauge transferability

- Representativeness and transferability assessment
  - Distance metric (Minkowski) computed across ~1,500 NUTS3 regions using environmental and some economic variables (economic data not included in distance)
  - Transferability criteria:
    - Predictive strength: pred-R^2 threshold of 0.5
    - Reliable linear trend: negative slope in transferability diagram (statistically significant)
  - Regions meeting criteria are considered transferable; results are weighted by pred-R^2 to derive Europe-wide per-farm ES values

- Outputs and how to use them
  - Per-farm ES values produced for NUTS3 regions where transferability criteria are satisfied
  - Weighting by pred-R^2 and capping to avoid extreme values (max 2x observed CS max; min value bounded by CS min)
  - Final products provide average per-farm ES by NUTS3 with units specified above
  - Notably, carbon outputs could be NULL for many regions due to transferability constraints

- Quality control, validation, and safeguards
  - CS ES validations against local data (CS-level validation)
  - Meta-model cross-validation (train/test split) and validation against region data
  - Iterative VIF-based variable reduction to minimize multicollinearity
  - Transferability criteria to ensure reasonable cross-region application
  - Outlier controls by capping extreme values
  - Acknowledgement of limited Europe-wide validation data; final maps are based on simulated data subject to peer review

- Assumptions and limitations
  - Linear relationship assumed between pred-R^2 and Minkowski distance in transferability
  - Transferability threshold set at pred-R^2 ≥ 0.5
  - Only environmental factors used to assess transferability due to data limitations
  - Economic data limitations hindered full Europe-wide transferability (Serbia and Balkans largely excluded from final outputs)
  - Differences in CS datasets (e.g., Catalonia with many more farms and crop types) affect upscaling consistency

- Economic data and data availability notes
  - Europe-wide economic data not available for all NUTS3 regions; proxies and synthetic data used where possible
  - Serbia and the Balkans largely excluded from final outputs due to economic data gaps
  - UK economic data drawn from FADN; other regions relied on simulated or proxied data
  - Data augmentation included synthetic farm generation within FADN regions to match NUTS3 designations

- Implications for monitoring frameworks
  - Demonstrates a structured pathway for regional-to-EU-scale ES monitoring using meta-models and transferability checks
  - Highlights critical data needs: consistent metadata, accessible per-farm and per-region data, and harmonized economic indicators
  - Emphasizes data governance, openness, and clear handling of uncertainties and extrapolations in monitoring outputs
  - Provides explicit QC steps and transferability criteria that can be adopted or adapted in governance and monitoring plans

- Related references and data sources
  - BESTMAP project outputs and CS data (Cord et al. 2023)
  - FADN and EUROSTAT data contexts; various environmental and soil datasets (SoilGrids, HYSOGs, Copernicus data)
  - Methodological foundations: meta-modelling approaches, AIC, VIF, and transferability concepts (Marie & Simioni 2014; Burnham & Anderson 2002; O'Brien 2007)