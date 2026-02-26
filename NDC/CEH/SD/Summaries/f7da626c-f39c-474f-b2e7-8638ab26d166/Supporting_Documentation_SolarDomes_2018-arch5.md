# Summary

- Context and scope
  - Rural site in North Wales, UK, part of Bangor University farm; close to the sea; eight solardomes used in 2018 with ozone manipulation.
  - Three domes were heated by +7°C to simulate tropical/subtropical conditions; data for biomass and physiology available only for these heated domes.
  - Ozone was added according to a weekly, computer-controlled profile (LabView); ozone episodes occurred day and night. Plants were watered as needed; exposure ended at different times by species.

- Experimental design
  - Four replicate pots per species/cultivar.
  - Continuous, hourly monitoring of ozone and meteorological conditions; ad-hoc plant physiology measurements during exposure; end-of-experiment biomass/yield measurements.
  - Species/cultivar set includes bean, cowpea, amaranth, and sorghum with multiple varieties; exposure lengths varied with growing season.

- Treatments and conditions
  - Treatments defined by ozone level, temperature, and heating:
    - Medium/High/Low ozone with ambient or +7°C heating.
    - Target ozone peaks around 35 ppb; high peaks up to 80–115 ppb depending on treatment.
  - Specific treatment descriptions combine ozone concentration and temperature conditions.

- Data assets (files and contents)
  - Plant_Physiology_2018.csv: 12 columns, 1365 rows; ad-hoc physiology measurements per plant/replicate; blank cells indicate missing readings.
  - Ozone_and_meteorology_2018.csv: 11 columns, 10008 rows; hourly ozone and meteorological data; gaps exist where logging failed; some fields are synthetic constants for model compatibility.
  - Biomass_and_Yield_2018.csv: 14 columns; end-of-experiment biomass and yield data; includes notes on which crops produced pods/seed heads; Amaranth and Sorghum specifics noted (e.g., seed weights only, yield not reached for some).
  - Data descriptions include specific column names like DOY, Date, Hour, Ozone (ppb), Light, Temperature, RH, Soil Moisture, Chlorophyll Content Index, and biomass/yield metrics.

- Data collection, instrumentation, and calibration
  - Ozone and meteorology logged automatically via LabView; data QA’d for range and plausibility; gaps filled per protocol.
  - Stomatal conductance measured with AP4 porometer; soil moisture with theta probe; chlorophyll content with CCM-200; daily calibration per manufacturer instructions.
  - Ozone analyzers externally calibrated; CCM-200 autocalibrates on use.

- Quality control and data integrity
  - Data QA checks for plausible ranges; outliers assessed; data validated and repaired when needed.
  - A dedicated Appendix details gap-filling and data integrity procedures (Appendix 1).

- Gap filling, provenance, and versioning
  - Gaps identified to ensure 24 hourly records per day; gaps ≤5 hours filled by averaging adjacent values.
  - Larger gaps checked against lab notes and, if appropriate, filled using values from the same time on adjacent days; patterns and solar system behavior considered for plausibility.
  - If ozone system not running, missing values replaced with a dummy 5 ppb value.
  - All changes are tracked; original data kept separate from amended data, maintaining traceability (filled and corrected copies).

- Data structure and accessibility
  - Data resources described with a clear structure: three CSV files, with detailed column counts and known missing data notes.
  - Additional methodological details reference the solardome facility and the DO3SE model (which requires fixed air pressure, wind speed, and a dummy precipitation value to run under well-watered conditions).
  - See facility overview: https://www.ceh.ac.uk/our-science/research-facilities/solardomes-and-ozone-fieldrelease-system

- Limitations and considerations for reuse
  - Exposure lengths varied by species; not all measurements were taken for every species or time point.
  - Some crops have incomplete data (e.g., Amaranth seed weight only; Sorghum yield not reached; blank cells indicate missing data).
  - Temperature and wind representations include fixed or dummy values to enable modeling; interpret model-derived inputs accordingly.
  - No analytical methods were applied to the data in this document; data are provided with QA and gap-filling notes to aid reuse.

- Metadata and references
  - Tables and column details are specified for each CSV, including notes about missing data and special cases.
  - Appendix 1 documents the gap-filling protocol and data alteration practices to ensure reproducibility and traceability.