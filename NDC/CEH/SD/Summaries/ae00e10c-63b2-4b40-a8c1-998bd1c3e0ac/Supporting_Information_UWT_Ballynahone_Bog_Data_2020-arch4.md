# Supporting_Information_UWT_Ballynahone_Bog_Data_2020

## Purpose and context
- Data originate from a transect across Ballynahone National Park (ASSI/SAC and Ramsar site) in Northern Ireland.
- Collected to assess potential NH3 emissions impact on Ballynahone Bog, a ammonia-sensitive peatland.
- Local site operator: Ulster Wildlife Trust (UWT); analysis conducted by UK Centre for Ecology and Hydrology Edinburgh (UKCEH).
- Sampling timeframe: monthly exposure cycles positioned along a bog transect.

## Methodology
- UKCEH ALPHA® samplers used as passive detectors for NH3.
- Sampling setup:
  - Citric acid coated filter captures ammonia.
  - PTFE membrane protects the filter; membrane oriented facing down during exposure.
  - Replicate samplers (to improve reliability) mounted on shelters on poles at ~1.5 m above ground.
- Analysis workflow:
  - Exposed samplers extracted into deionised water.
  - Water analysed by SEAL AA3 using colourimetry to determine ammonium concentration.
  - Ammonia concentration in air calculated from sampler data using a known uptake rate (0.003241315 m3 h-1; 2020 calibration) and exposure duration.
- Data quality checks:
  - Data flagged where concerns arise (detailed on page 4 of the document).

## Data processing and units
- Raw results converted to average ammonia concentration in air for the exposure period.
- Final dataset values expressed as micrograms of NH3 per cubic metre of air (µg NH3 m-3).

## Data structure and dataset
- Final dataset: UWT_Ballynahone_Bog_Data_2020.csv.
- Structure:
  - Each row represents one month of data for a single site.
  - Columns include: site name (and unique site identifier), network_id, parameter_id, exposure start/end dates and times, ammonia concentration, and data flag.
  - Concentration values are the monthly average NH3 concentration for the specified exposure period.
- Data dictionary details:
  - Columns cover: site name, unique site ID, network_id, parameter_id (alpha_NH3_g), measurement dates/times, measurement value, "less than" indicator (detection limit), verification ID, unit ID (24 = µg NH3 m-3), data capture percentage, validity flag, EMEP code, and Month-Year.
- Data quality flags and status:
  - Final data are flagged with various quality markers; site-specific details and data contents are provided on pages 3–5 of the document.

## Data quality and flags
- Quality rules applied:
  - Coefficient of variation (CV) < 15% across replicates: considered valid (flagged as 103). If CV ≥ 15% and replicates are discardable, data may still be considered valid after review.
  - Samples exceeding calibration range but deemed valid (no rerun possible due to instrument issues).
  - Missing data or metadata: indicated with -9999 in measurement or metadata fields.
- EMEP flags provide context about data capture and validity, with numerous codes indicating issues such as contamination, detection limits, calibration concerns, or representativeness. Examples include:
  - 999: Data capture = 0; Valid/Invalid = -1; Reasoning = Missing measurement.
  - 781/780/654/653/652: Various representativeness and contamination indicators.
  - 103: CV of replicates >15% but valid measurement.
- Data capture and validity fields accompany each record to facilitate data quality assessment.

## Site information
- Ballynahone bog site set includes eight locations:
  - Ballynahone bog_1 to Ballynahone bog_8
  - Start date: 01/09/2014 for all sites
  - End date: Ongoing
  - Coordinates (latitude, longitude) provided for each site
  - Height of air inlet above ground: 1.5 m for all sites
- The dataset tracks monthly data across these eight sites along the transect.

## Governance, provenance, and accessibility
- Data are collected by UWT with analysis by UKCEH Edinburgh.
- Documentation includes a detailed data dictionary, site information, and quality flags to support transparency, traceability, and re-use.
- The accompanying notes indicate quality concerns may be present (as per page 4), and the dataset contents are described across pages 3–5.

## Implications for data strategy and leadership
- Demonstrates the need for:
  - Well-documented data collection methods and processing workflows to ensure reproducibility.
  - Clear data quality criteria and flagging to communicate reliability and limitations to stakeholders.
  - Comprehensive metadata (sampling method, uptake rates, unit definitions, and data status codes) to support discoverability and cross-team use.
  - Collaboration across organizations (operator and analytical partner) to maintain data integrity and enable broader data sharing.
- Data leaders can leverage this example to:
  - Define data product requirements (structure, units, flags, and documentation).
  - Prioritize data governance tasks (metadata completeness, QA procedures, and data provenance).
  - Identify data gaps (granularity, representativeness, or spatial coverage) and plan collaborations to address them.