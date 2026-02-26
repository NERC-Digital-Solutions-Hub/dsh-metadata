# Survey of opinions and behaviours regarding home composting, alongside experimental data for disintegration and degradation of compostable materials, UK, 2019-2023

- Aim and scope
  - Large citizen science study (Big Compost Experiment) conducted 2019–2023 in the UK.
  - Aims: assess role and effectiveness of biodegradable/compostable packaging; engage the public and raise awareness of plastic waste; gather information on domestic compost habits and environments.
  - Data include both opinions/behaviours and experimental results on disintegration/degradation of compostable materials.

- Datasets and formats
  - Two CSV data files:
    - Big_Compost_Experiment-composter-items.csv: experimental results from home compost tests.
    - Big_Compost_Experiment-surveys.csv: qualitative and quantitative survey responses about opinions and behaviours.
  - Data collected via online survey and home-composting experiment accounts; stored in a database; PII removed to meet GDPR/Ethics.

- Data structure and key variables
  - composter-items file (experimental data)
    - id, dateCreated, dateUpdated, compostableType, productName, quantity, datePurchased
    - certificationMarks, certificationMarksOther
    - netBagUsed, degradationLevel (0–4), netBagFound, comments
    - composterId, dateStarted, dateNotified, dateFinished
    - composterType, region, compostingMethod, compostingTime
  - surveys file (opinion/behaviour data)
    - id, dateCreated, dateUpdated
    - likelihood to buy compostable packaging (likelyToBuyCompostable Packaging) with Yes/No/Unknown
    - reasons for likelihood (likelyToBuyCompostable PackagingReasons)
    - separatesFoodWaste (yes/no) and related reasons (doesntSeparateFoodWasteReasons, ...Other)
    - usesCouncilWaste, councilWasteItems, councilWasteItemsOther
    - usesComposter, compostItems, compostItemsOther
    - usesOtherStrategy, otherStrategy, otherStrategyItems, otherStrategyItemsOther
    - whereDoYouCompost, whereDoYouCompostOther
    - composterType, composterTypeOther
    - compostUses, compostUsesOther
    - compostLife, compostLifeOther
  - Notes: many fields use predefined categorical options (lists provided in the file descriptions).

- Temporal coverage and collection methods
  - Data collection period: 07 November 2019 to 30 August 2023.
  - Participants submitted data at variable times; data entry was voluntary.
  - Data collected via an online website survey and home composting experiment accounts.

- Data quality, privacy, and governance
  - Personal data (names/emails) removed to comply with GDPR and ethics requirements.
  - No additional data processing beyond initial collection; data shared voluntarily by participants.
  - Acknowledge potential biases from self-selected, voluntary sample and non-standardised self-report.

- How analysts can use this data
  - Descriptive analytics of attitudes vs. behaviours around compostable packaging.
  - Cross-dataset analyses linking survey responses with experimental results by composterId (e.g., association between attitudes to compostables and actual degradation outcomes).
  - Regional and composting-method analyses to explore variation in practices and effectiveness across UK regions and different composting approaches.
  - Time-based analyses of engagement, changes in attitudes, or product testing over the 2019–2023 period.
  - Data quality tasks: harmonise categorical labels, handle missing entries, merge datasets on composterId, and standardise region/composter-type taxonomies.
  - Potential models: predictors of likelihood to buy compostable packaging; factors associated with higher degradation levels or more complete disintegration.

- Related resources and access
  - For deeper details, see the 24-month analysis publication:
    - Frontiers in Sustainability article (2022): https://www.frontiersin.org/journals/sustainability/articles/10.3389/frsus.2022.942724/full
  - Dataset is provided as raw CSV files without further processing beyond removal of personal identifiers.