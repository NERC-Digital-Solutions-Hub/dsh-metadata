# Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution

## Overview
- Presents national-scale estimates of nutrient, sediment, and faecal indicator organisms (FIO) emissions to water in Scotland, separating agricultural and non-agricultural sources.
- Combines process-based modelling with spatially explicit representations of farms, land uses, and catchments to enable scenario testing of mitigation actions.
- Includes greenhouse gas (GHG) implications (nitrous oxide and methane) from agricultural sources and comparisons to official inventories.

## National emissions snapshot (N, P, Sediment, FIOs)
- Nitrate (N): total 73.3 kt; agriculture contributes ~60.1 kt (over 80%), with Sewage Treatment Works (STWs) and woodland also notable (about 7% each).
- Phosphorus (P): total 3.89 kt; agriculture contributes ~2.47 kt (about 67%); STWs next at ~0.76 kt.
- Sediment (Z): total ~1,685 kt; agriculture dominates (around two-thirds, ~1,0xx kt), with bank erosion and other sources making up the rest.
- Faecal indicator organisms (FIOs): total ~2.02 × 10^15 cfu; agriculture ~0.64 × 10^15 cfu (about 31%), while STWs ~0.92 × 10^15 cfu and urban/septic sources also contribute.
- Comparison with SNIFFER Screening Tool shows differences due to scope (e.g., septic tank counts and bank erosion not treated identically in both tools).

## National nitrous oxide and methane emissions
- Agriculture emits ~4,776 kt CO2-eq of N2O and ~3,154 kt CO2-eq of CH4 (total agricultural GHG footprint provided in the study’s framing).
- Across all sectors, agriculture accounts for about 86% of N2O and 55% of CH4; when aggregated with other sectors, agriculture contributes roughly 3.1% of total CH4 and 4.8% of total N2O in the national GHG budget (53.9 Mt CO2-eq total, including non-agricultural sectors).

## Spatial variation and sector apportionment
- Nitrate: loads are highest near population-centred sources (STWs, septic tanks), but most inland catchments have low per-hectare loads; agriculture dominates in 91% of inland catchments (>50% of total load), and in 45% of inland catchments agriculture accounts for the majority of total nitrate.
- Phosphorus: similar spatial pattern; agriculture dominates in about 79% of inland catchments; phosphorus losses are influenced by soil drainage and rainfall (not strictly source-limited).
- Sediment: agriculture dominates in many catchments (about 66%), with bank erosion contributing a sizable share in some catchments.
- FIOs: non-agricultural point sources (STWs and septic tanks) are major contributors in many areas, but agriculture still dominates in a substantial share of inland catchments (about 71%).

## Agricultural emissions: footprints and pathways (by farm type and land use)
- Farm-type footprints: Dairy often has the largest footprints for nitrate, phosphorus, sediment, and N2O (due to high stocking densities and fertilizer use); LFA cattle & sheep generally lower footprints; arable land can have high nitrate and phosphorus losses despite limited agricultural area.
- Land-use footprints: Arable land frequently shows high nitrate and phosphorus losses (and sediment), reflecting fertilizer use and soil/ drainage characteristics; grassland footprints depend on livestock density and manure management.
- Non-field sources: Generally smaller for most pollutants, but methane emissions are mostly livestock-location driven; non-field contributions can still be meaningful for methane.
- Source and pathway apportionment (examples):
  - Nitrate: Soil stores ~41% of emissions on arable land; fertiliser ~20%; manures ~24%; excreta at grazing ~14%.
  - Phosphorus: Soil losses ~74%; fertiliser ~11%.
  - FIOs: Excreta at grazing ~95% (most FIOs linked to livestock activity in pastures).
  - Nitrous oxide: fertiliser and excreta at grazing are major contributors; much of nitrate leaching is linked to long-term soil processes.
  - Methane: predominantly enteric emissions (livestock digestion) for cattle/poultry; slurry management also contributes.
- Pathways: nitrate leaching dominates on arable land; surface runoff and preferential flow are significant for phosphorus and sediment, especially where drains are present; FIOs mainly transport via surface runoff from grazing.
- Arable, grass, rough grazing, and urban/non-field areas show distinct dominance patterns in source types and pathways; arable land, though only ~12% of agricultural area, can contribute large shares to nitrate and phosphorus loads.

## Data, modelling framework, and outputs
- Modelling framework (MAGPIE) integrates process-based models (PSYCHIC for phosphorus/sediment; N-CYCLE, NITCAT, NCYCLE/NEAPN for nitrogen; MANNER/NARSES for ammonia; FIO-FARM for pathogens) with a 1 km2 grid and a common spatial-connectivity approach.
- Outputs are organized by source area, source type, delivery pathway, and farm type, enabling targeted mitigation analysis.
- Non-agricultural modules cover urban, road, montane/woodland sources with empirical or licensed-discharge data.
- Outputs are designed for policy use: scenario comparisons, prioritisation of mitigation actions, and actionable guidance in Priority Catchments.
- Data integration and delivery use the MAGPIE decision-support framework with GIS-based mapping to align farm types, land uses, and catchments.

## Verification and validation
- 6.1 OSPAR-COM data: modelled loads compared with 5-year average HMS data (2006–2010) for 56 catchments; adjustments made to match mineral sediment (SPM) vs organic matter component.
- 6.1.2 In-channel retention: applied Behrendt & Opitz (phosphorus and nitrate) and Vanoni (sediment) retention models to estimate delivery to the mouth.
- 6.1.3 Model vs observations:
  - Phosphorus: r^2 ≈ 0.74; generally good concordance but under-predicts low loads and over-predicts high loads; agriculture dominant in many catchments.
  - Nitrate: r^2 ≈ 0.67; similar pattern of over-prediction in some STW-dominated catchments.
  - Sediment: r^2 ≈ 0.41; more scatter, with higher measured loads in some rough grazing landscapes; overall moderate agreement.
- Faecal indicator organisms (FIOs): compared with Kay et al. (2008) and Tetzlaff et al. (2012) data; correlations reasonable but modelled annual loads tend to exceed some field measurements; urban catchments show stronger signals in observed data.
- GHG inventory comparison: nitrogen and methane emissions from agriculture aligned with official UK inventory but with notable differences due to methodology (e.g., explicit leaching fractions and soil-compaction effects) and assumptions around livestock housing time and slurry management.

## Data delivery and policy relevance
- Outputs enable scenario testing of uptake and effectiveness of mitigation actions (e.g., manure relocation, buffer strips, timing of applications).
- Spatially explicit outputs support prioritisation in Priority Catchments and inform on the relative importance of source areas, sources, and pathways.
- The framework supports integration with policy instruments (NVZ actions, SRDP/land-management measures) and provides a quantitative basis for evaluating trade-offs across water quality and greenhouse gas objectives.

## Key takeaways for Data Support perspective
- High-value, spatially explicit data and model outputs illuminate where and how agricultural and non-agricultural sources drive water quality outcomes.
- The integrated modelling approach yields actionable footprints by farm type and land use, enabling targeted interventions and scenario-based planning.
- Validation shows generally good correspondence with observed data for nutrients (better for phosphorus, nitrate) and more variable for sediment and FIOs, highlighting areas where data or model structure could be refined.
- The MAGPIE-enabled, GIS-based delivery supports decision-makers in prioritising actions, communicating results, and monitoring uptake and reuse of outputs.