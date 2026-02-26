# Data Overview

- Purpose and scope
  - Investigates mine water from legacy coal mines across the Midland Valley, Scotland, focusing on greenhouse gas (GHG) concentrations, physio-chemical water properties, metal concentrations, and carbon isotopes.
  - Aims to quantify sources, concentrations, fluxes and sinks of GHGs and heavy metals across 16 mine water outflows (MA1–MA16) and to assess treatment effects.

- Study area and timeline
  - 16 mine water outflows distributed from Lathallan Mill (MA1) in the northeast to Kames (MA16) in the southwest, spanning Fife, Central, Lothian, and Ayrshire coal fields.
  - Sampling conducted June 2022 to September 2022; included 4 treatment-system locations interspersed among the sites.

- Measured variables and data components
  - GHGs: CO2, CH4, N2O (concentrations and in-water saturations; partial pressures via headspace method).
  - Physio-chemical water properties: temperature, pH, conductivity, dissolved oxygen (DO) and DO saturation, major ionic species, dissolved carbon and nitrogen.
  - Metals: broad suite measured by ICP-MS (including Li, Be, B, Na, Mg, Al, Si, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, Ga, As, Se, Rb, Sr, Nb, Mo, Ag, Cd, Sb, Cs, Ta, Hg, Pb, U; some isotopes measured as indicated).
  - Organic carbon and nitrogen: total dissolved carbon (TDC), total dissolved nitrogen (TDN), dissolved organic carbon (DOC); dissolved inorganic carbon (DIC) inferred from measurements.
  - Isotopes: radiogenic carbon (Δ14C) and stable carbon (δ13C) for dissolved CH4 and CO2.

- Data collection and sampling methods
  - Direct outflow sampling was often not possible; water collected in 10 L buckets as near to outflows as feasible to minimize degassing.
  - GHG sampling used the headspace method with triplicate samples per location; ambient air samples collected for calibration.
  - For isotopes, 2+ mg of carbon per GHG required; 10–70 L of water processed; air stripped of CO2 prior to headspace sampling; careful handling to minimize degassing.
  - Samples for water properties collected at 10 cm below surface; conductivity, temperature, DO, DO%, pH measured in situ with a multi-parameter probe; additional bottle samples processed in lab.

- Treatment systems and sampling points
  - Four treatment locations sampled across treatment chains:
    - Cuthill (MA7): cascade, deep, reed, source, and outflow sampling points.
    - Kingshill (MA10): cascade, deep, reed, and outflow sampling points.
    - Mousewater (MA12): peroxide treatment with deep, reed, and outflow sampling points.
    - Pool Farm (MA11): peroxide treatment with source, deep, reed, and outflow sampling points.
  - Some sites had by-passes or maintenance affecting residence times (notably MA11 second reed pool bypassed during sampling).

- Data structure and units
  - Tables 3–5 (in CSV) cover:
    - Table 3: water physicochemical properties and GHG concentrations; location metadata; sample codes; coordinates; dates; and a comprehensive set of in-water measurements (Cond, Temp, pH, DO, DO%, TDC, DIC, TDN, chloride, nitrate, sulfate, Na, NH4, K, Ca, Mg, and gas partial pressures like pCH4air, pCO2air, pN2Oair; CH4/CO2 CH4Sat, CO2Sat, N2OSat, and CH4/CO2 concentrations in umol/L).
    - Table 4: ICP-MS metal concentrations with detailed metadata (location, date, filtration, element concentrations, RSDs, etc.).
    - Table 5: radiogenic and stable carbon isotope data for CH4 and CO2 (location, date, latitude/longitude, isotopic values, radiocarbon age, %Modern, etc.).
  - Units include: µmol/L for gas concentrations, µmol/L for most ions, mg/L for TDN/TDC/DOC/DIC, µmol/L for most ions, ppm/ppb for isotope-related measurements, and various table-specific fields described in the documents.

- Data quality and limitations
  - GHG measurements represent minimum concentrations due to possible outgassing from supersaturated waters and turbulence during sampling (e.g., at MA4, MA5, MA6, MA7, MA10, MA11).
  - Filtration and handling (e.g., filtration before TOC/ion analyses) can cause outgassing and potential underestimation of DIC and some dissolved gases.
  - Sample collection turbulence and near-surface degassing may introduce variability; care was taken to minimize degassing, but residual effects remain.
  - Data are complemented by notes on site geology and hydrological context to aid GIS integration and interpretation.

- GIS relevance and usage
  - Provides geolocated sample data (Latitude/Longitude) and site-level metadata (Location_Name, Location_Code, Location_Type) suitable for GIS mapping and spatial analyses.
  - Enables comparison of source vs. treatment-stage measurements and visualization of spatial patterns in GHGs, metals, and water chemistry across the Midland Valley.
  - Includes connections to treatment configurations (cascade vs. peroxide reed systems) for spatial planning, impact assessment, and policy/science communication.

- Acknowledgements and references
  - Funded by NERC through IAPETUS Doctoral Training Partnership; radiocarbon isotope work supported by NEIF.
  - Access supported by the Coal Authority and Severn Trent Services; collaborators acknowledged.

- How to use the data
  - Integrate CSV Tables 3–5 with GIS layers for sample locations, treatment infrastructure, and geology.
  - Use coordinates to plot sample points and create time-series or site-comparison maps of GHGs, metals, and ionic chemistry.
  - Leverage isotopic data to infer CH4 and CO2 origins and changes across environments and treatment stages.
  - Consider data caveats (outgassing, turbulence) when interpreting concentrations; report minimum concentrations where applicable.