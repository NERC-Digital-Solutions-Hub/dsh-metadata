# Monthly ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, new membrane validation, 2021

- Purpose and scope
  - Initial results from validating a new PTFE membrane for ALPHA® samplers.
  - Sampling conducted at four UK UKEAP network sites in 2021.
  - Sampling and analysis performed by UKCEH Edinburgh, with site duties shared by UKCEH, AFBI Hillsborough, and Ricardo AEA Chilbolton.

- UKCEH ALPHA® sampler method
  - Passive NH3 sampler using a citric acid coated filter to capture ammonia; protected by a white PTFE membrane facing downwards during exposure.
  - Replicates used to improve reliability; samplers deployed on shelter-mounted poles at about 1.5 m above ground.
  - Analysis: exposed samplers extracted into deionised water and analysed by SEAL AA3 (colorimetry) to determine ammonium concentration, which is converted to an average NH3 concentration for the exposure period.
  - Uptake rate for new membrane: 0.0039701 m3 h-1; exposure duration in hours used for concentration calculation.
  - Hillsborough site excluded from uptake-rate calculations due to unreliable exposure times.

- Uptake rate and exposure details
  - Uptake rate derived from data across three sites; Hillsborough excluded.
  - Site-level uptake rate information provided for Edinburgh sites (e.g., Edinburgh uptake rate OTC, Auch, Hills, Chilbolton) with collocation details.

- Data processing and quality control
  - Raw data evaluated against quality rules; flagged where concerns exist.
  - Quality rules:
    - CV of replicates < 15%: considered valid; otherwise replicates reviewed and may be discarded; valid results flagged as 103.
    - Values above calibration range but still valid if not possible to re-run due to instrument failure or sample loss.
    - Missing data indicated by -9999 in measurement fields or missing date/time metadata.
  - Final dataset: NH3_New_Membrane_2021.csv, containing accepted data values with appropriate flags; includes site names and spatial identifiers.
  - Data units: micrograms of NH3 per cubic metre of air (µg NH3 m-3).
  - Dataset contents and structure described (each row corresponds to one month of data for a single site; columns include site id/name, network_id, parameter_id, measurement start/end date/time, concentration, data flag, and metadata).

- Data structure and flagging
  - Columns include: site id, site name, network_id, parameter_id (alpha_NH3_g), measurement start/end dates and times, ammonia concentration, less-than indicator, verification id, unit id, Data capture, Validity_id, EMEP code, Month-Year, Comments.
  - EMEP flags and data status codes accompany measurements, providing context for data capture, validity, and reasons for any data adjustments (e.g., contamination, detection limits, representativeness).

- Site information
  - Edinburgh uptake rate sites with coordinates and metadata:
    - Edinburgh uptake rate OTC: start 01/03/2020; end ongoing; lat 55.863150; lon -3.209845; 1.5 m height; collocated with UKA00128.
    - Edinburgh uptake rate Auch: start 01/03/2020; end ongoing; lat 55.792160; lon -3.242900; 1.5 m height; collocated with UKA00451.
    - Edinburgh uptake rate Hills: start 01/03/2020; end ongoing; lat 54.452500; lon -6.083340; 1.5 m height; collocated with UKA00293.
    - Edinburgh uptake rate Chilbolton: start 01/01/2021; end ongoing; lat 51.149617; lon -1.438228; 1.5 m height; collocated with UKA00614.