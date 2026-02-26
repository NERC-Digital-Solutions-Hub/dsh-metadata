# Ecosystem services variables from the UK Environmental Change Network (ECN)

## Overview
- The Environment Change Network (ECN) conducts long-term environmental monitoring across a network of sites in the UK.
- This dataset provides ecosystem services variables for ECN sites, built around the Millennium Ecosystem Assessment (MA) framework.
- Purpose: support assessment of how ecosystems deliver services and how these services vary across sites and over time.

## Scope and framework
- 11 ECN sites included, with boundary decisions based on land ownership, land management, and social decision boundaries; boundaries sometimes align with ECN sites and sometimes with whole management units or basins.
- Variables are organized to cover a comprehensive set of ecosystem services, drawn from MA definitions and site knowledge.
- All variables are scaled to site area where appropriate and data for a single year (commonly 2009) or yearly/annual averages are used to reduce temporal variability.
- Data sources integrate:
  - ECN standard protocol data
  - Site manager data from other sources
  - Expert knowledge of site managers

## Sites and boundaries
- Site codes include ALI (Alice Holt), CAI (Cairngorm), DRA (Drayton), GLE (Glensaugh), MOO (Moor House), NOR (North Wyke), POR (Porton Down), ROT (Rothamsted), SNO (Snowdon), SOU (Sourhope), WYT (Wytham)
- Total area across all sites: 11,262 hectares
- Boundary characteristics frequently include land management and land ownership; some sites align with ECN site boundaries, others with entire water basins or management units

## Variables and structure
- Instrument comprises 73 ecosystem service variables (Variable_Number 1–73), spanning:
  - Provisioning and food resources (e.g., meat, cereals, eggs, fruits, vegetables, wool/fibre)
  - Material and energy resources (e.g., wood, hydro power)
  - Genetic resources and biochemicals
  - Cultural and aesthetic values (e.g., ornamental resources, cultural diversity, education, ecotourism, aesthetic indicators)
  - Regulating ecosystem services (air quality regulation, climate regulation, water regulation, erosion control, natural hazards)
  - Biodiversity and ecological functions (pollination, biological control, pest presence, habitat resources)
  - Human health and safety indicators (diseases, hazards)
  - Social and accessibility factors (population within proximity, ease of access)
  - Heritage and ecotourism metrics (special features, visitor numbers)
- Variable definitions are provided in the accompanying tables, including units (e.g., tonnes per hectare, MWh per site, yes/no), and specific measurement details (e.g., net CO2e flux, N/S deposition flux, annual butterfly counts)
- Example variable types include:
  - Food production: meat (tonnes ha-1), cereals/eggs/vegetables/fruit/mushrooms (yes/no or counts)
  - Fibre and materials: wool, wood, hydro output
  - Regulatory services: air quality and climate regulation (CO2e), water regulation and erosion
  - Cultural and social: cultural diversity, educational use, ecotourism visitors
  - Biodiversity indicators: pollinators, pests, natural hazards (fires), species counts
  - Heritage and aesthetics: number of features, number of CVs (conservation value types), etc.

## Data format and access
- Original format: Excel 2007
- Converted format: comma-separated values (CSV) for long-term storage
- Dataset structure includes:
  - Service type and variable definitions
  - Variable_ID and Variable_Number
  - Site-specific columns: ALI, CAI, DRA, GLE, MOO, NOR, POR, ROT, SNO, SOU, WYT
- Documentation includes Table 2 (variable definitions), Table 3 (dataset format and site mapping), and Table 1 (site-level boundary characteristics)
- Data availability and citation information provided for proper use and attribution

## Usage and implications
- Useful for cross-site comparisons of ecosystem services across the ECN network
- Allows creation of data products (dashboards, summaries) to enable self-service exploration of ecosystem services
- The dataset underpins analyses such as comparative ecosystem service delivery across long-term monitoring sites (as in the referenced Environmetrics paper)

## References
- Millennium Ecosystem Assessment (2005): Ecosystems and human well-being
- Dick, J. et al. (2011). A comparison of ecosystem services delivered by 11 long-term monitoring sites in the UK environmental change network. Environmetrics, 22(5), 639-648. DOI: 10.1002/env.1069
- Data availability and citation for the dataset: Ecosystem services variables from the UK Environmental Change Network (ECN). NERC Environmental Information Data Centre. DOI: 10.5285/2c5f823d-0dca-4e66b021-de3e81131979