# Data collection/generation methods

- Scope and approach
  - Describes how water samples were collected from different water bodies in the English Lake District and the Norfolk Broads, including on-bridge, shore, and boat-based sampling to access well-mixed water.

- Sampling methods by location
  - English Lake District: streams and rivers sampled from road/foot bridges or riverbanks using a custom off-bridge sampler; lake/broad surface samples collected by boat from pelagic areas (upper 10–30 cm) when possible; if boating was not feasible, lakes sampled from shore with the same off-bridge sampler, 2–5 m from shore.
  - Norfolk Broads: all rivers sampled by boat from well-mixed flow areas.

- Field measurements and sample handling
  - In-field measurements: water temperature, pH, and electrical conductivity (EC) measured on unfiltered samples immediately using handheld probes/meters.
  - Sample processing: water samples for NO3, NO2, NH4, and SRP filtered in the field (NO3 filtered to 0.2 µm for isotope analysis); NO2, NO3, NH4, SRP analyzed after filtration; NO2, NO3, NH4, SRP preserved on ice and stored at 4°C in the dark (NO3 isotope samples frozen at -20°C).
  - Isotopic samples: 20 or 10 nmol of NO3 converted to N2O for dual isotope analysis; samples treated with sulfamic acid if NO2 exceeded 0.01 mg NO2-N/L.

- Analytical methods and instrumentation
  - Nutrient concentrations: determined colorimetrically using an AQ2 Discrete Analyser.
    - NO2: USEPA Method 353.2 (sulfanilamide reaction; 0.01–0.1 mg NO2-N/L).
    - NO3: reduced to NO2 with copperized cadmium and measured; NO3 concentration calculated as difference between reduced and unreduced NO2.
    - NH4: USEPA Method 350.1 (hypochlorite/salicylate at alkaline pH; 0.02–1.0 mg NH4-N/L).
    - SRP: USEPA Method 365.1 (molybdate reaction with ascorbic acid; 0.005–1.0 mg PO4-P/L).
  - Nitrate dual isotope analysis: denitrifier method; isotopic compositions measured on an Isoprime TraceGas system with pre-concentrator/inlet and IRMS at NEIF (UKCEH Lancaster).
  - Isotopic standards and calibration: use of international standards USGS-34, IAEA-NO-3, USGS-35; calibration performed in triplicate with internal standards and environmental samples also in triplicate.

- Quality control and data integrity
  - Field blanks (using high-purity water) included to confirm no contamination.
  - Calibrations verified with externally certified reference standards.
  - Repeat analyses: 10% of samples re-analysed to assess precision.
  - Isotopic calibration: δ15N-NO3 and δ18O-NO3 calibrated against established international standards; performance criteria include replicate standard deviations (≤0.2‰ for δ15N-NO3 and ≤0.5‰ for δ18O-NO3) and triplicate runs for all standards.

- Data description and units
  - Measured parameters and units:
    - pH: negative log hydrogen ion concentration.
    - EC: µS/cm at 25°C.
    - Temperature: °C.
    - NO2, NO3, NH4: mg N/L (NaN indicates not analysed).
    - SRP: mg P/L.
    - δ15N-NO3: per mille relative to AIR-N2.
    - δ18O-NO3: per mille relative to VSMOW.
  - Isotopic data quality: standardized calibration against international references with specified tolerance levels.

- Data structure and fields
  - Datasets comprise multiple fields including:
    - Date_and_time (date and time of sample collection).
    - Sample_ID (field sample code).
    - Site/location identifiers (field sampling site code and coordinates).
    - Field measurements: Temperature, pH, EC.
    - Analyte concentrations: NO2, NO3, NH4, SRP.
    - Isotopic values: d15N_NO3, d18O_NO3.
    - Geographic location: Latitude, Longitude.
  - Note: the dataset is described as containing 13 columns with the above headers, providing a traceable record of when, where, and how each sample was collected and analyzed.