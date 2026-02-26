# Field practices and biosecurity blackboard pre-training survey

- A comprehensive questionnaire designed to collect field practices and biosecurity practices related to invasive non-native species (INNS) risk, field site work, equipment use, and training.
- Targeted at researchers and field workers across disciplines, including those who may engage in GIS-enabled field mapping and spatial analysis.

## What data the survey seeks to collect

- Demographics and role (e.g., disciplinary area, career stage) to contextualize responses.
- Field activities and sites:
  - Where fieldwork occurs (UK, overseas) and environment types (woodland, freshwater, upland, marine, coastal, urban, agricultural, etc.).
  - Number and frequency of field sites per week; whether multiple sites are visited in a day; travel modes to sites (on foot, vehicle, boat, etc.).
  - Transport and site-access considerations (road use, tyres/wheels cleaning, drying between visits, site re-entry protocols).
- Equipment and sample handling:
  - Use of field equipment, cleaning practices before/after site visits, drying procedures, and cross-site usage.
  - Cleaning methods (hand-picking biomass, rinsing, washing with detergent, disinfection, drying) for equipment, footwear, and outerwear.
- INNS risk and biosecurity:
  - Perceived risk of INNS spreading; awareness of guidance or campaigns; training in biosecurity.
  - Risk assessment requirements for field activities; whether INNS are considered in risk assessments and any mitigation procedures.
  - Practices to avoid cross-site contamination, planning of site visits to minimize INNS spread, supervision practices, and communication of INNS presence to staff.
- Training and guidance:
  - Familiarity with guidance/campaigns and any biosecurity training providers; self-reported training occurrence.
- Open comments:
  - Space for additional remarks on survey experience or biosecurity practices.

## Current data status and scope

- The instrument is extensive, but the presented responses show zero selections across questions, indicating this is an initial or pre-training instrument with no completed responses yet.
- The survey structure anticipates a wide array of field practices, from micro-level cleaning steps to macro-level field planning for INNS risk mitigation.

## Potential GIS-based data products and visualizations

- Field site inventory:
  - Point layers with attributes: site location, environment type, protected/SSSI status, country/region, and frequency of visits.
- INNS risk mapping:
  - Layered maps showing sites with known or suspected INNS presence, and risk scores based on field practices, transport routes, and cleaning adherence.
- Field logistics and contamination risk:
  - Routes and travel modes between sites, with indicators for cleaning before/after travel, tyre/wheel cleaning, and drying regimes.
  - Temporal layers showing when sites are visited and high-risk periods for INNS spread.
- Equipment and hygiene practices:
  - Attribute layers capturing cleaning methods used on equipment, footwear, and outerwear, enabling hotspot analysis of high-risk practices.
- Training and compliance dashboards:
  - Maps or dashboards showing locations of biosecurity training, guidance familiarity, and risk assessment requirements, mapped to sites or teams.
- Decision-support visualizations:
  - Prototypes for planning field campaigns to minimize INNS spread, with recommended sequencing of sites and time windows to reduce risk.

## Data quality, standards, and integration considerations

- Data standardization needed across disciplines to enable consistent GIS analysis (definitions of INNS, cleaning methods, environment types, etc.).
- Data provenance and consent: anonymization where appropriate, clear consent for data use, and ethical handling of location data.
- Integration challenges:
  - Data may come from multiple sources (field notes, equipment logs, training records); require cleaning and harmonization.
  - High-resolution spatial data may be necessary for precise risk assessment and routing analyses.

## Practical guidance for GIS specialists

- Develop a flexible data model:
  - Core entities: FieldSite (location, environment, protection status), Equipment (type, cleaning protocols), FieldVisit (dates, routes, site sequence), INNSPresence (species, risk level), Training (provider, date, status), RiskAssessment (procedures, mitigation).
- Prioritize visualization needs:
  - Interactive maps for stakeholders to explore field sites, INNS risk, and cleaning practices.
  - Dashboards that compare adherence to cleaning protocols across teams and sites.
- Establish data workflows:
  - Clear intake templates aligned with the survey questions to streamline GIS data capture and upkeep.
  - Regular updates to risk maps as new data on INNS presence or training status are collected.
- Align with field operations:
  - Use maps to plan field campaigns that minimize INNS spread (site sequencing, timing, and transport planning).
  - Support training needs by mapping which sites/teams lack biosecurity training or guidance familiarity.

## Next steps and considerations

- Await and incorporate actual survey responses to populate GIS-ready datasets.
- Define a minimum viable GIS data schema based on the survey structure to start prototyping maps and dashboards.
- Establish governance on data sharing, privacy, and consent for location-based data.
- Engage end-users (policy colleagues, field teams) to iterate on visualization designs that best communicate INNS risk and biosecurity practices.