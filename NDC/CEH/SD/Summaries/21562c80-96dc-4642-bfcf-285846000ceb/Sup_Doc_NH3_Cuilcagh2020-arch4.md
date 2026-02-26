Sup_Doc_NH3_UWT_Cuilcagh

## Overview
- Study area: around Cuilcagh in Ireland and Northern Ireland to observe how local ammonia levels affect vegetation.
- Roles: Ulster Wildlife Trust (site operations) and UK Centre for Ecology and Hydrology Edinburgh (analysis).
- Data aim: generate monthly NH3 air concentration data using UK CEH ALPHA samplers; inform understanding of ammonia exposure on vegetation.

## Data Collection and Measurement Methods
- Passive sampling with UK CEH ALPHA samplers using citric acid coated filters and a PTFE membrane; membrane oriented downwards during exposure.
- Samplers deployed at ~1.5 m above ground; mounted in shelters on poles; triplicate samplers per site for reliability.
- Exposure cycle: monthly, at the start of each month.
- Analysis: exposed samplers dissolved in deionised water; SEAL AA3 colorimetry to determine ammonium concentration; ammonia concentration in air calculated using known sampler uptake rate (0.003241315 m3 h-1), exposure duration, and lab blanks.
- Data are flagged where concerns arise and are included in the final dataset with quality notes.

## Data Processing and Quality Assurance
- Raw data quality checks applied:
  - Coefficient of variation (CV) of replicates < 15% deemed valid; higher CV prompts evaluation of replicates or notes.
  - Values > calibration range may be reported if rerun was not possible; still considered valid.
  - Missing data or metadata marked as -9999.
- Final dataset NH3_Cuilcagh2020.csv contains accepted values with appropriate flags.
- Data flags include site validity, verification status, data capture, and EMEP status codes to indicate measurement issues, validation, or contextual notes.
- EMEP coding captures reasons such as detection limits, contamination, sampling period adjustments, and other data quality annotations.

## Data Content and Structure
- Dataset: NH3_Cuilcagh2020.csv; each row represents one month of data for a single site.
- Key columns (examples):
  - Site name, unique site identifier, network_id (RSW)
  - Parameter_id (alpha_NH3_g)
  - Measurement start/end dates and times
  - Ammonia concentration (units: µg NH3 m-3)
  - Less than detection flag, verification id, unit id (24 = µg NH3 m-3)
  - Data capture percentage, Validity_id (1 = valid, -1 = not valid)
  - EMEP code and Month-Year
  - Comments
- Data are presented as monthly average concentrations for the exposure period.

## Site Information
- Sites included:
  - Boardwalk
  - Eshvagh
  - Corcashel
  - Grouse Project
  - Shridrinagh
- Each site has:
  - Start date: 01/02/2020
  - End date: Ongoing
  - Latitude and Longitude
  - Height of air inlet: 1.5 m
- Spatial identifiers and location metadata accompany the data values to support geospatial analyses and cross-site comparisons.

## Data Governance and Access
- Data provenance documented: sampling by Ulster Wildlife Trust; analysis by UK CEH Edinburgh.
- Dataset includes detailed metadata for each observation (dates, times, site, QA flags, and metadata flags).
- Data discovery is facilitated by explicit fields for site, network, measurement parameters, and metadata flags, supporting harmonization with broader ammonia data networks.

## Implications for Data Leaders
- Illustrates end-to-end data lifecycle: field collection, laboratory analysis, calculation to ambient concentration, and QA-driven flagging.
- Highlights importance of: 
  - Clear data standards and metadata (e.g., site IDs, network IDs, parameter IDs, timestamps, units, QA flags).
  - Replicate-based QA (CV checks) and explicit handling of data outside calibration ranges.
  - Use of standardized QA codes (EMEP flags) to communicate data quality and context.
  - Documentation of data provenance and collaboration across organizations for trust and reuse.

## Recommendations for Data Strategy and Community Engagement
- Strengthen data standardization:
  - Maintain uniform naming conventions, units, and metadata fields across datasets to improve interoperability.
  - Align QA flag definitions with broader data communities (e.g., EMEP) and provide human-readable mappings.
- Improve data discoverability and reuse:
  - Centralize datasets with clear data dictionaries, provenance statements, and access guidelines.
  - Provide data products at multiple levels (raw, quality-checked, aggregated) to serve diverse user needs.
- Enhance governance and collaboration:
  - Define co-ownership and governance roles for cross-network ammonia data initiatives.
  - Create a feedback loop with data users (policy colleagues, researchers) to ensure data products meet user needs and drive iterative improvements.
- Address data gaps and barriers:
  - Identify data gaps in spatial/temporal coverage and pursue coordinated data collection to reduce fragmentation.
  - Document data limitations and assumptions transparently to support informed use in vegetation impact assessments and policy contexts.