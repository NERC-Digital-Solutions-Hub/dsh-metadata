# Social science   questionnaire   dataset   on   people's   perception   on environmental and other risks, UK (2018)

- Purpose
  - Provides a UK-based dataset describing public perceptions of environmental and other risks, using best-worst scaling (BWS) to rank fear and perceived control across 16 risks.
  - Designed to support analyses of how demographics, health status, knowledge, and behaviors relate to risk perception, with potential for descriptive statistics, correlations, and predictive modeling.

- Data collection and sample
  - Online survey administered by Research Now, targeting UK residents who had contact with environmental waters in the past 12 months and who consumed bivalve shellfish.
  - Quota sampling used to reflect UK demographic distributions.
  - Data collection window: 15–20 February 2018.
  - Initial respondents: 1,006; final dataset after quality filtering: 806.
  - Respondents who provided repetitive answers were excluded.

- Survey design and key questions
  - Best-Worst Scaling (BWS) conducted in two blocks:
    - Block 1: identify which risk they fear the most/least.
    - Block 2: identify which risk they believe they have the most/least control over.
  - 16 risks included in the BWS, spanning air-, food-, and waterborne illnesses along with other hazards (some well-established; some recently evaluated).
  - Demographic and health data collected:
    - Age, gender, ethnicity, highest qualification, household income, people in the household.
    - Health status and gastroenteritis in the last 12 months; whether illness related to recreational activities or shellfish.
    - Knowledge of enteric pathogens; whether they have sought or would seek advice on symptoms.
    - Experience with the hazards and actions taken to reduce risk.

- Data structure and documentation
  - Dataset stored in a single CSV file; responses are de-identified; personal details removed.
  - Blank cells indicate no response.
  - Column headings correspond to survey questions; Appendix I contains the structured survey and codes.
  - Appendix II (referred to via Tables 1 and 2 in the text) provides additional mapping:
    - Table 1: List of 16 risk variables with definitions used in the BWS (e.g., terrorist attack, dementia, car accident, lung disease from air pollution, antibiotic resistance, diabetes, heart attack, pesticide residues, skin cancer, common cold, dog bite, bioaerosols, Salmonella poisoning, lightning, norovirus vomiting). Each risk has a BWS interpretation (e.g., fear of the event, or illness from exposure).
    - Table 2: Coding keys for non-specified questions:
      - Location: codes map to UK regions (e.g., South East England, London, etc.).
      - Highest qualification: 1 = Secondary school, 2 = College, 3 = University.

- Practical notes for analysts
  - The dataset enables exploration of:
    - Relative fear versus perceived control across the 16 risks.
    - Associations between demographics (age, education, region, income) and risk perceptions.
    - Relationships between health status (gastroenteritis history) and risk perceptions or protective behaviors.
    - Knowledge about enteric pathogens and propensity to seek information or advice.
    - Reported actions taken to reduce risk.
  - Potential analytic approaches:
    - Descriptive statistics for fear/control rankings.
    - Conditional or mixed logit models to analyze BWS data.
    - Regression analyses linking demographics, health status, and knowledge to risk perceptions and behaviors.
  - Data quality and limitations:
    - Self-reported, cross-sectional data; limited to shellfish-consumers with environmental water contact.
    - Possible non-response or reporting biases; blanks indicate missing data.
    - Regional granularity may be limited by sample size within certain UK areas.
    - Details rely on Appendix I and Tables 1–2 for exact question mappings and codes.

- Example usage notes
  - Researchers can reference the coded CSV, leverage the BWS structure to identify which risks are perceived as most/least fear-inducing and most/least controllable, and link these perceptions to demographic and health-related variables for targeted risk communication or policy insights.