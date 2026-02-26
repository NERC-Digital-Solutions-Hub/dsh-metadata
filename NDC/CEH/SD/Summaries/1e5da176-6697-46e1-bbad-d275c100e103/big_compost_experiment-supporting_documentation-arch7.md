# Survey of opinions and behaviours regarding home composting, alongside experimental data for disintegration and degradation of compostable materials, UK, 2019-2023

## Overview
- A UK citizen science study (Big Compost Experiment) conducted 2019–2023 to investigate biodegradable/compostable packaging and home composting.
- Aims include assessing public opinion, raising awareness of plastic waste, and gathering data on home compost habits and environments.
- Data types: qualitative and quantitative survey responses and home compost experiment results from UK participants.
- Data collected via an online survey and participant accounts; anonymised (GDPR/ethics compliant).

## Datasets and File Formats
- Data files (CSV):
  - Big_Compost_Experiment-composter-items.csv: item-level results from compost experiments and associated product metadata.
  - Big_Compost_Experiment-surveys.csv: survey responses about attitudes, behaviors, and related practices.
- Role of the data: supports analysis of attitudes toward compostable packaging, food waste practices, composting methods, and observed degradation of compostable items.

## Data Structure and Key Variables
- composter-items (experiment data)
  - id, composterId, dateCreated/dateUpdated, region (UK region), composterType, compostingMethod, compostingTime.
  - compostableType, productName, quantity, datePurchased, certificationMarks, netBagUsed, degradationLevel, netBagFound, comments.
  - Additional fields: dateStarted/dateFinished/dateNotified; composterType options include various outdoor/indoor systems; region categories reflect UK geography; degradationLevel ranges from 0 (intact) to 4 (no longer visible).
- surveys (survey data)
  - id, dateCreated/dateUpdated.
  - LikelyToBuyCompostablePackaging and LikelyToBuyCompostablePackagingReasons (open text).
  - SeparatesFoodWaste (yes/no) and Can include reasons for not separating (with predefined options and an open-text Other).
  - usesCouncilWaste and councilWasteItems (and Other), usesComposter and compostItems (and Other), usesOtherStrategy and otherStrategyItems (and Other).
  - Other related fields: whereDoYouCompost (home/work/other), composterType (and Other), compostUses (and Other), compostLife (observed organisms), and related open-text fields.
- Temporal coverage
  - Data collection: 07/11/2019–30/08/2023.
  - Reports indicate variable submission intervals by volunteers.
- Data collection/handling notes
  - Data collected via online survey/account; stored as raw CSV.
  - Personally identifiable information removed to meet GDPR/ethics; no additional processing applied.
  - Data shared on a voluntary basis.

## Spatial and Temporal Coverage
- Spatial: region field provides UK regional granularity (Greater London, East England, etc.), enabling regional mapping and analysis.
- Temporal: data captured over several years with multiple submission points; experiments had varying durations (3–24+ months as per compostingTime field).

## Quality and Limitations
- Quality control: data contributed voluntarily by participants; no additional processing beyond anonymisation.
- Limitations for GIS use:
  - Data are CSVs with regional and categorical fields; no geospatial files included.
  - Potential sampling bias due to voluntary participation; variable data completeness (some open-text fields may be incomplete).

## GIS and Data Visualization Opportunities
- Regional analysis: map attitudes toward compostable packaging and home composting practices by UK region.
- Material and process mapping: visualize degradation outcomes by compostableType, composterType, and compostingMethod.
- Temporal trends: explore changes in attitudes over 2019–2023 if time-series analysis is applied to date fields.
- Integrated visualizations: combine with external GIS datasets (e.g., local authority waste programs, composting facilities) to contextualize behavior and infrastructure.
- Data preparation steps for GIS:
  - Join region codes to a UK regional shapefile.
  - Normalize categorical fields (e.g., compostableType, certificationMarks) for consistent mapping.
  - Link open-text responses to qualitative analysis for enriched map popups or dashboards.

## Access, Provenance, and Documentation
- Data provenance: collected via a public-facing website survey and home composting experiments; anonymised for GDPR.
- Related publication: 24 months' analysis with a detailed survey flowchart available at Frontiers in Sustainability (link provided in the dataset description).
- File naming and structure: two primary CSV files as listed above; clear variable descriptions within each file’s schema.