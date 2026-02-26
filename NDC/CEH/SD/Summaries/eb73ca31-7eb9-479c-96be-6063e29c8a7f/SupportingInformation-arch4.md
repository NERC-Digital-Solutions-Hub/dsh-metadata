Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution

- A national-scale modelling study for Scotland that combines agricultural and non-agricultural pollutant sources to produce total emissions and assess mitigation strategies under WFD RBMPs.
- Key aim: quantify diffuse pollution from agriculture and other sources, and evaluate the effectiveness of measures in reducing nitrate, phosphorus, sediment and faecal indicator organisms (FIOs), plus associated greenhouse gas implications.

## What the study finds

- National emissions (present day):
  - Nitrate (NO3): Total 73.3 kt; Agriculture contributes 60.1 kt (≈ 82%); Sewage works ~7%; Woodlands ~7%.
  - Phosphorus (P): Total 3.89 kt; Agriculture ~67% of load; Sewage works ~18%.
  - Sediment (Z): Total 1,685 kt; Agriculture ~68%; Bank erosion ~20%.
  - Faecal indicator organisms (FIOs): Total 2.02 × 10^3 × 10^15 cfu; Agriculture ~31%; Sewage works ~46%; Septic tanks ~21%.
- Greenhouse gases (GHG) from agriculture (NH3-N2O and CH4):
  - N2O (kt CO2e): Agriculture ~4,775; CH4 (kt CO2e): Agriculture ~3,154.
  - Agriculture accounts for ~86% of Scotland’s N2O and ~55% of CH4.
  - Total Scotland GHG, including non-agriculture sectors, ~53.9 Mt CO2e; agriculture contributes ~3.1% of total for CH4 and ~4.8% for N2O.
- Spatial patterns:
  - Nitrate: agriculture dominates in most inland catchments; high loads near urban/sewage sources and in intensive farming areas.
  - Phosphorus: agriculture dominant in about 79% of inland catchments; soil type and drainage influence losses.
  - Sediment: agriculture dominant in about 66% of inland catchments; bank erosion and rainfall/under-drainage influence hotspots.
  - FIOs: sewage-related sources dominate in many catchments; agriculture dominates in about 71% of inland catchments.
- Agricultural vs non-agricultural contributions by land use:
  - Arable land often contributes large shares of NO3 and P due to intensive input/use and drainage.
  - Grassland and rough grazing show different patterns, with methane largely linked to stocking density and enteric emissions.
  - Non-field areas (yard/housing, storage, tracks) contribute meaningfully, especially for FIOs and methane under certain practices.

## Modelling framework and data architecture

- Integrated Framework Model:
  - Combines multiple process models (e.g., PSYCHIC for P/sediment; N-CYCLE/NITCAT for N; MANNER for N emissions; IPCC-based GHG factors; FIO-FARM) into a unified, auditable framework.
  - Outputs are spatially explicit by pollutant, source area, and delivery pathway (surface runoff, leaching, drainage, air).
- Data inputs and spatial framework:
  - Geography: Scotland-wide, with emphasis on inland Priority Catchments; outputs disaggregated by farm type and land cover.
  - Climate/Soils/Land use: 1961–1990 climate surfaces; Scottish soils knowledge base; land cover maps; farm-type classifications (nine Robust Farm Types).
  - Connectivity: enhanced field-to-watercourse linkage, including within-field transmission, boundaries, drainage, and boundary-type effects.
  - Farm management data: detailed assumptions on cropping, livestock calendars, manure/fertiliser use; JAC data disaggregated by farm type.
  - Non-agricultural inputs: urban/rural runoff, bank erosion, roads, septic/sewage, montane/woodland sources modeled to close the pollutant budget.
- Outputs and interpretation:
  - Scenario testing for policy uptake and mitigation actions (e.g., buffer strips, manure relocation, fertiliser timing).
  - Attribution via a source-apportionment coordinate system to identify key sources, areas, and pathways.
  - Verification against measured data and harmonised monitoring datasets.

## Verification, validation and data governance

- Verification against measured data:
  - Sediment, nutrients, and FIO comparisons with large-catchment data; use of retention models for in-channel processes (Behrendt & Opitz for N/P; Vanoni for sediment).
  - OSPAR-COM data (HMS network, 56 catchments) used for distance-to-sea loads; a flow-weighted correction factor (0.6) applied to SPM to account for organic matter, enabling fair comparison with mineral sediment in the model.
  - Nitrate and phosphorus loads show good correlations with r2 ≈ 0.67 (nitrate) and 0.74 (phosphorus); sediment correlation weaker (r2 ≈ 0.41) with systematic over/under-predictions in some catchments.
- FIOs validation:
  - Comparison with Kay et al. (2008) and Tetzlaff et al. (2012) in Scotland and northeast Scotland; modelled loads generally exceed base-flow observations but align with high-flow patterns in urban vs rural contexts.
- GH(G) verification:
  - Agricultural N2O and CH4 compared to official Scottish inventories; differences largely due to method differences (FracLeach assumptions, slurry management, soil compaction, and waterlogging impacts) and livestock housing assumptions.
  - Compaction/poaching can raise N2O by ~30%, leading to higher total N2O relative to inventory; methane increases largely tied to slurry management and housing time.

## Agricultural and non-agricultural pollutant components

- Agricultural emissions:
  - Nine farm types drive emissions; footprints highest for dairy (except FIOs) due to high stocking density and fertiliser use.
  - Arable land often shows higher nitrate and phosphorus footprints; sediment highest on arable due to bare soil over winter.
  - FIOs dominated by grazing excreta; methane dominated by enteric emissions (especially cattle).
  - Pathways: nitrate mostly leaching; phosphorus largely via soil and drains; sediment via runoff and drains; FIOs mainly via grazing/runoff.
- Non-agricultural emissions:
  - Urban roads and septic/sewage, montane woodland, bank erosion, and direct urban runoff contribute significantly, especially for FIOs and phosphorus/sediment transport.

## Data challenges and considerations for Data Leaders

- Data integration and standards:
  - Harmonising inputs from many models with different formats; ensuring strict provenance and traceability across the Framework Model.
- Uncertainty and variability:
  - Emission factors (IPCC-based) carry wide ranges; Scotland-specific adjustments needed but add uncertainty.
  - Bank erosion modelling is site-specific and non-deterministic; calibration relies on limited data.
- Data gaps and non-agricultural loads:
  - Non-agricultural sources are substantial; necessary to attribute loads accurately while maintaining policy relevance.
- Geographic and temporal resolution:
  - 1 km2 grid; monthly to annual timescales; reconciliation with RBMP reporting requires careful aggregation.
- Data governance and collaboration:
  - Cross-agency data sharing, consistent metadata, and agreed coordinate systems essential for reproducibility and cross-project comparability.

## Key takeaways for Data Leaders

- Build and maintain a cohesive, auditable data pipeline that integrates climate, soils, land use, farm management, and policy uptake into a single Framework Model.
- Ensure data provenance, metadata, and versioning across all models (PSYCHIC, N-CYCLE, MANNER, NEAPN, IPCC-based components) to support scenario testing and policy evaluation.
- Prioritise data standardisation and interoperability to enable scalable, spatially explicit pollutant load calculations across river basins and future scenarios.
- Invest in thorough verification: align model outputs with harmonised monitoring data and account for non-agricultural sources to enable robust policy interpretation.
- Use the source-coordinates framework to attribute mitigation actions to specific pollutant sources and pathways, supporting targeted interventions and transparent reporting.