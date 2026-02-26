# European-wide maps of modelled farmlevel ecosystem services, 2019.

- Purpose and scope
  - Describes generation methods, data structure, quality control, assumptions, limitations, and structure for three ecosystem services (ES) modelled at average per-farm level across Europe.
  - Uses a two-stage upscaling approach: case-study (CS) ES models inform a Europe-wide, simulated dataset (not directly validated with full Europe-wide farm data).
  - Final Europe-wide outputs are simulated and accompanied by limited simple quality checks; methodology undergoing peer review and may be superseded.

- Data structure and content
  - Three GeoPackage files, each named for the ES:
    - EU_2019_upscaling_carbon.gpkg — Carbon storage (tonnes C per ha)
    - EU_2019_upscaling_food.gpkg — Standard economic output (Euros per year)
    - EU_2019_upscaling_nutrient_export.gpkg — Nutrient export (kg N per year)
  - Each file contains one or more layers describing ES values with corresponding attributes.

- Case-study ecosystem services models (CS level)
  - Carbon sequestration: baseline soil organic carbon (SOC) model using abiotic factors (soil clay content, pH, bulk density, elevation, precipitation, temperatures) via a quasi-Poisson GLM; adjustments for land use and AES applied to compute final per-farm SOC.
  - Food production: WOFOST model used to simulate crop yields; results averaged over climate scenarios (RCP4.5 and RCP8.5); yields converted to standard economic output (€) using EUROSTAT coefficients (Spain uses observed values for Spain-specific crops).
  - Nutrient export: InVEST Nutrient Delivery Ratio (NDR) model simulated at farm level for nitrogen; outputs reflect annual nutrient export per farm.

- Case-study regions and data used
  - Regions (CS): Mulde (Germany), South Moravia (Czechia), Catalonia (Spain), Bačka (Serbia), Humber (UK).
  - Farm-level data include ES details, farm attributes (excluding spatial data), AES, and economic data; environmental variables accompany CS data.
  - Additional environmental variables aggregated from sources (Tables with pH, bulk density, clay content, available water capacity, SOC, temperature, precipitation, solar radiation, evapotranspiration, land cover, soil moisture, elevation, HOST soil groups, rooting depth).

- Generation and upscaling methodology
  - Meta-model approach: fast statistical emulators (fragmented meta-models) built from CS data to produce Europe-wide ES values.
  - Spatialization units: NUTS3 regions used as subregions; regions with insufficient data excluded to ensure enough data per region (prevalence leads to 19 regions retained).
  - Starting predictors: Europe-wide environmental data plus farm economic data (area, specialization, AES presence, economic size).
  - Variable selection and model building
    - Predictor set refined via variance inflation factor (VIF) to keep all predictors with VIF < 5.
    - Stepwise AIC used to improve model parsimony (forward and backward).
    - ES values log-transformed for modelling; linear regression with beta coefficients estimated.
    - Cross-validation: 75% training, 25% testing; model performance assessed via R²; final models applied to full CS data.
  - Representativeness and transferability
    - Representativeness measured across ~1,500 NUTS3 regions using Minkowski distance on selected environmental and socioeconomic attributes (economic data excluded from distance due to incomplete Europe-wide availability).
    - Transferability evaluated with “transferability diagrams”: predicted R² (pred-R²) versus Minkowski distance; fit assessed by linear trend and RMSE.
  - Transferability criteria
    - Predictive strength: pred-R² threshold set at 0.5 to indicate adequate transferability.
    - Linearity: transferability diagram must show a significant negative slope (reliable linear trend).
    - Regions meeting criteria are identified; results mapped to indicate transferable areas.

- Deriving average per-farm ES and handling data gaps
  - For regions meeting transferability criteria, meta-model coefficients applied to predict average per-farm ES for that NUTS3 region.
  - Values capped to avoid extremes: max 2x the highest CS ES value; minimum bounded by the lowest CS ES.
  - Europe-wide weighting: final per-farm ES values weighted by their pred-R²; pred-R² values derived from the corresponding Minkowski distance.
  - Data limitations
    - Europe-wide validation data mostly unavailable; CS validation performed locally.
    - Economic data gaps restricted transferability, especially for Serbia and the Balkans; UK data used proxy approaches; some CS regions (notably carbon) may yield null outputs.
    - 1257 of 1517 NUTS3 regions modelled (17% reduction) due to data gaps and proxies.
    - Catalonia’s large farm count and crop mix (fruits/olives) posed modelling differences (WOFOST applicability) and scaling challenges.

- Data quality control and assumptions
  - Quality control
    - CS ES models validated against local data (CS-specific validation).
    - Meta-models cross-validated within each CS region.
    - Iterative VIF-based reduction to remove multicollinearity.
    - Transferability criteria implemented to guard cross-region applicability.
    - Output caps applied to limit extreme values; acknowledge limited outside-CS validation.
  - Assumptions
    - Linear relationship assumed between pred-R² and Minkowski distance in transferability analysis.
    - Transferability threshold of 0.5 deemed adequate based on ecological contexts.
    - Only environmental factors driving transferability were considered (data limitations acknowledged).
  - Economic data constraints
    - Europe-wide economic data largely unavailable; reliance on simulated FADN data with synthetic farm-level mapping where needed.
    - UK proxies and regional aggregation used where data were incomplete; Serbia and the Balkans largely excluded from final outputs due to economic data gaps.

- Nature and units of outputs
  - Outputs provide average per-farm ES for each NUTS3 region (not total regional ES).
  - Output columns: fid, NUTS_ID, average_per_farm_ES.
  - Units per ES:
    - Carbon: tonnes C per ha per average farm
    - Food production: Euros per year per average farm
    - Nitrogen export: kg N per year per average farm
  - Carbon output may be null for some regions due to transferability criteria.

- Limitations and considerations for use
  - Outputs are simulated, with limited validation across Europe; regional transferability depends on environmental similarity.
  - Differences among CS (crop types, data density) influence comparability and upscaling reliability.
  - Economic data gaps constrain full Europe-wide outputs and weighting schemes.
  - The method emphasizes per-farm averages rather than total regional ES values.

- Practical implications for data governance and strategy (Data Leaders)
  - Data structure and provenance: clear documentation of CS data, input variables, and upscaling steps; explicit geo-referenced outputs per NUTS3 region.
  - Data quality and interoperability: extensive metadata, explicit assumptions, and quality-control steps; handling of missing data and proxies should be governed.
  - Transferability and standards: need for consistent metrics, regional representativeness assessment, and transparent transferability criteria to support cross-region data sharing.
  - Data gaps and governance actions: identify where Europe-wide validation data and economic data are missing; plan data acquisition or agreement for access across member regions to improve future upscaling and validation.
  - Stakeholder engagement and co-ownership: given the CS design and regional upscaling, involve national/regional partners to interpret region-specific outputs and refine ES modelling choices.