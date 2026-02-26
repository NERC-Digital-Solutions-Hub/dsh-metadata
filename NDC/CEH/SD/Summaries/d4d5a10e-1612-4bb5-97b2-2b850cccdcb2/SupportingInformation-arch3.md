# Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution

- Purpose and scope
  - Describes a modular, spatially explicit modeling framework to quantify how agricultural and non-agricultural measures affect nutrient, sediment, and faecal indicator organism (FIO) emissions, and how these relate to Water Framework Directive (WFD) objectives.
  - Aims to enable policy evaluation, inform future decisions, and support scoping of additional mitigation measures.

- Framework architecture and data
  - Integrates non-field and agricultural pollutant modelling to produce annual emissions for nitrate, phosphorus, sediment, and FIOs across Scotland.
  - Outputs are disaggregated by pollutant, representative farm type, source coordinates, and delivery pathways; includes non-field sources and, where relevant, in-channel retention.
  - Spatial reporting units focus on inland water bodies and coastal waters in Scotland; data inputs span climate, soils, land cover, farm structure, and movement/transfer pathways.
  - Source apportionment coordinates link emissions to specific farm activities and locations to avoid double counting across actions.
  - Includes both agricultural and non-agricultural pathways (e.g., soil, fertiliser, manure, grazing, surface runoff, drains, urban/sewage sources, bank erosion).

- National pollutant loads (5.1.1)
  - Nitrate total: 73.3 kt; agriculture >80% of total; STWs and woodland also contribute notably.
  - Phosphorus total: 2.47 kt; agriculture dominant (67%); STWs next (18%).
  - Sediment total: dominated by agriculture (68%); bank erosion (17%) significant.
  - FIOs total: agriculture 31%; STWs 46% and septic tanks 21% are major non-agricultural sources.
  - Comparison with SNIFFER Screening Tool shows differences due to scope and methodology (e.g., bank erosion, STW coverage).

- National greenhouse gas emissions (5.1.2)
  - Agriculture emits 4,775 kt CO2-e from N2O and 3,154 kt CO2-e from CH4 under current practice.
  - Official inventory figures are 4,188 kt CO2-e (N2O) and 2,967 kt CO2-e (CH4); differences reflect methodology and mitigation action inclusion.
  - Agriculture accounts for 86% of N2O and 55% of CH4 within the agricultural sector; when combined with other sectors, agriculture contributes 3.1% of total CH4 and 4.8% of total N2O to Scotland’s total GHG.
  - Total greenhouse gases (including carbon) estimated at 53.9 Mt CO2-e; agriculture contributes a modest share overall.

- Spatial variation of emissions (5.1.3)
  - Nitrate loads from non-agricultural sources (e.g., septic tanks, STWs) cluster along rivers; agriculture dominates in most inland catchments.
  - Phosphorus and nitrate patterns differ by pathway and rainfall/soil drainage: phosphorus strongly influenced by soil/drainage patterns; nitrate largely reflects livestock density and inputs.
  - Sediment loads show strong influence from agricultural practices but also bank erosion in certain catchments.
  - FIO loads concentrated in urban catchments and population centers; agriculture is dominant in many inland catchments but non-agricultural sources are important elsewhere.

- Agricultural emissions by farm type (5.2)
  - Nine representative farm types (e.g., Dairy, General Cropping, LFA Cattle & Sheep, Pigs, Poultry, etc.) with footprints for nitrate, phosphorus, sediment, FIOs, N2O, and CH4.
  - Dairy farms typically have the highest footprints for most pollutants due to stocking density and fertilizer use; LFA and rough grazing farms generally show lower footprints.
  - Arable land tends to drive higher nitrate and phosphorus losses (due to soil and drainage characteristics); arable land contributes a large share of national emissions despite occupying a smaller land area.
  - Non-field areas (yards, housing, manure storage, tracks) contribute variably by pollutant, with methane often strongly linked to livestock locations (high non-field contributions).
  - Source and pathway apportions show that:
    - Nitrate: soil, fertiliser, manure, grazing excreta; surface runoff is a key pathway (leaching dominates in some land uses).
    - Phosphorus: soil/delivery pathways; surface runoff and drains are dominant pathways (highly affected by drainage networks).
    - Sediment: runoff and drainage pathways predominate; arable lands show strong drainage-related transfers.
    - FIOs: mostly from grazing/excreta; some contribution from manure handling in certain farm types.
  - The framework allows detailed apportionment by source type and delivery pathway to support targeted interventions.

- Verification and validation (6)
  - Pollutant loads verified against OSPAR-COM data for 56 HMS catchments around Scotland; adjustments account for organic content in measured suspended solids (0.6 correction factor) and in-channel retention (Behrendt and Opitz for phosphorus; Vanoni for sediment).
  - Phosphorus: modeled loads correlate well with measured loads (r2 ≈ 0.74); some under-prediction at low loads and over-prediction at high loads; agriculture dominates in most catchments.
  - Nitrate: good correlation (r2 ≈ 0.67); some catchments show higher measured loads than modeled; agriculture dominates in most, with sewage works dominating a few.
  - Sediment: weaker correlation (r2 ≈ 0.41); higher measured values in catchments with substantial rough grazing; generally model over-predicts in some catchments.
  - Faecal indicator organisms (FIOs): comparisons with Kay et al. (2008) show higher annual loads in this project than base-flow estimates but consistent patterns by urbanization; Tetzlaff et al. (2012) show reasonable correlation (r2 ≈ 0.38) with field measurements.
  - Nitrous oxide and methane: project results compared with official GHG inventory (Thistlethwaite et al. 2010); differences explained by compaction/poaching effects, manure management, and FracLeach assumptions; overall, assessment highlights impacts of mitigation actions and differences in methodologies.

- Data governance and practical considerations
  - Some mitigation-action data are sensitive; not all action descriptions are publicly available.
  - Underlying data sharing and metadata considerations pose barriers; emphasis on quality assurance, data provenance, and transparent reporting.
  - Outputs are designed to support policy development and evaluation by SEPA, the Scottish Government, and researchers, with careful handling of data sensitivity and governance.

- Key takeaways for monitoring framework authors
  - A modular, spatially explicit, multi-model framework can quantify policy impacts on diffuse pollution.
  - Linking farm management data to pollutant pathways enables robust scenario testing and targeted interventions.
  - Explicit source apportionment coordinates help prevent double-counting across actions and support queryable analyses.
  - Verification against independent monitoring data is essential for credibility and policy relevance.
  - Data sensitivity and governance require careful management when sharing detailed mitigation-action data.