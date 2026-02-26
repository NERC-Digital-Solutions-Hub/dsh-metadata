# European-wide maps of modelled farmlevel ecosystem services, 2019.

## Overview
- Describes generation methods, data specifics, quality control, assumptions, and data structure for three ecosystem services (ES) modeled at average per-farm level across Europe.
- ES: carbon storage, food production, and nutrient export.
- Final Europe-wide outputs are simulated and provide simple per-farm averages; validation is limited due to data access constraints.
- Funded by the EU Horizon 2020 BESTMAP project; outputs may be superseded as peer review progresses.

## Data structure and outputs
- Three GeoPackage files, each corresponding to one ES:
  - EU_2019_upscaling_carbon.gpkg: Carbon storage (tonnes C per ha) per km2.
  - EU_2019_upscaling_food.gpkg: Standard economic output (Euros per year) per km2.
  - EU_2019_upscaling_nutrient_export.gpkg: Nutrient export (kg N per year) per km2.
- Final per-farm outputs are summarized for NUTS3 regions across Europe:
  - Output columns: fid, NUTS_ID, average_per_farm_ES.
  - Units: Carbon (tonnes C per ha per farm), Food (Euros per year per farm), Nitrogen export (kg N per year per farm).
- Note: Carbon results could not be produced for all regions; many regions have NULL for carbon.

## Case study ecosystem service models
- Carbon sequestration
  - Baseline soil organic carbon (SOC) modeled from abiotic factors (soil clay, pH, bulk density, elevation, precipitation, temperature) via a quasi-Poisson GLM using LUCAS data; adjustments for land use and AES applied.
- Food production
  - WOFOST model used to simulate crop yields (maize, sugar beet, wheat, sunflower, winter rapeseed, spring barley) under two climate scenarios (RCP4.5 and RCP8.5); yields converted to standard economic output using EUROSTAT coefficients.
  - Spain used observed values due to crop mismatch with WOFOST; six crops modeled at ~11 km2 resolution.
- Nutrient export
  - InVEST Nutrient Delivery Ratio (NDR) model simulated nitrogen (only nitrogen outputs used) at farm-level; mass-balance approach linking loads to land/crop types and delivery ratios.
- Case study regions (CS)
  - Mulde (Germany), South Moravia (Czechia), Catalonia (Spain), Bačka (Serbia), Humber (UK).
  - CS data include farm attributes, AES, economic data, and environmental data.

## Generation method: meta-modeling and upscaling
- Two-stage approach
  - Stage 1: Create transferable meta-models (statistical emulators) from CS data.
  - Stage 2: Assess transferability of meta-models across Europe.
- Meta-modeling details
  - Fragmented (multi-sub-model) approach to increase spatial detail and transferability.
  - NUTS3 regions used as analysis units; regions with insufficient data (<5% of farms in CS) excluded.
  - Starting predictors combine regional environmental data (FSU-based) and economic farm data (area, AES presence, economic size, farm specialization).
- Data preparation and predictors
  - Environmental predictors drawn from Europe-wide data (Table 3) aggregated to Farm Spatial Mapping Units (FSUs) to preserve farm anonymity.
  - Seasonal calculations defined (winter, spring, summer, autumn); seasonality aggregated for temperature, precipitation, solar radiation, etc.
  - Economic predictors: farm area, farm specialization, AES presence, economic size.
- Variable selection and fitting
  - Initial predictor set reviewed by ES experts (Table 4); VIF used to reduce multicollinearity (VIF < 5).
  - ES response variable log-transformed for modeling.
  - Stepwise forward/backward selection via AIC to obtain parsimonious models.
  - Training/testing: 75% train, 25% test; models also tested on full CS data.
  - Model accuracy metric: R-squared (R2) on test data.
- Across-region predictions
  - Each regional meta-model applied to the other 18 regions to assess inter-region transferability via pred-R2 (predicted R2).
- Representativeness and transferability
  - Representativeness measured with Minkowski distance in a multivariate space using environmental and socioeconomic attributes (economic data excluded due to incomplete Europe-wide availability).
  - Transferability diagrams plot pred-R2 against Minkowski distance; linear trend assessed and used to gauge transferability.
  - Transferability criteria
    - Predictive strength threshold: pred-R2 ≥ 0.5 (expert-judged reliability).
    - Trend criterion: negative, significant linear trend in the transferability diagram (t-test).
  - Regions meeting criteria mapped as “transferable”; results aggregated to estimate Europe-wide per-farm ES where conditions are suitable.
- Averaging per-farm ES
  - For regions meeting transferability criteria, meta-model coefficients applied to regional predictors to estimate average per-farm ES for that NUTS3 region.
  - Outlier control: values capped at twice the maximum observed CS value and floored at the minimum observed CS value.
  - Weighting: results weighted by regional pred-R2; requires Europe-wide economic data (not always available).
  - Final step produces Europe-wide average per-farm ES values; in some regions, data gaps prevented completion.

## Data processing details and variables
- Starting predictors include a mix of environmental variables (e.g., pH, bulk density, clay content, soil moisture, soil properties, topsoil organic carbon, temperature, precipitation, solar radiation, potential evapotranspiration, land cover, hydrology, root depth, elevation) and economic variables (farm size, AES presence, economic size, farm specialization).
- Seasonal aggregation and regional aggregation to FSUs preserve data privacy while providing comparable environmental features.
- Minkowski distance components (for representativeness) rely on environmental attributes; economic data are omitted in distance calculations.

## Quality control, limitations, and assumptions
- Quality control
  - CS ES validations against local data.
  - Meta-models undergo 75/25 train/test validation; predictions also tested against full CS data.
  - Input variables reduced by iterative VIF, maintaining low multicollinearity.
  - Transferability criteria implemented to ensure reasonable cross-region transfer.
  - Result capping to avoid extreme outliers; acknowledges limited external validation.
- Limitations
  - Europe-wide external validation data are lacking; transferability depends on limited proxies.
  - Economic data gaps necessitated proxies (FADN-based, with region-specific adaptations) and excluded some regions (e.g., Serbia and Balkans in final outputs).
  - Differences across CS (e.g., Catalonia’s crop mix and large farm counts) challenge uniform scaling.
  - Some outputs (carbon) have NULL in many regions due to data limitations.
- Assumptions
  - Linear relationship between pred-R2 and Minkowski distance in transferability.
  - Transferability cut-off of 0.5 is adequate based on expert judgement.
  - Only environmental factors considered in transferability explanations due to data limitations.

## Economic and regional data limitations
- Serbia and other Balkans not fully included in final outputs because meta-models rely on economic data.
- UK data rely on proxies from Farm Accountancy Data Network (FADN) due to incomplete Europe-wide data.
- Approximation approach for farm counts within FADN regions to assign NUTS3 designations; 1,257 of 1,517 NUTS3 regions modeled (17% reduction).
- Europe-wide validation remains challenging due to limited farm-level data outside CS sites.

## Differences across case studies
- Catalonia CS contained far more farms (over 42,000) and crops (e.g., fruits, olives) not fully compatible with WOFOST, causing scaling challenges.
- Crop-specific modelling differences influenced the Food ES transfer to the Europe-wide scale.

## Notes on outputs and interpretation
- Outputs are per-farm averages for each NUTS3 region, not total regional ES values.
- If a region lacks enough similarity or data to meet transferability criteria, the ES value may be NULL.
- Final maps and tables depend on transferability success and availability of economic data.

## References and data sources (selected)
- BESTMAP project, Cord et al., Hristov et al., Hiederer, Poggio et al., Eurostat/NUTS, FADN, InVEST user guide, WOFOST, LUCAS, various soil and climate datasets, and related methodological literature on meta-modelling and transferability.