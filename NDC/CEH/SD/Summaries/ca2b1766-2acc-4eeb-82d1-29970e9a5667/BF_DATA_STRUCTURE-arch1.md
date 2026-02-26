# UK Environmental Change Network (http://www.ecn.ac.uk) Frogs (BF)

## Overview
- Dataset from the UK Environmental Change Network (ECN) Frogs (BF) project.
- Originator: ECN Data Centre; hosted through ECN data portal (data.ecn.ac.uk).
- Owners: ECN programme funded by a consortium of UK government departments and agencies (e.g., Defra, Natural England, NERC, Scottish/Northern Ireland/Welsh authorities, and others).
- ECN requests acknowledgment of data usage and one reprint of any publication citing the data.

## Purpose and Methodology
- Phenology-based protocol: records spawning of Common Frog by counting egg masses in selected pools/ditches as an indicator of frog population health.
- Laboratory analyses on water samples accompany field observations.
- Along with data, accompanying quality information should be used to interpret results.

## Data Structure and Storage
- Data are stored in Oracle databases, split into two main data groups for each site:
  - D1BF_xxx tables: site-level field/egg-mass observations (core dataset).
  - D2BF_xxx tables: site-level laboratory analysis data (water chemistry and related measures).
- Each site has a 4-character site code (xxx) and a site description.
- Core metadata and data structure references:
  - SITECODE, LCODE, FROMDATE, SDATE, FIELDNAME, VALUE fields (core dataset fields).
  - Lab dataset includes SDATE, PHDATE, PHHOUR, PHMINS, FILTDATE, COMPDATE, and related fields.
- Site codes (examples):
  - T01 – Drayton
  - T02 – Glensaugh
  - T03 – Hillsborough
  - T04 – Moor House - Upper Teesdale
  - T05 – North Wyke
  - T06 – Rothamsted
  - T08 – Wytham
  - T09 – Alice Holt
  - T10 – Porton Down
  - T11 – Y Wyddfa - Snowdon
- Date ranges (approximate, site-dependent):
  - Varied from 1994 to 2012 across sites (e.g., Drayton 1994–2012; Snowdon up to 2012; others range 1994–2010/2012).

## Field Names and Measurements
- Broad set of chemical and physical water parameters (examples):
  - Alkalinity (ALKY); Aluminium; Calcium; Chloride; Conductivity (CONDY); Colour; Dissolved Organic Carbon (DOC)
  - Major ions: Ammonium (NH4N); Nitrate Nitrogen (NO3N); Phosphate Phosphorus (PO4P); Potassium; Sodium; Sulphate (SO4S)
  - Metals/trace elements: Iron; Magnesium; Calcium
  - Nutrients and others: Total Nitrogen (TOTALN); Total Dissolved Phosphorus (TOTALP)
  - Water quality and physical parameters: pH (PH, PH readings and QA), Depth; Surface Area (SURFAREA); Spawn/date-related metrics (SPAWNDATE, CONGDATE, LEAVEDATE, HATCHDATE)
  - Frog-specific metrics: NEWMASS (new spawn masses); CONGDATE (first congregation date); SPAWNDATE (first spawning date); PERCDEAD (percentage dead/diseased eggs); SPAWN-related counts
  - Temperature metrics: MAXTMP (max temp), MINTMP (min temp)
- Quality/data-flag fields: Q1–Q8 (quality codes corresponding to data quality aspects)
- Field lists include a wide range of additional fields (e.g., VOLUME, VACUUM, etc.) to support sample metadata and lab processing details.

## Quality Codes and Data Quality
- ECN quality codes are assigned by site managers to indicate data quality factors.
- Codes are drawn from a standard ECN list; a code of 999 indicates an unusual event with explanatory text.
- Typical code range and purpose:
  - 100–199: No information/time lost, sampling issues, or equipment problems
  - 200–299: Environmental or sampling-related issues during collection
  - 500–512: Laboratory-related issues or data processing concerns
  - 999: Unusual event (text explanation accompanies the dataset)
- Examples cover issues such as equipment failure, sample loss, contamination, weather disruptions, and other field/lab conditions.

## Data Access, Use, and Provenance
- Data reside in the ECN Oracle database and are organized per site with core and lab datasets.
- Metadata and accompanying quality information are provided to aid discovery and proper interpretation.
- Users are encouraged to reference data provenance and to share results back with ECN (e.g., reprints) to demonstrate data value.

## Practical Considerations for Analysts
- Data integration: be prepared to unify D1BF (field observations) and D2BF (lab analyses) across multiple sites with potentially different date ranges.
- Data cleaning: utilize the embedded quality codes and accompanying quality text for filtering and interpretation.
- Documentation: track data sources and maintain metadata to support reproducibility and portal discoverability.
- Modelling and analysis: combine phenology indicators (egg masses, spawning dates) with water quality measurements to explore correlations, temporal trends, and potential predictive relationships related to environmental change.
- Reporting: present findings with clear charts and explicit conclusions, acknowledging data quality constraints where relevant.