# Monthly atmospheric ammonia concentration data from Northern Ireland ALPHA ® Ammonia Monitoring Network, 2019-2020

## Overview
- Two data files record monthly atmospheric NH3 concentrations from 25 NI ALPHA® Monitoring Network sites for 2019 and 2020.
- Additional NH3 data (2019-2020) were collected at 4 sites using the UKCEH DELTA® method; one site was co-located with ALPHA® for inter-comparison.
- Network operated by AFBI and UKCEH; funded by DAERA.
- Data are used to validate and calibrate NH3 atmospheric models (e.g., FRAME) and to support CBED deposition estimates, improving understanding of policy impacts on NH3.

## Monitoring Network and Methods
- ALPHA® passive samplers (high-sensitivity) measure NH3 in air via citric acid-coated filters; samples exposed monthly.
- NH3 concentration derived from NH4+ on filters, converted to NH3 using a 17/18 factor; air volume sampled estimated from an annual field-calibrated uptake rate.
- 2019 uptake rate: 0.0031665 m3 h-1; 2020 uptake rate: 0.0031277 m3 h-1; LOD: 0.03 µg NH3 m-3.
- Sample processing includes extraction of NH4+ and colorimetric analysis; data managed in the AAGA Oracle database with automated calculation via a ShinyApp.

## Experimental Design and Sites
- NAMN in NI expands spatial coverage beyond the UK NAMN three-site presence in NI.
- 25 ALPHA® sites (24 rural, 1 urban) provide broad spatial distribution to compare with atmospheric transport models and to support validation of near-ground NH3 modelling.
- Hillsborough site targeted for evaluating local farm emissions; other sites cover diverse emission sources (agricultural, non-agricultural, and background).
- 2019-2020 site list includes coordinates (to two decimals for confidentiality) and start dates; most sites ongoing, with some DELTA-only sites.
- DELTA® sites (including Hillsborough) contribute additional gas and aerosol data, reported in a companion submission to EIDC.

## Quality Control and Data Processing
- Data are stored and processed in the AAGA system; NH3 concentrations are time-integrated monthly values (µg NH3 m-3).
- Three-stage QA process:
  - Stage 1: Automated QC with EBAS/EMEP flags; checks for date overlaps, monthly exposure windows, replicate precision, outliers, and missing samples.
  - Stage 2: Manual data review; assess lab blanks, sampler malfunctions, low/high outliers, and contamination assessments.
  - Stage 3: Expert review by experienced air-quality scientists; consider site knowledge, expected trends, year-to-year comparisons, inter-site comparisons, and co-locations.
- Data are released as time-stamped, version-controlled outputs with a “Ratified” status once all checks are satisfied.
- Missing data are flagged (e.g., -9999) and marked invalid where appropriate.
- Automated and manual QC flags follow EBAS/EMEP conventions to indicate data quality and issues.

## Data Structure and Flags
- Core dataset fields include: site_id, site_name, network_id (AFBI), parameter_id (alpha_NH3_g), measurement_start/end dates and times, concentration value, LOD indication, verification status, unit, data_capture, validity, EMEP flag, month, year, and site comments.
- Values are reported as monthly, site-level NH3 concentrations (µg m-3).
- EBAS/EMEP data flags cover V (valid), I (invalid), M (missing) with extensive sub-flags for issues such as contamination, instrument problems, sampling anomalies, and co-located measurements.
- Flags also denote values below detection limit, sampling period anomalies, and other data-quality notes. A complete flag set aligns with EBAS/EMEP standards and is used across UK-NNAM networks for consistency.

## Modelling, Policy Relevance, and Data Access
- NH3 measurements support calibration/validation of atmospheric dispersion and deposition models (e.g., FRAME, CBED).
- Data provide regional evidence to evaluate policy scenarios affecting NH3 emissions and deposition.
- Coordinated data submission and flagging across NI, NI DELTA, and broader UK networks ensures harmonised data use in national assessments and modelling.

## References and Resources
- EN 17346 (2020): Ambient air - Standard method for determination of ammonia using diffusive samplers.
- Key methodological and modelling references supporting sampling, calibration, and deposition modelling.
- Resources for NAMN/ALPHA and FRAME/CBED information, and EBAS flag lists are provided for data context and standard practices.