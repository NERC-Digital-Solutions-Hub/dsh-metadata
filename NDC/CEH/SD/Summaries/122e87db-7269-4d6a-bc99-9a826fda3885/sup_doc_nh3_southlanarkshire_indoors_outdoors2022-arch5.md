# Passive sampler ammonia measurements indoors and outdoors at a rural dwelling in South Lanarkshire, 2022

## Overview
- Two monitoring sites in a rural South Lanarkshire dwelling: one indoor (hall) and one outdoor (garden).
- Site operator duties performed by the dwelling owner; analysis conducted by the Centre for Ecology and Hydrology Edinburgh.
- Measurement period described as monthly exposure cycles; data pertain to 2022.
- Dataset and metadata are prepared to support reuse and discovery, with QA flags and provenance documented.

## Measurement method
- Instrument: CEH ALPHA® passive samplers using a citric acid coated filter to capture NH3; PTFE membrane protects the filter.
- Exposure: samplers deployed at ~1.5 m above ground, in replicate pairs, on shelters.
- Analysis: exposed samplers extracted into deionised water and analyzed by SEAL AA3 colorimetry to determine ammonium concentration; NH3 concentration in air calculated using uptake rate of 0.0038422 m3 h-1 and exposure duration.
- Spatial/temporal details: two sites (indoor and outdoor) with monthly exposure cycles; sampling protocol described in detail with figures referenced.

## Data processing and quality assurance
- Data flagged for quality concerns; final dataset NH3_SouthLanarkshire_indoors_outdoors2022.csv contains accepted values with flags.
- Quality rules:
  - Coefficient of variation (replicates) < 15% deemed valid; higher CV leads to evaluation of replicates or notes.
  - Values above calibration range may be valid if remeasurement/remediation not possible.
  - Missing data indicated by -9999 for measurement or metadata.
- Data structure:
  - Each row represents one month of data for a single site.
  - Key columns include site name, unique site identifier, network_id, parameter_id, measurement start/end dates and times, concentration (µg NH3 m-3), detection limit flag, verification status, unit id (µg NH3 m-3), data capture percentage, validity flag, EMEP code, and Month-Year.
- Data flags and codes:
  - EMEP flags are provided (e.g., data capture, validity, and reason codes such as contamination, below detection limit, sampling anomalies, etc.).
  - Examples include codes for valid measurements, contamination indicators, sampling anomalies, and other data quality issues.
- Data provenance: site names and spatial identifiers are documented; data capture percentage and validation status accompany each observation.

## Dataset contents and metadata
- Dataset name: NH3_SouthLanarkshire_indoors_outdoors2022.csv.
- Structure: contains monthly NH3 concentration data for each site, with associated metadata and quality flags.
- Units: micrograms of NH3 per cubic meter of air (µg NH3 m-3).
- Site information: indoor site located in hall; outdoor site located in garden; both share coordinates (latitude 55.64072, longitude 3.59705) and air inlet height (1.5 m).
- Start dates: indoor and outdoor sites begin 01/01/17; end dates marked as ongoing.

## Site information
- Indoor site:
  - Start date: 01/01/17; End date: Ongoing.
  - Location: hall of dwelling; coordinates 55.64072, 3.59705; inlet height 1.5 m.
- Outdoor site:
  - Start date: 01/01/17; End date: Ongoing.
  - Location: garden of dwelling; coordinates 55.64072, 3.59705; inlet height 1.5 m.

## Data governance, availability, and practical considerations for data stewards
- Clear metadata and QA framework enable dataset discoverability and reuse across datasets in similar monitoring programs.
- Replicate sampling, detailed measurement dates/times, and extensive flagging support traceability and data quality assessment.
- Data may require ongoing updates or revisions; robust documentation of data flags (especially EMEP-related codes) is essential for interoperability with broader environmental data ecosystems.
- Considerations for stewardship:
  - Maintain consistency of site identifiers and coordinate references across updates.
  - Ensure metadata fields (timestamps, detection flags, data capture) remain populated for each record.
  - Monitor and document any changes to measurement protocols or calibration references to preserve data comparability over time.