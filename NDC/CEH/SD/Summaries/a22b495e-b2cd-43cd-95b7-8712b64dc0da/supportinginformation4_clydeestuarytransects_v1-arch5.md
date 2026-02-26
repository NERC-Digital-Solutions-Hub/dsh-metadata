# Clyde estuary greenhouse gas and physiochemical water properties: Measurements across the tidal cycles - 2020-2022

## Overview
- Longitudinal measurements of greenhouse gas (GHG) concentrations and physio-chemical water properties in the Clyde estuary, Scotland, collected by power boat.
- Eight surveys conducted during 2021–2022 under varying tidal, river flow, and seasonal conditions; measurements at ten locations (L1–L10) along a transect from the tidal weir to offshore.
- Surface and near-bed samples (approximately 0.2 m below surface to 0.5 m above bed) to understand GHG sources/sinks and associated mechanisms.

## Study objectives
- Quantify sources, concentrations, fluxes, and sinks of GHGs within the Clyde estuary; compare anthropogenic and natural sources.
- Develop a model of controls and mechanisms of GHG production, transport, and atmospheric release.
- Determine how stratification, salinity, flow, mixing, sediments, and known pollutant sources (e.g., urban wastewater) influence GHG dynamics and water quality along the estuary.
- Supplementary single-point surveys (7–13 hours) across tidal cycles published separately.

## Site description and data collection
- Ten sampling locations along the Clyde estuary (L1 near the tidal weir to L10 offshore from River Leven).
- Locations chosen to capture effects of salinity, river flow, stratification, and hydraulics; spacing increases seawards as estuary becomes more homogeneous.
- Sampling periods: eight transects from Sep 2021 to May 2022; some locations inaccessible in last surveys due to rough weather.
- Depths: maximum water depth sampled up to 12 m; shallower inland sites (L3 typically < 6 m).
- Sampling regime: start at high tide inland, move seawards with the ebb; surface samples collected in a 10 L bucket; near-bed samples collected with depth measurement and a sampler lowered to 0.5 m above the bed.

## Data collection regime and in-field measurements
- In-field measurements at the time of sampling included conductivity (EC), temperature (TW), dissolved oxygen (DO), DO saturation (DO%), pH, and turbidity (NTU) on surface samples; water depth measured prior to near-bed sampling.
- Triplicate dissolved gas samples collected using headspace method with ambient air samples; samples stored in sealed vials for laboratory analysis.
- Ambient air samples collected at roughly 1 m above the estuary surface for headspace analysis.

## Analytical methods
- GHG analysis: headspace GC (Agilent 7890B) with headspace autosampler for CO2, CH4, and N2O concentrations; calibration using mixed gas standards.
- Turbidity: Turbidity meter (AQUAfast) on unfiltered samples.
- Nutrients and carbon: filtered sub-samples analyzed for total dissolved nitrogen (TDN), total dissolved carbon (TDC), dissolved organic carbon (DOC), nitrite-N, nitrate-N, ammonia-N (via SEAL AQ2), and dissolved inorganic carbon (DIC). Total phosphorus (TP) measured after acid digestion and colorimetric orthophosphate determination.
- SUVA analysis: absorbance at 254 nm (SUVA254) via UV/Vis spectrophotometry to indicate aromaticity of DOC.
- Additional analyses: pH, nitrate/nitrite/ammonia, iron; absorbance used to infer DOC character and potential anthropogenic influence.

## Data structure and units
- Data captured in transect-specific datasets with variables including:
  - Location code (L1–L10), latitude, longitude, distance from tidal weir, inter-location gaps, sampling date, time (GMT), surface water temperature, tidal range, river flow at high tide.
  - Depth-related fields: water depth, sample depth (surface/near-bed).
  - Physical-chemical measurements: conductivity, temperature, pH, DO, DO%, turbidity.
  - Organic and inorganic carbon/nitrogen species: DOC, TDC, DIC, TDN, TP, SUVA254, ABS254.
  - Nitrogen species: NH4+, NO2-, NO3-, TN.
  - Gas-related metrics: CH4 and CO2 concentrations (and CH4-C, CO2-C), CH4 and CO2 saturations, pCO2 in air, gas partial pressures (CH4, CO2, N2O) in air; CH4 saturation in water; CH4 concentration (umol/L) and CH4-C (µg/L); CO2 concentration (umol/L) and CO2-C (µg/L); N2O concentration (µmol/L) and N2O-N (µg/L).
- Table 2 provides the detailed units for each parameter (e.g., Latitude/Longitude with 6 decimal places; depth in m; EC in µS/cm; Temp in °C; pH unitless; DO in mg/L; SUVA254 in L mg-C-1 m-1; gas concentrations in µmol/L or ppmv; partial pressures in µatm).
- Missing data indicated with an asterisk; incomplete sampling due to rough weather noted for CET7 (locations L5–L10) and CET6/CET8 (locations L9–L10) and CET3 at L10.

## Calculations and data processing
- Dissolved gas concentrations and partial pressures computed using a headspace equilibration mass-balance approach:
  - Co_liq and Co_gas related to equilibrated concentrations with volumes of liquid and gas in syringes.
  - Gas concentrations converted to μmol/L and further to ppmv using Henry’s coefficient, barometric pressure, and the ideal gas law.
- Partial pressures adjusted for atmospheric conditions to derive dissolved gas metrics (e.g., pCO2, pN2O).

## Data quality, limitations, and stewardship notes
- Data collected and processed promptly (same day or within a week for gas analyses); samples preserved and kept cold where applicable.
- Data completeness affected by weather; several transects partially missing as noted.
- Documentation includes: sampling locations (Table 1), sampling dates with conditions (Table 2), depth and measurement details (Table 3), and detailed methodology in the accompanying text and supplementary Appendix 1.
- Data are accompanied by acknowledgement of funding and institutional support; data are intended to support discovery and reuse by others, with potential uploading to data portals and catalogues; formal data governance (standards, metadata, provenance, versioning, licensing) should be applied to ensure long-term accessibility and interoperability.

## Data management and governance considerations for Data Stewards
- Metadata depth: ensure complete capture of location coordinates, survey codes, sampling depths, dates/times, tidal context, river flow data source, and instrument configurations.
- Standardization: align units and parameter naming with the Table 2/unit conventions to facilitate cross-dataset integration.
- Provenance and documentation: preserve links to the main publication and supplementary Appendix 1; maintain clear data lineage from field collection to laboratory analysis and final data products.
- Access, licensing, and sharing: define data access policies, licensing, and any embargo periods; provide a stable DOI or identifier for dataset versions; plan for regular updates if future surveys are added.
- Data quality assurance: maintain a QA checklist for field sampling, sample handling, instrument calibration, and lab analyses; include notes on weather-related missing data and any anomalies observed.
- Reuse guidance: dataset suitable for hydrological and biogeochemical modeling of GHG production, transport, and atmosphere exchange in estuarine systems; clearly document uncertainties and detection limits.

## Acknowledgements and references
- Funded by Natural Environment Research Council (NERC) through the IAPETUS Doctoral Training Partnership (Grant NE/S007431/1).
- Collaboration and support from UK Centre for Ecology & Hydrology; Kelvin Harbour access facilitated by the Tall Ship Glenlee Trust and Clyde Maritime Centre.
- References include methodological and contextual sources for headspace gas analysis, SUVA, nutrient analyses, and related estuarine studies.