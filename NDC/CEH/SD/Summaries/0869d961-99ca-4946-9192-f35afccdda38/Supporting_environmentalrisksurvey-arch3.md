# Social science questionnaire dataset on people's perception on environmental and other risks, UK (2018)

- Purpose and scope
  - A UK-based online survey dataset aimed at understanding public perceptions of environmental and other health-related risks to inform policy scrutiny, evaluation, and future decision-making.
  - Uses best-worst scaling (BWS) to assess fear and perceived personal control across 16 risks, including environmental, health, and everyday hazards.

- Data collection and design
  - Collected via an online survey hosted by Research Now (USA) and distributed to UK residents who consume bivalve shellfish or engage in activities involving environmental waters within the past 12 months.
  - Sampling used quotas to reflect UK demographic distributions. Data collection occurred between 15–20 February 2018.
  - Initial sample: 1006 respondents; final dataset includes 806 respondents after excluding repetitive or invalid responses.
  - BWS structure: two blocks per respondent
    - Block 1: which risk they fear the most/least
    - Block 2: which risk they have the most/least control over
  - Additional questions cover demographics (age, gender, ethnicity, qualification, household income, household size) and health status, gastroenteritis experience, knowledge of enteric pathogens, and actions taken to reduce risk.

- Data content and structure
  - Single CSV dataset; all personal identifiers removed.
  - Column headings correspond to survey questions; any text responses preserved as provided.
  - Appendix I contains the detailed survey structure; Table 2 provides numeric coding for non-specified questions (e.g., “Where do you live?” and “What is your highest level of qualification?”).
  - Risks included in the BWS (16 items) cover a mix of well-known and emerging concerns, with paired definitions:
    - Examples include terrorism, dementia, car accidents, air pollution-related lung disease, antibiotic resistance, diabetes, heart attack, pesticide residues, skin cancer, common cold, dog bites, bioaerosols, Salmonella, lightning, and Norovirus.
  - Notation in the dataset distinguishes between the general risk and the “risk at home” variant for the BWS items (e.g., "Fire" vs. "Fire at home" mapping to different fear/control concepts).

- Population and responses
  - Respondents: adults in the UK with recent interaction with environmental waters or shellfish consumption.
  - Demographic and health data captured alongside risk perceptions; specific variables include age, gender, ethnicity, qualification, income, household composition, gastroenteritis history, knowledge of enteric pathogens, and advice-seeking behavior.

- Data quality, metadata, and governance
  - Metadata completeness relies on Appendix I and Table 2; some metadata issues commonly encountered in monitoring datasets (e.g., detailed provenance, variable definitions, and data sharing constraints) are noted as potential barriers in this context.
  - Data are structured to facilitate reuse in monitoring frameworks, with clear coding and anonymization to support open data practices.

- Reuse and applicability for monitoring frameworks
  - Enables monitoring of public risk perception trends across multiple environmental and health risks.
  - Supports segmentation analyses by demographics and health status to inform targeted risk communication and policy design.
  - The dual-block BWS design provides insights into both fear intensity and perceived personal control, useful for evaluating the effectiveness of interventions and risk communication strategies.
  - Can be integrated with environmental exposure data or policy scenarios to assess alignment between public perceptions and environmental health policies.
  - Potential data governance considerations include ensuring metadata completeness, clear data provenance, and appropriate sharing of underlying data for transparency.

- Limitations and considerations
  - Cross-sectional design limits causal inference and temporal trend analysis.
  - Self-reported data subject to bias (recall, social desirability).
  - Sampling relies on quotas rather than random sampling, which may affect representativeness.
  - Data interpretation requires careful handling of the BWS structure and coding (Appendix I and Table 2 guidance).
  - No published example studies listed for this dataset at the time of documentation (listed as N/A).