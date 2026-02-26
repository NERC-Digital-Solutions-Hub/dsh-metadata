# Social science   questionnaire   dataset   on   people's   perception   on environmental and other risks, UK (2018)

- Overview
  - An online survey conducted in the UK (15–20 February 2018) with 1006 participants; 806 responses included after quality checks.
  - Participants were adults who consume bivalve shellfish or engage in recreational activities involving environmental waters; quota sampling aimed to mirror UK demographic distributions.
  - Respondents completed the survey in under 5 minutes; duplicate or repetitive responses were excluded.

- Data Collection and Sampling
  - Collected via Research Now (USA) with an online panel.
  - Eligibility ensured representation across demographic groups through quotas.
  - Data cleaned to remove personal identifiers; final dataset contains 806 usable responses.

- Survey Instrument and Variables
  - Best Worst Scaling (BWS) used to gauge perceptions of 16 risks, spanning air, food, waterborne illnesses, and other hazards (e.g., terrorist attacks, dementia, car accidents, antibiotic resistance, diabetes, heart attack, Salmonella, Norovirus, etc.).
  - Two BWS blocks:
    - Block 1: respondents indicate the most/least feared risk.
    - Block 2: respondents indicate the most/least control over the risk.
  - Demographic and health data collected include age, gender, ethnicity, highest qualification, household income, people in the same household, gastroenteritis in the last 12 months, relation to shellfish, awareness of enteric pathogens, and past or intended seeking of medical/advice.
  - Respondents were asked about experiences with the hazards and actions taken to mitigate risks.

- Data Structure and Metadata
  - Dataset stored as a single CSV file; text responses retained as entered.
  - Personal details removed; blank cells indicate no response.
  - Survey items are present as coded column headings; Appendix I contains the code mappings.
  - Table 2 provides decoding keys for non-specified questions:
    - Where you live: region codes map to UK regions and nations (e.g., South East England, London, North West England, etc.).
    - Highest level of qualification: 1 = Secondary school, 2 = College, 3 = University.

- Data Quality, Governance, and Documentation
  - Anonymized data with structured coding to minimize identifiability.
  - Metadata includes questionnaire structure and column-heading codes; Appendix I documents the structured survey and coding scheme.
  - No explicit licensing or access conditions stated; publication mentions recent example uses but lists N/A (no published examples noted).

- Access, Reuse, and Stewardship Considerations
  - For data stewards, ensure adherence to:
    - Metadata completeness: confirm Appendix I and Table 2 mappings for proper interpretation of codes.
    - Data integrity: preserve the coding scheme (BWS blocks, variable naming, and region/qualification keys).
    - Format standardization: CSV with a single dataset file; verify text responses are kept intact where present.
    - Anonymization and privacy: confirm removal of personal identifiers and handling of any remaining sensitive fields.
    - Provenance: maintain records of data collection by Research Now (2018) and the listing of authors.
    - Governance and sharing: clarify licensing, terms of use, and any embargo or status of public availability.
  - Suggested use cases include risk perception research, policy development, and risk communication analyses, with attention to the UK-specific context and the BWS design when interpreting results.

- Limitations and Considerations for Users
  - Sample limited to shellfish consumers and people active around environmental waters; may affect generalizability to the broader population.
  - Data collected via an online panel; potential panel biases and nonresponse considerations.
  - The dataset combines quantitative BWS data with demographic/health context, requiring careful decoding of coded variables and understanding block structure for analysis.

- Appendix and Coding References
  - Appendix I: detailed survey structure and codes corresponding to CSV column headings.
  - Table 2: decoding keys for “Where do you live?” and “What is your highest level of qualification?” questions.