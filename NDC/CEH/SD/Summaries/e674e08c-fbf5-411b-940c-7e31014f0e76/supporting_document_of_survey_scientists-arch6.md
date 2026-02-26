# Supporting information for interpreting

- Overview
  - The document documents a survey-based dataset on knowledge management/knowledge transfer (KM/KE) practices among environmental scientists working on a joint international critical zone (CZ) project.
  - Purpose: compare knowledge transfer experiences and methods between Chinese and British scientists; extend sampling to broader Chinese environmental scientists to assess representativeness.
  - Key populations: Chinese and British scientists affiliated with the CZ project, plus additional Chinese scientists (participants recruited at a 2017 geochemistry conference).

- Data collection and collection methods
  - Survey administration: voluntary responses collected during project meetings or via email; additional Chinese respondents gathered at the 2017 International Geochemistry Conference in Guizhou.
  - Sample sizes:
    - Chinese and British scientists in CZ programme: 16–27 participants (per subgroup).
    - Additional Chinese scientists: 41 respondents.
  - Focus: knowledge transfer/knowledge exchange activities, outputs, collaboration with end users, and attitudes toward KE concepts.

- Data structure and contents
  - The dataset folder SurveyScientists contains 3 CSV files:
    - SurveyScientists_GeoConference2017.csv: responses from geo-scientists at the 2017 Geochemistry Conference in Guizhou, China.
    - SurveyScientists_ChinainCZO.csv: responses from Chinese and British scientists in the CZ programme.
    - SurveyScientist_UKinCZO.csv: responses from 7 British CZ scientists collected via email.
  - Each file encodes responses to a common set of questions (Q1–Q12 and associated sub-items such as Q3a, Q6a, Q7a, Q8a, Q9a, Q10a, Q11a) with defined response categories (e.g., Q1: 1=China, 2=UK, 3=Other; Q2: yes/no; Q6: multiple outputs; etc.).
  - Example question types include: country base, prior knowledge transfer experiences, types of knowledge transfer outputs, whether outputs were co-produced with end users, methods of KE processes, measurement of KE success, and interest in future KE training.

- Variables and coding notes
  - Many variables are categorical with numeric codes (e.g., country, yes/no, types of outputs, KE processes).
  - Some fields have sub-questions (e.g., Q3, Q6a, Q7a, Q8a, Q9a, Q10a, Q11a) to capture details or open-ended commentary.
  - Several sections are marked N/A (not applicable), indicating missing or inapplicable data for certain items or respondents.

- Potential analyses and data products
  - Cross-country comparisons of KE experience, types of outputs produced, and end-user involvement.
  - Assessment of how often KE activities are measured and by whom, and the perceived feasibility of applying KE approaches in projects.
  - Descriptive dashboards showing:
    - Proportion of respondents with KE experience.
    - Distribution of KE output types (policy briefs, guidance, webinars, training, decision-support tools, reports, etc.).
    - End-user involvement in production of outputs (co-produced vs. produced for end users vs. no KE).
    - Interest in further KE training and KE technique training.
  - Data quality checks and harmonization across the three files to enable integrated analyses.

- Data quality considerations and limitations
  - Small sample sizes and mixed sampling frames (CZ project members plus conference-based Chinese scientists) may limit generalizability.
  - Self-reported measures of KE activities may be subject to recall or social desirability bias.
  - Differences in sampling methods between Chinese and UK groups could affect comparability; careful harmonization recommended.

- Practical notes for data support
  - When building data products, consider separate cohorts (UK vs China) and the combined dataset to highlight regional differences.
  - Leverage Q1–Q12 structure to create a KE profiling dashboard (experience, outputs, end-user engagement, measurement, and training interest).
  - Predefine handling for N/A fields and ensure consistent mapping of coded responses across the three CSV files for integrated analyses.