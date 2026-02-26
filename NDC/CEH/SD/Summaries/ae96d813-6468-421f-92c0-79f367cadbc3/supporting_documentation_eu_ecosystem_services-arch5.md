# European-wide maps of modelled farmlevel ecosystem services, 2019

- Purpose and scope
  - Presents European-scale maps of three ecosystem services (ES) modelled at an average per-farm level: Carbon storage, Food production, and Nutrient export.
  - Outputs are upscaled from five case studies (CS) to Europe-wide coverage; CS results inform Europe-wide results, though Europe-wide data are simulated and only simple quality checks were possible.
  - Funded by the European Union’s Horizon 2020 BESTMAP project; methodology and outputs may be superseded by ongoing peer review.

- Data structure and outputs
  - Three GeoPackage files, each named for the ES:
    - EU_2019_upscaling_carbon.gpkg (Ecosystem service: Carbon storage; unit: tonnes C per ha per km2)
    - EU_2019_upscaling_food.gpkg (Ecosystem service: Standard economic output; unit: Euros per year per km2)
    - EU_2019_upscaling_nutrient_export.gpkg (Ecosystem service: Nutrient exported; unit: kg N per year per km2)
  - Each file contains a layer for the respective ES and records per NUTS3 region with:
    - fid (row ID)
    - NUTS_ID (region name)
    - average_per_farm_ES (average ES value per farm in that NUTS3 region)
  - Not all regions have data for every ES (e.g., carbon results may be NULL in several regions).

- Case studies and modelling approaches
  - Case study regions (CS):
    - Mulde, Germany; South Moravia, Czechia; Catalonia, Spain; Bačka, Serbia; Humber, UK.
  - Model descriptions per ES (CS level):
    - Carbon sequestration: baseline soil organic carbon (SOC) via a quasi-Poisson GLM using abiotic factors; adjustments for land use and AES.
    - Food production: yields simulated with the WOFOST model; multi-scenario climate inputs (RCP4.5 and RCP8.5) with regional adjustments to euros.
    - Nutrient export: InVEST Nutrient Delivery Ratio (NDR) model; outputs at farm level, using nitrogen data.
  - Output objective at CS: per-farm ES values aggregated to NUTS3 regional scale for Europe.

- Generation method (two-stage meta-modelling)
  - Stage 1: Create transferable meta-models (statistical emulators) using CS data and starting predictors.
    - Variables include Europe-wide environmental data and farm-level economic data (farm area, farm specialization, AES participation, economic size).
    - Variable selection and reduction via:
      - Variance Inflation Factor (VIF) to keep predictors < 5.
      - Stepwise AIC for model refinement.
    - Model form: linear regression on log-transformed ES values; predictors denoted as v1…vn.
    - Cross-validation: 75% training / 25% testing; performance assessed with R²; final model applied to full CS data.
  - Stage 2: Assess transferability across regions
    - Representativeness: compute Minkowski distance across NUTS3 regions using environmental and some economic predictors (economic data mostly excluded from distance due to incomplete Europe-wide data).
    - Up-scaling to 19 NUTS3 regions (derived from 5 CS × 3–5 regions per CS; filtered to ensure enough farms per region).
    - For transferability, apply a region’s meta-model to other regions and evaluate pred-R² against distance.
    - Transferability criteria:
      - pred-R² threshold of 0.5 (expert-judgement-based).
      - A reliable negative linear trend in transferability diagrams (assessed via t-test).
    - Regions meeting criteria are used to derive Europe-wide per-farm ES values; results weighted by pred-R².
    - Extremes capped: values not allowed to exceed 2× the maximum observed CS value; minimum values similarly protected.
    - Final per-farm ES values reflect average farm ES in each NUTS3 region, where transferability criteria are met; some regions may be null if criteria are not satisfied or data are missing.

- Representativeness and transferability
  - Representativeness measured with Minkowski distance in multi-variate space (environmental and, where data allow, economic variables).
  - Predicted ES in other regions compared to CS results via pred-R²; transferability maps identify which regions can reasonably adopt a meta-model from a CS.
  - Transferability maps aggregate across CS; higher sums indicate greater transferability potential for a given NUTS3 region.

- Data limitations, assumptions, and quality control
  - Key limitations:
    - Europe-wide validation data are not available; validation is limited to CS and meta-model cross-validation.
    - Economic data are incomplete across Europe; Serbia and the Balkans largely excluded from final outputs due to missing economic data; proxies used where possible.
    - Some CS crops (e.g., in Catalonia) differ from CSs in other regions, complicating upscaling (WOFOST applicability varies by crop).
    - Final outputs do not reflect total regional ES, but per-farm averages; some regions yield NULL values.
  - Assumptions:
    - Linear relationship between pred-R² and Minkowski distance in transferability analyses.
    - Transferability cut-off of pred-R² = 0.5 is adequate.
    - Only environmental factors drive transferability in the distance analysis (data limitations limited economic integration in distances).
  - Quality control and validation:
    - CS models validated against local data (Cord et al., 2023).
    - Meta-models cross-validated (75/25) and then tested against full region data.
    - Input variables reduced via iterative VIF; outlier caps applied to final results.
    - Transparency on data provenance and model steps; acknowledge ongoing peer review and potential methodological updates.

- Data governance and usage considerations for Data Stewards
  - Anonymization strategy: farm-level data protected by using Farm Spatial Mapping Units (FSUs) to derive region-level statistics rather than sharing raw farm data.
  - Metadata and provenance:
    - Clear documentation of ES definitions, units, case-study inputs, and upscaling methodology.
    - Explicit notes on data that are NULL or not included due to transferability or data gaps.
  - Reproducibility and updates:
    - Methodology relies on published CS work and publicly available data sources; potential updates as peer review progresses.
  - Limitations for use:
    - Outputs are modeled averages and may not reflect total regional ES or exact farm counts.
    - Economic data gaps may affect regional comparability; treat per-farm estimates with appropriate caution.

- Practical takeaways for data discovery and reuse
  - Access: three GeoPackage files containing per-farm ES averages by NUTS3 region for carbon, food, and nitrogen export.
  - Units to interpret: carbon (tonnes C per ha per average farm), food (Euros per year per average farm), nutrient export (kg N per year per average farm).
  - Coverage caveats: carbon and nutrient export results may be incomplete for some NUTS3 regions; results are contingent on transferability criteria being met.
  - Documentation alignment: methodology, data sources, modelling steps, and limitations are described to support understanding, governance, and potential re-use or updating of the datasets.