# Data Overview

- Study goal
  - Quantify sources, concentrations, fluxes, and sinks of greenhouse gases (GHGs) and heavy metals from mine water across 16 abandoned coal mine outflows in the Midland Valley, Scotland.
  - Identify origins of CH4 and CO2, assess whether origins and metal concentrations vary by environment, and evaluate the impact of treatment (oxidation, settling ponds, reed beds) on water properties and GHGs.

- Study design and sites
  - 16 mine water outflows sampled from MA1 (northeast) to MA16 (southwest), spanning Fife, Central, Lothian, and Ayrshire coal fields.
  - Sites include both direct mine outflows and those with treatment systems.
  - Four treatment locations sampled comprehensively:
    - MA7 (Cuthill) and MA10 (Kingshill) using cascades
    - MA11 (Pool Farm) and MA12 (Mousewater) using peroxide treatment
  - Sampling scope included source measurements and multiple points within treatment systems (e.g., cascade end, deep pool, reed bed, and outflow) to assess treatment effects.

- Data collected and variables
  - Water physico-chemical properties
    - Conductivity, temperature, pH, dissolved oxygen (DO and DO%), dissolved inorganic carbon (DIC), total dissolved carbon (TDC), dissolved organic carbon (DOC)
    - Major ions via ion chromatography (e.g., Cl-, NO3-, SO4-, Na+, NH4+, K+, Ca2+, Mg2+)
  - Greenhouse gases (GHGs)
    - CO2, CH4, N2O concentrations and related saturation/concentration metrics
    - Gas partial pressures in air (pCH4air, pCO2air, pN2Oair)
    - CH4 and CO2 isotopic analyses: δ13C and Δ14C (radiogenic)
    - CH4-C and CO2-C concentrations
  - Metal concentrations
    - Measured by ICP-MS on filtered and unfiltered water samples (extensive suite of elements: Li, Be, B, Na, Mg, Al, Si, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, Ga, As, Se, Rb, Sr, Nb, Mo, Ag, Cd, Sb, Cs, Tl, Hg, Pb, U, and others)
  - Sample metadata
    - Location code, site name, coordinates, sample date, sample type (source, cascade, deep, reed, outflow), filtration status, and sampling specifics
  - Isotope data
    - Radiogenic and stable carbon isotope data for dissolved CH4 and CO2, including sample codes, dates, lat/long, and associated grant/publication details

- Methods and analysis
  - Headspace gas sampling
    - Triplicate headspace samples collected with careful minimization of degassing; ambient air samples for calibration
  - Analytical instrumentation
    - Gas chromatography with headspace autosampler for CO2, CH4, N2O
    - TOC analyzer for TDN, TDC, DOC; IC for anions/cations; ICP-MS for metals
  - Isotope analysis
    - δ13C and Δ14C isotopes measured at NEIF Radiocarbon Laboratory
  - Data processing
    - Dissolved gas concentrations derived from headspace gas-liquid mass balance
    - Conversion to ppmv via ideal gas law; corrections for outgassing and equilibration
    - Notes on potential errors: CO2 estimates can have small errors due to carbonate equilibria; measurements likely represent minimum GHG concentrations due to supersaturation and turbulence
  - Data quality and limitations
    - Outgassing and turbulence during sampling potentially bias lower-bound concentrations
    - Filtration may cause outgassing of GHGs and underestimation of DIC
    - Some sites had measurement challenges (e.g., sampling depth or access), and one reed pool was bypassed during the survey

- Data structure and units
  - Tables 3–5 (CSV format) outline the data structure:
    - Table 3: Water properties and GHG concentrations
      - Includes: Location_Name, Location_Code, Location_Type, Sample_Code, Latitude, Longitude, Date, Cond (µS/cm), Temp (°C), pH, DO (mg/L), DO% , TDC (mg/L), DIC (mg/L), TDN (mg/L), various ion concentrations (µmol/L or related), gas partial pressures and saturation metrics (pCH4air, pCO2air, CH4Sat, CO2Sat, N2OSat), CH4 (µmol/L), CH4-C (µg/L), CO2 (µmol/L), CO2-C (mg/L), N2O (µmol/L), N2O-N (µg/L)
    - Table 4: ICP-MS element concentrations
      - Includes: sample details, filtration status, element concentrations (ppb or ppm) with sample-specific RSD data for many elements
    - Table 5: Radiogenic and stable carbon isotopes
      - Includes: Gas measured, Sample_Code, Date, δ13C, %Modern C, Radiocarbon Age and errors, etc.
  - Data are provided with missing values marked and a note on detection limits where applicable

- Acknowledgements and provenance
  - Funded by Natural Environment Research Council (NERC) via IAPETUS Doctoral Training Partnership; NEIF Radiocarbon Laboratory support
  - Access supported by The Coal Authority and Severn Trent Services
  - Data collected by researchers including Alison Brown and supported by Dr. Amy Pickard

- Key implications and potential uses
  - The dataset enables:
    - Tracing CH4 and CO2 origins in flooded, abandoned mine environments using carbon isotopes
    - Assessing how CH4 and CO2 origins may vary between mine environments and with treatment processes
    - Evaluating how heavy metal concentrations change across environments and in response to treatment
    - Assessing treatment system effectiveness (oxidation, cascade flow, reed beds) on GHG processing and metal removal
  - The multi-site, multi-stage sampling design supports cross-site comparisons and potential modeling of GHG fluxes and metal dynamics across mine waters in Scotland