# Social science questionnaire dataset on people's perception on environmental and other risks, UK (2018)

## Overview
- A UK-based social science dataset capturing perceptions of 16 risks using Best-Worst Scaling (BWS).  
- Collected from 806 usable respondents (out of 1006 invited) who live in the UK, consume bivalve shellfish, and engage in recreational activities involving environmental waters within the past year.  
- Includes demographic data, health status, knowledge about enteric pathogens, and prior experience with the hazards. Text responses are included as provided; personal details have been removed.

## Data collection and sample scope
- Method: online survey hosted by Research Now (USA).  
- Timeframe: 15–20 February 2018.  
- Sampling: quota sampling to reflect UK demographic distributions; attempts to ensure representativeness.  
- Eligibility: UK residents who consume shellfish and participate in water-related recreational activities within 12 months. Exclusions: duplicate responses; completing time under 5 minutes.  
- Response details: 1006 invited, 806 valid responses used in the dataset.

## Survey design and content
- Primary technique: Best-Worst Scaling (BWS) with two blocks.  
  - Block 1: respondents indicate which risk they fear the most/least.  
  - Block 2: respondents indicate which risk they believe they have the most/least control over.  
- Risks included: 16 items spanning air-, food-, and waterborne illnesses and other hazards (e.g., terrorist attack, dementia, car accident, antibiotic resistance, diabetes, heart attack, Salmonella, Norovirus, bioaerosols, pesticides, skin cancer, common cold, lightning, dog bite, etc.). Some risks are well-established, others more recently evaluated (e.g., antibiotic resistance, bioaerosols).  
- Additional questions: demographics (age, gender, ethnicity, highest qualification, household income, people in the same household), health status (gastroenteritis in last 12 months, relation to shellfish or recreation activities), knowledge of enteric pathogens, and whether they have sought or would seek advice on symptoms. Respondents indicated whether they experienced the hazards and whether they took any risk-reducing actions.

## Data structure and documentation
- Data file: a single CSV spreadsheet.  
- Data handling: text responses are preserved as entered; non-responses are blank.  
- Column headings: correspond to survey questions; codes are used for each question.  
- Documentation: Appendix I contains the structured survey and the codes used for column headings.  
- Example coding resources:  
  - Table 1 (in document) lists each risk variable name with its BWS definition (e.g., “Terrorist attack” vs “Being a victim of a terrorist attack”).  
  - Table 2 provides coded keys for non-specified questions (geography and education).

## Variables and coding detail
- Risk variables (examples): Terrorist attack, Dementia, Car accident, Lung disease, Antibiotic resistance, Heart attack, Skin cancer, Salmonella poisoning, Norovirus, Bioaerosols, Pesticide residues, Diabetes, Common cold, Dog bite, Lightning, etc. Each is paired with its BWS definition (e.g., “Getting dementia in your lifetime”).  
- Demographics: age, gender, ethnicity, highest level of qualification, household income, people in the same household, and geographic location.  
- Geography coding: “Where do you live?” mapped to discrete region codes (1–17) with corresponding region names (e.g., South East England, London, North West England, etc.).  
- Education coding: “What is your highest level of qualification?” with codes for Secondary school, College, University.

## Data quality, limitations, and governance
- Privacy: personal details removed to protect respondent anonymity.  
- Missing data: blank cells indicate non-response for that item.  
- Representativeness: based on an online panel with quota controls; cross-sectional design may limit generalizability beyond shellfish consumers engaging with environmental waters.  
- Measurement considerations: BWS provides relative importance/fear/control signals rather than absolute risk probabilities; responses may be influenced by recent events or framing.  
- Temporal relevance: data collected in 2018; perceptions may shift over time due to new events or information.

## Access, usage, and reuse
- Primary format: a single CSV dataset with accompanying metadata in Appendix I.  
- The document notes that recent example publications using this dataset are listed as N/A, indicating limited or no widespread reuse at the time of documentation.  
- Users should consult Appendix I for the exact question structure and coding schema to enable correct interpretation and integration with other datasets.

## Implications and potential use for Data Leaders
- Strategic value: supports understanding how different demographic groups perceive and prioritize a broad set of environmental and health risks, useful for risk communication and public health strategy.  
- Governance and metadata opportunities: clear mapping between questions, risk definitions, and coded responses facilitates data discoverability, reusability, and provenance tracking.  
- Analytical applications:  
  - Compare fear versus perceived control across demographics and regions.  
  - Explore associations between health status (e.g., gastroenteritis history) and risk perceptions.  
  - Assess knowledge gaps about enteric pathogens and uptake of risk-reduction recommendations.  
  - Integrate with other environmental or public health datasets to enhance risk communication planning for shellfish-related activities.  
- Data quality considerations: ensure alignment with broader data standards, maintain metadata completeness (Appendix I), and document any updates or corrections to coding schemes for cross-project interoperability.

## Appendices referenced
- Appendix I: complete structured survey and coding for column headings.  
- Table 2: Key for non-specified questions (e.g., geographic location and highest qualification codes).  
- Table 1: list of risks and their BWS definitions used in the survey.