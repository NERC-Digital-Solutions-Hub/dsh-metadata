# Passive sampler ammonia measurements indoors and outdoors at a rural dwelling in South Lanarkshire, 2021

## Overview
- Two sampling sites in a rural South Lanarkshire dwelling: inside the hall and outside in the garden, adjacent to grassland on a large dairy farm.
- Local site operator duties performed by the dwelling owner; analysis conducted by the Centre for Ecology and Hydrology Edinburgh.
- UKCEH ALPHA® passive samplers used to measure ammonia (NH3) in air; samplers exposed monthly at the start of each month.
- Data processing converts sampler extracts to average NH3 concentration in air using a known uptake rate.

## Methods and Processing
- UKCEH ALPHA® sampler: citric acid coated filter captures NH3; PTFE membrane protects the filter; membrane oriented downwards during exposure; samplers mounted ~1.5 m above ground on a shelter.
- Replicates used per site to improve reliability; samplers are housed in plastic containers for protection.
- Analysis: exposed samplers are extracted into deionised water and analysed by SEAL AA3 using colorimetry to determine ammonium concentration; NH3 concentration in air calculated from ammonium concentration using uptake rate 0.003241315 m3 hr⁻¹ and exposure duration.
- Data quality and flags: data are flagged for concerns; raw data were quality checked against rules.
- Data structure and dataset: final dataset named NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv; rows correspond to one month of data for a single site; columns include site identifier, site name, network id, parameter id, measurement start/end dates and times, ammonia concentration (µg NH3 m⁻3), data flags, verification status, unit id, data capture percentage, EMEP code, Month-Year, and comments.
- Data flags and EMEP: data status codes and EMEP flags are provided (e.g., 999 for missing/m etc.; 781/780 for detection-related notes; 103 for CV >15% but valid; mapping available in EMEP data flag references).

## Dataset contents and metadata
- Contents: monthly measurements per site; columns cover site name/ID, network, parameter, exposure start/end dates/times, concentration, detection/verification flags, units, data capture percentage, validity, EMEP status, Month-Year, and comments.
- Units: concentrations reported as micrograms of NH3 per cubic meter of air (µg NH3 m⁻³).
- Site details: two sites with precise coordinates and exposure details:
  - Inside: start 01/01/17; End ongoing; Latitude 55.64072; Longitude 3.59705; air inlet height 1.5 m; located in the hall of the dwelling.
  - Outside: start 01/01/17; End ongoing; Latitude 55.64072; Longitude 3.59705; air inlet height 1.5 m; located in the garden of the dwelling.

## Quality assurance and validation
- Quality rule: coefficient of variation (CV) of replicates must be <15%; if >15%, replicates are reviewed; if retained, the average is considered representative (flagged as valid, code 103).
- Some samples may exceed calibration range; still considered valid when rerun/dilution is not possible due to instrument issues.
- Missing data or metadata are indicated with -9999 for measurements or missing date/time metadata; such rows cannot be used for concentration calculations.
- Data capture and validity are explicitly recorded; data status codes (EMEP flags) accompany each record to indicate verification status and data quality.

## Data governance, sharing, and stewardship
- Data availability: final dataset contains accepted values with appropriate flags and notes; provenance includes the site, network, and measurement metadata.
- Proposed stewardship actions:
  - Ensure dataset is uploaded to relevant portals and catalogued with complete metadata.
  - Maintain versioning and update procedures; record data capture rates and any reprocessing or re-submissions (verification status field).
  - Provide clear definitions for all fields (site_id, parameter_id, measurement_start/end, data_capture, validity, EMEP flag, etc.) and a mapping for all data flags to their meanings.
  - Align metadata with common data standards to support interoperability with other datasets and portals (including EMEP/UK-AIR conventions).
  - Document data limitations, such as potential delays in data submission, calibration constraints, or instances where data could not be validated.

## Challenges and considerations for data stewards
- Potential gaps between user needs and available metadata; ensure metadata captures user-relevant details (contexts like nearby dairy activities or grassland influence).
- Timely data delivery and completeness of monthly records; manage missing months or fields and communicate limitations.
- Harmonizing data across different systems and formats (e.g., various exposure periods, units, or flag conventions) to enable cross-dataset interoperability.
- Handling large time-series data and legacy databases; ensure the dataset remains accessible and well-documented for future reuse.
- Addressing data quality issues (e.g., high CVs, out-of-range values) with transparent flagging and notes to support re-use.