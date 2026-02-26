# Well customer questionnaire

- Purpose: A field questionnaire used when water from sampled wells is sold to others. It targets groundwater customers to understand water use, safety practices, storage, alternative sources, and household characteristics. Consent is obtained before participation, and the instrument records whether the participant purchases well water, with participant and well details (area, Well ID, owner, customer).

- Recruitment and administration details:
  - Randomly selected groundwater customer who normally buys well water.
  - Collects participant consent via a consent form after presenting participant information.
  - Area options include Manyatta, Migosi, and others; includes well and owner identifiers for linkage.

- Structure of the questionnaire:
  - PART 1: GROUNDWATER USE
    - Q1: Quantity of water purchased yesterday (in jerrycans).
    - Q2: Whether any treatment is used to make water safer to drink (Yes/No/Don't know).
    - Q3: What is done to make water safer (list of possible methods; includes free-text “Other” and storage method choice for the greatest amount stored).
      - Methods include boiling, adding bleach/chlorine, filtering, letting stand to settle, straining, solar disinfection, and other.
    - Q4: Other water sources available for the household besides the well (e.g., piped water, rainwater, vendor water, surface water, etc.).
    - Q5: Source usage by purpose (for each source and purpose: drinking, cooking, washing, etc.; long list of source types by purpose; for each purpose, asks why the household uses that source with a coded response).

  - GROUNDWATER2030
    - Q1: Type of toilet facility used by the household (multiple options including flush/pour flush, pit latrine, composting, bucket, bush/field, etc.).
    - Q2: Household assets (clock, electricity, TV, non-mobile phone, refrigerator) with Yes/No/Don't know responses.
    - Q3: Primary cooking fuel (list including electricity, gas, biogas, kerosene, charcoal, wood, crop/animal dung, etc.).
      - If “No food cooked in household,” skip to Q6.
    - Q4: Cooking location (in-house, separate building, outdoors); if separate/outdoors, skip to Q6.
    - Q5: Existence of a separate kitchen room (Yes/No/Don’t know).
    - Q6: Ownership of a car or truck (Yes/No/Don’t know).
    - Q7: Main material of household walls (multiple construction options).
    - Q8: Number of days in the last seven days that meat, rice, and wheat products were served as part of a main meal (separate counts).
    - Q9: Number of days in the last seven days that cassava was the main meal (or don’t know).
    - Q10: In the last 30 days, how many days the household did not have enough to eat (days with skipping meals or hunger).
    - Q11: In the last 12 months, how many months at least one day existed without enough to eat (months with hunger).
    - Q12: Frequency of purchasing staples (maize, maize meal, potatoes) with categorical options: Daily, Twice a week, Weekly, Fortnightly, Monthly, Less frequently than once a month.
    - Q13: Weeks in the past 12 months with stock of maize, maize meal, or potatoes at home.

- Data types and coding:
  - Quantitative: numbers (e.g., jerrycans, days, weeks, months).
  - Categorical with fixed codes: Yes/No/Don't know (1/0/9), frequency categories (1–6), and various predefined options.
  - Open-text options: “Other (SPECIFY)” fields for methods, wall materials, and other attributes.
  - Some sections include skip logic (e.g., if no cooking in house, or if separate kitchen/outdoors, skip certain questions).

- Key data elements collected:
  - Water use and safety practices: quantity purchased, treatment, safety methods, and primary storage method.
  - Water source mix and purposes: types of sources used for various household needs, and reasons for source choices.
  - Household infrastructure and assets: toilet facilities, electricity, appliances, kitchen arrangements, and housing materials.
  - Food security indicators: past 7 days and past 30/12 months hunger indicators, including days without enough to eat.
  - Economic and consumption indicators: staple purchase frequency, stock duration, and potential affordability signals.
  - Area and identifiers: area, Well ID, owner name, and customer name for linkage to wells and households.

- Potential data quality considerations for Data Support:
  - Missing or unknown responses (use of 9 for don't know, gaps in consent status).
  - Recall bias for past consumption and hunger indicators (Q8–Q13 in Groundwater2030).
  - Variability in open-text responses requiring standardization (Other SPECIFY fields).
  - Consistency checks across sections (e.g., cross-referencing water source types with storage and treatment practices).
  - Need for linkage on Well ID, area, and participant identifiers to merge with other datasets (e.g., groundwater quality, sociodemographic data).

- Intended uses and analytics:
  - Assess groundwater consumer behavior: water sources, treatment, storage, and usage patterns.
  - Explore safety practices and potential gaps in safe drinking water preparation.
  - Correlate household infrastructure and assets with water use and food security indicators.
  - Build dashboards or reports to enable self-service insights for program managers or local authorities.
  - Inform policy or program interventions aimed at improving water safety, access, and household resilience.

- Ethical and consent considerations:
  - Interview begins with participant information and consent, ensuring participation is voluntary.
  - Data linkage possible through identifiers, underscoring the need for proper data governance and privacy safeguards.