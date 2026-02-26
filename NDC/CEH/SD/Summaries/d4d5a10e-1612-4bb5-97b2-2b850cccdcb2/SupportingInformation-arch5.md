# Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution

## Overview and aims
- Quantifies contributions of rural diffuse pollution measures (DP GBRs, NVZ Action Programme, SRDP) to reductions in agricultural pollutant emissions to water.
- Supports River Basin Management Plans (RBMPs) by evaluating current and potential uptake and their impact on water quality objectives under the Water Framework Directive (WFD).
- Provides a spatially explicit framework to compare current practice with scenario-based uptake of mitigation actions.
- Highlights data governance implications for managing multi-source, multi-format datasets and ensuring reproducibility.

## Data inputs and provenance
- Climate: CRU 1961–1990 baseline surfaces via Met Office.
- Soils: James Hutton Institute’s SSK1B.
- Land cover/use: OS Strategi, 2010 JAC, CEH Land Cover Map 2007; parish-level consistency checks.
- Agricultural statistics: 2010 JAC, fertiliser data (BSFP), SAPM land-management assumptions; farm typology (nine representative farm types).
- Non-agricultural pollutant data: urban/road runoff, montane/woodland emissions, bank erosion, other diffuse sources.
- Verification data: Harmonised Monitoring Scheme (HMS) for 56 catchments; licensed point sources (septic tanks, sewage effluent).
- Data governance notes: diverse formats and scales; provenance, versioning, metadata critical; some mitigation-action details are sensitive and outputs rely on auditable mappings.

## Framework model and data integration
- Core models integrated within a single rule-based framework:
  - PSYCHIC for phosphorus, sediment, and water balance.
  - NITCAT, NCYCLE, NEAPN for nitrate.
  - MANNER and NARSES for ammonia and nitrogen management.
  - FIO-Farm for faecal indicator organisms (FIOs).
  - IPCC (Tier 1/2) for methane and nitrous oxide.
- All models share a common hydrology (PSYCHIC) and landscape connectivity; exports are in 1 km2 cells.
- Nine farm types with representative source areas and delivery pathways.
- Data lineage and disaggregation by farm type, source area, and pathway are built into a unified “source apportionment” coordinate system to attribute emissions.

## 5.1.1 National nutrient, sediment and FIOs emissions
- Nitrate: total Scotland ≈ 73.3 kt; agriculture ≈ 80%+ of nitrate emissions; STWs and woodland are other significant sources (~7% each).
- Phosphorus: total ≈ 2.47 kt; agriculture dominant ≈ 67% of load; STWs ≈ 18%.
- Sediment: total load ≈ 1,685 kt; agriculture ≈ 68%; bank erosion ≈ 17% as the next significant source.
- FIOs: agriculture contributes ≈ 31% of total FIO load; STWs ≈ 46%, septic tanks ≈ 21%.
- Cross-model comparisons show differences with earlier SNIFFER screening tools due to methodological differences (e.g., scope of STWs, handling of bank erosion, leaching assumptions).

## 5.1.2 National nitrous oxide and methane emissions
- Agriculture drives N2O ≈ 4,775 kt CO2-e and CH4 ≈ 3,154 kt CO2-e (current practice in this project).
- Official inventory values are close but not identical; agriculture accounts for about 86% of N2O and 55% of CH4 in Scotland’s total greenhouse gas budget.
- Total greenhouse gas emissions (including non-agriculture sectors) ≈ 53.9 Mt CO2-e; agriculture contributes ~3.1% of CH4 and ~4.8% of N2O.

## 5.1.3 Spatial variation in emissions and sector apportionment
- Nitrate: other point sources (septic tanks, STWs) cluster along central/eastern Scotland rivers; agricultural loads per ha of agricultural land are substantially higher, with hotspots in intensive dairying (SW) and arable areas (NE).
- Phosphorus: patterns similar to nitrate; under-drained and high-rainfall areas show high phosphorus due to drainage pathways.
- Sediment: other diffuse sources can dominate in some catchments; agriculture is the dominant source in about 66% of inland catchments.
- FIOs: urban areas drive high loads; agriculture is dominant in about 71% of inland catchments, with patterns influenced by rainfall and livestock density.
- Nitrous oxide and methane across landscapes: N2O linked to stocking density and intensity; CH4 linked to stocking density.

## 5.2 Agricultural emissions
- Nine representative farm types show variable pollutant footprints; dairy farms typically have the highest footprints for nitrate, phosphorus, and sediment due to high stocking densities and fertiliser use; LFA cattle/sheep farms show lower footprints.
- Land-use footprints:
  - Arable land often has the highest nitrate and phosphorus footprints due to drainage and inputs.
  - Grassland footprints reflect livestock density; FIOs and methane tied to manure and grazing patterns.
  - Rough grazing has comparatively lower nitrate/phosphorus footprints but can have notable leaching due to drainage.
- Pathways and source apportionment:
  - Nitrate: major leaching (about 72%); significant contributions from soil stores, fertiliser, and excreta at grazing.
  - Phosphorus: soil contributions dominate; surface runoff and drainage pathways are both important.
  - Sediment: runoff is the dominant pathway, with substantial drainage-related transfer.
  - FIOs: mostly from excreta at grazing via surface runoff; elevated in urban/inflow areas.
  - Methane: predominantly enteric emissions; nitrous oxide arises from fertiliser and grazing with notable contributions from soil and manure management.
- Non-field emissions (yards, housing, storage, tracks) are variably important across pollutants, but methane is often tied to livestock presence rather than on-field losses.

## 6 Verification of pollutant loads
- 6.1 OSPAR-COM data
  - Uses HMS and GQA networks to compare measured loads (nitrate, phosphorus, suspended solids) with model outputs for 56 HMS catchments.
  - Adjustment: apply a correction factor of 0.6 to measured suspended solids to align with mineral sediment outputs (organic matter removed).
  - In-channel retention: Behrendt & Opitz (phosphorus and nitrate) and Vanoni (sediment) models used to estimate retention from catchment to mouth.
  - Findings:
    - Phosphorus: good correlation with model (r2 ≈ 0.74); agriculture dominates in ~40 of 56 catchments.
    - Nitrate: strong correlation (r2 ≈ 0.67); agriculture dominant in all but 4 catchments (those dominated by STWs).
    - Sediment: weaker correlation (r2 ≈ 0.41); higher measured loads in some rough-grazing catchments; agriculture dominant in ~66% of inland catchments.
- 6.2 Faecal indicator organisms (FIOs)
  - Compared with Kay et al. (2008) across catchments; this project yields higher annual loads due to annual timeframe, retention in lakes, and die-off.
  - FIO outputs generally higher for urban/semi-urban/rural classifications than Kay et al. base-flow estimates; measured data from Tetzlaff et al. (2012) show reasonable correlation (r2 ≈ 0.38) but measured values are typically about 50% of model totals in North Esk/Dee catchments.
- 6.3 Nitrous oxide and methane
  - Comparison with official GHG inventory (Thistlethwaite et al., 2010) shows differences driven by methodology:
    - Without compaction/poaching, project N2O ≈ 90% of inventory; adding explicit leaching reductions reduces indirect N2O, bringing project totals closer to inventory in some components.
    - Compaction/poaching increases N2O by ~30%, pushing total ~17% above inventory.
    - Methane differences largely arise from livestock housing schedules and slurry emission factors; this project’s Scottish livestock management yields higher methane than the national inventory in some components.
  - Overall, project results illuminate where mitigation actions could impact GHG emissions and where inventory methods diverge due to assumptions about management practices.

## Data governance implications for Data Stewards
- Diverse data streams (climate, soils, land use, farm management, urban and forestry sources) require robust provenance, metadata, versioning, and auditable lineage.
- Some mitigation-action data are sensitive; outputs must map back to auditable action descriptions without exposing sensitive details.
- Reproducibility hinges on transparent disaggregation by farm type, source area, and delivery pathway; standardized data schemas across interconnected models are essential.
- Large, multi-source datasets and cross-model linkages demand careful data quality controls, documentation of transformations, and clear sharing agreements.
- Verification against external data (OSPAR-COM, HMS, Kay et al., Tetzlaff et al.) demonstrates the need for documented reconciliation methods and clear assumptions when aligning modeled outputs with observations.
- Practical data stewardship takeaway: this study provides a blueprint for maintaining a governed data pipeline from raw inputs to policy-relevant outputs, emphasizing metadata richness, data lineage, and auditable mappings to mitigation actions.

## Practical relevance for data stewardship
- Demonstrates the value of a tightly governed data pipeline from diverse inputs to integrated policy-relevant outputs.
- Highlights the necessity of robust metadata, data lineage, and auditable mappings when handling sensitive mitigation-action data.
- Provides a scalable blueprint for maintaining consistent data schemas across multiple models, enabling comparability and reproducibility in future policy analyses and RBMP cycles.