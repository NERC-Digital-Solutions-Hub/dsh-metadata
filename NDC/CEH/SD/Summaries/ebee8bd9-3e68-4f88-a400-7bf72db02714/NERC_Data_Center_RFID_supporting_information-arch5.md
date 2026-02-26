# Supporting information for: Movement of songbirds between supplementary feeders in urban neighbourhoods in Southern England, UK

## Overview
- Dataset describes visits of PIT-tagged songbirds to RFID-enabled feeders.
- Seven species studied; Blue tits and Great tits were most abundant.
- Location: three towns in Southern England; period: 14 months (1 July 2013 – 31 August 2014); setup period first two months, main data collection in the following 12 months.
- Data intended for reuse and citation; available via the NERC Environmental Information Data Centre.

## Datasets and contents
- NERC_Data_Centre_RFID_raw_data.txt: bird tag, feeder site and garden, with time and date of each visit.
- NERC_Data_Centre_ringing_data.txt: ringing information per tag (ringing subsite, capture date, age per BTO aging system, sex/gender).
- NERC_Data_Centre_Coordinates.txt: coordinates showing relative positions of each feeder and ringing site (also noted in supporting documentation).
- 3 files collectively capture visitation events, bird identification, and spatial relationships among feeders and ringing sites.
- Access details: dataset citation and DOI provided; full details at the listed DOI links.

## Data collection and methods
- Hardware: RFID readers with antennae embedded in perches of standard seed feeders; custom Arduino-based components; 125 kHz frequency.
- Recording: data-loggers capture time, date, and tag ID; sampling pattern of 400 ms recording / 400 ms pause.
- Power: 12 V battery powering readers for 24/7 operation.
- Network design: 51 feeding stations across 17 networks; stations located in private gardens, average inter-station distance ~81 m.
- Setup: feeders installed 0.5 m from vegetation cover; gardens used with resident involvement; feeders installed 6 weeks before data collection.
- Maintenance: researchers conducted monthly visits (every 30 days) to replace batteries and download data.
- Species tagging: birds captured using mist nets and lures, ringed with BTO metal rings and PIT tags (8 mm ring with PIT).
- Scope: data collection period encompassed in 51 operational stations from 1 Sep 2013 to 31 Aug 2014.
- Related publication: data analysis and conclusions published in Cox et al. 2016.

## Access, reuse, and licensing
- Dataset citation: Cox, D.T.C.; Gaston, K.J. (2018). Movement of feeder-using songbirds: the influence of urban form. NERC Environmental Information Data Centre. DOI provided.
- Full dataset details available at the provided URLs; data are stored as text files described above.
- Reuse notes: data are structured to enable linking RFID visitation events with ringing data and spatial coordinates; users should reference the original publication for analysis context.

## Data governance considerations for Data Stewards
- Metadata and data dictionaries: ensure clear descriptions of fields (tag, site, garden, time/date, age, sex, coordinates).
- Data quality: verify alignment between RFID raw data and ringing data (tag IDs, capture dates, age classification).
- Provenance and lineage: maintain clear linkage to the Cox et al. (2016) analysis and the 2018 data-centre citation; record collection period, station details, and maintenance schedule.
- Formats and interoperability: three plain-text files; consider providing a data dictionary and, if possible, a machine-readable metadata file to improve interoperability.
- Availability and updates: data spans Sep 2013–Aug 2014; ongoing updates are not indicated; ensure clear notes on versioning and any data corrections.
- Access controls and licensing: dataset is published with a formal citation and DOI; maintain attribution guidance and accessibility through the NERC Environmental Information Data Centre.

## Provenance and related publications
- Principal investigator/data collector: Dr. Daniel T. C. Cox.
- Analysis/publication: Cox et al. (2016) Scientific Reports; Movement of feeder-using songbirds: the influence of urban form.
- Data centre hosting and licensing details available via linked DOIs.