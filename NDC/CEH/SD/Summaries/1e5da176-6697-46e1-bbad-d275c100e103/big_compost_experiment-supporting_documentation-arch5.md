# Summary: Survey of opinions and behaviours regarding home composting, alongside experimental data for disintegration and degradation of compostable materials, UK, 2019-2023

## Aim and Scope
- Large-scale citizen science study (Big Compost Experiment) conducted in the UK from 2019 to 2023.
- Aimed to investigate the role and effectiveness of biodegradable/compostable packaging, raise public awareness about plastic waste, and gather public opinion on compost habits and environments in the UK.
- Outputs include qualitative and quantitative survey responses and home compost experiment results from participants; data collected via online surveys and participant accounts, stored in a database.

## Data Holdings
- Two CSV data files:
  - Big_Compost_Experiment-composter-items.csv (compost experiment items per participant)
  - Big_Compost_Experiment-surveys.csv (survey responses)
- Data are raw, collected via an online portal, with personally identifiable information removed to meet GDPR and ethics requirements.
- Data accompany a 24-month analysis publication and related materials.

## Data Content and Variables
- composter-items.csv:
  - key fields include: id (participant survey/compost item id), dateCreated, dateUpdated, compostableType (product category tested), productName, quantity, datePurchased, certificationMarks, netBagUsed, degradationLevel, netBagFound, comments, composterId, dateStarted, dateNotified, dateFinished, composterType, region, compostingMethod, compostingTime.
  - Units are mostly numeric or standardized categorical descriptors; open-text fields for descriptions and comments.
- surveys.csv:
  - key fields include: id, dateCreated, dateUpdated, LikelyToBuyCompostablePackaging, LikelyToBuyCompostablePackagingReasons (open text), separatesFoodWaste, doesntSeparateFoodWasteReasons (including several predefined options and open text), usesCouncilWaste, councilWasteItems (with several categories), usesComposter, compostItems, composterType, whereDoYouCompost, compostUses, compostLife, and related open-text fields.
  - Data types include Yes/No/Unknown, 0/1 indicators, multiple select categories, and open-text responses.
- Nature of data:
  - Qualitative and quantitative measures of opinions, behaviours, and observed composting results.
  - Open-text responses provide contextual insights; structured fields support aggregation and analysis.

## Methods, Quality, and Stewardship
- Collection and Transformation:
  - Data collected via an online website survey and home composting experiment accounts; stored as raw CSV in a database.
  - No further data processing performed on these files within the project scope.
- Quality Control:
  - Data contributed voluntarily by participants; no additional quality control described beyond voluntary participation.
- Data Handling and Privacy:
  - Personally identifiable data (names, emails) removed to comply with GDPR and ethics requirements.
  - Indicates minimal data processing beyond collection; datasets represent participant-reported observations and survey responses.
- Temporal Coverage:
  - Data collection conducted between 07/11/2019 and 30/08/2023.
  - Submissions occurred at variable intervals across participants and time.

## Access, Documentation, and Publication
- File naming conventions provided for reproducibility and cataloguing.
- Related publication: 24 months’ analysis with survey flowchart available at Frontiers in Sustainability (link provided).
- Data are presented in CSV format; documentation includes a data dictionary embedded in the description of variables.

## Governance, Compliance, and Data Stewardship Considerations
- Data are suitable for discovery, reuse, and secondary analysis within contexts of citizen science, household waste management, and packaging biodegradability research.
- Practical governance notes:
  - Ensure comprehensive, machine-readable metadata and a formal data dictionary for long-term usability.
  - Consider licensing terms and usage rights to facilitate sharing while protecting participant privacy.
  - Establish data provenance, versioning, and update mechanisms if the dataset is extended or re-released.
  - Provide clear data quality notes, potential biases (voluntary participation, self-reported data), and limitations related to open-text responses.
  - Align with standard metadata schemas (e.g., include data collection methods, instruments used, definitions of variables, and coding schemes).

## Miscellaneous and Reference
- The dataset references a public publication for additional methodological details and survey flow (Frontiers in Sustainability, 2022).
- No explicit embargo or licensing information stated in the provided text; recommendation to accompany data with licensing and usage guidance for future data stewardship.