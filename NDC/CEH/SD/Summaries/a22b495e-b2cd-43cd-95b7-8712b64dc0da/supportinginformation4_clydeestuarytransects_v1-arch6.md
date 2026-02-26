# Supporting information Clyde Estuary greenhouse gas and physio-chemical water properties: Measurements across the tidal cycles - 2020-2022

## Data Overview
- Longitudinal measurement of greenhouse gas concentrations (CO2, CH4, N2O) and physio-chemical water properties in the Clyde estuary, Scotland.
- Eight surveys conducted during 2021–2022 under varying tidal, river flow, and seasonal conditions.
- Ten sampling locations along the estuary (L1 to L10), with measurements at the surface and near the bed to understand GHG sources/sinks and related mechanisms.

## Study Objectives
- Quantify sources, concentrations, fluxes, and sinks of GHGs in the Clyde estuary and compare anthropogenic vs. natural sources.
- Develop a model of controls/mechanisms for GHG production, transport, consumption, and atmospheric release.
- Determine how stratification, salinity, flow, mixing, and sediments along the estuary influence water quality and GHG generation; assess impact of known pollutant sources (e.g., urban wastewater).
- Complementary measurements include seven single-point surveys published by EIDC.

## Site Description and Data Collection
- Ten measurement locations (L1–L10) span from near the tidal weir to offshore, capturing transitions from freshwater to saline environments.
- Locations selected to reveal effects of salinity, river flow, stratification, and location on data interpretation; spacing increases seaward.
- The Clyde estuary is periodically dredged around L5; sampling sites placed off the main channel.
- Eight surveys (CET1–CET8) between Sep 2021 and May 2022; each survey sampled across locations, with depth context (surface ≈0.2 m below surface; near-bed ≈0.5 m above bed).
- Start at high tide inland and progress seaward on ebb; some locations unreachable in last surveys due to rough weather.
- Table 1 provides precise coordinates and positional context for L1–L10; Table 2 provides survey dates and conditions.

## Sampling Regime and Measurements
- Sampling by powerboat; surface samples collected in 10 L buckets; near-bed samples collected after depth measurement and a 30+ second submersion at 0.5 m above bed; duplicate/quality sampling avoided sediment disturbance.
- In-situ measurements at 10 cm below surface for conductivity, temperature, dissolved oxygen, DO saturation, and pH using portable meters and electrodes.
- Water samples for lab analysis collected in 2 L bottles and kept cool until processing.
- Dissolved gas samples collected in triplicate per location using headspace method, plus ambient air samples about 1 m above surface.
- Headspace method involves equilibration with three 200 mL syringes, high-speed mixing, and sealing into pre-evacuated vials.

## Analytical Methods
- Headspace gas analysis: Agilent 7890B GC with 7697A headspace autosampler; targets CO2, CH4, N2O; calibration with multi-gas standards.
- Turbidity: measured with AQUAfast turbidity meter on unfiltered samples.
- Filtration and sub-sampling: water filtered on site (GF/F 0.7 µm), sub-samples for TDN, TDC, DOC, nitrite, nitrate, ammonia, ions, and phosphorous; unfiltered samples retained for TP.
- DOC/TDN/TDC: measured with Shimadzu TOC-L; calibration with multiple standards; DIC derived from DOC-TDC.
- SUVA254: UV absorption at 254 nm to infer aromaticity of DOC; related to anthropogenic impact.
- Nitrogen and phosphorus species: NO2-, NO3-, NH4+ measured with SEAL AQ2; TP measured after acid digestion and colorimetric detection.
- pH, iron, and related parameters: measured and preserved according to standard protocols; potential ammonia interference noted at high salinity.

## Gas Calculations and Data Conversions
- Gas concentrations and partial pressures derived from headspace equilibration using mass-balance equations.
- Key relation: Coliq = Pgas × βT × PBAR + (Gas partial pressure adjustments), with βT as temperature-dependent Bunsen solubility and PBAR as barometric pressure.
- Concentrations converted to μmol/L and then to ppmv using the Ideal Gas Law (ppmv = μmol/L × R × T).
- Partial pressures reported for CH4, CO2, and N2O in the gas phase; CH4 and CO2 saturations and related metrics also provided.

## Data Structure and Units
- Data are organized in a CSV with standardized columns (e.g., Survey_Name CET, Location_Code L, Depth, Latitude, Longitude, Date, Time, Water_depth, Sample_depth, Cond, Temp, pH, DO, DO%, Turbidity, DOC, TDC, DIC, TDN, TP, ABS254, SUVA254, NH4, NO2, NO3, TN, TP, pCO2air, CO2, CH4, N2O, saturations, and related partial pressures).
- Units include: latitude/longitude (decimal degrees), distance (km), depth (m), conductivity (µS/cm), temperature (°C), pH (dimensionless), DO (mg/L), turbidity (NTU), DOC/TDN/TDC/TP (mg/L or mg/L equivalents), UV absorbance (m^-1), CH4/CO2/N2O concentrations (µmol/L), and partial pressures (µatm).
- Missing data indicated by asterisk markers in the CSV; specific gaps noted (see data notes).

## Data Quality, Gaps, and Limitations
- Some data not collected due to rough weather: CET7 (L5–L10), CET6 and CET8 (L9–L10), CET3 (L10).
- Overall data coverage varies by location and survey; Appendix notes provide detailed location-specific limitations.
- Data collection and analysis conducted by a multidisciplinary team; part of an IAPETUS 2 NERC PhD program.
- Data processed and analyzed with standard QA practices, with calibration against multiple gas standards and cross-checks through triplicate measurements.

## Data Management and Acknowledgements
- Data collected under NERC IAPETUS 2 DTP grant; laboratory and field support from UK Centre for Ecology & Hydrology and partner institutions.
- Photographic and site acknowledgements associated with specific sample locations.