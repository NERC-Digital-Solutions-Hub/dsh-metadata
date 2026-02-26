# Supporting information for Ammonia measurements from passive samplers at Fenn ' s, Whixall, Bettisfield, Wem & Cadney (2018)

- Purpose and context
  - Document provides supporting information for atmospheric ammonia measurements collected during the LIFE project under the Site Nitrogen Action Plan (SNAP) at Fenn's, Whixall, Bettisfield, Wem and Cadney Mosses SAC/SSSI.
  - Roles: Natural England operates sites; CEH Lancaster analyzes samples; CEH Edinburgh processes data.
  - Methodology used CEH ALPHA passive samplers, deployed monthly, to support environmental health monitoring and policy evaluation.

- Sampling design and deployment
  - Passive samplers positioned on shelters at approximately 1.5 m above ground.
  - Replicates used to improve reliability of airborne NH3 concentration estimates.
  - Monthly exposure cycles aligned with a regular sampling schedule.
  - Sites associated with the LIFE/SNAP project; site names and coordinates provided in the dataset.

- Analysis and concentration calculation
  - Ammonia captured on a citric acid coated filter protected by a PTFE membrane; diffusion allows NH3 capture.
  - Exposed samplers are extracted into deionised water and analyzed by SEAL AA3 colorimetric method to determine ammonium concentration.
  - Concentrations are converted to average air concentrations using a known uptake rate of 0.0028986 m3 h-1 for the ALPHA samplers (UKEAP 2018).

- Data quality assurance and control (QA/QC)
  - Replicate quality check: coefficient of variation (CV) across replicates must be < 15%; otherwise evaluative steps taken and may result in discarding replicates.
  - Missing samplers treated as invalid (-1) and value set to -9999.00 for missing data.
  - Deviations in sampler duration (longer/shorter exposure than monthly cycle) flagged.
  - Local contamination or anomalous conditions noted; results may be discarded if not representative; final reported data are averages of valid replicates.
  - Data maintained with detailed flags and quality status to support traceability and transparency.

- Final dataset and content
  - Dataset name: FWBWC_ammonia_measurements_2018.csv.
  - Content: accepted monthly ammonia concentration values for each site, with start and end dates, and data flags.
  - Units: micrograms of NH3 per cubic metre of air (µg NH3 m-3).
  - Data structure includes site name, unique site identifier, network id, parameter id, exposure start/end dates and times, concentration, and a data flag.

- Data fields and coding (illustrative)
  - Site information: site name, unique ID, network ID, parameter type.
  - Temporal coverage: measurement start date/time, measurement end date/time.
  - Measurement: ammonia concentration, flag for values below detection limit, verification status, unit ID, data capture percentage, validity flag.
  - Data status: EMEP data status code with associated flags and reasonings (e.g., detection limits, replicate CV, contamination, sampling period adjustments).

- EMEP and quality flags
  - Includes EMEP flag codes to document data quality, validity, and any special considerations.
  - Flags cover issues such as detection limits, contamination, CV of replicates, sampling timing, and local influences.
  - Flags enable transparent assessment of data suitability for policy evaluation and reporting.

- Site information and temporal scope
  - Example sites listed as MM01, MM02, MM03 with coordinates and a 1.5 m inlet height.
  - Start date: 01/07/2018; End date: ongoing for listed sites within the dataset.
  - Location details provided to enable spatial interpretation and integration with other environmental datasets.

- Relevance for monitoring frameworks
  - Demonstrates end-to-end monitoring workflow: site operation, sample collection, laboratory analysis, data processing, QC, and data dissemination.
  - Emphasizes importance of metadata, replicates, and provenance for data governance and decision-making.
  - Highlights common monitoring challenges (weather-related data gaps, animal interference, local contamination) and mitigation through replicate design and transparent flagging.
  - Provides a structured data format with comprehensive flags and documentation to support reuse in policy scrutiny and future environmental health decisions.