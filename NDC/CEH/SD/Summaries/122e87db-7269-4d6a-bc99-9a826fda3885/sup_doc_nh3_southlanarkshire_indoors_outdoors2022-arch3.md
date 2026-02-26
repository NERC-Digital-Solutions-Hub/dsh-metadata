# Passive sampler ammonia measurements indoors and outdoors at a rural dwelling in South Lanarkshire, 2022

- Overview
  - Study location: Two sites in a rural South Lanarkshire dwelling — indoor hall and outdoor garden (garden backs onto grassland part of a large dairy farm).
  - Sampling period: Monthly exposure cycles starting at the beginning of each month.
  - Local operators: Dwelling owner; analysis by Centre for Ecology and Hydrology (CEH) Edinburgh.

- Sampling Methodology
  - Instrument: CEH ALPHA® passive samplers with a citric acid coated filter to capture ammonia.
  - Protection: White PTFE membrane shields the filter; membrane oriented downwards during exposure.
  - Deployment: Replicates attached to a shelter on a pole at about 1.5 m above ground.
  - Purpose of replicates: Improve reliability of ambient NH3 concentration estimates.

- Analysis and Calculation
  - Post-exposure processing: Exposed samplers extracted into deionised water; NH3 concentration determined via SEAL AA3 colorimetry (ammonium measurement).
  - Conversion: Sampler ammonium concentration converted to an average NH3 air concentration using uptake rate of 0.0038422 m3 h-1 and exposure duration.
  - Output units: Micrograms of NH3 per cubic meter (µg NH3 m-3) for the specified exposure period.

- Data and Dataset
  - Dataset name: NH3_SouthLanarkshire_indoors_outdoors2022.csv.
  - Structure: Each row corresponds to one month of data for a single site; columns include site name, start/end dates, ammonia concentration, and a data flag.
  - Metadata and details: Site names listed on a separate page; dataset contents described on page 3; concentrations reported as average NH3 in air for the exposure period.
  - Data flags: Data flagged to indicate concerns; specifics documented on page 4.

- Data Quality and Validity
  - Quality checks:
    - Replicate precision: Coefficient of variation (CV) < 15% required for valid replicates; if CV > 15%, evaluation of replicates and notes; data considered valid and flagged accordingly (103) if the average is representative.
    - Calibration range: Values above calibration range can be valid if remeasurement was not possible.
    - Missing data: Represented as -9999 in measurement fields when data or metadata are incomplete.
  - Data status: Final dataset contains accepted values with appropriate flags; EMEP data flags and meanings compiled in accompanying documentation (per EMEP/UK-AIR conventions).

- Data Flags and Coding
  - Examples of data flag purposes:
    - Valid/invalid status (e.g., 1 for valid, -1 for not valid).
    - Reasons such as missing measurement, below detection limit, above range, sampling anomalies, contamination, or local influence.
  - Data status codes correspond to UK/EMEP flag definitions, aiding interpretation of data quality and provenance.

- Site Information and Instrument Details
  - Indoor site:
    - Location: Hall of the dwelling.
    - Coordinates: 55.64072, -3.59705.
    - Inlet height: 1.5 m above ground.
    - Start date: 01/01/17; End date: Ongoing.
  - Outdoor site:
    - Location: Garden of the dwelling.
    - Coordinates: 55.64072, -3.59705.
    - Inlet height: 1.5 m above ground.
    - Start date: 01/01/17; End date: Ongoing.

- Relevance for Monitoring Frameworks
  - Demonstrates a structured approach to environmental health monitoring with:
    - Clear measurement methodology and replication strategy to improve reliability.
    - Defined data processing workflow from sampler to concentration, including uptake-rate-based conversion.
    - Comprehensive QA/QC rules, including replication precision checks, calibration considerations, and missing data handling.
    - Detailed metadata and dataset documentation to support transparency, reproducibility, and data governance.
  - Highlights potential data governance considerations for monitoring frameworks, such as ensuring metadata completeness, data flagging for quality, and clear data sharing/availability pathways.