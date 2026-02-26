# Sup_Doc_NH3_Edinburgh_Uptake_Rate

## Overview
- Report on initial results to determine the uptake rate for ALPHA® samplers measuring NH3 in air, prepared and analyzed at UK CEH Edinburgh (with AFBI Hillsborough support).
- Local site operator duties performed by CEH and AFBI; analysis by CEH Edinburgh.
- Samplers exposed monthly; first-year data not used for uptake rate calibration due to COVID-19 data losses and insufficient data points.

## Monitoring Methodology
- Sampler: CEH ALPHA® passive sampler with citric acid coated filter to capture NH3; protected by a white PTFE membrane; membrane oriented downwards during exposure.
- Deployment: Replicate samplers (to improve reliability) mounted on a shelter on a pole at ~1.5 m above ground.
- Analysis: Exposed samplers extracted into deionised water; analyzed by SEAL AA3 using colorimetry to determine ammonium concentration.
- Conversion: Ammonia concentration in air calculated from ammonium concentration using a fixed uptake rate of 0.003241315 m3 hr-1 and exposure duration.
- Data structure: Final dataset NH3_Edinburgh_Uptake_Rate_2020.csv contains monthly data per site with site name, exposure period, ammonia concentration (µg NH3 m-3), and a data flag.

## Data Quality, Metadata and Flags
- Data are flagged to indicate concerns; details appear in the accompanying documentation.
- Quality checks:
  - CV of replicates < 15% supports validity; if >15%, replication and notes reviewed; valid results may still be used (flag 103).
  - Some values exceed calibration range but are kept as valid if re-measurement was not possible.
  - Missing data or metadata marked with -9999 (prevents concentration calculation).
- Data status and flags:
  - Includes data capture percentage, validity identifiers (e.g., 1 = valid, -1 = not valid), and data status codes (EMEP flags) to denote verification and data quality issues.
  - Numerous EMEP-related codes specify reasons for data treatment (e.g., detection limits, contamination, nearby activities, representativeness of sampling period, etc.).

## Dataset Contents
- Each row represents one month of data for a single site, with fields:
  - Site name and unique identifier, network_id, parameter_id
  - Measurement start/end dates and times (exposure period)
  - Ammonia concentration (µg NH3 m-3)
  - Below-detection/flag indicators (e.g., less than detection limit)
  - Verification status, unit id, data capture, validity, EMEP code, and month-year
  - Comments on data and other metadata

## Site Information
- Edinburgh uptake rate OTC: start 01/03/2020; end ongoing; coordinates 55.863150, -3.209845; air inlet height 1.5 m; collocated with UKA00128 (UKEAP)
- Auch: start 01/03/2020; end ongoing; coordinates 55.792160, -3.242900; air inlet height 1.5 m; collocated with UKA00451
- Hills: start 01/03/2020; end ongoing; coordinates 54.452500, -6.083340; air inlet height 1.5 m; collocated with UKA00293

## Implications for Monitoring Frameworks
- Demonstrates a structured approach to environmental health monitoring:
  - Use of replicated passive samplers to improve reliability.
  - Clear, standardized calculation of air NH3 concentration from surface measurements via a known uptake rate.
  - Rigor in data quality management, including CV checks, calibration constraints, and explicit data flags.
  - Comprehensive metadata and site information to enable auditability and reproducibility.
- Highlights governance considerations:
  - Necessity to set data management standards at source and publicly share underlying data where feasible.
  - Implementation of data capture metrics and detailed flagging to communicate data quality and limitations to stakeholders.
- Reflects challenges aligned with monitoring frameworks:
  - Data gaps due to external disruptions (COVID-19) impacting calibration and uptake rate determination.
  - Potential barriers such as data access, metadata adequacy, and ensuring timely, up-to-date data across sites.
  - The need for data governance processes to handle flags, verification, and data sharing while maintaining clarity for decision-makers.

## Key Takeaways for Policy and Decision-Making
- When designing environmental monitoring programs, incorporate:
  - Replicate measurements and a well-defined analytic workflow to derive concentrations from uptake rates.
  - A robust quality assurance framework with transparent flagging and metadata requirements.
  - Clear documentation of site-specific details (location, height, collocation) to support interpretation and comparability.
  - Contingency plans for data gaps and disruptions to calibration to maintain continuity in policy-relevant indicators.