# Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution

## Overview
- Comprehensive Scotland-wide assessment of nutrient, sediment, and faecal indicator organism (FIO) emissions under current practices.
- Combines agricultural and non-agricultural sources to provide national totals and catchment-level footprints.
- Uses a detailed modelling framework to apportion emissions by source, area, pathway, and farm type, and to estimate impacts of mitigation actions.

## Data inputs and modelling framework
- Data sources and spatial framework
  - Nitrate, phosphorus, sediment, and FIO emissions modelled for Scotland (excluding cross-border catchments).
  - Inputs include farm-level data from representative farm types, land use, soils, climate, and hydrology; outputs are spatially resolved on a 1 km2 grid.
- Core modelling components
  - Process-based models driving an export-coefficients framework (Framework Model) for pollutant emissions.
  - Key models cover phosphorus/sediment balance (PSYCHIC), nitrate processes (NITCAT, NCYCLE, NEAPN), ammonia emissions (MANNER, NARSES), methane/nitrous oxide (IPCC-based with Scotland-specific adjustments), and faecal indicators (FIO-FARM).
  - Shared hydrology and delivery framework; explicit source apportionment by source type, area, pathway, form, and timescale.
- Farm-type representation and management data
  - Nine Representative Farm Types reflecting Scotland’s farming system (based on 2010 June Agricultural Census with expert adjustments).
  - Management workbooks capture livestock, manure storage, cropping, grazing calendars, and fertiliser timing/quantities.
  - Allocation of crops and livestock to farm types; spatial and temporal scheduling informs manure/fertiliser timing and pathways.
- Mitigation actions
  - Actions linked to measures (DP GBRs, NVZ, SRDP) with defined effectiveness, applicability, and efficiency.
  - Net effects from multiple actions combined multiplicatively; overlap accounted to avoid overestimation.
- Non-agricultural and GHG components
  - Non-agricultural diffuse sources (urban, roads, banks) and bank erosion integrated via additional export coefficients.
  - Greenhouse gases (CH4, N2O) evaluated against IPCC-based calculations with Scotland-specific adjustments.

## National emissions and sector shares (5.1.1)
- Nitrate, phosphorus, sediment, and FIOs total emissions for Scotland (present day/current practice)
  - Nitrate: total 73.3 kt; agriculture ≈ 60.07 kt N (dominant role).
  - Phosphorus: total 2.47 kt; agriculture ≈ 2.47 kt (dominant source, STWs ~18%).
  - Sediment: total 1,685 kt; agriculture ≈ 1,049 kt (bank erosion notable, 17% from bank erosion).
  - FIOs: total 2,020 ×10^9 cfu; agriculture ≈ 636 ×10^9 cfu (STWs dominant at 46%; septic tanks 21%).
- Cross-comparison with SNIFFER (2004)
  - Differences largely due to scope (SNIFFER population-based approach vs Scotland-only STW discharges to fresh waters) and methodological updates.
  - Notable difference: bank erosion contributes about 20% of sediment loads in this study (absent in the SNIFFER tool).

## National nitrous oxide and methane emissions (5.1.2)
- Agricultural N2O and CH4 calculated using a modified IPCC approach
  - Agriculture: N2O ≈ 4,775 kt CO2e; CH4 ≈ 3,154 kt CO2e (present practice).
  - Official inventory (Thistlethwaite 2010): N2O ≈ 4,188 kt CO2e; CH4 ≈ 2,967 kt CO2e.
  - Agriculture accounts for 86% of national N2O and 55% of national CH4; total Scotland GHG ≈ 53.9 Mt CO2e, with agriculture contributing ~3.1% of CH4 and ~4.8% of N2O.
- Comparative notes
  - Differences arise from treatments of soil compaction/poaching and indirect nitrogen leaching (FracLeach) assumed in inventory vs explicit calculations in this project.
  - Including compaction/poaching raises N2O by about 17% relative to inventory; methane emissions are sensitive to livestock housing assumptions and manure management.

## Spatial variation and sector apportionment (5.1.3)
- Nitrate
  - Other point sources (septic tanks, STWs) cluster along central/eastern Scotland rivers; loads >5 kg ha-1 in some sites.
  - 93% inland catchments have nitrate loads <0.5 kg ha-1; agriculture dominates the total in 91% of inland catchments (50%+ of total in 45%).
- Phosphorus
  - Spatial pattern similar to nitrate; phosphorus losses are strongly influenced by soil drainage and rainfall; agriculture dominates in ~79% of inland catchments.
- Sediment
  - Other diffuse sources can be large in some catchments; bank erosion contributes ~52% of the total other-diffuse sediment load; agriculture dominates in ~66% of inland catchments.
- FIOs
  - Urban and population-driven sources dominate central catchments; agriculture dominates 71% of inland catchments, with variability by land use.
- GHG spatial interpretation
  - Nitrous oxide and methane patterns primarily reflect stocking density and agricultural intensity, with en-route contributions from various source types.

## Agricultural emissions by farm type and land use (5.2)
- Farm-type footprints
  - Dairy farms often have the highest footprints for all pollutants except FIOs due to high stocking density and fertiliser use.
  - LFA cattle/sheep farms show the lowest footprints for nitrate, phosphorus, sediment, FIOs, and methane among livestock systems.
  - Arable land generally shows the highest nitrate and phosphorus footprints; rough grazing patterns show variable sediment losses due to drainage and rainfall.
- Land-use breakdown
  - Arable land: nitrate and phosphorus losses are high; soil is a major source for nitrate; preferential flow dominates phosphorus/sediment transport on arable land.
  - Grassland: significant FIOs mainly from grazing excreta; methane largely linked to enteric fermentation.
  - Rough grazing: lower nitrate but higher leaching on some pathways; sediment pathways influenced by drainage and rainfall.
  - Non-field areas (yards, tracks, manure storage) contribute variably, with methane and FIOs sometimes concentrated in these zones.
- Pathways and forms
  - Nitrate losses: soil source dominates arable (56%), leaching (groundwater) prominent; grassland leaching ~69% of nitrate losses from grass.
  - Phosphorus losses: soil/delivery via preferential flow is dominant on arable land; surface runoff and drains important (roughly 44–48% each).
  - Sediment: surface runoff dominates (56%); preferential flow important where drains exist.
  - FIOs: grazing excreta most important (around 95% nationally); manure storage/farmyards contribute less to direct waterborne loads.
  - Methane: largely enteric; methane emissions scale with stocking density.

## Verification, outputs, and reporting (Chapter 6)
- Data sources for validation
  - OSPAR-COM HMS data: measured loads from 56 catchments (2006–2010 average) used to compare with model outputs; adjustments for organic content in sediment.
  - In-channel retention: Behrendt and Opitz (phosphorus/nitrate) and Vanoni (sediment) retention models applied to account for downstream losses.
- Model-data comparisons
  - Phosphorus: strong correlation (r2 ≈ 0.74); under-prediction at low loads, over-prediction at high loads; agriculture dominant in ~40 of 56 catchments.
  - Nitrate: good correlation (r2 ≈ 0.67); some over-prediction in high-load catchments; agriculture dominant in most catchments.
  - Sediment: weaker correlation (r2 ≈ 0.41); over-predictions linked to catchments with high rough grazing.
- Faecal indicator organisms (FIOs)
  - Comparisons with Kay et al. (2008) show higher modeled loads than base-flow studies, with consistent relative patterns by land use; single-catchment Skews observed due to urban/point sources.
  - Dee and North Esk data (Tetzlaff et al., 2012) show reasonable correlation (r2 ≈ 0.38) but measurements often ~50% of modeled loads.
- Greenhouse gases verification
  - N2O and CH4 modeled vs official inventory (Thistlethwaite 2010)
  - Overall alignment, with notable differences mainly from housing/compaction assumptions and slurry management; compaction/waterlogging can raise N2O estimates significantly.
- End-to-end goal
  - Integrate evidence on mitigation rule compliance, farm management, and hydrology to quantify current and potential reductions in agricultural diffuse pollution and to inform policy and catchment-scale management in Scotland.

## Uncertainties and limitations
- IPCC emission factors carry wide ranges; absolute emissions carry uncertainty, though relative changes under mitigation are robust.
- Bank erosion and boundary permeability estimates rely on limited data with high variability.
- Connectivity/delivery modelling depends on boundary data quality and tile drainage classification.
- Some mitigation-action data restricted in public extracts due to sensitivity; overall outputs still reflect action-type effects and uptake estimates.

## End-to-end objective
- Quantify current and potential future reductions in agricultural diffuse pollution by integrating mitigation rule compliance, farm management practices, and hydrological processes to inform policy and catchment-scale management in Scotland.