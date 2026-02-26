# Supporting information Clyde Estuary greenhouse gas and physio-chemical water properties: Estuary Transect measurements - 2021-2022

## Overview
- Dataset reports greenhouse gas concentrations (CO2, CH4, N2O) and physio-chemical water properties collected in the Clyde estuary, Scotland, along the Braehead pontoon during seven survey events from August 2020 to May 2022.
- Measurements span surface and near-bed depths across different tidal states to understand GHG sources/sinks, transport mechanisms, and responses to tidal regime, stratification, temperature, and river flow.
- Data complement separate eight longitudinal transect surveys published by EIDC.

## Study context and objectives
- Main Clyde estuary aims:
  - Quantify sources, concentrations, fluxes, and sinks of GHGs; compare anthropogenic vs. non-anthropogenic sources.
  - Develop a model of controls/mechanisms for GHG production, transport, consumption, and atmospheric release.
  - Determine activity of sources/sinks under varying conditions (tidal regime, stratification, temperature, river flow).
- Specific objectives for this dataset:
  - Assess how tidal-cycle changes (depth, salinity, stratification, flow) affect water quality and GHG generation.

## Site description
- Location: Braehead pontoon, middle of inner Clyde estuary, coordinates ~55.876932°N, 4.360132°W.
- Proximity to tidal weir (7.9 km): freshwater-saltwater interface; dredging ongoing at the survey period.
- Sampling position: outer side of the pontoon facing north; water depth ranges 3–7 m (tidal dependent).

## Data collection and sampling regime
- Sampling occasions: seven surveys (CEP1–CEP7) between Aug 2020 and May 2022.
- Depths: surface (~0.2 m below surface) and near-bed (~0.5 m above bed) samples; depth-based sampling decisions avoided sediment disturbance.
- Measurements at each survey:
  - In situ water properties: conductivity, temperature, DO, DO saturation, pH; turbidity.
  - Water chemistry: total dissolved nitrogen (TDN), total dissolved carbon (TDC), dissolved organic carbon (DOC), nitrite-N, nitrate-N, ammonia-N, total phosphorus (TP) in filtered/unfiltered samples; SUVA254; absorbance at 254 nm.
  - Gas sampling: headspace method for dissolved gas concentrations; ambient air samples collected at ~1 m above surface; three 200 mL syringes per sample for equilibration, with vials sealed for GC analysis.
  - GHG evasion: CO2 and CH4 evasion measured in triplicate for CEP6 and CEP7 using a floating chamber and gas analyser, noting limitations under wind/wave conditions.
  - Ancillary data: wind speed (2 m above pontoon), tide information, and river flow data from SEPA/UKCEH gauges for mid-survey timing.
- Data handling: samples processed the day after collection; atmosphere-water equilibration performed prior to GC analysis; all samples stored cool until lab processing.

## Analytical methods
- Gas analysis: concentrations of CO2, CH4, N2O determined by Agilent GC with headspace auto-sampler; calibration with mixed gas standards in each run.
- Turbidity: measured with AQUAfast turbidity meter.
- Water chemistry analyses (filtered and unfiltered as appropriate):
  - DOC, TDN, TDC, DIC via Shimadzu TOC-L with calibration standards.
  - Nitrite-N, nitrate-N, ammonia-N via SEAL AQ2; methods include colorimetric reactions and reductions; dilution for high concentrations.
  - Total phosphorus via alkaline persulfate digestion and colorimetry (molybdenum-blue) with four standards per run.
  - SUVA254 from UV-Vis absorbance at 254 nm (indicator of DOC aromaticity).
- Data processing: CH4, CO2, N2O concentrations and partial pressures calculated using headspace mass-balance equations; conversions to ppmv using the Ideal Gas Law; temperature-corrected solubility βT factors applied as per Wanninkhof references.
- Sample handling notes: some data marked as missing with an asterisk; CEB1 (Aug 2020) lacked near-bed data.

## Data products, variables, and units
- Data are presented in CSV format with explicit column headers and units (detailed in accompanying Table 1/Table 2 in the dataset documentation).
- Key variables include:
  - Spatial/temporal: Latitude, Longitude, Date, Time (GMT), Depth, Depth from surface.
  - Physical/chemical: Cond (µS/cm), Temp (°C), pH, DO (mg/L), DO% (%), Turbidity (NTU), DOC (mg/L), TDC (mg/L), DIC (mg/L), TDN-N (mg/L), TP (mg/L), ABS254, SUVA254.
  - GHGs: CH4 (µmol/L), CH4-C (µg/L), CO2 (µmol/L), CO2-C (mg/L), N2O (µmol/L), N2O-N (µg/L), CH4(evasion) mg/m2/d, CO2(evasion) g/m2/d, CH4 saturation (%), CO2 saturation (%), N2O saturation (%).
  - Gas concentrations in air: pCO2air (µatm) for CO2, pN2Oair (µatm) for N2O.
- Note on data gaps and caveats are included (e.g., bed sampling missing for CEP1; dredging-related mixing effects; potential biases in evasion measurements under wind/wave).

## Gas calculations and data interpretation
- Dissolved gas concentrations derived from headspace equilibrations using mass-balance equations and gas constants.
- Partial pressures converted to water/air concentrations; carbon units converted to ppmv via ideal gas law.
- Evasion rates derived from chamber measurements with time-limited intervals to avoid headspace saturation biases; wind speed and wave conditions acknowledged as factors affecting accuracy.

## Data quality, limitations, and QA
- QA considerations and potential biases:
  - Dredging activity may mix saline and fresh waters, affecting gas and nutrient distributions.
  - Bed samples sometimes unavailable (CEB1) or incomplete mixing in depth samplers.
  - Evasion measurements have limitations under higher wind and wave conditions; shielding effects deemed minimal but acknowledged.
  - Temperature-dependent solubility and headspace equilibration assumptions introduce uncertainty.
- Missing data flagged with asterisks in the CSVs; documentation specifies which parameters were not collected in certain surveys.

## Data availability and governance
- Data and supporting information published as part of the Clyde Estuary greenhouse gas and physio-chemical water properties project; associated with Estuary Transect measurements (2021-2022).
- Data hosted/documented through Environ. Inf. Data Cent. (EIDC) and linked publications, including Supporting Information and related transect datasets.
- Documentation provides detailed metadata, units, and descriptive notes to support reuse, interpretation, and reproducibility.
- Data stewardship and authorship acknowledged; data supported by NERC IAPETUS Doctoral Training Partnership and, for access, collaboration with Braehead pontoon operators.

## Acknowledgements and references
- Funding: Natural Environment Research Council (NERC) through IAPETUS Doctoral Training Partnership (Grant No. NE/S007431/1).
- Contributions: field access facilitated by Intu SGS, Global Mutual, and Savills; data collection led by Alison Brown with support from Dr. Amy Pickard.
- References include foundational methods for headspace gas analysis, dissolved gas calculations, and related environmental chemistry methodologies.