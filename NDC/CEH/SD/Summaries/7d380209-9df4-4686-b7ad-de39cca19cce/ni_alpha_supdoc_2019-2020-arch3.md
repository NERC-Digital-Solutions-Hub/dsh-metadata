# Monthly atmospheric ammonia concentration data from Northern Ireland ALPHA ® Ammonia Monitoring Network, 2019-2020

- A description of the NI ALPHA® Ammonia Monitoring Network data for 2019 and 2020, comprising monthly NH3 concentration data from 25 sites, with additional DELTA® measurements at 4 sites and one co-located site for method inter-comparison.
- The network supports model validation and calibration (e.g., FRAME) and aims to improve confidence and reduce uncertainty in NH3 modelling and deposition estimates (CBED framework).

## Overview and purpose

- Network: ALPHA® passive samplers deployed at 25 sites across Northern Ireland (24 rural, 1 urban) plus DELTA® measurements at related NI sites; co-located site used for inter-method comparison.
- Primary use: validate and calibrate atmospheric NH3 models and deposition estimates, informing policy scenarios and emissions inventories.
- Operators and funding: joint operation by AFBI and UKCEH; DAERA funding.
- Data products: clean, ratified NH3 concentrations (µg NH3 m-3) with detailed quality flags for reliability and traceability.

## Experimental design and monitoring network

- NAMN context: NI contributes three NAMN sites; this expansion provides broader spatial coverage and improved spatio-temporal NH3 data.
- Sampling approach: monthly, time-integrated sampling using high-sensitivity ALPHA® passive samplers mounted at ~1.5 m height; remote site visits for sampler exchange.
- Spatial coverage and sources: sites cover cattle, sheep, pigs, poultry, non-agricultural and background sources to characterize local emission signatures and enable validation of transport models against measured NH3.

## Methods and data collection

- Analyte and units: atmospheric NH3 measured, reported as µg NH3 m-3.
- Sampling technology: UKCEH ALPHA® passive samplers with citric acid impregnation; samples exposed monthly, with triplicate samplers for each measurement to estimate precision.
- Analysis: NH4+ from citrate-coated filters converted back to NH3 concentration; lab analysis via colorimetry on SEAL system; uptake rate used to estimate air volume sampled.
- Calibration and detection: annual uptake rates previously field-calibrated; limit of detection (LOD) 0.03 µg NH3 m-3.

## Data processing, quality control, and ratification

- Data management system: AAGA Oracle-based database and ShinyApp automate calculation of NH3 concentrations and QC flags.
- Three-stage data quality process:
  - Stage 1: automated QC flags and consistency checks (date overlaps, monthly exposure windows, replicate precision, outliers, missing samples).
  - Stage 2: manual review of laboratory blanks, sampling malfunctions, outliers (low and high), and corrective actions.
  - Stage 3: expert/project manager review assessing site knowledge, expected patterns, seasonal trends, and cross-site/ co-located comparisons; ratification decisions lead to a final time-stamped, versioned dataset.
- Output: a standardized, ratified dataset with data values, flags, and metadata; records correspond to one month of data per site.

## Data structure and contents

- Core dataset fields (examples):
  - site_id, site_name, network_id, parameter_id
  - measurement_start_date/time, measurement_end_date/time
  - measurement (NH3 concentration, µg m-3)
  - less_than (LOD indicator), verification_id, unit_id
  - data_capture (0 missing/rejected, 100 accepted), validity_id (1 valid, -1 invalid)
  - EMEP_code (flagging status across verification and data flags)
  - MONTH, YEAR, Comments
- Data are time-integrated monthly concentrations; site locations are provided with coordinates (rounded for confidentiality).

## Data flags and harmonisation

- Flags based on EBAS/EMEP conventions, grouped into three main categories:
  - V (Valid) and I (Invalid) and M (Missing) data, with sub-flags addressing issues such as contamination, sampling anomalies, instrument problems, and values relative to detection limits.
  - Examples include flags for co-location data, contaminated filters, sample period deviations, extreme values, and corrected data entries.
- Flag usage aligns NI NAMN practices with broader European monitoring standards for consistency and cross-network comparability.

## Modelling links and policy relevance

- Data underpin:
  - Calibration and validation of the FRAME model and derivation of Frame-based NH3 deposition estimates (CBED).
  - Assessment of how policy scenarios affect NH3 concentrations and related deposition outcomes.
- Co-located DELTA measurements provide cross-method validation to support robust interpretation of concentrations.

## References and resource locators

- EN 17346 (2020): standard method for NH3 determination using diffusive samplers.
- NAMN and ALPHA®/DELTA® monitoring methodology and uptake rate calibrations.
- FRAME model information; CBED concentration-based deposition framework.
- EBAS/EMEP flag lists and data submission standards for cross-network compatibility.

## Considerations and challenges for monitoring frameworks

- Data gaps and access: ensuring timely access to complete datasets and maintaining consistent metadata.
- Data governance: maintaining robust data processing, version control, and transparent flagging/rating procedures.
- Inter-organisational silos: coordinating data sharing and harmonising flags across NI networks and higher-tier European frameworks.
- Metadata quality: ensuring complete, accurate site, method, and sampling details to support reproducibility and data integration.
- Communication of findings: translating complex QC and flag information into accessible, policy-relevant insights.