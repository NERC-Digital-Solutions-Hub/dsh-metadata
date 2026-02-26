# Survey of opinions and behaviours regarding home composting, alongside experimental data for disintegration and degradation of compostable materials, UK, 2019-2023

## Overview
- Big Compost Experiment was a voluntary UK citizen science study (2019–2023) focusing on compostable plastics and home composting.
- Aims:
  - Investigate the role and effectiveness of biodegradable and compostable packaging in the UK.
  - Engage the public and raise awareness about plastic waste issues.
  - Gather information and public opinion on biodegradable/compostable packaging and domestic compost habits/environments in the UK.

## Data assets
- Two CSV data files:
  - Big_Compost_Experiment-composter-items.csv: qualitative and quantitative data from home compost experiments per participant.
  - Big_Compost_Experiment-surveys.csv: survey responses on opinions, behaviours, and domestic waste practices.

## Data structure and content
- Big_Compost_Experiment-composter-items.csv
  - Participant and experiment identifiers (e.g., id, composterId).
  - Timestamps (dateCreated, dateUpdated) and product details (compostableType, productName, quantity, datePurchased).
  - Certification marks (certificationMarks, certMarksOther) and packaging details (netBagUsed, netBagFound).
  - Degradation observations (degradationLevel) and qualitative results (comments).
  - Composting setup (composterType, region, compostingMethod, compostingTime) and process timings (dateStarted, dateFinished).
- Big_Compost_Experiment-surveys.csv
  - Participant identifiers and timestamps (id, dateCreated, dateUpdated).
  - Attitudinal and behavioural items (e.g., likelyToBuyCompostablePackaging, likelyToBuyCompostablePackagingReasons).
  - Household waste practices (separatesFoodWaste, usesCouncilWaste, councilWasteItems, councilWasteItemsOther).
  - Home composting practices (usesComposter, compostItems, compostItemsOther, composterType, composterTypeOther, compostUses, compostUsesOther).
  - Other strategies and locations (usesOtherStrategy, otherStrategy, otherStrategyItems, otherStrategyItemsOther, whereDoYouCompost, whereDoYouCompostOther).
  - Observations and outcomes (compostLife, compostLifeOther).
- Both files include enumerated categories and multiple open-text fields; some fields allow missing values.

## Collection and scope
- Data collection method: online voluntary survey and home composting experiment accounts.
- Coverage: UK participants.
- Temporal coverage: 07/11/2019 – 30/08/2023.
- Data storage: raw data in CSV format within a database; personally identifiable information (names, emails) removed to meet GDPR and ethics requirements; no further data processing recorded.

## Data governance and quality
- Quality control: data contributed voluntarily by participants; no additional processing beyond collection.
- Ethics and privacy: PII removed; GDPR compliance noted.
- Documentation: descriptive variable lists and file descriptions provided; data referenced to a published 24-month analysis for details and flowchart.

## Access, format, and documentation
- File format: CSV for both datasets.
- Documentation: includes detailed variable descriptions and valid value vocabularies (e.g., product categories, region codes, composter types, timing categories).
- Related publication: 24 months’ analysis available at Frontiers in Sustainability (link provided in the summary).

## Temporal coverage and collection cadence
- Data collection occurred over nearly four years with variable submission intervals by volunteers.
- Final data capture date: 30 August 2023.

## Related resources and references
- Publication: 24 months’ analysis of the study, with additional details including a survey flowchart.
- Link: Frontiers in Sustainability article (URL provided in the dataset summary).

## Strategic value for Data Leaders
- Data assets cover both behavioral survey data and experimental results on compostable materials, enabling cross-analysis of attitudes, practices, and real-world degradation outcomes.
- Rich metadata and structured variable dictionaries support discoverability, reuse, and integration with other sustainability or consumer-behavior datasets.
- Data governance practices highlighted (de-identification, GDPR compliance) illustrate practical handling of citizen-science data and ethical considerations.
- Potential data challenges to address in future initiatives include standardizing variable definitions across datasets, improving data quality through guided responses, and enhancing metadata for discoverability and cross-study interoperability.