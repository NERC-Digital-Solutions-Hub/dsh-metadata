# Data Overview

- Purpose: Measure greenhouse gas (GHG) concentrations and physio-chemical water properties over two years to understand GHG sources, sinks, and mechanisms in the River Clyde system.
- Scope: 26 locations across the River Clyde and major tributaries, plus 2 estuary locations, sampled from Jan 2020 to Dec 2021 (monthly; 21 campaigns due to Covid-19 restrictions).
- Aims:
  - Quantify sources, concentrations, fluxes, and sinks of GHGs (source-to-sea) and compare anthropogenic vs natural and land-use impacts.
  - Develop a model of controls and mechanisms for GHG production, transport, consumption, and transfer to the atmosphere.
  - Determine conditions under which different sources/sinks are active within the catchment, river, and estuary.

## Study design and site description

- Locations: 26 measurement sites along the Clyde catchment and its major tributaries, plus 2 Clyde estuary sites; sites span from near-source to Glasgow Green and estuary points.
- Site coding: Location codes indicate Clyde river (C), tributary (T), loch inflow (L), and estuary (E).
- Sampling strategy: Points aligned with SEPA gauging stations when possible; samples taken near entry points of tributaries; sampling between upper and lower catchment sections on consecutive days.
- Logistics: Samples collected monthly from river bank or bridges; where access was limited (snow, Covid), some locations were missed.

## Sampling and field measurements

- Water sampling: 10 L plastic bucket samples collected; analyses conducted on same day or shortly after.
- In situ measurements: Conductivity, temperature, dissolved oxygen (DO), DO%, and pH measured 10 cm below surface using portable meters.
- Gas sampling: Dissolved gas samples collected in triplicate using headspace method; ambient air samples collected at consistent heights; samples preserved in sealed vials.
- Handling: Water samples filtered in lab for chemical analyses; a portion preserved for later TOT analyses; processing aimed to minimize delay.

## Analytical methods and parameters

- GHG analysis: Headspace gas concentrations for CO2, CH4, and N2O measured with a GC (Agilent 7890B) and headspace auto-sampler; calibration with mixed standards; analyses run within one week of collection.
- Water chemistry: 
  - Filtration: Whatman GF/F; analyses for TDN, TDC, DOC via Shimadzu TOC-L; DIC derived from TDC–DOC; SUVA254 measured to assess aromaticity of DOC.
  - Ions: Ion chromatography (IC) for major anions/cations using a mixed standard; some samples were frozen/thawed; high Na can suppress NH4+ signals.
  - Phosphorus: Total phosphorus (TP) quantified after persulfate digestion using acid molybdenum blue colorimetry.
- Quality controls: Standards run with each batch; samples analyzed together per survey; some samples refrigerated or delayed due to logistics; data integrity cross-checked with time-series, spatial plots, and river flow data.

## Gas partial pressures and calculation framework

- Approach: Mass-balance calculations to derive dissolved gas concentrations and gas partial pressures from headspace equilibration data.
- Key relationships: Equilibria between liquid and gas phases, with gas concentration derived from partial pressures, solubility (βT), and barometric pressure; results converted to μmol/L and then to ppmv using the Ideal Gas Law.

## Data structure, units, and limitations

- Data format: Comprehensive CSV with standardized columns (survey name, location, sample code, latitude/longitude, date/time, depth, conductance, temp, pH, DO, DO%, DOC, TDN, TDC, DIC, TP, SUVA254, major ions, gas partial pressures, CH4, CO2, N2O etc.).
- Units: Detailed in Table 2; examples include µS/cm, °C, mg/L, µmol/L, and µatm for gas partial pressures.
- Missing data: Marked with an asterisk; several gaps noted due to weather (snow), Covid restrictions, or instrument limitations (e.g., DO measured only from Dec 2021; some ammonium data affected by high sodium).
- Data notes: Some sites had incomplete data early in the study; certain estuary measurements may be affected by high salinity and urban inputs, complicating NH4+ data.

## Quality control and data governance

- Field and lab QC: Regular instrument checks; use of multiple standards; cross-checks with hydrological data (river flow) to assess outliers and non-stationarity.
- Data handling: Suspect data removed and flagged with asterisk; emphasis on consistent processing across the two-year survey.

## Acknowledgements and references

- Funding: Natural Environment Research Council (NERC) through the IAPETUS Doctoral Training Partnership (Grant No. NE/S007431/1).
- Access acknowledgments: Glasgow City Council (Govan pier), Braehead pontoon access.
- Key references: Methods for dissolved gas estimation, gas exchange, DOC/SUVAs, and standard analytical techniques cited in the document.

## Appendix and site visuals

- Appendix 1: Detailed sample locations with coordinates, distances, and site descriptions; photos included for each site.
- Site-level context: Descriptions highlight land use (semi-natural to urban), proximity to wastewater treatment plants (UWWTP), gauging stations, and potential pollution sources (e.g., outfalls, mining inflows).