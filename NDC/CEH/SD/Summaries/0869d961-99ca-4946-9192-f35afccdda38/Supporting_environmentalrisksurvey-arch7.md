# Social science questionnaire dataset on people's perception on environmental and other risks, UK (2018)

## Overview
- A UK-based social science dataset capturing public perceptions of environmental and other risks (2018).
- Collected via an online survey of UK residents who consume bivalve shellfish and partake in water-related recreational activities within the previous 12 months.
- Sample: 1006 participants invited; 806 responses included after removing duplicates; responses to questions are provided with personal details removed.
- Uses best-worst scaling (BWS) to assess perceptions across 16 defined risks, including air-, food-, and waterborne illnesses and other hazards.
- Demographic and health-related questions accompany risk perceptions (age, gender, ethnicity, qualification, household income, household size, recent gastroenteritis, knowledge of enteric pathogens, and information-seeking behavior).
- Dataset structure supports mapping and spatial analysis, with coded location and qualification responses.

## Data collection
- Hosted by Research Now (USA) and distributed to eligible UK participants.
- Field period: 15–20 February 2018.
- Quota sampling ensured demographics reflected UK distributions; data quality controls excluded repetitive responses.
- Completion time per survey was under 5 minutes.

## Survey design (Best-Worst Scaling)
- 16 risks included in the BWS (varying from well-established to newly evaluated concerns).
- Two blocks:
  - Block 1: respondents select the most feared and least feared risk.
  - Block 2: respondents select the risk they believe they have most/least control over.
- Risks cover health, environment, and other hazards (examples include infectious diseases, accidents, and environmental stressors).

## Data structure and access
- Single CSV dataset; text responses preserved as provided.
- Personal identifiers removed; blank cells indicate no response.
- Column headers align with survey questions; Appendix I contains coding for the questions.
- Table 2 provides mapping keys for non-specified responses to “Where do you live?” and “What is your highest level of qualification?” (regional and educational codes).

## Variables and topics
- 16 risk variables (as defined in the BWS setup), including:
  - Examples such as terrorist attack, dementia, car accident, lung disease from air pollution, antibiotic resistance, diabetes, heart attack, pesticide residues, skin cancer, common cold, dog bite, bioaerosols, Salmonella poisoning, lightning, Norovirus vomiting bug, etc.
- Each risk is paired with a defined description used in the BWS tasks.

## Demographics and health data
- Collected: age, gender, ethnicity, highest level of qualification, household income, household size.
- Health and experience measures: history of gastroenteritis in the last 12 months, link to shellfish consumption or recreational activities, knowledge of enteric pathogens, whether respondents have sought or would consider seeking advice about symptoms, and whether they have experienced the hazards described in the BWS.

## Geographic information
- Geographic response captured via coded regions (e.g., UK regions and constituent countries) rather than precise coordinates.
- Table 2 provides the coding scheme for “Where do you live?” responses and regional classifications.

## Data quality and limitations
- Data cleaned to remove repetitive responses; inclusion criteria reduced from 1006 to 806 respondents.
- Responses are self-reported and collected via an online panel; results may reflect sampling and response biases typical of quota-based online surveys.
- Geographic granularity is region-based rather than precise geolocation; data suitability for fine-grained spatial analysis may be limited by region-level coding.

## Potential GIS applications
- Map-based visualization of risk perception by UK region or demographic segment.
- Spatially contextualize perceived risk against environmental exposure indicators, shellfish consumption patterns, or water quality data.
- Integrate with other geospatial datasets to explore correlations between perceptions and regional environmental conditions or policy contexts.
- Prototypes can be tested with end users to inform public-facing maps and decision-support tools for policymakers, clients, or the public.

## Appendix details
- Appendix I: Codes used for survey column headings in the dataset.
- Table 2: Key mappings for non-specified responses to “Where do you live?” and “What is your highest level of qualification?” to regional and educational categories.