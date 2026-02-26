# European-wide maps of modelled farmlevel ecosystem services, 2019

- Purpose and scope
  - Describes generation methods, data nature, units, quality control, assumptions, limitations, and data structure for three ecosystem services (ES) modelled at an average per-farm level across Europe.
  - Aims to upscale ES from five case-study regions to Europe-wide, producing average per-farm ES values by NUTS3 region.
  - ES: Carbon storage, Food production, Nutrient export (nitrogen).

- Data structure and content
  - Dataset comprises three GeoPackage files, each containing a layer for one ES:
    - EU_2019_upscaling_carbon.gpkg — Carbon storage (tonnes C per ha; per km2 context listed)
    - EU_2019_upscaling_food.gpkg — Standard economic output (Euros per year)
    - EU_2019_upscaling_nutrient_export.gpkg — Nutrient exported (kg N per year)
  - Case studies informing Europe-wide results (CS ES models existed separately; CS results inform Europe-wide outputs).
  - Final outputs are average per-farm ES values per NUTS3 region across Europe; some regions may have NULLs if criteria not met.

- Case studies and ES modelling at CS level
  - Five CS regions: Mulde (Germany), South Moravia (Czechia), Catalonia (Spain), Bačka (Serbia), Humber (UK).
  - ES modelling at CS level:
    - Carbon sequestration: baseline soil organic carbon (SOC) via quasi-Poisson GLM using abiotic factors, adjusted for land use and AES.
    - Food production: WOFOST crop model; end-of-season yields under two climate scenarios (RCP4.5 and RCP8.5); yields converted to standard economic output using EUROSTAT coefficients.
    - Nutrient export: InVEST Nutrient Delivery Ratio model; outputs aggregated to farm level, using nitrogen data.

- Generation method and upscaling approach
  - Two-stage approach:
    - Stage 1: Create transferable meta-models (statistical emulators) from CS data using fragmented meta-models to enhance spatial detail and transferability.
    - Stage 2: Assess transferability of meta-models across regions.
  - Inputs and data sources
    - ES data from BESTMAP (Cord et al., 2023) for five CS regions; per-farm ES values and farm attributes; AES and economic data.
    - Europe-wide environmental predictors (Table 3) and farm-level economic data used as starting predictors.
  - Meta-model framework
    - Linear regression on logged ES values:
      ES_log = β0 + β1·ν1 + ... + βn·νn + ε
    - Predictor selection via variance inflation factor (VIF) to keep multicollinearity below 5; stepwise AIC used for model refinement (forward/backward).
    - Training/testing: 75% training, 25% testing; cross-validation across CS regions; accuracy assessed with R².
  - Spatial and regional structuring
    - Regions defined as NUTS3 subregions; regions with <5% of farms excluded to ensure enough data; 19 NUTS3 regions retained across CS regions.
    - Environment data summarized at Farm Spatial Mapping Units (FSUs) via zonal statistics to preserve anonymity; seasonal aggregation for climate variables.

- Transferability and representativeness analysis
  - Representativeness: used Minkowski distance to measure multivariate similarity between NUTS3 regions based on selected environmental variables (no economic data included in distance due to data gaps).
  - Transferability assessment: for each CS meta-model, predicted ES values were compared across regions to derive pred-R² when applied to other regions.
  - Transferability diagrams: plot pred-R² (accuracy) against Minkowski distance; linear trend fitted to evaluate transferability.
  - Criteria to deem transferability adequate
    - Predictive strength: pred-R² threshold of 0.5 (region considered transferable if below a Minkowski distance cut-off at which pred-R² ≥ 0.5).
    - Trend reliability: linear trend with negative slope and statistical significance (t-test).
  - Output: maps indicating transferability potential; final per-NUTS3 averages weighted by pred-R² and transferability presence. Maximum possible transferability score is 19 (across 19 CS NUTS3 regions).

- Data preparation and predictors
  - Starting predictors (economic and environmental) compiled for each analysis region:
    - Farm area (ha), farm specialization, economic size (Euros), AES presence.
    - Environmental variables drawn from CS data and European grids (soil properties, climate, topography, land cover, etc.).
  - Predictor selection and reduction
    - Initial set of environmental and economic predictors per ES (Table 4); variables kept if influential; multivariate reduction via VIF (cut-off 5).
    - Categorical predictors (farm specialization, AES presence) retained but not subjected to VIF pruning.

- Quality control and limitations
  - Quality control
    - CS ES validated against local data; meta-models cross-validated; input variables subjected to VIF reduction.
    - Transferability criteria used to guard against applying models to dissimilar regions.
    - Final weighted averages capped to avoid extreme values (max 2× observed CS max; minimum not below observed CS min).
  - Limitations and assumptions
    - Europe-wide validation data unavailable; outputs only simple data quality checks feasible.
    - Linear relationship assumed between pred-R² and Minkowski distance; transferability threshold set at 0.5; economic data gaps affect transferability for some regions.
    - Economic data gaps: Serbia and many Balkan regions lacked Europe-wide economic data; UK proxy data used; 1257 of 1517 NUTS3 regions modelled (17% reduction).
    - Differences among CS (e.g., Catalonia with >42,000 farms; crop portfolio not fully compatible with WOFOST across all CS) pose scaling challenges.

- Economic data and transferability caveats
  - Transferability relied on environmental predictors; economic data were not universally available across Europe.
  - Serbia and Balkans could be included in transferability analysis via environmental distance but not in final ES production due to missing economic data.
  - Data sources for proxies included FADN (and UK weighting for lack of full data); several proxies aggregated or simulated to align with NUTS3 regions.

- Nature and units of the final outputs
  - Output format: for each ES, a dataset with columns:
    - fid (row ID)
    - NUTS_ID (NUTS3 region name)
    - average_per_farm_ES (average ES for farms in that NUTS3 region)
  - ES units
    - Carbon: tonnes C per ha per average farm
    - Food production: Euros per year per average farm
    - Nitrogen export: kg N per year per average farm
  - Note: Carbon outputs may be NULL for many regions if transferability criteria not met.

- Quality control and validation context
  - CS ES validation against local data (Cord et al., 2023).
  - Meta-model validation via cross-validation within CS regions and testing across the full CS data.
  - Data normalization, outlier handling, and capping procedures documented.

- Data provenance and ongoing status
  - Outputs originate from the BESTMAP project ( Horizon 2020, grant no. 817501).
  - Methodology and results may be superseded as peer review progresses.
  - Acknowledges data and methodological limitations due to access constraints and regional data gaps.

- References and context (selected)
  - Cord et al. (2023) and BESTMAP project documentation
  - InVEST model documentation for nutrient delivery
  - WOFOST crop model and related climate scenario data
  - FADN data and European statistical units (NUTS3)
  - Relevant data sources for soil, climate, and land cover (e.g., SoilGrids, HYSOGs, Copernicus datasets)