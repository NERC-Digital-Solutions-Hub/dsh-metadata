# Monthly ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, new membrane validation, 2022

## Overview
- Initial results from validating a new PTFE membrane for ALPHA® samplers used to measure atmospheric NH3.
- Sampling and analysis are performed by UKCEH Edinburgh and partner sites (AFBI Hillsborough and Ricardo AEA Chilbolton); local site operator duties shared among UKCEH Edinburgh staff.
- Samplers are exposed in monthly cycles at the start of each month; results are converted to average NH3 concentration in air using a specific uptake rate.

## UKCEH ALPHA® Sampler Method
- Passive samplers use a citric acid coated filter to capture ammonia; a white PTFE membrane protects the filter and allows diffusion of NH3.
- Membrane is oriented downwards during exposure; samplers are mounted on a shelter at about 1.5 m above ground.
- Replicates are used per site to improve reliability.
- Analysis: exposed samplers are extracted in deionised water and analyzed with SEAL AA3, which uses colorimetry to determine ammonium concentration.
- NH3 concentration in air for the exposure period is calculated using the sampler’s uptake rate (0.0041741 m3 hr-1) and the exposure duration.
- Data flagged for quality concerns; the final dataset is NH3_New_Membrane_2022.csv and units are micrograms per cubic metre (µg NH3 m-3).

## Data structure and content
- The final dataset contains one row per month per site, with:
  - Site ID, Site name, network_id (NM), parameter_id (alpha_NH3_g)
  - Measurement start date/time and measurement end date/time (exposure period)
  - Measurement (ammonia concentration in µg NH3 m-3)
  - Less than indicator (-9999 for missing or below detection)
  - Verification id (1: Verified, 2: Preliminary verified, 3: Not verified)
  - Unit id (24 = µg NH3 m-3)
  - Data capture percentage
  - Validity_id (1 = valid, -1 = not valid)
  - EMEP code and related flags (data status and validation details)
  - Month-Year and Comments
- The dataset includes a detailed header describing the column meanings and data status.

## Data quality and flags
- Quality checks:
  - CV of replicate ALPHA samplers: if CV < 15%, data is considered valid (flag 103). If CV > 15%, data are evaluated to decide whether to discard replicates; if the average is representative, the data remain valid with flag 103.
  - Data greater than calibration range may still be considered valid if re-measurement was not possible.
  - Missing data are represented as -9999 in the concentration field.
- Data status and flags:
  - EMEP flags provide additional context (e.g., detection limits, contamination, sampling anomalies, nearby activities).
  - Examples include codes indicating below detection limit, below quantification limit, contamination, or other valid/invalid reasons, with accompanying reasoning.
  - Overall data validity is captured by the Validity_id field (1 = valid, -1 = not valid) and related EMEP status codes.
- The dataset also includes a data capture percentage field to indicate completeness per row.

## Site information
- Four sites in the UKEAP network with uptake rate details:
  - Edinburgh uptake rate OTC (start 01/03/2020; ongoing)
    - Latitude 55.863150, Longitude -3.209845; air inlet height 1.5 m; collocated with UKEAP UKA00128
  - Edinburgh uptake rate Auch (start 01/03/2020; ongoing)
    - Latitude 55.792160, Longitude -3.242900; air inlet height 1.5 m; collocated with UKEAP UKA00451
  - Edinburgh uptake rate Hills (start 01/03/2020; ongoing)
    - Latitude 54.452500, Longitude -6.083340; air inlet height 1.5 m; collocated with UKEAP UKA00293
  - Edinburgh uptake rate Chilbolton (start 01/01/2021; ongoing)
    - Latitude 51.149617, Longitude -1.438228; air inlet height 1.5 m; collocated with UKEAP UKA00614

## Access and usage notes
- The dataset NH3_New_Membrane_2022.csv contains the accepted concentration values and flags for quality and data status.
- Additional dataset structure details are provided on pages referenced in the document (e.g., page 3 for contents, page 4 for data flags, page 5 for site names and identifiers).
- Units are µg NH3 m-3; monthly exposure periods are used for the reported concentrations.

## Practical takeaways for data support and product development
- Data are produced from multiple organizations and laboratories, requiring careful integration and harmonization of formats and flags.
- Clear documentation of data quality rules (CV criteria, calibration range, missing data handling) supports end-user trust and correct interpretation.
- The inclusion of replication quality indicators, data capture percentages, verification statuses, and EMEP flags enables nuanced data filtering for self-serve analytics, dashboards, or reporting products.
- For broader adoption, ensure end users understand how to interpret CV-based validity, detection/quantification limits, and flag reasons, as well as the site-specific context from the four monitoring locations.