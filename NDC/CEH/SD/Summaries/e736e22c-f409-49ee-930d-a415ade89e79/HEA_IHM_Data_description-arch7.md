# HEA/IHM data collection guide for NERC upload

- The document describes a dataset from the HEA (Household Economy Approach) and IHM (Individual Household Method) collected in 16 communities in Katakwi district, plus 42 households in Anyangabella and 51 households in Kaikamosing, collected in December 2020. It focuses on crop calendars and the underlying data collection methodology.

## Methodology (HEA and IHM)

- HEA approach
  - Demarcates rural livelihood zones based on land use, climate, rainfall, markets, and other economic information.
  - Identifies a reference year and selects representative sample locations across zones.
  - Conducts village-level interviews to define wealth-group characteristics (e.g., very poor to better-off).
  - Uses focus-group interviews within wealth groups to establish typical incomes and expenditures for the reference year.
- IHM approach
  - Semi-structured interviews with field-use of open-IHM software for in-field data checking and analysis.
  - Stage 1: identify livelihood zones and survey sites; collect contextual economic data from focus groups.
  - Stage 2: interview selected households covering income sources, assets, demography, production (crops/livestock), employment, wild foods, transfers, and household characteristics.
  - In-field data validation with checks for internal consistency; households revisited if anomalies are found.
  - Data entered into open-IHM software, enabling rapid analysis and data quality control.

## Data content and structure

- Data scope
  - Quantitative information on household or individual livelihoods.
  - Monetary data in Uganda Shillings (UGX) for HEA (per wealth group) and IHM (per individual).
  - HEA data is reported by Community and Wealth Group; IHM data is reported per individual.
- Key data headings and categories (examples)
  - Community Disposable Income (DI): income remaining after food energy needs; may be negative.
  - DI with Standard of Living (STOL): standardisation by household size or adult equivalent; includes costs of essential items and social inclusion.
  - DI with Standard of Living: subheadings include Family Group Size and Disposable Income; additional fields such as KCal Requirement and STOL costs.
  - Cash Income: multiple subcategories including Crop Cash Income, Employment, Livestock, Transfers, Wild Foods; reported as monetary values.
  - Food Income: income from all sources in kilocalories (kcal).
  - Land Assets: owned land by household/wealth group; includes upland and wetland classifications.
  - Livestock Assets: types and counts of owned livestock.
  - Custom Report Spec: auto-generated data summaries and self-explanatory fields.
- Additional IHM categories
  - Calculate Adult Equivalent (kcal basis for STOL and DI).
  - Report HH Members Character (age, sex, household head status, etc.).
  - Report Population by Age/Sex (summary counts).
- File structure
  - Each file corresponds to one aspect of data (HEA or IHM); HEA files present data by community and wealth group; IHM files present data by individual.

## Data collection and quality assurance

- Data collected by local Ugandan partners.
- Conducted in the local language and translated into English by collectors.
- Field workflows include cross-checking responses with context data, in-field data entry, and revisits for anomalies to ensure data integrity.

## Purpose and potential GIS applications

- Designed to support vulnerability assessment and livelihood impact modelling.
- Enables targeted policy development to enhance resilience at household and community levels.
- GIS-relevant use cases
  - Map livelihood zones and wealth-group distributions across communities.
  - Visualise disposable income, caloric coverage, and standard-of-living costs by zone or wealth group.
  - Map assets (land and livestock) and income streams to support spatial planning and resilience analysis.
  - Overlay crop calendars with livelihood data for spatial decision-making.

## Provenance and status

- Collected in December 2020 by a local partnership.
- Data set is presented as a complete dataset.
- All monetary data presented in UGX; some advanced categories (e.g., Micronutrients) are under development.