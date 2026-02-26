# Sup_Doc_NH3_SouthLanarkshire_indoors&outdoors

## Overview
- Location: two sites in a rural area of South Lanarkshire (one indoor in a dwelling hall, one outdoor in the dwelling garden) adjacent to grassland on a dairy farm.
- Responsibility: dwelling owner handles site operation; Centre for Ecology and Hydrology (CEH) Edinburgh performs analysis.
- Purpose: measure ammonia (NH3) concentrations in air using CEH ALPHA® passive samplers; monthly exposure cycles.

## Methods

- Sampler and deployment
  - CEH ALPHA® sampler uses a citric acid coated filter to capture NH3; a white PTFE membrane protects the filter.
  - Membrane faces downward during exposure; samplers mounted about 1.5 m above ground on shelter posts.
  - Replicates used per site to improve reliability.

- Analysis workflow
  - Exposed samplers are extracted into deionised water.
  - Water extract analyzed by SEAL AA3 colorimetry to determine ammonium concentration.
  - Ammonia concentration in air calculated from ammonium concentration using a known uptake rate of 0.003241315 m³ h⁻¹ and exposure duration.

- Data handling and quality
  - Data flagged for concerns; raw data reviewed against quality rules.
  - Validity criteria include:
    - Coefficient of variation (CV) of replicates: CV < 15% → valid (flag 103). If >15%, replicates reviewed and may be discarded; otherwise the average is used.
    - Data beyond calibration range can still be considered valid if remeasurements were not possible.
    - Missing data flagged as -9999 for measurement or metadata.
  - Dataset contains accepted values with appropriate flags; documentation includes data structure and codes (e.g., CV rule, calibration range, and other validity flags).

## Data structure and content

- Dataset name: NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv
- Contents
  - Each row represents one month of data for a single site.
  - Columns include: site name, unique site identifier, network_id (RSW), parameter_id (alpha_NH3_g), measurement start/end dates and times, ammonia concentration (µg NH3 m⁻3), data flag, detection-limit flag, verification id, unit id, data capture percentage, validity id, EMEP code, and Month-Year.
  - Concentration units: micrograms NH3 per cubic meter (µg NH3 m⁻3).
- Site information
  - Inside: hall of dwelling; coordinates 55.64072, 3.59705; air inlet height 1.5 m; start 01/01/17; ongoing.
  - Outside: garden of dwelling; same coordinates and height; start 01/01/17; ongoing.
  - Both locations are indoor/outdoor pairings within the same overall site area.

## Data quality and flags

- Quality indicators and flag usage
  - 103: valid measurement with CV of replicates < 15%.
  - Other data flags indicate various data issues or verification statuses; EMEP codes accompany data for status and reason (e.g., below detection, contamination, sampling periodicity, etc.).
- Data integrity
  - Missing data and metadata are denoted (-9999) where applicable.
  - Flags and codes provide context for data consumers on reliability, representativeness, and potential local influences.

## Governance, access, and stewardship

- Operators and analysis
  - Site operation by dwelling owner; analysis conducted by CEH Edinburgh.
- Data management
  - Data are organized with detailed metadata and quality flags to support discoverability, provenance, and cross-network comparability.
  - Final dataset emphasizes accepted data values with accompanying quality and flag information to guide interpretation and use.

## Relevance for data leadership

- Demonstrates end-to-end data workflow from field deployment to laboratory analysis and quality-assured data products.
- Highlights importance of replicates, clear metadata, and standardized quality flags to ensure data is trustworthy for decision-making and cross-network collaboration.
- Provides a concrete example of addressing data accessibility barriers (through explicit data structure, flags, and documentation) to support effective data strategy and governance in environmental monitoring.