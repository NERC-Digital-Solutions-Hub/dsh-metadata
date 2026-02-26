# Sup_Doc_NH3_UWT_Cuilcagh

## Overview
- Data from the Cuilcagh area in Ireland and Northern Ireland to observe the impact of local NH3 on vegetation.
- Site operator: Ulster Wildlife Trust; analysis performed by UK Centre for Ecology and Hydrology (CEH) Edinburgh.
- Measurements use UK CEH ALPHA® passive samplers to monitor ammonia concentrations; samplers exposed monthly at the start of each month.

## Sampling and Analysis Method
- Passive ALPHA® sampler: citric acid–coated filter captures NH3; PTFE membrane protects the filter; membrane oriented downward during exposure.
- Exposure setup: replicate samplers (triplicates) attached to shelters on poles at ~1.5 m above ground.
- Analysis workflow: exposed samplers extracted into deionised water; NH3 measured by SEAL AA3 colorimetry; ammonium concentration converted to ambient NH3 using uptake rate (0.003241315 m3 h-1) and exposure duration.
- Data flags indicate data quality concerns; raw data screened against quality rules.

## Data Content and Structure
- Final dataset: NH3_Cuilcagh2020.csv (accepted values with appropriate flags).
- Each row represents one site's monthly measurement; columns include:
  - Site name and unique identifiers (site, network_id, parameter_id)
  - Measurement period: start date/time and end date/time (dd/mm/yyyy and hh:mm)
  - Measured ammonia concentration (µg NH3 m-3)
  - Data qualifiers: less than flag, verification id, unit id (24 = µg NH3 m-3), data_capture %, validity_id, EMEP code, Month-Year, and Comments
- Concentrations are monthly-averaged NH3 in air; units are micrograms per cubic metre.

## Data Quality and Validation
- Quality rule: coefficient of variation (CV) of replicates < 15% indicates reliable replicates; if CV > 15%, data may be reassessed or discarded; valid data flagged as 103.
- Some measurements exceed calibration range but are still treated as valid due to instrumentation constraints.
- Missing data or metadata are encoded as -9999 in the relevant fields.
- The dataset explicitly notes and flags data with concerns (refer to page 4 for specifics).

## Flags and Metadata
- EMEP flags provide context for data validity and data issues. Examples include:
  - 999: Data capture = 0; Valid/Invalid = -1; Reason = Missing measurement
  - 781, 780: Values below detection or below quantification limits; data considered valid
  - 103: CV of replicates >15%; still considered valid measurement
  - Other codes indicate issues such as contamination nearby, atyp sampling period, or laboratory/field anomalies
- Data status and interpretation are captured in the EMEP code field (and related “Reasoning” notes).

## Site Information
- Monitoring sites (start_date 01/02/2020; end_date ongoing; height of air intake 1.5 m) include:
  - Boardwalk: 54.218694, -7.823424
  - Eshvagh: 54.190490, -7.846421
  - Corcashel: 54.187536, -7.973599
  - Grouse Project: 54.130905, -7.896038
  - Shridrinagh: 54.119063, -7.995085
- Each site has a consistent intake height and spatial identifiers to support dataset integration.

## Data Governance, Provenance, and Access
- Responsibility lies with an organisation managing large datasets, ensuring data governance, metadata clarity, and up-to-date datasets.
- Roles include coordinating data from site operators and processing/quality-assuring data before sharing.
- Documentation and data flags are provided to enhance discoverability and reuse by others.

## Considerations for Data Stewards
- Data may reflect an incomplete view of user needs and priorities; ongoing engagement with data creators and users is important.
- Timeliness of data transfer from field sites and adherence to metadata standards are key challenges.
- Compatibility across multiple systems and formats; handling large datasets; and integrating older databases may require bespoke solutions.