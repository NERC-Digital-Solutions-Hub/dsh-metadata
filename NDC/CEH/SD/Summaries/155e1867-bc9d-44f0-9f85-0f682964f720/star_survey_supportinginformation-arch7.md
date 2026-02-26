# Strengthening Thailand's Agricultural Drought Resilience (STAR)

- Overview
  - A three-year (2018-2021) project funded by UKRI and TSRI to enhance drought resilience in Thailand’s agricultural sector.
  - Partners: UK (Centre for Ecology and Hydrology, Cranfield University) and Thailand (Chulalongkorn University, King Mongkut's University of Technology Thonburi, Chiang Mai University).
  - Focus: understand drought characteristics, impacts on food production and farmers’ livelihoods, and support proactive drought management through monitoring, warning, and targeted communication.
  - National scope with detailed work in the Ping catchment.

- Data collection (survey scope and methodology)
  - Target: villages in the Ping catchment with drought history; aim to represent typical agricultural production typologies.
  - Sampling: village headperson select farm household heads; trained enumerators conducted interviews after informed consent.
  - Coverage: 176 questionnaires completed in January 2020; provinces include Chiang Mai, Lamphun, Kamphaeng Phet, and Tak.
  - Quality control: enumerators trained; initial interviews reviewed; STAR project member observed throughout data collection.
  - Ethics: approved by Cranfield University Research Ethics System (CURES) CURES/9419/2019.
  - Language: questionnaire written in English, translated to Thai, then back-translated to English for analysis.

- Data description and structure
  - Guidance: use the STAR Survey Questionnaire (document not included here) for interpretation.
  - Dataset contents: 176 anonymised responses; each participant has a unique identifier (identifier_id2).
  - Data types: both quantitative and qualitative; units are as specified in the questionnaire.
  - Columns and layout:
    - Columns A–M: participant identifiers and interview location (province, village, district).
    - Columns N onward: responses to questions.
    - Example: Q1_age stored in column N.
    - For multi-choice questions (e.g., Q5), multiple columns exist (Q5_1, Q5_2, ..., Q3_12) corresponding to each option.
  - Geographic information: location at the province, village, and district level; suitable for integration with GIS mapping at village-level resolution.

- Data use, guidance, and interpretation
  - The dataset is intended to support analyses of socioeconomic impacts of historical droughts and factors influencing adaptation decisions, as well as communication patterns among farmers.
  - The data are designed to be combined with other data sources (e.g., hydrometeorological or socioeconomic datasets) for richer GIS analyses.
  - Users should reference the accompanying STAR Survey Questionnaire for context and variable definitions.

- Spatial context and GIS considerations
  - Primary spatial granularity: village-level within the Ping catchment.
  - Potential GIS products: maps of risk appraisal, adaptation behavior, drought communications, and demographic attributes across villages and provinces.
  - Data integration: plan to harmonize with other data sources that may have different resolutions; be mindful of potential resolution mismatches and data standards gaps noted by STAR.
  - Privacy and ethics: dataset is fully anonymised; uses a unique identifier to protect respondent identities.

- Limitations and data gaps
  - Lack of comprehensive hydrometeorological and broader socioeconomic databases in Thailand identified as a research gap.
  - Data standards may be inconsistent across datasets; combining multiple sources requires careful normalisation.
  - The dataset focuses on the Ping catchment, with national scope but deeper local detail only in the Ping area.