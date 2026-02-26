# ECN Breeding Bird Survey Data Description

## Overview
- ECN Data Centre (Centre for Ecology and Hydrology) is the dataset originator; ECN is sponsored by a consortium of UK government departments and agencies.
- Purpose: support monitoring of environmental health to scrutinise policy, understand causes and consequences of environmental change, and inform future decisions.
- Dataset usage requests: acknowledge data usage and provide one reprint of any citing publication.

## Governance and Stewardship
- Data owners include multiple UK government departments and agencies (e.g., Defra, Natural England, Scottish Government, Environment Agency, NERC, etc.).
- Protocols: ECN has standard operating procedures to ensure data comparability across sites; accompanying bb.pdf explains data collection.
- Data sharing and metadata: data should be shared with accompanying quality information; data governance and openness standards are expected at the data source.
- Data quality: data are quality assured, cleaned, transformed, analyzed, and reported clearly (reports, charts, dashboards).
- Data dissemination: outputs shared with stakeholders; ongoing consultation; data sharing of underlying datasets as appropriate.

## Data Content and Structure
- Primary dataset: Breeding Bird Survey data collected via transects within 1 km squares; each bird observation includes distance from transect.
- Methodology: Breeding Bird Survey conducted according to British Trust for Ornithology (BTO) protocols; transects walked twice per year; designed for national-scale monitoring (site data limited for detailed ecological relationships).
- History: Originally used Common Bird Census (lowland) and Moorland Bird Survey (upland); Breeding Bird Survey replaced both at ECN sites.

### Data Download Schema
- SITECODE: unique ECN site code
- LCODE: location ID (unique with site)
- VISIT: early (E) or late (L)
- SDATE: sampling date
- TRANSECT: transect identifier
- FIELDNAME: bird species code
- VALUE: count of birds observed
- DISTANCE: distance category from transect (1 = within 25 m, 2 = 25–100 m, 3 = >100 m)
- F: field flag indicating in-flight observation

### Supporting Documentation
- ECN_BB2.csv: survey timing, weather (CLOUD, RAIN, WIND, VISIBILITY)
- ECN_BB3.csv: habitat information by transect (FIRSTHL and SECONDHL codes; multiple levels)
- ECN_BB_qtext.csv: site-level quality notes (text explanations; applicable dates and ongoing status)

### Site Codes and Locations
- Explanatory site codes (e.g., T01 Drayton, T02 Glensaugh, T03 Hillsborough, T04 Moor House, T05 North Wyke, T06 Rothamsted, T07 Sourhope, T09 Alice Holt, T10 Porton Down, T11 Snowdon, T12 Cairngorms) with geographic coordinates.
- Additional information available at ECN catalogue link.

### Bird Species Codes
- Extensive mapping of two-letter species codes to common and scientific names (e.g., AC = Arctic Skua/Arctic Tern, BB = Blackbird, BK = Black Grouse, etc., including XX for No Birds Present and YW for Yellow Wagtail).
- Purpose: enable standardized recording across sites and time.

### Habitat Codes
- BTO habitat recording system:
  - Level 1: main habitat type (A–J)
  - Level 2: category within main habitat
  - Levels 3–4: subcategories and habitat features (e.g., disturbance, shrub layer, dead wood, grazing, proximity to roads, etc.)
- Examples include:
  - A – WOODLAND with Level 2–4 codes detailing composition, disturbance, shrub/field layers, dead wood presence
  - B – SCRUBLAND/young woodland, C – Semi-natural Grassland/Marsh, D – Heathland/Bogs, E – Farmland, F – Human Sites, G – Water Bodies, H – Coastal, I – Inland Rock, J – Miscellaneous
- Levels 2–4 codes provide granular habitat descriptors to support environmental association analyses.

## Usage Notes and Limitations
- Data are designed for national-scale monitoring; site-level analyses for environmental drivers require integration with other data sources (e.g., broader BTO datasets).
- Data should be used in conjunction with accompanying quality metadata to assess suitability for specific analyses.
- Initial bird monitoring programs existed prior to ECN; ECN Bird Survey data superseded those earlier protocols at ECN sites.

## Data Access and Communication
- Data access is accompanied by specific metadata and quality information; public sharing of underlying data is part of governance requirements.
- The dataset encourages clear communication of complex findings and transparent data governance to facilitate reuse by policymakers and researchers.

## Challenges and Considerations for Monitoring Frameworks
- Common challenges applicable to this dataset:
  - Data gaps or limited data at site-level specificity for certain analyses.
  - Access constraints and the need to coordinate across multiple organisations (silos).
  - Requirement to publicly share datasets can hinder use of some data.
  - Metadata quality and completeness vary; ensuring robust metadata is essential for reuse.
  - Data formats require transformation for integration with other datasets (standardisation of fields and codes).
  - Communicating complex results clearly to stakeholders; establishing governance for data storage, sharing, and updating.