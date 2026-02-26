# Supporting information Clyde Estuary greenhouse gas and physio-chemical water properties: Estuary Transect measurements - 2021-2022

- Study purpose and scope
  - Document the Clyde estuary transect measurements of greenhouse gases (CO2, CH4, N2O) and physio-chemical water properties collected during seven surveys between August 2020 and May 2022.
  - Aim to understand GHG sources, sinks, production/transport mechanisms, and how tidal cycle, stratification, temperature, and river flow modulate these processes.
  - Includes coordination with a secondary longitudinal transect survey (published by EIDC).

- Site and sampling design
  - Location: Braehead pontoon, Clyde estuary, Scotland (latitude 55.876932°N, longitude 4.360132°W).
  - Rationale: mid-estuary site with a salinity gradient; 7.9 km from the tidal weir.
  - Sampling frame: seven campaigns (CEP1–CEP7) spanning August 2020 to May 2022 to cover a tidal cycle; sampling times adjusted to capture ebb and flood tides.
  - Depth range at site: 3–7 m (surface to near-bed variability; estuary dredged in 2020).

- Sampling regime and data collected
  - Depths and depths of samples: surface approximately 0.2 m below surface; near-bed approximately 0.5 m above bed; surface and near-bed samples collected where possible.
  - Parameters measured in situ: conductivity (EC), temperature, dissolved oxygen (DO) and DO saturation, pH; turbidity.
  - Water samples for laboratory analysis: filtered and unfiltered subsamples for total dissolved nitrogen (TDN), total dissolved carbon (TDC), dissolved organic carbon (DOC), dissolved inorganic carbon (DIC), nitrite (NO2–), nitrate (NO3–), ammonia (NH4+), total phosphorus (TP); SUVA254 (absorbance at 254 nm) to assess aromaticity of DOC.
  - Gas measurements: headspace sampling for CO2, CH4, N2O concentrations; ambient air samples collected at ~1 m above the surface; three 200 mL syringes per sample for headspace equilibration.
  - Gas evasion measurements: CH4 and CO2 evasion rates obtained with a floating chamber (GGA) deployed ~2 m from the pontoon; triplicate measurements for ~3 minutes per time point (method chosen to avoid headspace saturation effects and minimize wind shielding).
  - Additional data: wind speed measured at 2 m above the pontoon to support evasion calculations.

- Analytical methods and instrumentation
  - Gas concentrations: Agilent 7890B GC with headspace autosampler for CO2, CH4, N2O; calibration with mixed standards in known concentrations.
  - Turbidity: Thermo Scientific AQUAfast turbidity meter.
  - Nutrients and DOC/DIC: filtration and analysis on day after collection; TOC-L for TDN, TDC, DOC; absorbance at 254 nm using UV/Vis spectrophotometer for SUVA254.
  - Nitrite, nitrate, ammonia: SEAL AQ2 analyzer; colorimetric and reduction-based methods; precautions for high salinity with potential interference on ammonia measurement.
  - Phosphorus: unfiltered TP quantified after acid digestion (K2S2O8) and colorimetric phosphate determination (molybdenum blue method).
  - Data handling: all samples run in batches with multiple standards; samples refrigerated and processed within 16–24 hours where applicable.

- Data calculations and units
  - Headspace gas data converted to liquid concentrations via a mass-balance approach and equilibrium assumptions (gas-liquid partitioning with temperature-dependent solubility).
  - Partial pressures in air and water computed; conversions to μmol/L and ppmv using the ideal gas law.
  - Gas evasion rates expressed as mg m−2 d−1 for CH4 and CO2.
  - Units and data structure aligned to a detailed CSV schema (see Table 1/Table 2 in the dataset): includes latitude, longitude, date, time (GMT), water depth, sample depth, conductivity (µS/cm), temperature (°C), pH, DO (mg/L), DO% saturation, turbidity (NTU), DOC (mg/L), TDC (mg/L), DIC (mg/L), TDN-N (mg/L), TP (mg/L), SUVA254, NH4+, NO2−, NO3−, TN, CH4, CH4-C, CO2, CO2-C, N2O, N2O-N, CH4(evasion), CO2(evasion), N2O(evasion), and comments (e.g., dredging or depth sampler notes).

- Data structure, quality, and caveats
  - Data availability: seven surveys with associated depth- and position-specific measurements across surface and near-bed environments; includes both water-column chemistry and greenhouse gas metrics.
  - Missing data: indicated in the CSV with an asterisk where data were not collected (e.g., CEP1 surface-only data at the near-bed).
  - Notable caveats:
    - Evaporation chamber measurements can be influenced by wind; low wind assumed for minimal shielding effects.
    - Chamber measurements may be affected by wind-driven waves; high wind conditions not suitable for evasion measurements.
    - Some samples near bed were not collected in CEP1 due to sampling constraints.
  - Data interpretation guidance: SUVA254 as an indicator of dissolved organic matter aromaticity and potential anthropogenic influence; nitrates and ammonia measurements can be affected by matrix effects at higher salinities.

- Data provenance and acknowledgments
  - Primary analysis and data handling conducted by Alison Brown as part of an IAPETUS 2 NERC-funded PhD project.
  - Funding: Natural Environment Research Council (NERC) through IAPETUS Doctoral Training Partnership (Grant No. NE/S007431/1).
  - Access and permissions: Braehead pontoon access facilitated by Intu SGS, Global Mutual, and Savills.
  - Related work: Estuary transect measurements published by the Environmental Information Data Centre (EIDC); supporting information cited for methods and data interpretation.

- Appendix and references
  - Appendix 1 includes sampling photographs of the Braehead pontoon, nearby dredging activity, and equipment.
  - References cover headspace equilibration methods, gas exchange calculations, and related estuarine chemistry literature.