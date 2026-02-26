# Questionnaire form

## Overview
- A structured, multi-section survey instrument used to collect household farming data related to demographics, farm characteristics, drought experiences, adaptation strategies, compensation and support, and drought warning information.
- Intended to support drought resilience work (STAR) by enabling analysis of how farms perceive, respond to, and are informed about drought.
- Captures both quantitative (counts, ratings, scales) and qualitative (open-ended) responses, with skip patterns and conditional questions.

## Data captured by the questionnaire

- Section 1: Background information and farming activities
  - Respondent demographics (age, education) and farm characteristics (farm type, crops/animals, land area, tenure, years farming, household/workforce, dependents, labor).
  - Asset inventory (tractors, ponds, tanks, wells, vehicles, electronics, etc.) and technology access (Wi-Fi, mobile phones, smartphones, electricity).
  - Farm production flow (land irrigation, irrigation sources and methods, crops irrigated, where production goes to—subsistence/local/national/export).
  - Economic and market details (annual income band, other income sources, and other economic activities).
  - Household capacity and infrastructure (household land ownership, percentage rented, number of workers, irrigation percentages).
  - Perceived changes over the last 10 years in cultivated area, animals, crop/animal variety, and non-agricultural income sources.
  - Perceptions of farm performance and drought preparedness.

- Section 2: Drought experiences and perceptions
  - Definition and experiences of drought (frequency in last 10 years; years when droughts occurred).
  - Impacts across multiple domains (crop quality/yield, pests/disease, feed availability, livestock, income, input costs, prices, farmer wellbeing).
  - Any positive outcomes from drought.
  - Attitudes toward future drought risk, information adequacy, and perceived severity.

- Section 3: Drought adaptation strategies
  - Adoption of specific adaptation measures (e.g., boreholes, ponds, dams, microdams, water tanks, water buying, other measures) and perceived effectiveness.
  - Measures affecting crop choices and cultivation timing; adoption of drought-tolerant or high-value crops; soil and moisture management practices.
  - Livestock and feed management adaptations; income diversification tactics.
  - Willingness and constraints (time, money) to implement additional adaptation strategies; perceived availability and relevance of appropriate adaptation options.
  - Documentation of other strategies not yet covered and their potential long-term changes.

- Section 4: Compensation and support
  - Awareness and receipt of drought-related compensation and other supports (e.g., inputs, financial relief).
  
- Section 5: Drought warning and adaptation advice
  - Exposure to drought warnings and advice from organizations or individuals; information recall and delivery channels (face-to-face, village meetings, radio, SMS, print, online).
  - Actions taken or not taken in response to information; reasons for not acting.
  - Number and nature of organizations informing the farm; evaluation of information usefulness, timeliness, relevance, accuracy, and accessibility.
  - How information is monitored and used to prepare for drought; preferred formats and channels for communication.

## Data types and structure

- Mix of quantitative and qualitative data:
  - Numeric counts (e.g., number of animals, assets).
  - Categorical selections (farm type, irrigation methods, crops, channels of information).
  - Ordinal scales (Likert-style agreement and confidence questions).
  - Open-ended text responses (definitions, reasons, descriptions of other strategies).
- Conditional logic and skip patterns:
  - Follow-up questions depend on previous answers (e.g., if “Yes” to adaptation measure, then ask about effectiveness; if farm has animals, ask animal-management questions).
- Time-series and longitudinal potential:
  - Questions reference changes over the last 10 years and past drought experiences, enabling retrospective trend analysis.
- Organization- and channel-specific data:
  - When information comes from multiple organizations, questions capture organization name, information type, delivery channels, frequency, and perceived usefulness.

## Data governance and stewardship implications

- Metadata and data dictionary needs:
  - Define each variable (name, code, data type, allowed values, units, skip logic, default values).
  - Harmonize coding across sections (e.g., organization names, channel identifiers) to enable interoperability.
- Data quality and validation:
  - Implement consistency checks for related items (e.g., irrigation method vs. land area, asset counts vs. household income).
  - Address potential recall bias in drought frequency and impacts; consider data quality flags for open-ended responses.
- Privacy and consent:
  - Ensure respondent anonymity where appropriate; document consent and permissible uses of data.
- Data storage, sharing, and cataloging:
  - Centralize data storage with clear provenance, versioning, and access controls.
  - Prepare the dataset for sharing to data portals and catalogs; include data schema, field definitions, and methodology.
- Interoperability and standards:
  - Align with broader drought and resilience data schemas where possible (e.g., standard categories for drought impacts, adaptation measures).
  - Use consistent formats for dates, geographic identifiers, and organization names to enable linkage with other datasets.
- Usability and discoverability:
  - Provide a data dictionary and codebook; offer data in machine-readable formats (e.g., CSV/JSON) in addition to any scanned forms.
  - Document skip logic, sampling design (if any), and interviewer instructions to support reuse.

## Potential data quality and operational considerations

- Recall and reporting bias due to self-reported past events and perceptions.
- Variability in interpretation of drought definitions and impacts across respondents.
- Variation in organization names and information channels requiring standardization.
- Need for ongoing data governance to manage updates, corrections, and re-collection across waves or STAR iterations.

## Alignment with Data Stewards aims

- Ensures datasets are accurate, well-documented, and shareable to support discovery and reuse.
- Captures metadata-rich, governance-relevant information about drought experiences, adaptation, and information flows.
- Facilitates understanding of user needs (farmers and organizations) and supports the development of usable, standards-compliant datasets for broader analysis and governance.
- Highlights data availability and limitations (e.g., disclosure, funding, organization-specific channels) to inform data sharing and use.
- Supports a catalog-friendly dataset with clear provenance, enabling discoverability by researchers, policymakers, and practitioners.