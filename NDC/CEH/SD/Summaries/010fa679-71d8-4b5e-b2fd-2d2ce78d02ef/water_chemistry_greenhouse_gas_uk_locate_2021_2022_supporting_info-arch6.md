# UK water chemistry and greenhouse gas emissions study, LOCATE, 2021-2022: Supporting information

- Project aim and scope
  - Multidisciplinary LOCATE project to understand carbon flow from land to ocean.
  - Field campaign to characterise diurnal greenhouse gas emissions from inland water bodies and how they vary by water body type and season.
  - Method: floating chambers deployed for 24 hours to measure emitted gases; samples compared from start to end of 24-hour period.
  - Collaboration across multiple UK institutions; sampling conducted July 2021 to March 2022.

- Data collected and key variables
  - Physicochemical field measurements: pH, conductivity, dissolved oxygen (DO), temperature; multiple probes yield Temp_av.
  - Dissolved/nutrient chemistry: DOC (dissolved organic carbon), TdN (total dissolved nitrogen), TP (total phosphorus), SRP (soluble reactive phosphorus), UV/Vis absorbance (Abs_at_254; SUVA).
  - Greenhouse gases: dissolved CH4, CO2, N2O; and chamber-derived concentrations for CH4, CO2, N2O at time 0 and after 24 hours.
  - Site metadata: Site_name, Site_type (e.g., Broad, Dyke, Loch, Pond), Date, Latitude, Longitude, Time (GMT); presence of floating chambers (Chambers).
  - Data structure: dataset MERLIN 2022-2023 with columns covering site info, field measurements, and laboratory results (Tables 1–3 referenced in the study).

- Sampling locations and design
  - Sampling across the UK at ponds, streams, lochs, dykes, broads, and wetlands.
  - Timeframe: July 2021 – March 2022.
  - Site selection emphasized geographical and land-type variation.
  - Figure 1 provides a map of sampling sites; Table 1 lists site names, types, dates, and coordinates.

- Field collection methods
  - Water samples collected with a 60 mL syringe; SRP and DOC filtered through 0.45 µm filters.
  - Sample bottles: sterile HDPE or glass containers; careful labeling with site code, date, and project.
  - Floating chambers: inverted basins with floats, calibrated volume and cross-sectional area; three-way tap to sample air; chambers covered to minimize light/temp variation.
  - GHG sampling: headspace method for dissolved gases at start; duplicate samples for each site; gas withdrawn after 24 hours via syringe into pre-evacuated vials.

- Sample storage and handling
  - TP, SRP, and spare filtered samples frozen at -18°C until batch analysis.
  - DOC and TdN, UV/Vis samples stored at 4°C and analyzed within a week.
  - Greenhouse gas samples stored at room temperature until batch analysis.

- Laboratory analyses and QA/QC
  - DOC and TdN: Shimadzu TOC-LCPH with TNM L, using 680°C catalytic oxidation; NPOC as DOC proxy; calibration with standards; blanks and duplicates included; replicate + outlier handling rules.
  - UV/Vis: SUVA via absorbance at 254 nm (A254) with pathlength correction and normalization to DOC.
  - Total phosphorus and SRP: SEAL AQ2 Discrete analyser; digestion with potassium persulfate to convert all P to orthophosphate; colorimetric molybdenum-blue method; calibration with multiple standards; blanks used.
  - GHG analyses: Agilent 7890B GC with μECD (N2O) and FID (CH4, CO2); concentrations calibrated with mixed standards; results expressed in ppmv and converted to µg L using Henry’s law; average of duplicates used per site.
  - Data standards and documentation: detailed column descriptions and units provided (Table 3); data recorded with site names, coordinates, and time alongside analytical results.

- Data structure and units
  - MERLIN 2022-2023 dataset structure described (Table 3): 
    - Site metadata: Site_name, Site_type, Date (dd/mm/yy), Latitude, Longitude, Time (GMT), Chambers.
    - Field data: Conductivity, Conductivity_temp, pH, pH_temp, DO, DO_temp, Temp_av.
    - Chemistry: DOC, TdN, C_N, Abs_at_254, SUVA, TP, SRP.
    - Dissolved gas concentrations: CH4_C, CO2_C, N2O_N.
    - Chamber gas concentrations: Chamber_CH4_C_time_0, Chamber_CH4_C_time_24, Chamber_CO2_C_time_0, Chamber_CO2_C_time_24, Chamber_N2O_N_time_0, Chamber_N2O_N_time_24.
  - Units and decimal places detailed for each variable (e.g., Conductivity in µS/cm, DO in mg/L, pH with two decimals, SUVA as unitless, TP/SRP in mg/L, gas concentrations in µg/L or ppm where applicable).

- Dataset completeness and exclusions
  - Table 4 documents data exclusions with reasons across multiple sites and dates (e.g., missing time, DO_temp not recorded, sample contamination, pH or CH4/C data missing, and other unspecified omissions).
  - Exclusions indicate data quality issues or incomplete measurements at specific sites/dates, affecting dataset completeness and subsequent analyses.

- Outputs and acknowledgements
  - Outputs include a map of sampling locations (Figure 1) and detailed sample/site tables (Table 1) within the supporting information.
  - Acknowledgements note permissions and support from partner organizations.
  - References provide methodological and analytical context for the measurement techniques used.