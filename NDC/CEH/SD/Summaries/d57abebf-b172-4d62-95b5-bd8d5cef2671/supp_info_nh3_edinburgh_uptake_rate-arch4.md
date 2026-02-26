# Ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, 2022

## Overview
- Initial results from a study to determine the uptake rate for ALPHA® passive samplers used in the UK and similar climates.
- Sampling across four UK UKEAP network sites in 2022; monthly exposure cycles starting at the beginning of each month.
- Local site operations by UKCEH Edinburgh, AFBI Hillsborough, and Ricardo AEA; analysis by CEH Edinburgh.

## UKCEH ALPHA® Sampler Method
- Passive sampler using a citric acid coated filter to capture NH3; protected by a white PTFE membrane facing downwards during exposure.
- Replicate samplers mounted on a shelter at ~1.5 m above ground.
- Analysis: samplers extracted with deionised water; NH3 concentration determined by SEAL AA3 colorimetry; results converted to ambient NH3 concentration using uptake rate of 0.0038422 m3 h-1 and exposure duration.

## Data management and quality assurance
- Data flagged for concerns; final dataset named submissions_ED_UR_NH3_2022.csv; includes site identifiers and spatial metadata.
- Quality rules applied:
  - Coefficient of variation (CV) of replicates < 15% considered valid (flagged as 103 if representative).
  - Values above calibration range may be valid if instrument issues prevented re-run.
  - Missing data marked as -9999.
- Data capture and validity fields accompany measurements; detailed EMEP flags are provided to indicate data status and issues.

## Dataset structure and metadata
- Each row represents one month of data for a single site.
- Columns include: site id, site name, network_id (ED_UR), parameter_id (alpha_NH3_g), measurement start/end dates and times, ammonia concentration (µg NH3 m-3), less-than flag, verification id, unit id (24 = µg NH3 m-3), data capture percentage, validity_id (1 = valid, -1 = not valid), EMEP flag, Month-Year, and Comments.
- The final dataset contains the accepted data values with appropriate flags and notes.

## Data flags and interpretation
- EMEP-related flags documented to indicate data capture quality, validation status, and potential issues (e.g., contamination, detection limits, sampling duration).
- Examples include:
  - 999: missing measurement
  - 781/780: values around detection/quantification limits
  - 103: CV of replicates >15% but still considered valid
  - Various codes indicating contamination, local influences, or sampling conditions

## Site information
- Edinburgh uptake rate OTC: start 01/03/2020; ongoing; coordinates 55.863150, -3.209845; sampler height 1.5 m; collocated with UKA00128.
- Auch: start 01/03/2020; ongoing; coordinates 55.792160, -3.242900; collocated with UKA00451.
- Hills: start 01/03/2020; ongoing; coordinates 54.452500, -6.083340; collocated with UKA00293.
- Chilbolton: start 01/01/2021; ongoing; coordinates 51.149617, -1.438228; collocated with UKA00614.

## Practical implications for data strategy
- Demonstrates a structured data lifecycle: standardized sampling, replicates for reliability, formal data processing pipeline, and explicit QC flags for transparency.
- Rich metadata supports data discoverability, provenance, and reuse across networks.
- Clear data structure and flagging enable quick assessment of data quality and reliability for downstream analysis and policy support.
- Highlights ongoing needs for data coordination, standard metadata, and timely quality checks to maintain trust and utility across multiple sites and partners.