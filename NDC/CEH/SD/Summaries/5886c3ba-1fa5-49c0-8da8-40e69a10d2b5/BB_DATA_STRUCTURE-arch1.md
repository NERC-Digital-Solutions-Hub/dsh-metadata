# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- UK Environmental Change Network (ECN) dataset from the Breeding Bird Survey.
- Method: birds recorded on transects within 1 km squares, with distance from transect noted.
- Transects walked twice per year; survey designed for national-scale insights.
- Site-based data are limited for pinpointing precise relationships between populations and environmental change; recommended to use alongside broader programs (e.g., BTO data) to mitigate limitations.

## Dataset provenance and owners
- Originator: ECN Data Centre, Centre for Ecology and Hydrology.
- Sponsors: consortium of UK government departments/agencies funding site monitoring or network coordination (e.g., BBSRC, Defra agencies, Natural England, SEPA, etc.).
- Usage acknowledge and publication: acknowledge data use and send one reprint of any citing publication.

## Protocol and data comparability
- Standard operating procedures to ensure comparability across ECN sites.
- See accompanying bb.pdf for data collection explanations.
- Used to ensure consistent, cross-site data quality and comparability.

## Usage notes
- Birds recorded on transects with distance categories (within 25 m, 25–100 m, >100 m; in flight noted separately).
- Methodology aligned with the Breeding Birds Survey (BTO).
- Two visits per site per year (early and late); site-level data limited for direct population-environment links.
- Data should be used with accompanying quality information to understand data reliability.

## Data structure and download fields
- Core fields in ECN_BB1/ECN_BB.csv:
  - SITECODE: unique ECN site code
  - LCODE: location ID (unique with site)
  - VISIT: early (E) or late (L)
  - SDATE: sampling date
  - TRANSECT: transect identifier
  - FIELDNAME: bird species code
  - VALUE: count of birds observed
  - DISTANCE: distance category code
  - F: bird in flight (any distance)

- Supporting documentation:
  - ECN_BB2.csv: survey timing and weather data (start/end times, CLOUD, RAIN, WIND, VISIBILITY)
  - ECN_BB3.csv: habitat context per transect (FIRSTHL and SECONDHL levels 1–4)
  - ECN_BB_qtext.csv: site-level quality text attachments (date ranges, field affected, and ongoing status)

## Site and species/habitat codes (Explanatory information)
- Site codes (examples):
  - T01 Drayton; T02 Glensaugh; T03 Hillsborough; T04 Moor House - Upper Teesdale; T05 North Wyke; T06 Rothamsted; T07 Sourhope; T09 Alice Holt; T10 Porton Down; T11 Snowdon; T12 Cairngorms.
  - Coordinates provided; full list available in documentation.
- Bird species codes and names: extensive crosswalk between short codes (e.g., AC, AF, BL, etc.) and full species names (e.g., Arctic Skua, Arctic Tern, Blackbird, etc.).
- Habitat codes:
  - Level 1: main habitat category (A–J), e.g., A = Woodland, B = Scrubland, C = Semi-natural Grassland/Marsh, etc.
  - Level 2: subtype (e.g., A > Broadleaved woodland; B > Regenerating scrubland; C > Grassland/marsh; etc.).
  - Level 3 and Level 4: detailed habitat features (e.g., coppice, disturbance, shrub layer density, grazing, boundary features, water body type, etc.).
- Quality notes: site managers can attach text explaining data quality circumstances (effective dates, duration, continuing impact).

## Access, metadata, and reporting
- Data sources are tracked; datasets can be uploaded with metadata to portals to improve discoverability.
- Researchers are encouraged to cite ECN data and include a reprint of publications citing the data.