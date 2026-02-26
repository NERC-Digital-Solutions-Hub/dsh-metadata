# Data Overview

- Objective and scope
  - Investigates mine water from legacy coal mines across the Midland Valley, Scotland, focusing on greenhouse gases (GHGs), physio-chemical properties, metal concentrations, and carbon isotopes.
  - Aims to quantify origins, concentrations, fluxes, and sinks of CH4, CO2, and metals; assess changes across different flooded mine environments; evaluate treatment effects (oxidation, settling ponds, reed beds) on water properties and metal/GHG concentrations.

- Study design and locations
  - Sixteen mine water outflows (MA1–MA16) sampled across the Midland Valley, spanning Fife, Central/Lanarkshire, Lothian, and Ayrshire coal fields.
  - Sites include both untreated outflows and those with treatment systems.
  - Four treatment locations sampled along treatment pathways (two with cascade, two with peroxide): MA7 (Cuthill) and MA10 (Kingshill) as cascades; MA11 (Pool Farm) and MA12 (Mousewater) as peroxide systems.
  - Sampling occurred June–September 2022; site locations include detailed geographic and geological context.

- Data types and key measurements
  - Water properties and GHGs: conductivity, temperature, pH, dissolved oxygen (DO) and DO saturation, dissolved carbon species, and concentrations of CO2, CH4, and N2O; CH4 and CO2 are the main focus due to high source concentrations.
  - Dissolved inorganic and total carbon: TDC, DIC, DOC, TDN.
  - Ionic and metal concentrations: major cations/anions (e.g., Cl-, NO3-, SO4-, Na+, NH4+, K+, Ca2+, Mg2+) and a wide suite of metals measured by ICP-MS.
  - Carbon isotopes: radiogenic Δ14C and stable δ13C for dissolved CH4 and CO2.
  - Isotopes and gas data also include CH4 and CO2 concentrations in μmol/L, CH4-C and CO2-C, and gas saturation/partial pressures, plus partial pressures of CH4, CO2, and N2O in air.

- Sampling and data collection methods
  - Water samples collected as near as possible to mine water outflows; where depth or turbulence prevented direct in-situ sampling, a bucket method was used.
  - Headspace gas sampling in triplicate using 200 mL syringes with a three-way valve; air and water equilibrated to determine gas concentrations; ambient air samples collected for reference.
  - For isotope analyses, large-volume water collection (10 L) with degassing precautions (soda lime CO2 removal) and careful headspace filling to minimize degassing before analysis.
  - Water properties measured in situ with a portable meter (conductivity, temperature, pH, DO, DO%); samples filtered for lab analyses.

- Analytical methods
  - GHGs: gas chromatography (Agilent 7890B) with headspace sampler to quantify CO2, CH4, and N2O; standard sets run in each GC analysis.
  - Carbon and other dissolved measures: filtration (0.7 μm) followed by lab analyses (TOC-L for TDN, TDC, DOC; ion chromatography for anions/cations; ICP-MS for metals).
  - Isotopes: radiogenic and stable carbon isotopes measured at NEIF Radiocarbon Laboratory.
  - Data handling: dissolved gas concentrations derived via mass-balance and headspace equilibration equations; concentrations converted to μmol/L and then to ppmv using the Ideal Gas Law; corrections for outgassing and equilibrium considerations discussed.

- Data structure and units
  - Tables provide comprehensive details on units and columns for:
    - Water physicochemical properties and GHG concentrations (Table 3)
    - ICP-MS elements (Table 4)
    - Radiogenic and stable carbon isotopes (Table 5)
  - CSV data include: location data, date, location type (source, cascade, reed, deep, outflow), sample code, latitude/longitude, and site-specific measurements.
  - Missing data are indicated in the CSVs with asterisks; several measurements may reflect minimum concentrations due to outgassing and turbulence.

- Data quality and limitations
  - Potential underestimation of GHGs due to outgassing prior to or during sampling, especially at highly supersaturated sites and where turbulence occurs.
  - Turbulence during sampling and high flow/slopes at some sites contributed to potential measurement biases; reported values are minimum estimates of concentrations.
  - DIC measurements may underestimate total inorganic carbon due to pre-filtering outgassing.
  - Some ion concentrations (e.g., high Ca/Mg) can cause peak overlaps, affecting NH4+ quantification in certain samples.

- Data use and accessibility (Data support context)
  - Data are organized for self-service exploration, enabling dashboards or pivot-table-style analyses.
  - Comprehensive metadata and column definitions are provided to support data reuse, cross-site comparisons, and integration with other datasets.
  - Outputs include spatially distributed site data (MA1–MA16) and treatment-path measurements, suitable for analyses of treatment efficacy and geochemical processes in flooded mine environments.

- Acknowledgements and references
  - Supported by NERC and NEIF facilities; data/isotope analyses performed at NEIF Radiocarbon Laboratory and UKCEH Edinburgh, with collaboration from the Coal Authority and Severn Trent Services.