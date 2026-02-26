# Data collection/generation methods

- Objective and scope
  - Description of how water samples were collected from different water bodies (streams/rivers in the English Lake District, lakes/broads) and the associated field measurements and laboratory analyses.
  - Sampling aimed to capture well-mixed water portions and pelagic surface waters, with shore sampling when boat access was limited.

- Sampling locations and approach
  - English Lake District: streams and rivers sampled from road bridges, foot bridges, or riverbanks using a custom off-bridge sampler; lakes/broads sampled from pelagic areas within the upper 10–30 cm, or from shore 2–5 m from the shoreline if boats unavailable.
  - Norfolk Broads: all rivers sampled by boat from well-mixed flow areas.

- Field measurements and sample handling
  - In-field measurements: water temperature, pH, and electrical conductivity measured on unfiltered samples immediately after collection using handheld probes/meters (WTW 3420 and WTW 340i).
  - Sample filtration: NO3, NO2, NH4, and SRP filtered in the field using 0.45 µm syringe filters immediately after sampling; NO3 samples for stable isotope analysis filtered to 0.2 µm.
  - Storage: all water samples kept on ice and stored at 4°C in the dark; NO3 isotope samples frozen at -20°C until analysis.

- Nutrient analyses (NO2, NO3, NH4, SRP)
  - NO2 and NO3: colourimetric analysis on an AQ2 Discrete Analyser; NO3 determined by reduction to NO2 using copperised cadmium coil; NO3 concentration calculated as the difference between NO2 measurements with and without cadmium reduction.
  - NH4: determined by reaction with hypochlorite and salicylate at alkaline pH (USEPA Method 350.1).
  - SRP: determined by formation of antimony phospho-molybdate complex reduced by ascorbic acid (USEPA Method 365.1).
  - Analytical ranges: NO2 0.01–0.1 mg NO2-N/L; NO3 0.012–2.0 mg NO3-N/L; NH4 0.02–1.0 mg NH4-N/L; SRP 0.005–1.0 mg PO4-P/L.

- Nitrogen and oxygen isotope analysis of nitrate
  - Dual isotope signatures (δ15N-NO3 and δ18O-NO3) measured using the denitrifier method.
  - Interference management: if NO2 > 0.01 mg NO2-N/L, samples treated with sulfamic acid to remove interference.
  - Conversion to N2O: 20 or 10 nmol of NO3 converted to N2O depending on NO3 concentration.
  - Instrumentation: Isoprime TraceGas preconcentrator inlet and autosampler coupled to Isoprime isotope ratio mass spectrometer at NEIF (NERC National Environmental Isotope Facility, UKCEH Lancaster, UK).
  - Calibration standards: δ15N-NO3 calibrated with USGS-34 (-1.8‰) and IAEA-NO-3 (+4.7‰); δ18O-NO3 calibrated with USGS-34, USGS-35, and IAEA-NO-3 (-27.9‰, +57.5‰, +25.6‰). USGS-35 not used for δ15N due to interference.
  - Quality control: standards run in triplicate along with an internal NO3 standard; at least one environmental sample run in triplicate; typical replicate precision: ≤0.2‰ for δ15N-NO3 and ≤0.5‰ for δ18O-NO3.

- Quality control and data integrity
  - Field blanks included in each sampling visit to confirm no contamination during collection/processing.
  - External certified reference standards used for calibrations; 10% of samples reanalyzed to assess precision.
  - Calibration and replicate data quality ensured through triplicate runs of standards and environmental samples; reported precisions are stated (0.2‰ for δ15N-NO3 and 0.5‰ for δ18O-NO3 or better).

- Data structure and units
  - Datasets contain 15 fields/columns:
    - Date_and_time: date and time of sample collection
    - Sample_ID: site code for field sample collection
    - N, W: additional identifiers (interpreted within dataset context)
    - Temperature: field water temperature (°C)
    - pH: field water pH
    - EC: field electrical conductivity (µS/cm at 25°C)
    - NO2: nitrite concentration (mg N/L)
    - NO3: nitrate concentration (mg N/L)
    - NH4: ammonium concentration (mg N/L)
    - SRP: soluble reactive phosphorus concentration (mg P/L)
    - d15N_NO3: δ15N of nitrate (‰, relative to AIR-N2)
    - d18O_NO3: δ18O of nitrate (‰, relative to VSMOW)
    - Latitude: site latitude (decimal degrees)
    - Longitude: site longitude (decimal degrees)

- Data storage and accessibility
  - Field and laboratory data are stored with associated metadata, including collection date/time and exact site coordinates, to support traceability and reuse.