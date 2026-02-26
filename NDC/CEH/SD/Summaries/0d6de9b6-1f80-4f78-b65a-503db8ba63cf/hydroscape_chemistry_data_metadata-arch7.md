# Data collection/generation methods

- Overview
  - Describes field sampling and laboratory analyses for water quality parameters in the English Lake District and the Norfolk Broads.
  - Focuses on collecting and processing samples for nutrient analyses (nitrate, nitrite, ammonium, soluble reactive phosphorus) and stable isotope composition of nitrate (δ15N-NO3 and δ18O-NO3).

- Sampling scope and approach
  - Water samples collected from rivers and lakes using location-appropriate methods to sample well-mixed areas.
  - Lakes/Broads: surface water (upper 10–30 cm) sampled by boat from pelagic areas; if boat access is restricted, sample from shore about 2–5 m from the shoreline.
  - Rivers in the Norfolk Broads sampled by boat from well-mixed flow areas.
  - Sampling locations include multiple sites across the English Lake District and Norfolk Broads.

- Field sampling and sample handling
  - In-field measurements: water temperature, pH, and electrical conductivity (EC) measured on unfiltered samples with handheld probes.
  - Filtration and preservation:
    - NO2, NO3, NH4, and SRP samples filtered in the field using 0.45 μm filters.
    - NO3 isotopic samples filtered to 0.2 μm.
    - All water samples kept on ice and stored at 4°C in the dark; NO3 isotope samples frozen at -20°C.
  - Analyses performed on filtered samples shortly after collection.

- Analytical methods for nutrients
  - Nitrite (NO2) and nitrate (NO3) by colorimetric analysis on an AQ2 Discrete Analyser.
  - NO3 reduction to NO2 for measurement using copperised cadmium coil; NO3 concentrations calculated as the difference between measurements with and without cadmium reduction.
  - Ammonium (NH4) determined by a colorimetric method (USEPA Method 350.1).
  - Soluble reactive phosphorus (SRP) determined by a colorimetric method (USEPA Method 365.1).

- Isotope analysis and QA for NO3
  - Dual isotope analysis (δ15N-NO3 and δ18O-NO3) using the denitrifier method.
  - Interference removal: if NO2 > 0.01 mg NO2-N/L, samples treated with sulfamic acid before isotopic analysis.
  - Nitrogen and oxygen isotopes converted to N2O for IRMS analysis using 10 or 20 nmol NO3 depending on concentration.
  - Isotope ratios measured at the NEIF facility (Isoprime IRMS with preconcentrator/inlet).
  - Calibration and quality control:
    - Calibrations with internationally recognized standards (USGS-34, IAEA-NO-3, USGS-35); triplicate runs for standards and internal NO3 standard; at least one environmental sample run in triplicate.
    - Reported standards: δ15N-NO3 relative to AIR-N2; δ18O-NO3 relative to VSMOW.
    - Reproducibility: SD ≤ 0.2‰ for δ15N-NO3 and ≤ 0.5‰ for δ18O-NO3.

- Data structure and variables
  - Datasets contain 13 columns with headers including:
    - Date_and_time: date and time of sample collection
    - Sample_ID: site code for field sample
    - Temperature: field water temperature (°C)
    - pH: field pH (unitless)
    - EC: electrical conductivity (μS/cm at 25°C)
    - NO2: nitrite concentration (mg N/L)
    - NO3: nitrate concentration (mg N/L)
    - NH4: ammonium concentration (mg N/L)
    - SRP: soluble reactive phosphorus concentration (mg P/L)
    - d15N_NO3: δ15N of nitrate (‰, relative to AIR-N2)
    - d18O_NO3: δ18O of nitrate (‰, relative to VSMOW)
    - Latitude and Longitude: site coordinates (decimal degrees)
  - Note: Concentrations are given as mg N/L for nitrogen species and mg P/L for SRP; units for isotopes are per mille.

- Data quality and controls
  - Field blanks included to check for contamination.
  - External certified standards used to calibrate nutrient analyses; repeated analyses (≈10% of samples) to assess precision.
  - Isotope standards and environmental samples run in triplicate; quality control reports standard deviations within defined thresholds.