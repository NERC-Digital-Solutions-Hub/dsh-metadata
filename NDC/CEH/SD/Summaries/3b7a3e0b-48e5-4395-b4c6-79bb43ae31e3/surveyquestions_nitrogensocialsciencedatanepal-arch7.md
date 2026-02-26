# SANH WP 1.3 Harmonised Individual Questionnaire

## Overview
- A harmonised household-level questionnaire for the South Asian Nitrogen Hub project, funded by UKRI.
- Aims to improve nitrogen management in agriculture and assess environmental impacts through multi-section, time-stamped data.
- Data are designed to be linked across household, plots, crops, inputs, management practices, information sources, attitudes, expenditures, assets, and subsidies.
- Structure supports GIS-ready analyses by capturing location, seasonality, and cross-cutting variables (e.g., livestock, inputs, income, assets).

## GIS-relevant data elements by section

### Section 9 — Livestock
- Species owned in the past 12 months (e.g., Cattle, Buffalo, Yak, Goat, Sheep, Camel, Horse, Pig, Poultry) with multiple species possible per household.
- For each species: primary reasons for keeping (e.g., revenue, milk, meat, transport, dowry, ceremonial uses).
- Counts per species and turnover channels (how animals leave the farm: sale, slaughter, gift, theft, etc.).
- Time-based indicators: weeks animals spent in various housing conditions (yard, open house, closed house).
- Cross-species aggregation possible to map herd composition and livestock dynamics spatially at the household level.

### Section 10 — Information Sources
- Attendance at crop demonstrations/trainings in the last 2 years; whether trainings covered fertilizer/manure use.
- Decision-support and information-seeking behavior: primary information sources (family, traders, extension agents, government, media, internet).
- How information informs decisions on fertilizer use and whether farmers keep written records of fertilizer and yield.
- Data can be used to map information access and diffusion patterns geographically and over time.

### Section 11 — Adoption, Drivers and Barriers
- Inventory of selected farm practices/technologies (e.g., decision support tools, green manures, agroforestry, anaerobic digestion, foliar fertilization).
- Awareness vs. current use vs. dis-adoption of each practice.
- Country-specific and potentially regionally augmented practices.
- Enables spatial analysis of adoption hotspots and barriers when linked to location data.

### Section 12 — Attitude, Behaviour, Perception and Opinion
- General propensity to try new technologies and risk tolerance in decision-making.
- Perceived changes needed to alter fertilizer use and beliefs about the benefits/risks of synthetic fertilizer vs. manure.
- Attitudes toward soil, weather, environmental considerations, and farm productivity trade-offs.
- Useful for correlating socio-psychological factors with GIS-driven patterns of technology uptake.

### Section 13 — Expenditure and Income (Excerpt)
- Average monthly household expenditures across categories (food, clothing, education, health, transport, utilities, festivals, savings, debt, etc.).
- Captures consumption patterns and financial stressors that can influence spatial patterns of fertilizer adoption or investment capacity.

### Section 14 — Household Wealth/Asset
- Home ownership status, number of rooms, flooring, lighting, cooking fuel, water sources, communications devices, internet access, access to electricity, and transport ownership.
- Assets as proxies for wealth and access to services; includes inventory of agricultural assets (power tiller, irrigation pump) and financial access (distance to banks, loans, crop insurance, insurance awareness).
- Comprehensive basis for mapping socio-economic status and infrastructure access spatially.

### Section 15 — Subsidy
- Direct subsidies received in the past 12 months (e.g., fertilizer, machinery, irrigation charges, seed, output price support, others).
- Enables spatial assessment of subsidy reach and targeting effectiveness when linked to location.

## Data model and GIS integration considerations
- Linking identifiers: Household IDs to enable per-household GIS features; integration with Section 2–3 plot-level data and Section 4 crop-management data.
- Spatial enablement: Include administrative hierarchies (country, state/province, district, village) and precise geocoordinates or geocoded centroids for households to support per-area mapping.
- Temporal dimension: Multi-year and multi-season data (e.g., Section 9 weeks in housing, Section 10 training within 2 years) for dynamic GIS analyses.
- Coding harmonisation: Standardise species names, practice codes, subsidy categories, and expenditure items; maintain crosswalks for consistent GIS attributes.
- Data quality: Implement range checks, unit harmonisation (areas, costs, quantities), and cross-links between plots, crops, and inputs to ensure reliable spatial analyses.
- GIS outputs: Prepare per-plot or per-household features (points or polygons) with attributes for livestock, practices, information sources, attitudes, assets, and subsidies; enable export to CSV/GeoJSON/Shapefile for visualization.

## GIS product opportunities
- Livestock distribution maps: spatially map species composition and livestock turnover by household across districts.
- Adoption and information diffusion maps: visualize where practices are adopted and how information sources correlate with uptake.
- Asset and wealth mapping: spatial patterns of wealth indicators, infrastructure access, and service proximity.
- Subsidy and input access layers: overlay subsidies, fertilizer/manure access, and credit facilities with farm locations.
- Livestock-management and nutrient-uptake analyses: correlate livestock presence with fertilizer practices and nitrogen management indicators when integrated with crop/plot data.
- Temporal GIS analyses: track changes across seasons and years to monitor evolution of practices, subsidies, and asset ownership.

## Practical implementation notes
- Capture geographic identifiers and, where possible, obtain precise household coordinates to enable robust GIS mapping.
- Develop a robust crosswalk for taxonomy (species, practices, subsidies) to ensure consistent GIS attribute naming.
- Plan data delivery workflows to support GIS use (clean CSV/GeoJSON/Shapefile exports) and seamless integration with existing boundary shapefiles and environmental layers.

## Summary of intended GIS outcomes
- A rich, linkable per-household dataset with cross-sectional and multi-season data on livestock, practices, information access, attitudes, expenditures, assets, and subsidies.
- Enabling map-based visualization and spatial analysis of livestock demographics, nitrogen-management-related practices, information diffusion, socio-economic status, and subsidy distribution across study areas.