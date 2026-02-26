# Column heading explanations for 1_Spatial_dataset.csv

- Overview
  - Provides detailed explanations, units, and notes for each column in the 1_Spatial_dataset.csv file.
  - Focuses on spatial coordinates, soil properties, and radionuclide contamination measurements (e.g., 90Sr, 137Cs, 134Cs, 154Eu, 238Pu, 239+240Pu).
  - Includes measurement methods (e.g., HPGe gamma spectrometry, radiochemical techniques) and data quality information (uncertainties, dates).

- Identification and location fields
  - Code: Database serial number – a unique ID.
  - Identifier: UIAR unique label – chemical analysis number.
  - Latitude: Decimal degrees; coordinates determined with satellite GPS (Trimble/ Magellan receivers) in WGS-84.
  - Longitude: Decimal degrees; same GPS context as Latitude.
  - GPS accuracy: Approximately 100 m with a systematic deviation around 300 m.

- Site and soil property fields
  - ADR: Absorbed dose rate at 1 metre height; Units: micro Gray per hour (μGy/h); measured with certified dosimeters (DRG-01T).
  - Hr: Hydrolytic acidity (Kappen method); Units: mg equivalent of H+ per 100 g dry soil; defined by GOST 26212-91.
  - Ca: Exchangeable calcium in soil; Units: mg per 100 g soil.
  - pH_KCl: Salt-extracted soil acidity (dimensionless); based on GOST 26483-85.
  - pH_H2O: Water-extracted soil acidity; Dimensionless; based on GOST 26423-85.
  - P2O5: Mobile phosphorus content in soil; Units: mg per 100 g soil.
  - Humus / Mobile potassium content: Related soil organic matter content and mobile potassium; units include mg per 100 g soil or percentage as applicable; notes reference GOST standards (e.g., GOST 26207-91, GOST 26213-91).
  - Soil_type: Classification of soil type (USSR/FAO/UNESCO framework); notes reference Stolbovoi (2000) and related soil resources literature.
  - Date_of_activity_measurement: Date of measurement; format dd-mmm-yy.

- Radionuclide contamination fields
  - 137Cs: Terrestrial density of soil contamination with 137Cs; Units: kBq/m².
  - 134Cs: Terrestrial density of soil contamination with 134Cs; Units: kBq/m².
  - 154Eu: Terrestrial density of soil contamination with 154Eu; Units: kBq/m².
  - 90Sr: Terrestrial density of soil contamination with 90Sr; Units: kBq/m².
  - 238Pu: Terrestrial density of soil contamination with 238Pu; Units: kBq/m².
  - 239+240Pu_kBq_m-2: Terrestrial density of soil contamination with 239+240Pu; Units: kBq/m².
  - For each radionuclide, notes include:
    - Measurement method details (e.g., gamma spectrometry with HPGe detectors; relative efficiency ~30%; energy resolution ~1.90 keV FWHM at 1333 keV).
    - Specific instrumentation or radiochemical approaches (e.g., radiochemical methods for 90Sr; alpha spectrometry for Pu isotopes).
    - Any treatment steps before measurement (e.g., sample boiling in 6 M HNO3 for Pu measurements).
    - Associated notes on data interpretation and references to standard procedures.

- Uncertainty and quality metadata
  - Relative_uncertainty_137Cs_%: Relative uncertainty of 137Cs determination at 95% confidence.
  - Relative_uncertainty_134Cs_%: Relative uncertainty of 134Cs determination at 95% confidence.
  - Relative_uncertainty_154Eu_%: Relative uncertainty of 154Eu determination at 95% confidence.
  - Relative_uncertainty_90Sr_%: Relative uncertainty of 90Sr determination at 95% confidence.
  - Relative_uncertainty_238Pu_%: Relative uncertainty of 238Pu determination at 95% confidence.
  - Relative_uncertainty_239+240Pu_%: Relative uncertainty of 239+240Pu determination at 95% confidence.
  - Additional fields capture date of Pu measurement and any sample treatment details that influence uncertainty estimates.

- Temporal and measurement context
  - Date_of_activit(y)_measuremen(t): Date when soil activity or measurements were performed (format implied in dataset).
  - Date_of_Pu_measurement: Specific date for Pu measurements; includes notes on sample processing.

- Data provenance and references
  - Notes and external references within the column notes (URLs to GOST standards and related documents) provide methodological grounding.
  - References section lists key publications on soil contamination around Chernobyl (e.g., 90Sr near Chernobyl, hot particles, territory contamination with radionuclides, radiochemical analysis guidance).

- Practical usage considerations for Data Support
  - The dataset merges geographic, chemical, and radiological data to enable spatial analysis and self-serve exploration (e.g., dashboards, pivot tables, maps).
  - Users should account for heterogeneity in data formats and potential gaps (patchy data across sites and times).
  - Data quality warrants careful handling of units, measurement methods, and uncertainty fields when combining columns or comparing sites.
  - Cross-referencing by Code/Identifier supports linking measurement results with site metadata and historical records.
  - The documentation supports reproducibility by detailing standards (GOST) and measurement procedures, aiding data validation and quality assurance.