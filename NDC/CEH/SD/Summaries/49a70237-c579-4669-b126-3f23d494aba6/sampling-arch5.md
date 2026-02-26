# Sampling Design

## Overview
- Timeframe: May 2014 to September 2014
- Study site: Mabalane district, Gaza province
- Village selection: seven villages along a forest degradation gradient (undisturbed to degraded, driven by charcoal production); similar infrastructure, soils, rainfall, and vegetation
- Objective: understand seasonality within a village and, if needed, use one seasonal calendar per geographic area (south vs north of Mabalane)
- Methodology per session: fieldwork led by a researcher with a local-language assistant (Changana)

## Data Collection Scope and Methods
- Seasonal calendar
  - Group discussions (5–10 participants), 1 hour per session
  - Materials: 12 month cards, activity cards, stones/seeds
  - Purpose: map seasonality of forest-related activities (e.g., agricultural cycles, charcoal production, fruiting)
  - Fixed-stone method to quantify proportions over time
- Trend analysis
  - Structured discussions to identify past changes in forest product availability and use
  - Timelines and time landmarks facilitated with ground cards
- Participatory mapping and ES focus
  - Identify key ecosystem services (e.g., charcoal production, wood for charcoal, firewood, hunting)
  - Determine past changes, drivers (licenses, outsiders, new laws), and expected future states (10-year horizon)
- Village profiles and governance
  - Leader interviews; multi-language capability (English, Portuguese, Changana)
  - Documentation of village name, GPS point, date, leader details, and village characteristics
- Wealth ranking
  - Quick/rigid exercise to categorize households into wealth classes (poorest, poor, better-off, rich)
  - Requires a reliable household list; typically 2 hours
  - Includes discussion of criteria such as agriculture, housing, education, health, and social relations

## Data Structure and Variables
- VillageProfile
  - Village name, GPS point, date, leader name, age, function, years in village
  - Village characteristics: structure (households, governance), education, health, water, land rights (DUAT), migration, livelihoods (LH Activities), commercial activities (COM Activities), market access
- ForestUse
  - Products used/transformed/traded, origins, involvement of producers
- CommoditizedES
  - Charcoal: production sites, sale points, quantity estimates, licenses, associations, external actors, governance (local decision-making, licensing revenue)
  - Agriculture: main crops, mashambas/fields, distances, productivity, market connections, extension presence
  - Livestock: main species, sale patterns, pasture
  - Others: additional traded forest products
- Change
  - Social change: major changes, timing, perceived improvement or deterioration
  - Environmental change: changes in forest area, plant/animal diversity, water availability/quality, soil; implications for daily life
  - Reasons for change: deforestation, market access, climate, etc.
- WealthRanking
  - Household list, four wealth classes, intra-class ranking, criteria discussion (attitude, agriculture, housing, education, nutrition, social relations)

## Language, Translation, and Accessibility
- Protocols documented in English and Portuguese with local-language (Changana) support
- Materials include bilingual sections to facilitate field work and participant understanding

## Data Quality, Provenance, and Ethics
- Field protocol followed; leader interviews and group discussions introduce multiple perspectives
- Potential biases and data quality considerations:
  - Recall bias for past changes and ten-year projections
  - Group dynamics influencing responses
  - Translation and interpretation differences across languages
- Privacy and sensitivity considerations:
  - Contains governance details (licenses, associations, outside actors), household wealth information, and GPS locations
  - Requires careful handling, potential anonymization or access restrictions
- Data provenance:
  - Documented processes, session structures, and participant roles (researcher, local assistant)

## Governance, Access, and Sharing Considerations
- The document does not specify a data sharing policy
- Recommendations for Data Stewards:
  - Define consent and anonymization requirements for village profiles, wealth rankings, and responsible-use statements
  - Establish data licensing and access controls (e.g., restricted access for sensitive governance information)
  - Capture metadata on languages used, data collectors, and field protocols
  - Store multilingual data with clear mappings between languages and translations
  - Include provenance metadata (dates, sessions, facilitator roles, translation notes)

## Technical Design and Interoperability
- Data are multi-format and bilingual; harmonization is necessary for cross-site analysis
- Suggested data formats: structured tabular data (CSV/JSON) for VillageProfile, ForestUse, CommoditizedES, Change, and WealthRanking; GIS-ready file for GPS coordinates
- Standardized vocabularies and codes recommended for:
  - Ecosystem services (ES categories)
  - Governance concepts (licenses, associations, outsiders)
  - Temporal references (months, seasons, past/future timepoints)
- Consider linking to a central data catalog with stable identifiers for villages, ES categories, and governance entities

## Reuse Potential and Recommendations
- Reuse opportunities:
  - Comparative analyses of forest-dependency, seasonality, and governance across villages along a degradation gradient
  - Studies on the social-ecological dynamics of charcoal production, licensing, and market access
  - Baseline data for longitudinal studies on environmental change and livelihood adaptation
- Recommended next steps for Data Stewards:
  - Develop a formal data dictionary and metadata schema
  - Create data collection templates aligned to a unified schema to enable interoperability
  - Implement data governance policies addressing consent, privacy, and access
  - Prepare data packages with anonymized village-level outputs and clearly defined licensing
  - Pilot a central data repository with versioning, provenance tracking, and multilingual support