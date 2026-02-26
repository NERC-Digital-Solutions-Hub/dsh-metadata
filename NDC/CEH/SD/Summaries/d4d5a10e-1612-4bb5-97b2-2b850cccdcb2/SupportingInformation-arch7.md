# Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution

## Executive overview
- The document quantifies national nutrient, sediment, and faecal indicator organism (FIO) emissions and compares model outputs to observed data.
- It presents spatial patterns, farm- and source-level apportionments, and the relative contributions of agricultural and non-agricultural sectors across Scotland.
- It includes validation against OSPAR-COM data, in-channel retention, and greenhouse gas inventories, with emphasis on spatially explicit GIS-ready outputs and scenario analysis for policy measures.

## National pollutant emissions (5.1.1) by sector
- Nitrate (N): Total 73.3 kt; agriculture >80% of total; sewage works (STWs) 7%; woodland 7%.
- Phosphorus (P): Total 2.47 kt; agriculture dominates (67%); STWs 18%.
- Sediment: Total load dominated by agriculture (68%); bank erosion 17%.
- FIOs: Agriculture contributes 31%; STWs 46%; septic tanks 21%.
- Comparison with earlier SNIFFER tool shows differences mainly due to methodology (e.g., STW coverage, bank erosion inclusion, and leaching factors).

## National greenhouse gas emissions (5.1.2)
- Nitrous oxide (N2O): Agriculture 4,775 kt CO2-e; total across sectors 5,539.9 kt CO2-e.
- Methane (CH4): Agriculture 3,154 kt CO2-e; total across sectors 5,770.1 kt CO2-e.
- Agriculture accounts for about 86% of N2O and 55% of CH4 in Scotland; total GHG using project agriculture outputs plus other sectors from official inventory ≈ 53.9 Mt CO2-e.
- Net takeaway: agriculture is a major N2O contributor and a sizable CH4 contributor within the national GHG budget.

## Spatial variation and sector dominance (5.1.3)
- Nitrate loads per catchment: other point sources ( septic tanks, STWs) concentrated along rivers; agriculture dominates inland catchments (50%+ of total in 91% of inland catchments).
- Phosphorus: similar spatial pattern to nitrate; agriculture dominates inland catchments (79%).
- Sediment: non-agricultural diffuse sources (e.g., bank erosion) contribute notably in some catchments; agriculture dominates 66% of inland catchments.
- FIOs: urban areas drive high loads; agriculture dominates inland catchments (71%), but point sources and urban diffuse sources are prominent in others.
- Spatial patterns for N2O and CH4 in agriculture reflect stocking density and land use intensity (N2O also influenced by fertiliser practices).

## Agricultural emissions and farm-type footprints (5.2)
- Nine representative farm types (e.g., Dairy, Cereals, General Cropping, Pigs, Poultry, LFA and Lowland Cattle & Sheep, Mixed, Horticulture).
- Footprints by farm type show:
  - Dairy farms typically have the highest footprints for most pollutants (due to high stocking densities and fertiliser use), except FIOs where cattle/pig manure patterns matter.
  - LFA cattle & sheep farms have relatively low footprints (less intensive).
  - Arable land tends to drive higher nitrate and phosphorus losses; rough grazing and grassland impact FIOs and methane differently.
- Air- and water-borne pathways differ by farm type:
  - Nitrate: soil leaching dominates arable lands; fertiliser and manure also important.
  - Phosphorus: soil and drainage pathways dominate; surface runoff and preferential flow are key pathways.
  - Sediment: runoff and preferential flow linked to drainage patterns; arable land shows strong drainage-related transport.
  - FIOs: grazing Excreta dominate, especially in grassland systems.
  - Methane: mainly enteric emissions; non-field sources account for substantial methane in some farm types.
- Spatial apportionment by source area and source type demonstrates:
  - Soil stores and leaching major nitrate sources in many land uses.
  - Phosphorus losses strongly tied to soil and drainage pathways.
  - Non-field areas (yards, housing, tracks) contribute variably, with some farm types showing substantial emissions from manure storage.

## Source and pathway apportionment (Tables 5.2.x)
- Nitrate: arable soils (56% soil), leaching (69%), fertiliser (21%), manure (21%), excreta at grazing (14%).
- Phosphorus: soil-driven (74%), surface runoff and drainage paths (approx. 44–48%), with soil contributions strongest; fertiliser and grazing pathways also present.
- Sediment: surface runoff dominant (56%), with significant contributions from drainage pathways.
- FIOs: excreta at grazing dominates (about 87–95% depending on land use); urban and other diffuse sources contribute less.
- Non-field areas (yards/housing, tracks/for ds, etc.) contribute variably, often with high shares in methane and FIOs due to livestock presence and manure handling.
- Pathways: surface runoff, leaching, preferential flow, and direct deposition are differentially important across land uses and pollutants.

## Non-agricultural pollutant modelling
- Includes urban roads, montane/woodland runoff, bank erosion, septic tanks, and sewage effluents.
- Bank erosion and urban diffuse sources are significant for sediment and FIOs in some catchments.

## Mitigation actions and effects (framework around 5.2 and 5.1.3)
- Actions mapped to auditable on-farm practices (e.g., relocate manure heaps, buffer strips, timing/rate changes).
- Each action has:
  - Effectiveness (P): theoretical maximum reduction under optimal conditions.
  - Applicability (A): proportion of source area where action can be applied.
  - Efficiency (E): adjustment for local constraints (slope, land type, etc.).
- Net effect of multiple actions uses multiplicative logic with overlap and area-adjustment:
  - For action i: R_i = P_i × E_i; combined effects account for overlaps and partial uptake.
  - If actions cover all source areas: N = 1 − product(1 − R_i); partial coverage uses area-weighted overlap logic.
- Local modifiers (soil compaction, poaching, waterlogging) adjust emissions; these modifiers are integrated to reflect condition-specific changes in runoff and emission factors.

## Soil compaction, poaching and waterlogging (4.4)
- Condition-specific multipliers modify runoff, infiltration, and emissions (notably N2O) in affected areas.
- Waterlogging increases surface runoff and can raise N2O; methane uptake effects are discussed but secondary to main pathways.

## Verification and validation (6)
- 6.1 OSPAR-COM data:
  - Uses HMS network measurements and river flows; SPM data corrected with a factor of 0.6 to align with mineral sediment modeled.
  - Comparison covers 56 HMS catchments; adjustments made to enable fair comparison with modeled outputs.
- 6.2 Faecal indicator organisms (FIOs):
  - Comparisons with Kay et al. (2008) for base and high-flow conditions; Tetzlaff et al. (2012) for Dee and North Esk catchments.
  - Model generally overestimates high-flow and underestimates base-flow in some cases; urban catchments show higher relative loads.
- 6.3 Nitrous oxide and methane:
  - Uses a modified IPCC approach; differences with official inventories stem from leaching fractions and Scotland-specific livestock management assumptions.
  - Including soil compaction, poaching, and waterlogging increases N2O relative to inventory by ~30%; methane from cattle manure shows notable differences due to slurry management assumptions.
  - Overall comparison shows notable but explainable deviations due to methodology and Scottish farming practices.

## Geospatial data considerations and outputs (GIS-focused)
- Outputs are spatially explicit loads by water body, disaggregated by farm type and land cover.
- Provides footprints of individual pollutants with source-type, source-area, and delivery-pathway breakdowns.
- Scenario results illustrate reductions from mitigation actions, suitable for GIS mapping and policy planning.
- Data layers include land cover, farm types, boundary permeability, connectivity index, drainage/soil conditions, and water body associations.
- Scale: 1 km2 grid with catchment-level aggregation aligned to WFD reporting units; Scotland-wide with emphasis on Priority Catchments and Operational Areas.

## Data sources, scale, and uncertainties
- Uses national datasets: June Agricultural Census (JAC), Strategi land cover, JAC parish-level allocations, CEH LCM 2007, boundary datasets, and farm-type distributions.
- Resolution: 1 km2 with catchment-level aggregation; outputs designed for GIS-based decision support.
- Uncertainties acknowledged: emission factors (IPCC-based with region-specific adjustments), boundary permeability estimates, bank erosion calibration, and data gaps in non-agricultural inputs.

## End-user relevance for GIS Specialists
- Provides a rigorous, spatially explicit framework to map diffuse pollution sources and mitigation effects across Scotland.
- Enables querying by source coordinates to assess mitigation effectiveness for specific fields, land uses, or water bodies.
- Supports scenario planning and visualization of policy impacts on river water quality within GIS environments.
- Delivers an auditable integration of farm management data, land cover, soils, climate, and hydrology into map-based decision support.