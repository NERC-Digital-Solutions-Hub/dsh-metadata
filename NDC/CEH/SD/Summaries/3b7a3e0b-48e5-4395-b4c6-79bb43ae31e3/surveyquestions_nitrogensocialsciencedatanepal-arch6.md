# SANH WP 1.3 Harmonised Individual Questionnaire

- Purpose and scope
  - A harmonised survey instrument (South Asian Nitrogen Hub) funded by UKRI to improve nitrogen management in agriculture.
  - Collects basic household demographics, farm characteristics, and detailed livestock data to support data-backed insights and products.
  - Designed for country adaptability, with season-based structure and detailed data quality checks.

- How this section fits the Data Support role
  - Provides a data backbone by locating, standardising, and enriching livestock and related household data for end-user exploration.
  - Enables cross-country, cross-season analyses and supports development of dashboards, reports, and other data products.

- Section 9: LIVESTOCK
  - Objective
    - Capture livestock ownership and use over the past 12 months, including the species owned and the highest livestock units on the farm.
  - Species covered (examples)
    - Cattle, Buffalo, Yak, Goat, Sheep, Horse, Camel, Pig, Poultry (and possibly other species via “Other” in prompts).
  - For each species (where applicable)
    - Ownership: whether the species was owned for at least 1 month in the past 12 months (may be multiple species).
    - Reasons for keeping: categories include revenue generation, home consumption (milk/meat), festivals, coping with revenue shortfalls, dowry, transport/racing/draft/animal power, and others.
    - Numbers: exact counts per species; identification of which species has the highest number of livestock units (the emphasis is on the most numerous species).
    - Movement out of the farm: how animals left the farm in the last 12 months (sale, barter, slaughter for sale/household needs, death, theft, dowry, etc.).
    - Housing for animals: number of weeks the species spent in different housing types over the past 12 months (yard, open animal house, closed animal house).
  - Cross-species prompts
    - The instrument repeats 9.5–9.7 questions for the species with the highest livestock units on the farm (and continues similarly for other species encountered: e.g., Cattle, Buffalo, Yak, Goat, Sheep, Horse, Camel, Pig, Poultry).
  - Data quality notes
    - Complex repeat structure; potential recall bias and varied terminologies across regions.
    - Requires careful enumerator training, consistent coding, and robust data dictionary to ensure comparability across regions and seasons.

- Section 10: INFORMATION SOURCES
  - Training and demonstration participation
    - Attended crop demonstrations/trainings in the last 2 years? Yes/No.
    - If yes, whether any trainings covered fertilizer and manure use/management.
  - Information sources and decision support
    - Where decisions on fertilizer use are sourced (family/neighbours, traders, extension agents, government, print media, radio/TV, internet, etc.).
    - Whether respondents actively sought advice in the last 2 years.
    - Use of decision-support tools (government/private guidelines, computer programs, smartphone apps, leaf colour charts, soil testing results, etc.).
  - Information quality and usage
    - Reasons for not using more information; whether advice is followed exactly or modified.
    - Descriptive prompts about how decisions on fertilizer quantities are made and whether written records of fertilizer use/yield are kept.
  - Data quality considerations
    - Emphasis on provenance, sourcing, and verification of information sources; potential development of cross-country validation checks.

- Section 11: ADOPTION – DRIVERS AND BARRIERS
  - Practices/technologies inventory
    - List of general practices/technologies (e.g., decision support tools, green manure, agroforestry, anaerobic digestion, midseason drainage, foliar fertilization, etc.) plus country-specific items.
  - Awareness and use
    - For each practice: whether the farmer has heard of it, is currently using it, or has adopted and later stopped (dis-adopted).
  - Data capture goals
    - Identify drivers and barriers to adoption to inform data-driven policy and extension efforts.

- Section 12: ATTITUDE, BEHAVIOUR, PERCEPTION AND OPINION
  - Technology openness and risk
    - General self-assessment of willingness to try new technologies; risk tolerance in decision-making.
  - Fertiliser decisions and change factors
    - What could change fertilizer usage and why; perceptions about the impact of synthetic fertilizer vs manure on harvest yields and soil health.
  - Quantitative attitudes
    - Scales (0–5) to assess beliefs about fertilizer/manure benefits, management trade-offs, and dependencies on weather.
  - Decision-context questions
    - How farmers think about record-keeping, how they weigh past experiences, and how they consider information sources when applying fertilizer.

- Section 13: HOUSEHOLD EXPENDITURE
  - Monthly expenses
    - Detailed categories (food, clothing, education, health, taxes, festivals, durable assets, debt repayment, etc.) and monthly costs.
  - Notes
    - Combines production-derived consumption with market purchases for a holistic view of household economics.

- Section 14: HOUSEHOLD WEALTH/ASSET
  - Home ownership and housing characteristics
    - Ownership status, number of rooms, floor material, lighting and cooking fuel, drinking water source, electricity/internet access, and dwelling features.
  - Assets and capabilities
    - TVs, smartphones, internet access, power tillers, irrigation pumps, and other farm equipment.
    - Transport ownership (human-, animal-, motor-powered).
  - Financial and risk management
    - History of farm investment loans, access to financial services, distance to financial institutions.
    - Crop insurance status and potential compensation scenarios.
  - Crop insurance and seasonality prompts
    - Insurance details and season-specific implications for risk management.

- Section 15: SUBSIDY
  - Direct subsidies received in the past 12 months
    - Subsidies by category: synthetic fertilizer, agricultural machinery purchase, irrigation charges, output price support, seed, others.
  - Data intent
    - Assess exposure to subsidies and potential effects on input choices and farm economics.

- Data quality, governance, and outputs (overall)
  - Harmonisation and structure
    - Country-adaptable codes, season-based sections, structured response formats, and detailed skip logic.
  - Data dictionary and validation
    - Emphasis on consistent coding (species, practices, inputs), crosswalks for country adaptations, and robust data cleaning pipelines.
  - Outputs and data products
    - Supports dashboards and self-serve analyses (e.g., livestock composition, adoption patterns, input use, household economics, and asset ownership) with cross-cutting analyses by season, country, and farm type.
  - Ethics and governance
    - Informed consent, confidentiality, research-only data usage, and enumerator responsibilities.

- Practical recommendations for Data Support
  - Develop a comprehensive data dictionary aligning crop codes, fertilizer types, unit conventions, and seasonal labels.
  - Implement validation rules and automated checks during data entry to catch inconsistencies.
  - Create country crosswalks to preserve harmonised structures while accommodating local adaptations.
  - Plan data cleaning pipelines to harmonise units, reconcile multi-season entries, and merge related data (fertilisers, seeds, yields, income).
  - Establish data provenance and versioning to support reproducibility and audits.