# Supporting_Information_UWT_Ballynahone_Bog_Data_2020

## Overview
- Data from a transect through Ballynahone National Park, an ASSI/SAC and Ramsar site in Northern Ireland, collected to assess ammonia NH3 impacts on Ballynahone Bog.
- Ammonia-sensitive peatland ecosystem managed by Ulster Wildlife Trust (UWT); analysis by UK Centre for Ecology and Hydrology Edinburgh.
- Monthly passive sampling along the transect using UKCEH ALPHA samplers to monitor NH3 concentrations.

## Data Collection and Methods
- UKCEH ALPHA® samplers are passive devices with citric acid-coated filters and a PTFE membrane; mounted at ~1.5 m height.
- Replicate samplers used to estimate ambient NH3 concentration; exposed at the beginning of each month.
- Analysis involves extracting samplers into deionised water and measuring ammonium via SEAL AA3 colorimetry; NH3 concentration in air derived using a calibration uptake rate of 0.003241315 m³ h⁻¹ and exposure duration.
- Data flagged to indicate concerns (details on page 4).

## Quality Assurance and Validity
- Raw data quality checks:
  - Coefficient of variation (replicates) must be <15%; if >15%, replicates may be discarded; if representative, data considered valid and flagged as 103.
  - Values exceeding calibration range but deemed valid due to instrument issues (no dilution possible).
  - Missing data indicated by -9999 in data field or missing date/time metadata.
- Final dataset: UWT_Ballynahone_Bog_Data_2020.csv with accepted values and appropriate flags.
- Dataset contents include site identifiers, exposure period, ammonia concentration (µg NH3 m⁻³), and a data flag.

## Dataset Structure and Field Descriptions
- Each row represents one month’s data for a single site.
- Core columns: site name, start date, end date, ammonia concentration for the exposure period, data flag.
- Additional identifiers and metadata: station name, network_id, parameter_id, measurement start/end dates and times, less than detection flag, verification id, unit id, data capture, validity, and EMEP status code.
- Month-Year column provides the time reference (mmm-yy).
- Concentrations are reported in micrograms of NH3 per cubic metre (µg NH3 m⁻³).

## EMEP Flags and Data Status
- EMEP-related flags accompany data to describe capture, validity, and contextual reasoning (e.g., below detection limit, contamination, sampling duration issues, observational validity).
- Example rationales include detection limits, contamination from local sources, and sampling duration considerations.

## Site Information
- Ballynahone bog_1 to Ballynahone bog_8 details:
  - Start_date: 01/09/2014; End date: Ongoing.
  - Latitudes and longitudes: provided for each site.
  - Height of air inlet above ground: 1.5 m.
- Sites form a transect through Ballynahone Bog to monitor spatial variation in NH3 exposure.

## Relevance for Analysts Monitoring the Environment
- Demonstrates standardized, transparent data collection, QA, and reporting aligned with environmental health monitoring practices.
- Replication, calibration, and detailed flagging enable robust interpretation and traceability.
- Structured dataset supports integration with other environmental datasets and wider accessibility of underlying data for policy assessment and monitoring over time.