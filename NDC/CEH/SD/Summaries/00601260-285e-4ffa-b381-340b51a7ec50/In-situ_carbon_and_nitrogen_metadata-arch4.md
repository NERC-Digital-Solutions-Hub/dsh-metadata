# Fieldwork Protocol

- Field procedures
  - Water samples collected manually from surface water and multilevel piezometers at 10 and 20 cm using a syringe.
  - In-situ measurements: dissolved oxygen and temperature using YSI ProODO or EcoSense ODO200.
  - Samples filtered (0.45 μm then 0.22 μm) and frozen for analysis.
  - Diffusive equilibrium in thin-film (DET) gels deployed upstream and mid-stream in sandy reaches, placed at least 72 hours before sampling.
  - Porewater headspace gas sampled in-situ via headspace equilibrium; 7 ml water + 14 ml helium drawn into syringe, shaken, and headspace collected in a pre-evacuated exetainer.

- Laboratory processing and solute extraction
  - Gel slices weighed to determine water volume; assumed water content of saturated gel is 95%.
  - Gel slices eluted with 5 ml ultrapure water for 24 hours on ice; eluates stored frozen.
  - Isotopic analyses performed on dissolved nitrate/nitrite and CO2 from gel eluates and water samples.

- Isotopic and chemical analyses
  - Denitrifier method used for δ15NNO3+NO2 and δ18O NO3+NO2 in the laboratory.
  - δ13C of CO2 measured with isotope ratio mass spectrometry.
  - Nutrients and DOC: continuous flow analyser for NH4+, NO3-, NO2-; TOC analyser for DOC.
  - Gases (CO2, CH4, N2O) analyzed by gas chromatography with appropriate detectors (FID, TCD, μECD).
  - Headspace concentrations converted to porewater concentrations using Henry’s constant.

- Calibration, standards and quality control
  - GC-ECD, GC-FID, GC-TCD and continuous flow analyser calibrated daily with multi-point standards; inclusion of blanks and periodic external references to correct drift.
  - Reported accuracy, precision, and limits of detection for each instrument (e.g., N2O, CH4, CO2, NH4+, NO3-, NO2-, TOC).
  - Isotope analyses calibrated against international standards (USGS, IAEA) with in-house references; long-term precision reported for δ15N, δ18O, and δ13C.
  - Temperature and dissolved oxygen calibrated per manufacturer protocols (factory calibration for DO and 100% air saturation reference).

- Data structure and schema
  - Two CSV data files:
    - In-situ_carbon_and_nitrogen_data (27 columns)
      - Key fields: Piezo_ID, Depth, Sediment_Type, Season, Reach, Dissolved_Oxygen, Temperature, CO2, CH4, N2O, NH4, NO3, NO2, DOC, d15N_NO3+NO2, d18O_NO3+NO2, d13C_CO2, plus per-measurement errors.
      - Datasets include units (e.g., mg/L, mg N/L, mg C/L) and isotopic values in per mil.
    - In-situ_DET_gel_data (11 columns)
      - Key fields: Gel_ID, Depth, Season, NH4, NO3, d15N_NO3+NO2, d18O_NO3+NO2, d13C_NO3+NO2 (with associated errors).
  - Notes on data completeness:
    - Some samples lack isotope data due to insufficient nitrate.
    - Some piezometer sampling difficult, resulting in missing gas samples.

- Data content and units
  - Field measurements include temperature (°C) and DO (mg/L).
  - Nutrients: NH4, NO3, NO2 (mg N/L or mg N/L); DOC (mg C/L); CO2, CH4, N2O (mg/L or μg/L depending on measurement).
  - Isotopic ratios: δ15NNO3+NO2, δ18ON O3+NO2, δ13C_CO2 (per mil, ‰).
  - Depth, sediment type, season, and reach are recorded to contextualize results.

- Data provenance and workflow
  - DET gels deployed prior to sampling; samples processed in lab with gel elution and back-equilibration.
  - In-situ samples converted to lab-ready measurements through standardised extraction and instrumentation workflows.
  - Calibration standards and reference materials used to ensure cross-method comparability and traceability.

- References and methodological basis
  - Denitrifier method for nitrogen and oxygen isotopes (Casciotti et al.; Sigman et al.; Kaiser et al.).
  - Automated colorimetric methods for nitrate, nitrite, ammonium (Antweiler et al.).
  - Gas solubility and headspace gas analysis procedures (Hudson; Wilhelm et al.).
  - Instrumentation calibration and performance references provided for each analytical method.