# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- Butterfly Monitoring data from ECN sites, collected under the UK Environmental Change Network programme.
- Data designed for GIS-based mapping and spatial analysis of butterfly populations.
- Field protocol aligns with the national Butterfly Monitoring Scheme; transects are surveyed weekly during spring/summer.

## Data structure and contents
- Core data (download fields):
  - SITECODE: Unique code for each ECN Site.
  - LCODE: Location ID (unique within site).
  - SDATE: Sampling date.
  - SECTION: Transect section ID (transect divided into up to 15 sections).
  - FIELDNAME: Species code (see below).
  - VALUE: Measured variable value (butterfly observations).
  - BROODED: Number of broods recorded (S = single-brooded, D = double-brooded).
- Supporting documentation (ECN_IB2.csv):
  - SHOUR, SMINS: Sampling hour and minutes.
  - RECORDER, RECCODE: Recorder identifiers.
  - TEMP: Temperature.
  - SUNPERC: Percentage of sunshine.
  - WSPEEDB: Wind speed (Beaufort scale).
  - WEEK: Week number.
- Quality information (ECN_IB_qtext.csv):
  - Site-level quality notes with fields for SITECODE, LCODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION.
- Purpose of linked metadata:
  - Site codes, location coordinates, and species codes enable spatial joins and map-based analyses.

## Site metadata (Explanatory information)
- Site codes T01–T12 with:
  - Site name (e.g., Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, etc.).
  - Geographic coordinates (latitude and longitude) for each site.
- Additional context and access:
  - Further site information available at the provided CEH catalogue URL.

## Species codes (Explanatory information)
- Numeric codes mapped to butterfly species:
  - Examples: 10 = Black-veined white (Aporia crataegi), 12 = Dark green fritillary, 100 = Small white (Pieris rapae), 102 = Silver-studded blue, 110 = Grizzled skipper, 122 = Red admiral, 125 etc.
- Full mapping covers a wide range of common and Latin names for British butterflies; some entries include both Latin and common names.

## Data collection protocol
- Standard operating procedures to ensure comparability across sites.
- Data collected using transects on a weekly schedule from 1 April to 29 September.
- Observation method:
  - Butterflies seen flying within or passing through an imaginary 5m x 5m x 5m box in front of the observer are recorded.
- Conditions:
  - Recording typically at 13–17°C if sunshine ≥ 60%; otherwise, recording allowed if not raining (upper limit 15°C at northern upland sites).
- Quality controls:
  - Use accompanying quality information when utilizing the data.
- Source documentation:
  - ib.pdf accompanying the dataset explains data collection in detail.

## GIS relevance and usage
- Spatial components: site coordinates (T01–T12) and location IDs (LCODE) enable precise mapping of survey locations and transect sections.
- Temporal components: date (SDATE) and week (WEEK) support temporal analyses and trend mapping.
- Attribute components: species codes (FIELDNAME) linked to abundance (VALUE) and brood information (BROODED) for population assessments.
- Quality and context: ECN_IB_qtext.csv provides data quality context for site-specific observations and potential data issues.

## Data usage and attribution
- ECN requests acknowledgment of data use to gauge dataset impact and value.
- Request to send one reprint of any publication citing the ECN data.

## Access and additional information
- Supporting site metadata and broader dataset details are available at:
  - https://catalogue.ceh.ac.uk/id/813712d4-d162-4edeaff8-cf1c337bdc27