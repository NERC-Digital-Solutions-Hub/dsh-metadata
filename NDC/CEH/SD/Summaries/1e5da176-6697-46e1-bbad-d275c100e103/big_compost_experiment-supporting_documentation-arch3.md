# Survey of opinions and behaviours regarding home composting, alongside experimental data for disintegration and degradation of compostable materials, UK, 2019-2023

## Summary
- A voluntary UK citizen science study (Big Compost Experiment) conducted from 2019 to 2023.
- Aimed to assess the role and effectiveness of biodegradable/compostable packaging, interface with the public, raise awareness of plastic waste issues, and gather public opinions and domestic composting behaviours.
- Produces both qualitative and quantitative survey responses and home compost experiment results on compostable plastics, stored as raw CSV data.
- Data collected via online surveys and participant accounts; anonymised (GDPR/ethics compliance); no processing beyond raw data.

## Datasets Included
- Big_Compost_Experiment-composter-items.csv
  - Participant compost experiment data (e.g., product tested, degradation level, composting method, maturity, region, composter type, etc.).
  - Includes metadata-like fields such as dateCreated, dateUpdated, composterId, and region.
- Big_Compost_Experiment-surveys.csv
  - Participant survey responses (e.g., likelihood to buy compostable packaging, food waste separation practices, composting practices, what items are composted, use of councils or personal composters, reasons for responses, etc.).
  - Includes fields on disposal behaviours, constraints, and household waste strategies.

## Data Formats and Variables
- File format: CSV for both datasets.
- Key variable categories (examples):
  - Participant identifiers (id, composterId), timestamps (dateCreated, dateUpdated, dateStarted, dateFinished).
  - Product/compost items: compostableType, productName, quantity, certificationMarks, netBagUsed, degradationLevel.
  - Household behaviours: separatesFoodWaste, usesCouncilWaste, councilWasteItems, usesComposter, compostItems, whereDoYouCompost, composterType.
  - Survey responses: likelyToBuyCompostablePackaging, likelyToBuyCompostablePackagingReasons, other strategy items, compostUses, compostLife.
  - Temporal and regional details: region, compostingTime, compostingMethod.

## Temporal Coverage
- Data collection: 07/11/2019 – 30/08/2023.
- Submissions occurred at variable intervals by volunteers.

## Collection Methods and Governance
- Data collected via online website survey and home composting experiment accounts.
- Data stored in a database as raw CSV; personally identifiable information removed to meet GDPR and ethics requirements.
- No data processing beyond raw collection; metadata included to describe variables and survey structure.
- Accessibility: open data represented in CSV; references to publication for further methodology and analysis.

## Quality, Limitations, and Governance
- Quality control: data contributed voluntarily by participants; no additional processing reported.
- Limitations relevant to monitoring and policy evaluation:
  - Self-selected, voluntary participation may introduce biases and limit representativeness.
  - Some data fields rely on participant self-reporting, which can affect accuracy.
  - Metadata standardization and completeness may vary across items (e.g., optional fields, open-text responses).
- Governance considerations:
  - Data anonymisation aligns with GDPR/ethics; data sharing is public, but remaining metadata requires careful interpretation.
  - Useful for understanding public attitudes toward compostable packaging and domestic composting practices, with potential implications for waste management policies and labeling schemes.

## Implications for Monitoring Frameworks and Policy Evaluation
- Provides a rich source of behavioural and attitudinal indicators related to home composting, consumer perceptions of compostable packaging, and waste management practices at the household level.
- Helps identify gaps between policy aims (e.g., adoption of compostable packaging) and public behaviour (e.g., food waste separation, use of composting systems).
- Data structure supports analysis of:
  - Public willingness to buy compostable packaging and underlying reasons.
  - Household composting practices, equipment types, and end-use outcomes.
  - Barriers to effective composting (space, knowledge, local services) as reported by participants.
- Demonstrates the value and challenges of integrating citizen science data into monitoring frameworks, including data governance, metadata quality, and the need for clear communication of complex findings.

## Access and Reference
- Data and results referenced with the Frontiers in Sustainability publication (24 months' analysis): https://www.frontiersin.org/journals/sustainability/articles/10.3389/frsus.2022.942724/full