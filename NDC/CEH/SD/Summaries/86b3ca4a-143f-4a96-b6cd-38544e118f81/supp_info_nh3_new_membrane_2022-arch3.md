# Monthly ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, new membrane validation, 2022

## Overview
- Study purpose: validate a new PTFE membrane for ALPHA® passive samplers and measure NH3 in air across four UKEAP network sites.
- Collaboration: UKCEH Edinburgh, AFBI (Hillsborough), Ricardo AEA (Chilbolton).
- Sampling cadence: monthly exposures at the start of each month; replicates used to improve reliability.
- Target outcome: dataset of ammonia concentrations in air to support environmental monitoring and policy evaluation.

## UKCEH ALPHA® sampler method
- Sampler design: ALPHA® passive sampler with a citric acid coated filter to capture NH3, protected by a white PTFE membrane (membrane facing downward during exposure).
- Deployment: replicate samplers mounted on shelters on poles at ~1.5 m above ground.
- Analysis workflow: exposed samplers extracted into deionised water; NH3 quantified by SEAL AA3 colorimetry; results converted to average NH3 concentration in air for the exposure period.
- Uptake rate: 0.0041741 m3 h-1 for the new membrane, used to convert sample data to ambient NH3 concentration.
- Data quality notes: data flagged where concerns arise; detailed site operator and laboratory notes accompany data.

## Data structure and quality control
- File and dataset: final dataset named NH3_New_Membrane_2022.csv; rows represent one month of data per site; columns include site name, network_id, parameter_id, exposure dates, NH3 concentration, and data flags.
- Key data fields:
  - Site identifier and site name
  - Network identifier (NM)
  - Parameter type (alpha_NH3_g)
  - Measurement start/end dates and times
  - NH3 concentration (µg NH3 m-3)
  - Flags for detection limit, verification status, data capture percentage, and data validity
  - Data status codes and EMEP-related flags
  - Month-Year and comments
- Data capture and validity:
  - Valid data require a CV of replicates < 15% (flagged as 103 if valid measurement).
  - Values outside calibration range may be present but can remain valid if not re-run.
  - Missing measurements are represented by -9999; incomplete metadata prevents calculation.
- Data flags and metadata (EMEP-related codes):
  - Examples of common codes: 999 (missing data), 781 (below detection limit, valid), 780 (below detection/quantification limit), 668/660 (valid with specific considerations), 653/652/651 (reasonable sampling conditions with local influences), among others.
  - Data status and reason codes provide context for validity, contamination, and local influences (e.g., traffic, agricultural activity, industrial contamination).

## Dataset contents and accessibility
- The dataset contains:
  - Site identifiers, site names, network IDs, parameter types
  - Exposure start and end dates and times
  - Monthly ammonia concentration values in µg NH3 m-3
  - Data capture percentages and validity indicators
  - Verification status and EMEP data flags
- Documentation notes:
  - The contents and structure are detailed (e.g., page references in the original document describe site names, spatial identifiers, and data fields).
  - Observations and flags are provided to aid independent verification and transparent data governance.

## Site information
- Sites and setup:
  - Edinburgh uptake rate OTC (collocated with UKA00128)
  - Auch uptake rate (collocated with UKA00451)
  - Hills uptake rate (collocated with UKA00293)
  - Chilbolton uptake rate (collocated with UKA00614)
- Spatial context: each site includes coordinates (latitude and longitude) and the height of the air inlet (1.5 m) above ground.
- Timeframe: uptake rate data are ongoing, with start dates around 2020 onward; Chilbolton monitoring begins 2021.

## Governance, challenges, and relevance to monitoring frameworks
- Data governance and openness:
  - Emphasis on being able to share underlying data; datasets include comprehensive metadata and data flags to support transparency.
  - Quality assurance steps cover data cleaning, transformation, and clear presentation of findings (through dataset tables and accompanying notes).
- Common challenges addressed:
  - Data gaps and metadata gaps: procedures to flag missing data (-9999) and to annotate metadata and calibration status.
  - Access and interoperability: standardised dataset structure with explicit field definitions and quality flags to facilitate reuse and cross-site comparisons.
  - Data silos and governance needs: distributed collaboration among institutions with a centralized dataset and clear data-status/EMEP flagging for consistent interpretation.
- Relevance for policy and monitoring:
  - Provides validated NH3 concentration measurements using a newly validated membrane, enabling more robust environmental health monitoring.
  - Supports evaluation of ammonia exposure trends across multiple UK sites, informing air quality assessments and policy decisions.