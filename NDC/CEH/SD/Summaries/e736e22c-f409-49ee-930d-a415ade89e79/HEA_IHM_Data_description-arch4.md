# HEA/IHM data collection guide for NERC upload

## Overview
- Dataset comprises HEA (Household Economy Approach) data from 16 communities in Katakwi district and IHM (Individual Household Method) data from Anyangabella (42 households) and Kaikamosing (51 households), collected in December 2020.
- Data are aimed at illustrating crop calendars and livelihood indicators to support vulnerability analysis and resilience-focused policy development.
- Source materials reference EfD (Evidence for Development) methodology resources.

## Methodology

- HEA methodology
  - Demarcate rural livelihood zones based on land use, climate, rainfall, markets, and economics.
  - Identify a reference year via local informants and purposively select sample locations representing variation within zones.
  - Conduct village interviews to define wealth-group characteristics and establish typical household profiles per wealth group.
  - Interview focus groups from each wealth group to determine typical incomes and expenditures in the reference year.
  - Use baseline data to simulate impacts of shocks on access to food and basic needs.

- IHM methodology
  - Identify livelihood zones, select survey sites, and gather contextual local economy information via focus groups.
  - Conduct semi-structured household interviews using open-IHM software for in-field data checking and analysis.
  - Collect comprehensive data on demography, assets, crop/livestock production, employment, wild foods, transfers, and relevant household characteristics (e.g., gender of head, education).
  - Enter data into open-IHM software with in-field consistency checks; revisit households if anomalies arise and amend datasets as needed.

- Data validation
  - In-field checks for internal consistency, biological adequacy, and alignment with observed living conditions; anomalies trigger follow-up.

- Documentation and sourcing
  - Information drawn from EfD’s HEA/IHM methodology resources; dataset accompanied by reference URLs.

## Data structure and contents

- Data scope
  - HEA: data reported per community and wealth group (three wealth groups), including workforce/sample site details and disposable income metrics.
  - IHM: data reported per individual, covering multiple income sources and household characteristics.

- Key data categories
  - Monetary and consumption metrics (in UGX and kilocalories): 
    - Community Disposable Income (DI), including DI with Standard of Living (SoL) and DI with SoL adjustments (adult equivalents, etc.).
    - Cash Income categories (e.g., crops, livestock, employment, transfers, wild foods).
    - Food Income categories (calorie-based equivalents across similar subcategories).
  - Assets and capital
    - Land Assets (types: upland, upland rented, wetland) and livestock assets (by type).
  - Welfare and household characteristics
    - Adult Equivalent calculations, household composition, headship, and education.
    - Population breakdown by gender and age ranges.
  - Micronutrients (development in progress) and other data columns
    - Custom report specifications and data summaries as automatically generated.

- Granularity and output
  - HEA data present at community-wealth-group level; IHM data present at the level of individual households.
  - Data types include monetary values (UGX), energy (kcal), household size, and asset inventories.

- Completeness
  - Described as a complete data set, with accompanying documentation to aid interpretation.

## Data collection context and governance

- Local data collection team comprised of Ugandan partners.
- Data collected in local language and later translated into English by the data collectors.
- Dataset intended to support vulnerability assessment and targeted policy development at both household and community levels.

## Relevance and considerations for Data Leaders

- Methodological clarity is essential: HEA vs. IHM approaches yield different data resolutions (wealth-group vs. individual).
- Data quality controls are integrated into fieldwork (in-field checks, revisits for anomalies) and open-IHM data entry.
- The dataset supports resilience analysis, requiring clear metadata on units (UGX, kcal), definitions (DI, SoL), and conversion rules (adult equivalents).
- Governance notes emphasize local collaboration and translation processes, affecting metadata, discoverability, and reuse.