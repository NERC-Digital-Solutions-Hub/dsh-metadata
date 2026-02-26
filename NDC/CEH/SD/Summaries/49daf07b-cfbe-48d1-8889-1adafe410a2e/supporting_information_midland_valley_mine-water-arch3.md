# Data Overview

- Purpose and scope
  - Investigates properties of mine water from legacy coal mines across the Midland Valley, Scotland, focusing on greenhouse gases (GHGs), heavy metals, and water chemistry.
  - Aims to quantify sources, concentrations, fluxes, and sinks of GHGs and metals; determine origins of CH4 and CO2; assess changes across mine environments; evaluate effects of treatment processes (oxidation, settling ponds, reed beds) on water quality and GHGs.

- Study design and locations
  - Measurements conducted June–September 2022 at 16 mine water outflows (MA1–MA16) spanning northeast to southwest Midland Valley, including sites with and without treatment.
  - Some sites include treatment systems (e.g., reed pools, cascades; several with peroxide treatment), while others discharge directly to rivers/streams.
  - Additional sampling at four treatment locations to evaluate treatment system impacts on GHG processing and metal removal.

- Measured parameters and data collected
  - Greenhouse gases: CO2, CH4, N2O; CH4 and CO2 isotopes (Δ14C, δ13C) in dissolved forms.
  - Physico-chemical water properties: temperature, pH, conductivity, dissolved oxygen (DO), DO saturation, dissolved inorganic carbon (DIC), total dissolved carbon (TDC), total dissolved nitrogen (TDN), dissolved organic carbon (DOC).
  - Ion concentrations: major cations/anions (e.g., Cl−, NO3−, SO4^2−, Na+, NH4+, K+, Ca2+, Mg2+).
  - Metals: broad suite measured by ICP-MS (e.g., Li, Be, B, Na, Mg, Al, Si, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, Ga, As, Se, Rb, Sr, Nb, Mo, Ag, Cd, Sb, Cs, Te, Hg, Pb, U, etc.).
  - Isotope data for dissolved CH4 and CO2; additional sample metadata and measurement dates.

- Sampling and analytical methods
  - Headspace gas sampling to determine dissolved gas concentrations; samples collected in triplicate with ambient air references.
  - Gas analysis by GC (CO2, CH4, N2O) with standard gas mixtures for calibration.
  - Water samples filtered and analyzed for TDN, TDC, DOC (TOC analyzer); DIC calculated from TDC and DOC.
  - Ion chromatography for anions and cations; calibration across multiple standards; occasional limitations due to high Ca/Mg.
  - ICP-MS for a wide range of metals; samples acidified prior to measurement; both filtered and unfiltered analyses.
  - Radiogenic and stable carbon isotopes measured at NEIF Radiocarbon Laboratory.
  - Data handling includes careful documentation of sample location codes, sampling points (source, cascade end, deep, reed, outflow), and dates.

- Data quality, units, and reporting
  - Detailed tables outline units and column headers for physical properties, GHG concentrations, ICP-MS elements, and carbon isotopes.
  - Some data marked as below detection limits; missing values flagged in CSVs.
  - Acknowledges potential underestimation of GHGs due to outgassing, turbulence during sampling, and supersaturation effects; measurements are presented as minimum observed concentrations.

- Data interpretation and calculations
  - Dissolved gas concentrations derived via headspace mass-balance; conversions to ppmv using gas solubility, barometric pressure, and temperature.
  - Recognizes dynamic carbonate equilibria can affect CO2 estimates, with an estimated error generally <5%.
  - Notes potential biases from sampling turbulence and handling, especially at MA4 (bubble formation) and MA7/MA11 (sample disturbance).

- Data structure and accessibility
  - Data are organized into multiple CSV files with explicit schema:
    - Table 3: water properties and GHGs (location, coordinates, sample codes, measurements, and units).
    - Table 4: ICP-MS element concentrations and related metadata.
    - Table 5: radiogenic and stable carbon isotope data.
  - Comprehensive metadata includes latitude/longitude precision, sampling dates, and location types (source, cascade, reed, deep, outflow).

- Timeline and acknowledgements
  - Data collection supported by NERC through IAPETUS Doctoral Training Partnership; isotope analyses supported by NEIF.
  - Access to survey sites provided by The Coal Authority and Severn Trent Services; thanks extended to collaborators and sample support personnel.

- Implications for monitoring frameworks
  - Demonstrates a structured approach to selecting environmental health measures: origins and transformations of CH4/CO2, metal fluxes, and treatment effectiveness.
  - Highlights the importance of robust data governance and metadata to enable data reuse, replication, and evaluation across governance boundaries.
  - Shows integration of multiple measurement technologies (gas headspace methods, TOC, IC, ICP-MS, isotope labs) to provide a comprehensive environmental health dataset.
  - Illuminates practical monitoring challenges relevant to policies: data availability, access, metadata quality, data sharing constraints, and the need to document and mitigate measurement biases (outgassing, turbulence, and sample handling).