# Data collection/generation methods

- Scope and sampling design
  - Study areas: streams and rivers in the English Lake District; lakes/broads surface samples; Norfolk Broads rivers.
  - Sampling approaches:
    - English Lake District: from road/foot bridges or riverbanks using a custom off-bridge sampler to sample well-mixed flow.
    - Lakes/Broads: surface samples collected by boat from pelagic areas when possible; if boat unavailable, shore sampling 2–5 m from shore using the same sampler.
    - Norfolk Broads: all rivers sampled by boat from well-mixed areas.
  - Measured parameters include water temperature, pH, electrical conductivity, nitrate, nitrite, ammonium, soluble reactive phosphorus, and stable isotopes of nitrate.

- Field measurements and sample collection
  - In-field measurements of temperature, pH, and EC performed immediately on unfiltered samples using handheld probes (WTW 3420 and WTW 340i).
  - Sample filtration in the field:
    - NO3, NO2, NH4, SRP filtered through 0.45 µm cellulose acetate syringe filters.
    - NO3 for isotopes filtered to 0.2 µm.
  - Sample handling:
    - All samples kept on ice until lab return; storage at 4°C in the dark.
    - NO3 isotope samples frozen at -20°C until analysis.

- Laboratory analyses (nutrients)
  - NO2, NO3, NH4, SRP concentrations determined colorimetrically with an AQ2 Discrete Analyser.
  - NO2: EPA method 353.2 (0.01–0.1 mg NO2-N/L).
  - NO3: Reduced to NO2 in-field using a copperised cadmium coil; NO3 calculated as the difference between NO2 measurements with and without cadmium reduction (range 0.012–2.0 mg NO3-N/L).
  - NH4: EPA method 350.1 (0.02–1.0 mg NH4-N/L).
  - SRP: EPA method 365.1 (0.005–1.0 mg PO4-P/L).

- Isotope analysis
  - Dual isotope signatures of NO3 (δ15N-NO3 and δ18O-NO3) measured by the denitrifier method.
  - Interference management: if NO2 > 0.01 mg NO2-N/L, samples treated with sulfamic acid to remove interference.
  - Nitrate conversion: depending on NO3 concentration, 10 or 20 nmol NO3 converted to N2O for analysis.
  - Instrumentation: Isoprime TraceGas preconcentrator inlet with auto-sampler connected to Isoprime isotope ratio mass spectrometer at NEIF (UKCEH Lancaster).

- Units and data types
  - pH: unitless.
  - EC: microsiemens per centimeter (µS/cm) at 25°C.
  - Temperature: °C.
  - NO2/NO3/NH4: mg N/L.
  - SRP: mg P/L.
  - δ15N-NO3: per mille (‰) relative to Air-N2.
  - δ18O-NO3: per mille (‰) relative to VSMOW.

- Quality control and calibration
  - Field blanks (using >18.2 MΩ MilliQ water) to check for contamination; no contamination detected.
  - Calibration with externally certified reference standards.
  - 10% of samples reanalyzed to assess precision.
  - Isotope standards and calibrations:
    - δ15N-NO3 calibrated with USGS-34 and IAEA-NO-3 (−1.8‰ and +4.7‰).
    - δ18O-NO3 calibrated with USGS-34, USGS-35, IAEA-NO-3 (−27.9‰, +57.5‰, +25.6‰); USGS-35 excluded for δ15N due to interference (δ17O-NO3).
  - Replicates: international standards, internal NO3 standard, and at least one environmental sample analyzed in triplicate per run.
  - Precision: standard deviation ≤0.2‰ for δ15N-NO3 and ≤0.5‰ for δ18O-NO3.

- Data structure and variable definitions
  - Core fields (headers and descriptions):
    - Date_and_time: date and time of sample collection.
    - Sample_ID: site code for field sample collection.
    - N, W: (context suggests nitrite and related field coding; see below for complete list)
    - Temperature: field water temperature (°C).
    - pH: field water pH.
    - EC: field electrical conductivity (µS/cm at 25°C).
    - NO2: nitrite concentration (mg N/L).
    - NO3: nitrate concentration (mg N/L).
    - NH4: total ammonia concentration (mg N/L).
    - SRP: soluble reactive phosphorus concentration (mg P/L).
    - d15N_NO3: δ15N of nitrate (‰, relative to AIR-N2).
    - d18O_NO3: δ18O of nitrate (‰, relative to VSMOW).
    - Latitude: decimal degrees of field sample site.
    - Longitude: decimal degrees of field sample site.
  - Note: the dataset documents 13 columns in one section but lists additional geographic and field measurement columns, effectively capturing both field measurements and laboratory isotope results for each sample.