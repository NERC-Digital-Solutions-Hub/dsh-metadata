# Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution

- National emissions (scotland, current practice)
  - Nitrate: total 73.3 kt; agriculture 60.1 kt (>80%); Sewage works 7%; woodland 7%.
  - Phosphorus: total 3.89 kt; agriculture 67%; sewage works 18%; others smaller.
  - Sediment: total (still) 1,685 kt; agriculture dominates 68%; bank erosion 17%.
  - Faecal indicator organisms (FIOs): agriculture 31%; sewage works 46%; septic tanks 21%.
  - Major comparison note: differences with the SNIFFER tool arise from differing treatment of STWs (population-based vs. discharges to fresh water) and methodology for bank erosion and leaching.

- National nitrous oxide and methane emissions (agriculture vs total)
  - Agriculture N2O: 4,775 kt CO2-e; Agriculture CH4: 3,154 kt CO2-e (current practice).
  - Relative to Scotland’s total GHG budget (53.9 Mt CO2-e): agriculture accounts for about 86% of N2O and 55% of CH4 within the agricultural sector; when integrated with non-agricultural sectors from official inventories, agriculture contributes about 3.1% of total CH4 and 4.8% of total N2O.
  - Overall, the model’s agriculture results are compared to official inventories to assess differences, including adjustments for soil compaction, poaching, and other factors.

- Spatial variation and sector apportionment (by catchment)
  - Nitrate: other point sources (septic tanks, STWs) cluster along central/eastern Scotland; agriculture dominates in most inland catchments (over 50% in 91% of inland catchments; over 90% in 45%).
  - Phosphorus: similar spatial pattern to nitrate; agriculture dominates in about 79% of inland catchments.
  - Sediment: other diffuse sources can be large; bank erosion contributes about 52% of other diffuse loads; agriculture dominates in 66% of inland catchments.
  - FIOs: urban centers drive the highest loads; agriculture dominates in 71% of inland catchments, though higher loads also occur in urban/semi-urban contexts.
  - Per-hectare patterns confirm agriculture generally more impactful in nitrate/phosphorus loads, with arable land showing particularly high nitrate/phosphorus intensities in some regions; upland areas show lower intensities.

- Agricultural emissions (footprints by farm type and land use)
  - Representative farm types: nine types (e.g., Dairy, Pigs, Arable, LFA cattle, etc.) with footprints calculated per farm type.
  - Dairy farms typically have the highest footprints for most pollutants (except FIOs), due to high stocking densities and fertilizer use.
  - LFA cattle and sheep farms show lower footprints due to extensive, low-intensity practices and larger rough grazing areas.
  - Land-use patterns: arable land often yields the largest nitrate/phosphorus/sediment footprints (despite only 12% of agricultural area), driven by intensive inputs; rough grazing and grassland footprints vary with stocking and drainage; non-field areas contribute variably, with methane being more linked to livestock location (roughly half the year on pasture).
  - Pollutant footprints by source and pathway show:
    - Nitrate: 41% from soil stores; 20% from fertiliser; 24% from manure; 14% from excreta at grazing; pathway emphasis on leaching (about 72% of nitrate losses via leaching).
    - Phosphorus: 74% from soil; 11% from fertiliser; drainage and runoff pathways split roughly 44% surface runoff and 48% preferential flow.
    - Sediment: surface runoff dominates (56%); notable contributions from under-drainage and runoff pathways.
    - FIOs: excreta at grazing accounts for about 95% of national FIO emissions; surface runoff is a major delivery pathway (about 87%).
    - Nitrous oxide: strong contributions from fertiliser and grazing excreta (roughly 32% each); other contributions from various forms; many N2O emissions linked to post-application and soil processes.
    - Methane: predominantly enteric (about 83% nationwide).
  - Form and pathway detail: phosphorus losses occur significantly as particulate phosphorus on arable lands; nitrate losses include substantial leaching from soils, especially on arable land with drainage; FIOs largely originate from grazing and manure in near-field areas; non-field areas (yards, storage) contribute variably, especially to FIOs and methane.

- Verification and data testing (Section 6)
  - OSPAR-COM comparison: Loads exported to UK marine areas are compared with HMS/GQA data from 56 HMS catchments; a correction factor of 0.6 applied to measured suspended solids to align with mineral sediment in the model.
  - In-channel retention: phosphorus and nitrate retention estimated with Behrendt & Opitz (2000) type models; sediment retention via Vanoni (1975) scaling with catchment area.
  - Model vs measurements (OSPAR-COM): phosphorus loads show good correlation (r^2 ≈ 0.74); nitrate loads also correlated (r^2 ≈ 0.67); sediment correlation weaker (r^2 ≈ 0.41); FIO comparisons with Kay et al. (2008) and Tetzlaff et al. (2012) show reasonable alignment but with known differences in base/high flow conditions and residence-time effects.
  - FIOs and catchment comparisons: Faecal indicator bacteria loads in Dee/North Esk show reasonable correlation (r^2 ≈ 0.38) but measured values often about half of modelled totals; base/high flow differences reflect methodological differences and retention effects.
  - Nitrous oxide and methane (GHG) verification: model vs official inventory shows notable differences due to methodology (FracLeach assumptions, soil compaction, waterlogging). Without mitigation actions, agriculture N2O is lower than inventory; with compaction effects included, N2O rises and can exceed inventory totals. Methane shows closer agreement, though livestock management assumptions (housing time, slurry emission factors) drive differences.

- Practical implications and use
  - The framework provides a quantitative means to assess the effectiveness of DP GBRs and other mitigation measures in reducing nitrate, phosphorus, sediment, and FIO emissions from agriculture.
  - Enables scenario analysis to identify actions and uptake levels needed to reach Good Ecological Status (GES) and informs policy decisions on uptake of mitigation actions.
  - Produces detailed pollutant footprints by farm type and catchment, enabling targeted interventions and cost-benefit considerations.
  - Supports cross-validation with observational data to calibrate and improve models and to understand regional variation and local scale requirements.

- Geographic and reporting scope
  - Focus: Scotland; cross-border Solway Tweed and Northumbria RBDs excluded.
  - Emissions estimated for all Scottish river water bodies, with emphasis on Priority Catchments and Operational Areas defined for RBMP cycles (draft 2015, 2021, 2027).

- Data foundations and methodology (high-level)
  - The analysis integrates climate, soils, land cover, and farm management data with a suite of process-based models (PSYCHIC, NITCAT, NCYCLE, NEAPN, MANNER, IPCC-derived GHGs, FIO models) to produce spatially explicit emission footprints.
  - Involves calibration against farm management data, national statistics (JAC 2010, SAPM, BSFP), and monitoring data; outputs are reconciled with monitoring networks and official inventories where possible.

- Core takeaway for analysts
  - The study provides a comprehensive, spatially explicit, farm-type–level accounting of agricultural and non-agricultural pollutant emissions in Scotland, linking management practices to environmental outcomes and enabling targeted policy interventions and robust scenario testing.