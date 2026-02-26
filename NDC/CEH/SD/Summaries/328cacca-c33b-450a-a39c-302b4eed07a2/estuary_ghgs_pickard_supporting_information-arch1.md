# UK estuary greenhouse gas and nutrients data set

- Study design and scope
  - Sampling conducted at seven UK estuaries: Clyde, Forth, Tay (central Scotland); Conwy, Clwyd (northern Wales); Dart, Tamar (southwest England).
  - Four coordinated sampling campaigns: July and October 2017; January and April 2018.
  - Estuaries sampled to span the salinity gradient; sampling locations chosen upstream to downstream with target salinities of 1, 2, 5, 10, 15 and >25 ppt, though not always achieved.
  - In situ measurements of temperature and salinity at each location; salinity-based site selection varied by survey.

- Field sampling and locations
  - Use of rigid inflatable boats or fixed points (e.g., bridges) due to logistics.
  - Six sampling locations per estuary used for greenhouse gas and water chemistry analyses.
  - Depth and positioning documented with latitude/longitude, day, month, and year; position 1 is furthest upstream (freshwater) and position 6 is most saline downstream.

- Greenhouse gas sampling and analysis
  - Gas sampling methods
    - Clyde, Clywd, Conwy, Forth, and Tay: duplicate samples collected using headspace equilibration method (40 mL estuary water equilibrated with 20 mL ambient air in a syringe; shaken underwater for equilibration), with subsequent injection into pre-evacuated vials for GC analysis. An ambient air sample also collected at each site.
    - Tamar and Dart: samples collected in 500 mL borosilicate bottles from the bucket and overfilled to remove air bubbles; poisoned with mercuric chloride prior to GC analysis.
  - Analysis and instrumentation
    - Instruments: gas chromatograph (Agilent 7890B) with a flame ionisation detector for CH4 and CO2; micro electron capture detector for N2O; headspace autosampler used for Clyde/Clywd/Conwy/Forth/Tay.
    - Detection limits: CH4 40 ppb; CO2 5000 ppb; N2O 5 ppb.
    - Calibration with standard concentrations spanning ambient to elevated levels; standards traceable to NOAA references for Tamar/Dart analyses.
  - Gas solubility and temperature considerations
    - Total dissolved gas concentrations calculated from headspace and ambient air using Henry’s Law and the Bunsen solubility method with temperature and salinity corrections.
    - Tamar/Dart samples equilibrated at ~25°C prior to GC analysis.
  - Data handling and reporting
    - CH4, CO2, and N2O concentrations reported with appropriate units; N2O, CH4, CO2 solubility and saturation values also derived where applicable.

- Water chemistry analyses
  - Dissolved organic carbon and total dissolved carbon
    - DOC analyzed at UKCEH Centralized Analytical Chemistry Laboratory (0.45 μm filtered samples) using Shimadzu TOC-L with combustion and infrared absorbance.
    - TDC measured for freshwater samples (includes inorganic and organic carbon) with a LoD of 0.6 mg/L C; freshwater acidification/purge steps differ from GO-SHIP-related methods.
  - Freshwater nutrients (Position 1; with exception at Conwy where positions 1–6 were analysed)
    - Major anions (including NO3−N) by Dionex ICS2000; LoD 0.06 mg/L N; QC samples included.
    - NH4−N measured by colorimetric indophenol blue method; LoD 0.033 mg/L N; multiple controls and calibration procedures described.
    - Total Nitrogen (TN) measured by Shimadzu TOC-L with TNM-L module (0–10 mg/L N; LoD 0.08 mg/L N).
    - Total Phosphorus (TP) measured via K2S2O8 digestion and molybdenum blue colorimetry; LoD 0.008 mg/L P; including blanks and certified references.
    - Soluble reactive phosphorus (PO4−P) measured colorimetrically (880 nm) with LoD 0.005 mg/L P.
  - Saline nutrients (Positions 2–6)
    - Analyzed at Plymouth Marine Laboratory using SEAL Analytical AAIII autoanalyser.
    - Methods for NO3−+NO2−, NO2−, NH4+, PO4−, and SiO4 measured per GO-SHIP protocols; LoDs vary by analyte (e.g., NO3−, PO4−, SiO4 0.02 μmol/L; NO2− 0.01 μmol/L; NH4+ 0.04 μmol/L).
  - Data formatting and units
    - Data presented to two decimal places; Table 1 provides column descriptions and units.
    - Distinct laboratories for freshwater vs saline analyses can yield missing values in certain columns (marked with an asterisk in the dataset).
    - Position and salinity descriptions allow linking chemical measurements to specific salinity regimes.

- Data quality, structure, and availability
  - The dataset comprises measurements across seven estuaries, four sampling campaigns, and multiple analyte classes (GH gases and nutrients).
  - Missing values are explicitly indicated; freshwater and saline analyses are conducted at different laboratories, causing gaps across related columns.
  - Data are organized with clear metadata in Table 1, including estuary name, sampling position, geographic coordinates, date, salinity, temperature, and the suite of nutrient and gas concentrations.

- References and methodological foundations
  - Gas analysis and solubility corrections referenced to established methods and literature for methane, nitrous oxide, and carbon dioxide in estuarine waters.
  - Nutrient analyses aligned with GO-SHIP analytical protocols and established colorimetric and ion chromatography methods.
  - Calibration standards and traceability align with recognized oceanographic chemistry practices and relevant methodological papers.