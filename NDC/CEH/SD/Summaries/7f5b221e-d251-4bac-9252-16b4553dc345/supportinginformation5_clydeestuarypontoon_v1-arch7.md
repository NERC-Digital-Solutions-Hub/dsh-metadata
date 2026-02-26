# Supporting information Clyde Estuary greenhouse gas and physio-chemical water properties: Estuary Transect measurements - 2021-2022

- Scope
  - Measurements of greenhouse gases (CO2, CH4, N2O) and physio-chemical water properties in the Clyde estuary, Scotland.
  - Sampling across tidal cycles at the Braehead pontoon location, August 2020 to May 2022, over 7 survey events (CEP1–CEP7).

- Study objectives (main)
  - Quantify sources, concentrations, fluxes and sinks of GHGs; compare anthropogenic and natural sources.
  - Develop a model of controls/mechanisms for GHG production, transport, consumption and release to atmosphere.
  - Identify conditions (tidal regime, stratification, temperature, river flow) that regulate active sources and sinks.

- Specific objectives for this portion
  - Determine how tidal-cycle changes (water depth, salinity, stratification, flow) affect water quality and GHG generation.

- Site description and data context (GIS relevance)
  - Location: Braehead pontoon, inner Clyde estuary, ~7.9 km from the tidal weir (fresh vs. saltwater influence); coordinates provided.
  - Environment: estuary dredging activity; depth ranges 3–7 m at measurement site; extended to >15 m in the main channel.
  - Sampling design: seven survey dates; both ebb and flood tides represented; surface and near-bed samples (0.2 m below surface and ~0.5 m above bed for near-bed samples).

- Data collected (variables and units)
  - GHG concentrations: CO2, CH4, N2O in water; CH4 and CO2 evasion rates; CH4, CO2, N2O partial pressures (in air and water saturation metrics, µatm or as % saturation; CH4 and CO2 evasion in mg m^-2 d^-1).
  - Physio-chemical water properties: conductivity (µS/cm), temperature (°C), pH, dissolved oxygen (mg/L and % saturation), turbidity (NTU), dissolved organic carbon (DOC), total dissolved carbon (TDC), dissolved inorganic carbon (DIC), total dissolved nitrogen (TDN-N, mg/L), nitrite-N (NO2-N), nitrate-N (NO3-N), ammonia-N (NH4-N), total phosphorus (TP), SUVA254 (L mg-C^-1 m^-1).
  - Data format: measurements compiled in a CSV with explicit units; missing values marked with an asterisk where applicable.
  - Sampling regime details: headspace gas sampling from water using syringes; ambient air samples; replicate measurements for gas analyses; filtration and subsampling for chemical analyses; turbidity and other parameters measured in situ or in-lab.

- Analytical methods (techniques and instruments)
  - Gas analysis: Agilent 7890B GC with headspace auto-sampler for CO2, CH4, N2O.
  - Total organic carbon and related metrics: Shimadzu TOC-L analyzer; filtration with GF/F filters.
  - Nitrogen/phosphorus: SEAL AQ2 analyzer for NO2-N, NO3-N, NH4-N, TP after appropriate sample preservation and digestion.
  - UV/Vis spectroscopy for SUVA254 (254 nm) to assess DOC aromaticity.
  - Turbidity: Thermo Scientific AQUAfast NTU meter.
  - Quality control: multiple mixed gas standards per run; calibration and running of standards for TDN, TDC, DOC, and SUVA; replicate measures.

- Gas exchange calculations (how concentrations were derived)
  - Headspace equilibration method to derive dissolved gas concentrations and partial pressures.
  - Mass-balance approach using liquid and gas volumes, temperature, barometric pressure, and Henry’s law solubility adjustments to compute in-water concentrations and gas-phase partial pressures.
  - Conversion to common units (ppmv) via the Ideal Gas Law.

- Important data notes and caveats
  - Some data gaps: missing values marked with an asterisk; CEP1 had surface sampling only (no near-bed data).
  - Dredging and depth sampling considerations may influence salinity stratification and mixing; depth sampling near the bed can be affected by disturbed bed or mixing events (noted in data comments).
  - Evasion measurements sensitive to wind/wave conditions; high wind not suitable for evasion measurements.

- Data provenance and authorship
  - Primary data collection and compilation by Alison Brown (IAPETUS 2 DTP, NERC) with support from Dr. Amy Pickard; photographic appendix by Alison Brown.
  - Acknowledgements include NERC funding and access permissions from Braehead site partners.

- GIS and data use implications for map-based products
  - Geographic context: precise latitude/longitude per sample; depth and tidal conditions captured, enabling time- and tide-aware mapping.
  - Potential map products:
    - Point maps of GHG concentrations and evasion at Braehead Pontoon over time, with tide phase as an attribute.
    - Time-enabled layers showing changes in dissolved gas concentrations and water properties across survey dates.
    - Attribute joins to longshore transects (CEP L6) and other estuary datasets to investigate spatial gradients when broader sampling data exist.
    - Maps correlating GHG metrics with salinity proxies, depth, and river flow to illustrate mechanisms of GHG production and release.
  - Data integration notes:
    - Data are primarily single-location per survey; when combining with multi-location transect data, treat as a fixed-point time series at a mapped location.
    - Ensure units and column definitions are preserved; the CSV includes a unit reference table to guide GIS attribute schema.

- References and further information
  - Supporting information and methods published alongside Clyde Estuary GHG studies; key methodological references include headspace equilibration calculations, standard gas concentrations, and water chemistry analysis methodologies.

- Appendix (contextual)
  - Sampling photographs and equipment illustrations relevant for spatial interpretation and site visualization.