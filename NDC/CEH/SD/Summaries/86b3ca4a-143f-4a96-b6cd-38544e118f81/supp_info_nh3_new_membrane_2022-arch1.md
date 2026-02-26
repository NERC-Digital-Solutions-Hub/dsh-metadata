# Monthly ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, new membrane validation, 2022

## Overview
- Report of initial results validating a new PTFE membrane for ALPHA® passive ammonia samplers.
- Work conducted and analysed across UKCEH Edinburgh, with duties shared by UKCEH, AFBI (Hillsborough), and Ricardo AEA (Chilbolton).

## Methodology

- UKCEH ALPHA® sampler
  - Passive sampler measuring NH3 in air using a citric acid coated filter.
  - PTFE membrane protects the filter; membrane oriented downwards during exposure.
  - Replicates used per site for reliable air concentration estimation.
  - Exposed ~1.5 m above ground on a shelter.

- Analysis
  - Exposed samplers extracted into deionised water.
  - NH4 concentration measured by SEAL AA3 colorimetry and converted to NH3 concentration in air.
  - Uptake rate used for conversion: 0.0041741 m3 h-1, based on the new membrane.
  - Exposure duration in hours used to compute average NH3 concentration for the period.

## Data quality and validation

- Data quality rules
  - Coefficient of variation (CV) of replicates: CV < 15% indicates reliable replication; otherwise replicates may be discarded or flagged.
  - Some measurements exceed calibration range but are deemed valid if re-measurement wasn’t possible due to instrument issues.
  - Missing data are marked with -9999; incomplete date/time metadata render concentration calculations impossible.
- Final dataset
  - NH3_New_Membrane_2022.csv containing accepted data with appropriate flags.
  - Includes site identifiers, exposure period start/end dates and times, NH3 concentrations (µg NH3 m-3), and data flags.
- Data structure details (highlights)
  - Columns cover: site id, site name, network_id (NM), parameter_id, measurement start/end dates and times, ammonia concentration, less-than flag, verification id, unit id, data capture percentage, validity_id, EMEP code, Month-Year, and Comments.
  - Data capture and quality flags align with documented EMEP and UK-AIR conventions.

## Data flags and EMEP codes

- Common flag semantics
  - 103: Valid measurement with CV of replicates >15%—assessed for representativeness.
  - -1: Not valid; missing data or invalid measurement.
  - 1: Valid measurement (flags simplified in text; full mapping provided via EMEP codes).
- EMEP flag details cover
  - Data capture status (e.g., 0 or 1), validity, and various reasonings (e.g., detection limit, contamination, nearby activities, sampling anomalies, etc.).
  - Examples include codes for detection limit below, estimation in range, contamination concerns, and sampling conditions (e.g., agricultural or industrial influences).

## Dataset contents and structure

- Final dataset: NH3_New_Membrane_2022.csv
  - Rows: one row per month per site.
  - Key fields: site name, start/end dates, exposure period, NH3 concentration (µg NH3 m-3), data flag.
- Site and measurement metadata
  - Site identifiers and names, network_id, parameter type (alpha_NH3_g), measurement period, and data status flags.
  - Values expressed as monthly average NH3 concentration for the exposure period.

## Sites and uptake information

- Four UKEAP network sites (monthly measurements conducted at each):
  - Edinburgh uptake rate OTC
  - Edinburgh uptake rate Auch
  - Edinburgh uptake rate Hills
  - Edinburgh uptake rate Chilbolton
- Site details
  - Start dates: e.g., 01/03/2020 or 01/01/2021, ongoing end dates.
  - Coordinates:
    - OTC: latitude 55.863150, longitude -3.209845
    - Auch: latitude 55.792160, longitude -3.242900
    - Hills: latitude 54.452500, longitude -6.083340
    - Chilbolton: coordinates not fully listed here, but included in collocated sites.
  - Inlet height: 1.5 m above ground
  - Collocated with specific UKA identifiers (e.g., UKA00128, UKA00451, UKA00293, UKA00614)

## Practical considerations for analysts

- Data availability and scale
  - Validation focuses on new membrane performance; monthly data provide a basis for detecting seasonal or site-specific patterns.
- Data integration
  - Data from multiple datasets require harmonisation, especially with flag meanings and calibration status.
- Interpretation
  - Use replicates and CV-based validity checks to assess reliability; pay attention to data capture and potential contamination or anomalies flagged by EMEP codes.
- Reproducibility
  - Final dataset includes metadata and flags to enable auditability and discoverability of raw data and processing logic.