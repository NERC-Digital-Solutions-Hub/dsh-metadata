# UK Environmental Change Network (ECN) bird data: 1995-2012

## Overview
- ECN bird data cover 1995–2012 from the UK Environmental Change Network, funded by a consortium of UK government departments and agencies.
- Data aim to understand environmental change through bird monitoring, using Breeding Birds Survey (BBS) methodology and site-specific observations.
- Data usage should acknowledge ECN and, where possible, include one reprint of any citing publication.

## Data Collection and Scope
- Birds are recorded on transects within 1 km squares; distance from transect is recorded.
- Transects are walked twice per year; methodology follows the BBS organized by the British Trust for Ornithology (BTO).
- ECN site data are designed for national-scale survey context and have limited detail on precise population–environment relationships; recommended to combine ECN data with broader monitoring programs (e.g., BTO data) to mitigate limitations.
- At program start, two other bird protocols were used (Common Bird Census and Moorland Bird Survey); these were replaced by the BBS approach.
- Metadata accompany the data to enable quality assessment and reproducibility.

## Data Structure and Coding
- Core data structure:
  - SITECODE, LCODE, VISIT (E = early, L = late), SDATE, TRANSECT, FIELDNAME (bird species code), VALUE (count), DISTANCE (category), with F representing birds observed in flight.
- Distance categories:
  - 1 = within 25 m of transect
  - 2 = between 25 and 100 m
  - 3 = greater than 100 m
  - F = in flight
- Additional metadata tables:
  - ECN_BB2.csv: observation timing and weather (FROM_HOUR, FROM_MINS, TO_HOUR, TO_MINS; CLOUD, RAIN, WIND, VISIBILITY)
  - ECN_BB3.csv: transect habitat observations (YEAR, TRANSECT, FIRSTHL1–FIRSTHL4, SECONDHL1–SECONDHL4; habitat codes by levels 1–4)
- Habitat coding system (BTO):
  - Level 1: single code A–J (main habitat type)
  - Level 2: subcategory within Level 1 (e.g., A: woodland → 1 Broadleaved, 2 Coniferous, etc.)
  - Levels 3 and 4: more detailed descriptors of habitat features (e.g., coppicing, disturbance, shrub density, dead wood)
- Site codes:
  - T01 to T12 with site names and geographic coordinates, plus date ranges for each site (e.g., T01 Drayton; T12 Cairngorms). Date ranges span 1995–2012 across sites.
- Bird species codes:
  - Comprehensive two-letter codes mapping to species names (e.g., AC for Arctic Skua, AE for Arctic Tern, etc.), covering a wide range of passerines, waterbirds, raptors, and other taxa.
- Data quality and accompanying information:
  - Quality information must be used when analyzing ECN data.
  - Data are designed to be used with accompanying metadata to ensure proper interpretation and reproducibility.

## Site Coverage
- Multiple UK sites included (examples: Drayton, Glensaugh, Hillsborough, Moor House – Upper Teesdale, North Wyke, Rothamsted, Sourhope, Alice Holt, Porton Down, Snowdon, Cairngorms) with varying observation periods within 1995–2012.
- Each site has specific geographic coordinates and end dates for data collection.

## Usage Guidance and Limitations
- Data are best used in conjunction with broader, more uniform monitoring datasets (e.g., BTO) to mitigate limitations of site-based, coarse-resolution relationships.
- Datasets should be used with their accompanying quality and habitat metadata to contextualize observations and enable robust analyses.
- For reproducibility, maintain provenance by tracking data sources and metadata (e.g., ECN_BB2.csv, ECN_BB3.csv) and cite ECN data accordingly.

## Access and Acknowledgment
- ECN Data Centre (Centre for Ecology and Hydrology) provides data and contact information (ecn@ceh.ac.uk; http://data.ecn.ac.uk).
- Acknowledge data use and share citations, including sending a reprint of any publication citing ECN data.