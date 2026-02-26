# Survey of opinions and behaviours regarding home composting, alongside experimental data for disintegration and degradation of compostable materials, UK, 2019-2023

## Overview and aims
- UK citizen science study (Big Compost Experiment) conducted 2019–2023 to investigate the role and effectiveness of biodegradable/compostable packaging in the UK.
- Aimed to raise public awareness of plastic waste issues and gather information on public opinion and domestic compost habits.
- Data support potential: analyze attitudes toward compostable packaging, domestic composting behaviours, and results from home compost experiments; create accessible data products for exploration and decision-making.

## Data assets and formats
- Two CSV data files compiled from online surveys and home compost experiments:
  - Big_Compost_Experiment-composter-items.csv: records from home compost experiments (item-level observations and experiment details).
  - Big_Compost_Experiment-surveys.csv: participant survey responses on opinions, behaviours, and household waste practices.
- Data collected via an online voluntary platform; dataset stored in a database and exported as raw CSVs.
- Personal data (names, emails) removed to meet GDPR and ethics requirements; no additional processing applied beyond cleaning for submission.

## Data contents at a glance
- composter-items file (experimental data)
  - Key fields include: id, dateCreated, dateUpdated, compostableType, productName, quantity, datePurchased, certificationMarks, netBagUsed, degradationLevel, netBagFound, comments, composterId, dateStarted, dateNotified, dateFinished, composterType, region, compostingMethod, compostingTime.
  - Describes product tested, packaging types, composting setup, and observed degradation outcomes.
- surveys file (opinion/behaviour data)
  - Key questions include: likelihood to buy compostable packaging; reasons for that choice; food waste separation at home; use of council waste collections and/or home composters; items put in composting; other waste strategies; where composting occurs; type of composter; what compost is used for; observed life in the composter.
  - Contains both structured responses (yes/no, categories) and open-text fields for detailed responses.
- Note: where participants did not submit data, corresponding fields contain no value.

## Temporal coverage and collection methods
- Data collection period: 07/11/2019 – 30/08/2023.
- Data gathered from volunteers at varying times; responses are self-reported via an online platform.

## Data quality and privacy
- Data voluntarily provided by participants; no additional data processing beyond basic CSV export.
- Personally identifiable information removed to comply with GDPR and ethics requirements.
- Potential limitations: self-selection bias; variable response completeness; mixed data types (qualitative and quantitative).

## How to use and potential data products
- Data exploration and self-service dashboards to compare:
  - Attitudes toward compostable packaging by region, composting method, and awareness of certification marks.
  - Household waste practices (food waste separation) and their relationship to composting activity.
  - Degradation outcomes by compostable type, packaging, and composter type.
- Possible data synthesis tasks:
  - Join composter-items with surveys via composterId/participant id to correlate observed degradation with user attitudes and behaviours.
  - Analyze factors associated with likelihood to buy compostable packaging and its stated reasons.
- Related resource:
  - 24 months of analysis publication for deeper methodology and findings: Frontiers in Sustainability (link provided in dataset summary).

## Practical considerations for data support
- Data preparation tips:
  - Validate and harmonize categorical codes (e.g., compostableType, composterType, region) and date fields.
  - Handle missing values in both files, noting that non-submissions are represented as blanks.
  - Link records across files using identifiers (composterId and participant-related fields) for integrated analyses.
- Data interpretation cautions:
  - Self-reported behaviours may not reflect actual long-term practices.
  - DegradationLevel is participant-observed and subjective; consider corroborating with auxiliary data or experiment protocols if available.

## Access to further details
- Publication reference for detailed methodology and analysis: 24 months' analysis available at Frontiers in Sustainability (link in dataset description).