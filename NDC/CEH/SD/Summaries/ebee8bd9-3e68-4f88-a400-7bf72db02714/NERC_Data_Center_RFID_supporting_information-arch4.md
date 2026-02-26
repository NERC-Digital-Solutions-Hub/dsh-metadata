# Supporting information for: Movement of songbirds between supplementary feeders in urban neighbourhoods in Southern England, UK

## Overview
- Dataset accompanying a study on movement of feeder-using songbirds in Southern England.
- Birds fitted with PIT tags visited RFID-enabled feeders; seven species recorded; Blue tits and Great tits were most abundant.
- Data collected in three towns over 14 months (1 July 2013 – 31 August 2014); initial setup period of two months, followed by main data collection in the remaining 12 months.

## Data assets
- NERC_Data_Centre_RFID_raw_data.txt: tag (unique PIT ID), site and garden of feeder visited, time and date of visit.
- NERC_Data_Centre_ringing_data.txt: ringing subsite, capture date, age (BTO aging), sex, and gender for each tag.
- NERC_Data_Centre_Coordinates.txt: coordinates for relative positions of each feeder and ringing site; details in supporting documentation.
- Data are linked to a single overarching study and accompanied by supporting docs for metadata.

## Methodology and data collection
- Hardware and setup:
  - RFID reader and antenna integrated into feeder perches; custom Arduino-based construction.
  - Antennas approx. 40 mm × 32 mm; 125 kHz.
  - Data logging records time/date and tag ID; 400 ms recording on, 400 ms pause; 4 GB memory per log.
  - Power supplied by 12 V battery with 24/7 operation.
- Study design and site setup:
  - Each network comprised 17 RFID feeding stations; 51 stations total.
  - Stations in private gardens, average 81 m apart (±20 m SD); feeders placed ~0.5 m from cover when possible.
  - Gardens volunteered for participation; feeders installed ~6 weeks before data collection to allow familiarisation.
  - All stations operational from 1 Sept 2013 to 31 Aug 2014.
- Data collection process:
  - Each feeding station included feeder, RFID reader, antenna, power source, stand, and squirrel baffle; bottom suspended ~1 m above ground.
  - Seed type kept constant across feeders.
  - Maintenance: researcher visited stations every 30 days to replace batteries and download data.
- Bird capture and tagging:
  - Birds caught in private green spaces at two locations per network; effort maximised for catching blue tits and great tits.
  - Mist nets and tape lures used; birds ringed (BTO metal) and fitted with PIT tags (8 mm ring, molded PIT tag).
- Documentation and publication:
  - Primary analysis and conclusions reported in Cox et al. (2016) and related Scientific Reports publication.

## Data governance, provenance, and reuse
- Citation and access:
  - Dataset citation: Cox, D.T.C.; Gaston, K.J. (2018). Movement of feeder-using songbirds: the influence of urban form. NERC Environmental Information Data Centre. DOI provided.
  - Full details available via the DOIs linked in the dataset description.
- Provenance and structure:
  - Three linked data files (RFID raw data, ringing data, coordinates) that connect visitor events to individual birds via unique tag IDs.
  - Metadata and supporting documentation describe how to interpret coordinates and linking between datasets.

## Relevance for data leadership and data systems
- Demonstrates end-to-end data lifecycle: instrument design, data capture, storage (4 GB per logger), monthly data downloads, and linkage to biological metadata (ringing data).
- Highlights the importance of:
  - Clear data structures and unique identifiers to enable linking across datasets (tag IDs, site/garden IDs).
  - Comprehensive metadata, including coordinates and installation context, to support spatial analyses and reproducibility.
  - Documentation and citation trails to facilitate reuse and attribution.
- Useful for cross-network coordination, data standardization, and interoperable urban ecology datasets.