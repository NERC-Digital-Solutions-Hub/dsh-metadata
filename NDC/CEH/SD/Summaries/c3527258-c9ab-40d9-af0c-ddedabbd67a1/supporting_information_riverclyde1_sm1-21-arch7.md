# River Clyde GHG concentrations and physio-chemical water properties (January 2020 - December 2021)

- Purpose for GIS use
  - Create map-based data products to understand GHG sources/sinks and associated water chemistry across the Clyde catchment.
  - Support policy, client, and public-facing visualisations of spatial patterns and temporal changes.

- Scope and dataset overview
  - 26 locations along the River Clyde and major tributaries, plus 2 estuary locations (E27, E28).
  - Sampling period: Jan 2020 – Dec 2021; 21 campaigns (monthly sampling but COVID-related hiatus Apr–Jun 2020).
  - Headspace gas measurements for dissolved gases (CO2, CH4, N2O) with partial pressures; corresponding gas concentrations converted to μmol/L and ppmv.
  - Water chemistry and physico-chemical properties: conductivity, temperature, DO, DO%, pH; DOC, TDN, TDC, DIC, TP, SUVA254; major ions (Cl-, NO3-, SO4-, Na+, NH4+, K+, Ca2+, Mg2+); NH4+ detection limitations in high-sodium contexts.
  - Spatially explicit data enriched with site coordinates (WGS84), site codes, sampling dates, and depth information.

- Study objectives (GIS-relevant)
  - Quantify GHG sources, fluxes, and sinks entering the Clyde (source-to-sea) and compare anthropogenic vs natural/semi-natural/urban impacts.
  - Develop a mechanistic model of GHG production, transport, and atmospheric release within the catchment.
  - Identify conditions under which different sources/sinks are active and produce spatially explicit insights for management.

- Site description and data collection (geospatial context)
  - Sampling locations distributed from near-source segments to Glasgow Green and major estuary inlets; locations aligned where possible with SEPA gauging stations.
  - Tributaries and major inflows sampled near entry points to the main river; estuary positions included.
  - Location code scheme: C = Clyde main river, T = tributary, L = loch inflow to Clyde, E = estuary.
  - Data products to GIS: a georeferenced point for each sampling event with associated attributes.

- Sampling regime (logistics for mapping time)
  - Samples collected in 10 L buckets from river banks or bridges; same-day filtration and processing.
  - Upper catchment (day 1) and lower catchment (day 2) sampling in each campaign.
  - Triplicate headspace gas samples collected for each location; ambient air samples also taken for calibration.

- Analytical methods (traceability and data integration)
  - Gas analysis: Agilent GC with headspace sampler; standards for CH4, CO2, N2O; results linked to gas standards.
  - Water analyses: filtration for DOC/TDN/TDC; TOC analyzer; SUVA254 from UV absorbance; IC for anions/cations; TP via colorimetric method after digestion.
  - Data processing includes calibrations, cross-checks, and consolidation of day 1/2 samples; some samples refrigerated or diluted; missing data flagged.

- Gas calculations and units (key GIS attributes)
  - Dissolved gas concentrations derived from headspace equilibrations using mass-balance equations and temperature-dependent solubility; concentrations expressed in μmol/L and converted to ppmv using the Ideal Gas Law.
  - Columns in the dataset include: pCH4, pCO2, pN2O (air phase partial pressures); CH4 Sat, CO2 Sat, CH4, CH4-C, CO2, CO2-C, N2O, N2O-N, etc.
  - Table 2 provides the mapping of parameters, column headers, and units for GIS-ready integration.

- Data quality and caveats (data governance for maps)
  - Missing data flagged with an asterisk; several gaps due to weather, access, or methodological limitations.
  - DO measurements started December 2021; NH4+ measurements can be confounded by high Na+ in some urban/industrial-impacted sites.
  - Some samples may have been diluted or affected by lab conditions; outliers and suspect data removed and flagged.

- Appendix 1: Sample locations (geospatial metadata)
  - Detailed coordinates and descriptions for each sampling site (sample codes like L1-T-RCRoger Clench, etc.), plus photos and site notes.
  - Location coding and positional context support precise GIS mapping and network analysis.

- Practical GIS workflow implications
  - Create a point shapefile/GeoJSON with fields: location_code, sample_code, latitude, longitude, date_sampled, time_gmt, depth_m, cond_uS_cm, temp_C, pH, DO_mg_L, DO_percent, TDN_mg_L, TDC_mg_L, DOC_mg_L, DIC_mg_L, TP_mg_L, SUVA254, Cl_umol_L, NO3_umol_L, SO4_umol_L, Na_umol_L, NH4_umol_L, K_umol_L, Ca_umol_L, Mg_umol_L, pCH4_air, pCO2_air, pN2O_air, CH4_umol_L, CH4_C_ug_L, CO2_umol_L, CO2_C_mg_L, N2O_umol_L, CH4_Sat_pct, CO2_Sat_pct, N2O_Sat_pct.
  - Build time-enabled layers to explore 2020 vs 2021 spatial patterns and seasonal shifts; link to a Clyde river network shapefile and SEPA gauge points for context.
  - Generate derived GIS metrics such as gas flux indicators, estuary vs river zone comparisons, and urban vs rural tributary influences.
  - Maintain metadata and data quality flags, preserve asterisk-missing indicators in the GIS attributes for transparent interpretation.

- Data provenance and references
  - Data collected under NERC IAPETUS 2 DTP with relevant acknowledgments; methodological references provided for gas exchange, SUVA interpretation, and analytical techniques.
  - Appendix and supplementary information contain site-level details for reproducibility and mapping.