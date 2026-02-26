# VIRAQUA survey

- Purpose and scope
  - Aimed at collecting data on upset stomachs, shellfish consumption, recreational water contact, and knowledge of related pathogens.
  - Designed to understand hazard-related fear and control perceptions, and how people respond to health information.
  - Developed by researchers at Bangor University and the University of Manchester; not-for-profit and intended for academic research only; responses confidential and not used for marketing.

- Survey logistics
  - Estimated completion time: about 15 minutes.
  - Administered with Sawtooth Software; sections include demographic questions, dietary/exposure questions, health symptoms, information-seeking behaviors, and repeated Hazards of Life assessments (fear and control).

- Data collected (types and instruments)
  - Demographics and socioeconomics
    - Self-identified gender (open-ended in text), age/occupation categories (e.g., Semi/manual, Skilled manual, Supervisory/clerical, Intermediate/managerial, Higher managerial).
    - Household income-related structure via Chief Income Earner in the household.
    - Location data (questions about where the respondent lives).
  - Dietary and exposure data
    - Eating habits related to filter-feeding shellfish (mussels, oysters, cockles, clams, scallops) across multiple contexts (restaurant, home, ready meals, raw/cooked, pickled).
    - Frequency and context of contact with UK recreational waters (various activities and settings).
  - Health symptoms and experiences
    - Upset stomach in the last 12 months; potential links to shellfish or water exposure.
    - Behavior changes after illness (e.g., avoiding shellfish in restaurants or at home; ensuring shellfish is well cooked; sharing information with others).
    - Guidance sought in the last year; sources of advice (government sites, NHS, FO agencies, newspapers, friends/family, internet sources); intent to consult these sources in the future.
  - Knowledge of pathogens
    - Awareness of specific bugs (e.g., MRSA, Norovirus, Cryptosporidium, E. coli, Listeria, Campylobacter, Salmonella, Shigella, Rotavirus, Pseudomonas, etc.) with presence/level of knowledge for each.
  - Hazards of Life (fear and control modules)
    - Sets of four hazards presented per page; respondents identify the hazard they fear the most and least, and later the hazard over which they have the most and least control.
    - Hazards include topics like heart attack, Salmonella, Norovirus, pesticide residues, lung disease from air pollution, antibiotic resistance, dementia, fire, diabetes, common cold, dog bites, skin cancer, bioaerosols, etc.
    - Multiple rounds track consistency of fear and control across different hazard groupings.
  - Experience with hazards and exposure
    - Questions about personal or close-relatives’ experiences with listed hazards, to contextualize fear/control ratings.
  - Attitudinal and cognitive aspects
    - Perceived ease of understanding the hazards, and perceived difficulty of making the choices.
  - Finish and data integrity
    - Sections to capture completion status (finish, complete, screenout, overquota).
    - Note about redirection in regular mode to external links after completion.

- Data governance and privacy considerations
  - Confidentiality assurances: responses are confidential and retained for academic research only; not used for marketing.
  - Non-commercial use: explicitly stated as not for private company purposes.
  - Instrument provenance: created by Bangor University and the University of Manchester; data likely linked to versioned survey instruments and response trackers.
  - Data access and sharing
    - The document emphasizes academic research use and confidentiality; explicit public sharing or licensing terms are not described in detail.
  - Data hygiene and structure
    - Large set of coded response variables (e.g., effs_r1, wsfsf_r1_c1, hcsf_r1, fear/control blocks) requiring robust documentation for reuse.
    - Rich metadata requirements implied by numerous variable names and question blocks, suggesting a need for a comprehensive data dictionary.

- Data quality and provenance considerations for Data Stewards
  - Complex, multi-section instrument with numerous derived and placeholder codes; ensure consistent variable naming, coding schemes, and documentation.
  - Per-question logic includes multiple categorical and ordinal scales; maintain validation rules and value tables to support interoperability.
  - Repeated “Hazards of Life” modules generate longitudinal-like lines of data within a single survey instance; plan for structure that preserves the sequence of question blocks.
  - Presence of placeholders and potential data quality artifacts (e.g., inconsistent option labels, scrambled metadata) requires careful data cleaning and provenance tracking.

- Practical recommendations for data management
  - Develop a detailed data dictionary mapping each variable name (e.g., effs_r1, wsfsf_r1_c1, und_r1, eoh_r1) to:
    - Question text and section
    - Response options and coding
    - Data type, allowed values, and missing value conventions
    - Derived fields and skip patterns
  - Establish metadata standards aligned with the instrument’s structure, including versioning, deployment date, and environment (e.g., Sawtooth Software platform version).
  - Implement privacy safeguards:
    - Anonymize or de-identify any direct location data beyond high-level aggregates as appropriate.
    - Limit access to raw PII in accordance with the stated use for academic research only.
  - Data quality controls:
    - Validate that coded responses conform to predefined value ranges.
    - Check for inconsistent responses across related sections (e.g., shellfish exposure vs. illness reports).
  - Data lifecycle and sharing:
    - Document retention periods, access controls, and licensing for any shared datasets.
    - Provide clear governance on whether data may be shared publicly, with restrictions (e.g., aggregated only) or with researchers under data-use agreements.
  - Usage context for analysts:
    - Provide guidance on interpreting The Hazards of Life sections, including the design intent of fear vs. control measures and how to handle repeated-question structures.

- End-user impact and opportunities
  - The dataset enables analysis of risk perception and information-seeking behaviors related to GI illnesses and environmental hazards.
  - Potential for cross-topic analyses linking dietary exposure, water contact, illness experiences, knowledge of pathogens, and hazard perception.
  - Useful for risk communication research, public health surveillance, and policy engagement when complemented with appropriate metadata and access controls.

- Summary of document status
  - Comprehensive survey instrument with demographic, dietary/exposure, health, information-seeking, knowledge, and hazard-perception components.
  - Emphasizes confidentiality, academic use, and non-commercial purpose.
  - Rich but complex data structure requiring careful governance, documentation, and data quality management to enable safe sharing and reuse.