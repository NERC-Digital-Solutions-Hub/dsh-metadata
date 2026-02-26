# Strengthening Thailand's Agricultural drought Resilience (STAR)

## Purpose and scope
- A comprehensive questionnaire designed to collect household-level data on farming demographics, farm characteristics, drought experiences, adaptation strategies, compensation/support, and drought warning information.
- Aims to inform STAR by understanding exposure, impacts, responses, information sources, and perceived effectiveness of adaptations.

## Data collected: overview by sections

- Section 1: Background information and farming activities
  - Respondent demographics (age group, education)
  - Farm type and production focus
  - Household farm size, assets (land, animals, crops), and tenure
  - Infrastructure and connectivity (Wi‑Fi, mobile phones, electricity)
  - Household labor and income context; irrigation details (sources, methods, percentages)
  - Historical changes over the past decade (area, animals, crops, non-agricultural income)

- Section 2: Drought experiences and perceptions
  - Definition of drought by respondents
  - Frequency of drought experiences in the last 10 years and recall of specific years
  - Impacts on crops, livestock, income, input costs, and farmer wellbeing
  - Perceived outlook: likelihood of negative drought impacts, information sufficiency, and severity
  - Self-assessed information status: awareness of drought risks

- Section 3: Drought adaptation strategies
  - Range of adaptation measures (water management, crop adjustments, irrigation changes, soil and water conservation)
  - Whether each measure reduced drought impacts (perceived)
  - Prioritization of crops (drought-tolerant vs high-value) and other prioritized strategies
  - Measures to improve soil moisture and aquifer recharge; animal and feed management during droughts
  - Income diversification and other adaptation options
  - Barriers to implementing longer-term adaptations and other unlisted strategies

- Section 4: Compensation and support
  - Availability and receipt of financial compensation
  - Other types of support received (seeds, debt relief, etc.)

- Section 5: Drought warning and adaptation advice
  - Past notifications of impending drought and information received
  - Information on what to do under drought and actions taken (or reasons for inaction)
  - Information flow from other farmers and organizations, and the breadth of organizations involved
  - Channels used to receive information (face-to-face, village meetings, radio, TV, social media, etc.)
  - Frequency of drought-related communications and perceived usefulness/accuracy of information
  - Evaluation of organizations providing drought information (trust, timeliness, relevance, format)

## GIS-relevant data opportunities and outputs

- Spatially-enabled household data
  - Geolocated farm points with attributes: farm size, type, irrigation method, water sources, ownership/tenure, assets, connectivity, income band
  - Temporal layers to capture drought frequency and adaptation uptake over time

- Water and land features
  - Water sources (river, canal, well, tubewell) and irrigation infrastructure (drip, flood, surface, etc.)
  - Proximity to rivers, canals, reservoirs; groundwater/water availability indicators

- Drought exposure and impacts
  - Drought frequency and severity indicators by location
  - Reported impacts by sector (crops, livestock, income, wellbeing) mapped to spatial units

- Adaptation and information networks
  - Locations of information-providing organizations and their channels
  - Spatial patterns of adaptation measures adoption (e.g., drip irrigation, drought-tolerant crops)

- Data products for end users
  - Interactive dashboards and maps for policymakers, extension services, and farmers
  - Scenario-based maps showing potential outcomes under different adaptation choices
  - Network maps of information dissemination to identify outreach gaps

## Data quality, standards, and integration challenges

- Data quality considerations
  - High reliance on self-reported data with potential recall bias (last 10 years)
  - Heterogeneous data sources and varying resolutions
  - Privacy and anonymization requirements for farm-level data

- Standards and interoperability
  - Need for consistent coding for farm types, irrigation methods, water sources, and adaptation measures
  - Harmonization across multi-site data collection (regions, communities)

- Data integration
  - Combining household data with environmental layers (soil moisture, rainfall, river/discharge, reservoir levels)
  - Aligning temporal scales (annual and seasonal drought indicators) with survey timing

## Stakeholders and data governance

- Primary participants: farmers and farming households
- Information-providers and channels: community organizations, government agencies, NGOs, private sector actors
- Channels for data use: policy planning, extension services, disaster risk reduction, climate resilience programs

## Practical guidance for GIS specialists

- Design a geodatabase structure that clearly links spatial locations with rich attribute data from Sections 1–5
- Define standardized codebooks for variables (farm type, irrigation method, water source, adaptation measures)
- Create spatial layers representing: farm locations, land area, irrigation infrastructure, water sources, environmental features, and information networks
- Incorporate temporal dimensions to analyze drought frequency and adaptation over time
- Build user-friendly map templates and dashboards that cater to policymakers and field officers, with clear legends and filters
- Ensure data privacy and anonymization when sharing spatial datasets
- Facilitate iterative, user-centered development: start with prototype maps and collect feedback from end users

## Key takeaways for effective GIS-enabled drought resilience work

- The questionnaire provides rich, multi-dimensional data suitable for geospatial analysis when geocoded
- It enables mapping of exposure (drought frequency/impacts) and response (adaptation uptake, information access)
- Integrating survey data with environmental datasets can support risk assessment, targeted interventions, and monitoring of STAR outcomes
- Attention to data quality, standardization, and stakeholder feedback is essential to develop reliable, actionable map-based products