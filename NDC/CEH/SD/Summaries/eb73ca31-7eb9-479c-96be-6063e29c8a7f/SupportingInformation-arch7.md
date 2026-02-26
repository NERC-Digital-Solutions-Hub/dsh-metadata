# Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution

## Overview
- Objective: quantify how Diffuse Pollution General Binding Rules (DP GBRs) and other mitigation measures reduce pollutant emissions from agriculture to water, aiding Water Framework Directive (WFD) compliance in Scotland.
- Approach: integrates catchment surveys with process-based models to assess current and future uptake of mitigation actions.
- Outputs are spatially explicit, enabling interrogation by location, farm type, and land use to support policy and practice.

## Modelling Framework and Spatial Structure
- Core model: a meta-model of export coefficients built on process-based models (e.g., PSYCHIC) to estimate pollutants from farm inputs.
- Spatial explicitness: all models share a common water balance/drainage framework and a landscape connectivity/delivery model.
- Reporting units: Scotland-wide outputs are calculated for inland river water bodies (~3,300) and coastal water bodies (~15,400).
- Disaggregation: results are broken down by nine Robust Farm Types (RFTs) and land-cover types (cultivated land, improved grassland, rough grazing), linked to Water Framework Directive typology and land-use/farm census data.

## Data Inputs and Spatial Layers
- Climate: 1961–1990 baseline across Scotland.
- Soils: dominant textures per 1 km2 cell (SSK1B).
- Land cover/use: detailed mapping of non-agricultural cover and crop distribution aligned with the June Agricultural Census (JAC) 2010; CEH Land Cover Map 2007 for reallocation where needed.
- Landscape connectivity: refined index capturing within-field and slope-to-channel transmission losses, boundary permeability, artificial drainage, and tile drainage.
- Farm data: nine representative farm types (e.g., Dairy, Specialist Pigs, Specialist Poultry, Pigs, Cereals, General Cropping, Horticulture, LFA cattle & sheep, Lowland cattle & sheep, Mixed); management calendars and crop/livestock allocations derived from JAC 2010 and regional counts.
- Management practices: manure/storage, fertiliser calendars, cropping details, and fertiliser timings aligned with national surveys.
- Non-agricultural and point sources: urban, roads, bank erosion, septic tanks, STWs; modeled with EMC/empirical coefficients and licensing/population data.
- Source apportionment framework: emissions disaggregated by coordinates including pollutant type, source, area, pathway, and management type to support targeted mitigation analyses.

## Agricultural Emissions and Pathways
- Farm-type footprints: pollutant footprints vary by farm type; dairy often shows the highest overall footprint due to stocking density and fertiliser use.
- Land-use footprints: arable land typically has higher nitrate and phosphorus losses; rough grazing shows different dominant pathways due to drainage and erosion patterns.
- Pathways and forms: 
  - Nitrate: major leakage via leaching from soils; contribution by soil source, soil leaching, fertiliser, and grazing excreta.
  - Phosphorus: strong role of soil transport and surface runoff; under-drainage and preferential flow are key conduits.
  - Sediment: surface runoff dominates; runoff and drains contribute heavily, with significant influence from land use and drainage presence.
  - FIOs: largely from grazing/excreta, with urban and STW sources also important.
  - Methane and nitrous oxide: methane mainly from enteric fermentation; N2O linked to fertiliser/manure and grazing excreta, with notable effects from soil moisture and compaction.
- Source/apportionment detail: emissions decomposed by source type (soil, fertiliser, manure, grazing excreta, etc.) and delivery pathway (surface, leaching, preferential flow, etc.), enabling precise attribution of reductions to specific practices.

## Mitigation Actions and Effects
- Policy actions mapped to auditable measures (e.g., relocating manure heaps, buffer strips, timing of fertiliser application).
- Action metrics: effectiveness (P), applicability (A), and implementation efficiency (E); net reductions are calculated with multiplicative and overlap-adjusted methods to avoid overestimation.
- Local condition adjustments: treatments account for slope, field boundaries, soil and drainage status; actions can be selectively applied where appropriate.

## Outputs, Policy Relevance, and GIS Implications
- Spatial outputs: region-wide, water-body–specific emissions by pollutant, farm type, and land cover; linked to potential mitigation uptake and scenario analysis.
- Policy relevance: quantifies agricultural contributions to nitrate, phosphorus, sediment, FIOs, methane, and nitrous oxide; supports targeting of DP GBR/NVZ/SRDP uptake and catchment interventions.
- GIS applicability: enables map-based exploration of emissions, source attribution, and mitigation impact across catchments and water bodies; supports scenario planning and priority-setting for interventions.

## Verification, Validation, and Uncertainty
- Data sources for validation: OSPAR-COM (nitrate, phosphorus, suspended solids) across 56 HMS catchments; Behrendt & Opitz (phosphorus/nitrate retention) and Vanoni (sediment retention) models for in-channel losses.
- Key validation outcomes:
  - Phosphorus: strong correlation with measured loads (r^2 ≈ 0.74); agriculture dominant in many catchments; some under/over-prediction in extremes.
  - Nitrate: good correlation (r^2 ≈ 0.67); agriculture dominant in most catchments; some catchments show STW/diffuse contributions.
  - Sediment: weaker correlation (r^2 ≈ 0.41); higher variability linked to grazing intensity and bank erosion in certain areas.
- Faecal indicator organisms (FIOs): compared with Kay et al. (2008) and Tetzlaff et al. (2012) data; project outputs generally higher than some surveillance datasets (annual vs. event-based) but maintain relative patterns across urban/rural land uses.
- Greenhouse gases: nitrogen and methane emissions compared with official Scotland inventory; differences attributed to methodological choices (FracLeach, compaction, grazing management) and scenario settings; overall, mitigation actions shift the N2O and CH4 estimates relative to inventory baselines.

## Practical Notes and Limitations
- Some mitigation actions are not fully disclosed due to data sensitivity.
- Emission factors carry uncertainties (IPCC-based, model refinements, nitrate leaching variability); emphasis on relative changes and policy impact rather than absolute totals.
- FIO and bank erosion modelling rely on empirical/calibration data with site-specific variability.
- The complete project includes additional mitigation descriptions and future management scenarios beyond the presented extract.

## Endnotes
- The full report contains further chapters detailing mitigation actions and projected management scenarios, complementing the results summarized here.