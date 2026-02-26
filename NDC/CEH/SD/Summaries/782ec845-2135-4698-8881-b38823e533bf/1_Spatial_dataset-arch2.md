# Column heading explanations for 1_Spatial_dataset.csv

- Purpose of document
  - Defines metadata for the spatial dataset 1_Spatial_dataset.csv, including field meanings, units, data provenance, measurement methods, uncertainties, and references to ensure consistent interpretation and quality control for environmental monitoring.

- Key identification and location fields
  - Code: database serial number (unique ID)
  - Identifier: UIAR unique label - chemical analysis number
  - Latitude/Longitude: sampling site coordinates in decimal degrees, determined via GPS (Trimble, Scout/Master, Magellan NAV DLX-10) using WGS-84
  - GPS accuracy: ~100 m typical, with a systematic deviation of about ~300 m

- Radiological measurements (contaminant concentrations per area)
  - ADR: Absorbed dose rate at 1 metre height; units micro Gray per hour (µGy/h); measured with certified dosimeters DRG-01T
  - 137Cs, 134Cs, 90Sr, 238Pu, 239+240Pu, 154Eu: terrestrial density or activity of radionuclides; units typically kiloBecquerels per square metre (kBq/m^2)
  - Measurement methods: gamma spectrometry using HPGe detectors (e.g., 30% relative efficiency, 1.90 keV FWHM at 1333 keV), with specific notes per nuclide about treatment or counting conditions
  - Relative_uncertainty_*: 95% confidence interval uncertainties for each nuclide (percent), with notes on calculation or treatment variations (e.g., boiling in 6M HNO3)
  - 90Sr, Pu isotopes: additional notes on radiochemical methods and sample treatments (e.g., Pavlotskaya 1997 reference, digestion and plutonium extraction procedures)
  - Date_of_Pu_measurement: date of plutonium measurement

- Soil chemical and physical properties
  - Hr: Hydrolytic acidity (Kappen method, GOST 26212-91); units: milligrams of H+ per 100 g dry soil
  - Ca: Exchangeable calcium; units: mg per 100 g soil
  - pH_KCl: soil acidity measured in salt (KCl) extraction; dimensionless
  - pH_H2O: soil acidity measured in water extraction; dimensionless
  - P2O5: Mobile phosphorus content; units: mg per 100 g soil
  - Humus: Organic matter content (notes indicate a relationship to Humus/mobile potassium content and related GOST standards; units given as milligrams per 100 g soil and percentage in different entries)
  - Soil_type: classification of soil using USSR/FAO/UNESCO systems; notes reference to habitat type and FAO/UNESCO correlations; sources linked to GOST 26207-91 and FAO soil map references
  - Date_of_activity_measurement: date of measurement for soil parameters

- Data quality, provenance, and references
  - Notes and web references accompany many fields (GOST standards, Russian documentation, and measurement details)
  - References cited for radiological and soil analytical methods (e.g., Kashparov et al., Pavlotskaya 1997, IIASA-related soil classifications)

- Practical implications for Analysts Monitoring the Environment
  - The dataset provides spatially resolved, standardized measurements of environmental radiation and soil chemistry for site-based monitoring
  - Metadata supports quality assurance, data cleaning, and interoperability with other datasets via explicit units, measurement methods, uncertainties, and provenance
  - The presence of GPS accuracy details and standardized analytical methods aids reproducibility and cross-site comparisons

- Potential considerations for use
  - Some field descriptions (e.g., Humus/Soil_type notes) contain garbled text; may require data curation to ensure consistency
  - GPS accuracy limitations should be considered when integrating with high-resolution spatial analyses
  - Ensure alignment of units and conversion across isotopes (kBq/m^2) and confirm any dataset-specific conventions for reporting (e.g., treatment variants in uncertainty fields)