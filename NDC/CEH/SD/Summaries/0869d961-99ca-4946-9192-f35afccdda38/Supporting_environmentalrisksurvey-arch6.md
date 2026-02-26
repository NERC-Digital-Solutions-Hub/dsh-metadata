# Social science questionnaire dataset on people's perception on environmental and other risks, UK (2018)

## Overview
- Online survey conducted for UK residents who consumed bivalve shellfish and had contact with environmental waters in the past 12 months.
- Data collection hosted by Research Now (USA) between 15–20 February 2018.
- Invitations: 1006 participants; included: 806 after screening and quality checks (responses under 5 minutes and repetitive answers excluded).
- Sampling used quotas to reflect UK demographic distributions.

## Survey design and measures
- Best-Worst Scaling (BWS) focusing on 16 risks, evaluated in two blocks:
  - Block 1: which risk they fear the most/least.
  - Block 2: which risk they believe they have the most/least control over.
- Demographic and health information collected: age, gender, ethnicity, highest qualification, household income, number of people in household, health status.
- Health-related questions: gastroenteritis in the last 12 months, relation to recreational activities or shellfish consumption, knowledge of enteric pathogens, and whether they have sought or would consider seeking advice about symptoms.
- Risk list includes a mix of well-known and newer risks (air-, food- and waterborne illnesses, etc.).

## Data structure and content
- Dataset stored in a single CSV; personal details removed; blank cells indicate non-responses.
- Column headings correspond to survey questions; Appendix I contains coding for the questions.
- Table 2 provides numeric codes for non-specified responses:
  - Where you live: regional codes mapped to UK regions (1–17 with region names).
  - Highest level of qualification: 1 = Secondary school, 2 = College, 3 = University.

## Variables and coding
- 16 risk items with two representations in the dataset:
  - Example pairings include: terrorist attack vs. being a victim; dementia vs. getting dementia; car accident vs. being injured in a car accident; antibiotic resistance vs. getting ill from resistant bugs; diabetes vs. getting diabetes; heart attack vs. suffering a heart attack; and others (pesticide residues, skin cancer, common cold, dog bite, bioaerosols, Salmonella poisoning, lightning, Norovirus vomiting bug).
- Structural data captured for each respondent’s perceptions and self-reported demographics and health experiences.

## Data quality and usage notes
- Text responses captured as provided.
- No personal identifiers; data suitable for aggregation and analysis at the group level.
- No published example datasets cited at the time of documentation (N/A).

## Potential uses for data support and products
- Create self-serve analyses of risk perceptions by demographics, region, and health status.
- Develop dashboards or pivot-table style reports comparing fear versus perceived control across the 16 risks.
- Analyze relationships between knowledge of enteric pathogens, past gastroenteritis, and risk perceptions.
- Leverage the coded regional and qualification data to explore geographic and educational patterning in risk perception.
- Use Appendix I coding and Table 2 mappings to streamline data cleaning and integration with other datasets.