# Dataset Originator

- Originator: ECN Data Centre, Centre for Ecology and Hydrology (http://data.ecn.ac.uk; ecn@ceh.ac.uk)
- Owners: UK Environmental Change Network (ECN) partners including multiple UK government departments and agencies (list includes AE, DEFRA, Natural England, NERC, Scottish and Welsh authorities, etc.)
- Use requirement: Acknowledge data use and send one reprint of any publication citing ECN data

## Protocol and aim

- ECN uses standard operating procedures to ensure data comparability across sites.
- Methodology for bat surveys involves mapping bat species with detectors and recording behavior along transects.
- Survey design: transects walked four times per year in four three-week windows; surveys halted in heavy rain or strong winds.
- Limitations: management of links between bat populations and environmental change is constrained; integrating ECN data with broader monitoring helps mitigate limitations.
- Quality: use accompanying quality information when using data; datasets are tracked with metadata and provenance.

## Data structure and key fields

- Data download fields:
  - SITECODE: unique code per ECN site
  - SDATE: sampling date
  - TRANSECT: transect identifier
  - BATLOC_ID: location of bat sighting/hearing (unique per survey date)
  - FIELDNAME: variable measured (see species and habitat codes)
  - VALUE: measured value
  - ACTS: bat seen
  - ACTH: bat heard
  - ACTF: bat feeding buzz heard
- Supporting documentation
  - ECN_BA2.csv: survey conduct details (bat detector type, adjustments, references, analysis methods)
  - ECN_BA3.csv: habitat observations on transects (habitat codes)
  - ECN_BA_qtext.csv: site manager quality notes (textual context affecting data quality)
- Quality and site notes are linked via ECN_BA_qtext.csv; accompanying PDFs provide full methodological context

## Site codes and locations

- Explanatory information – Site Codes (examples):
  - T01 Drayton (52°11'37.95"N 1°45'51.95"W)
  - T02 Glensaugh (56°54'33.36"N 2°33'12.14"W)
  - T03 Hillsborough, T04 Moor House - Upper Teesdale, T05 North Wyke, T07 Sourhope, T08 Wytham, T09 Alice Holt, T10 Porton Down, T11 Y Wyddfa - Snowdon
- Full site list includes coordinates and site names for each ECN site

## Species codes and meanings

- Provided as abbreviated codes with Latin and common names, for example:
  - Bb = Barbastella barbastellus (Barbastelle)
  - Es = Eptesicus serotinus (Serotine)
  - M = Myotis (Myotis spp.)
  - Ms = Myotis bechsteinii
  - Pp = Pipistrellus (Pipistrelle)
  - Ppl = Pipistrellus pipistrellus (Common pipistrelle)
  - Ppg = Pipistrellus pygmaeus (Soprano pipistrelle)
  - Rf = Rhinolophus ferrumequinum (Greater horseshoe)
  - Rh = Rhinolophus hipposideros (Lesser horseshoe)
  - UU = Unidentified bat
  - XX = No bats found
  - And other Myotis, Nyctalus, Plecotus, etc. codes are listed with Latin and common names

## Habitat codes and habitat types

- Habitat coding uses numeric codes 1–43 with descriptive types, including:
  - 1 Hedgerows
  - 2 Treelines (continuous canopy)
  - 3 Treelines (discontinuous)
  - 4 Stone walls
  - 5 Footpaths; 6 Tracks/bridleways; 7 Roads
  - 8 Ditches; 9 Streams (uncanalised)
  - 10 Fast-flowing rivers; 11 Slow rivers
  - 12 Canals
  - 13 Semi-natural broadleaved woodland; 14 Broadleaved plantations; 15 Semi-natural coniferous woodland
  - 16 Coniferous plantations; 17 Semi-natural mixed woodland; 18 Mixed plantation
  - 19 Young plantation; 20 Recently felled woodland
  - 21 Parkland; 22 Tall scrub; 23 Low scrub
  - 24 Beach (dunes, mudflats, shingle)
  - 25 Lowland heaths; 26 Heather moorland
  - 27 Bog; 28 Wet ground
  - 29 Ponds; 30 Lakes
  - 31 Standing man-made water
  - 33 Upland unimproved grassland; 34 Lowland unimproved grassland
  - 35 Semi-improved grassland; 36 Improved grassland
  - 37 Arable; 38 Amenity grassland
  - 39 Rock surfaces; 40 Quarries and open-cast mines
  41 Bare soil; 42 Built land (urban areas, gardens, transport corridors)
  - 43 Others (unspecified)
- These codes allow linking bat observations to habitat context during surveys

## Usage notes and guidance

- Bat detection is conducted with a bat detector, with activity coded as seen (ACTS) or heard (ACTH) or feeding buzz (ACTF)
- Four transect visits per year are spread across defined date windows; weather conditions affect survey viability
- Data quality: relies on accompanying quality notes and standardized protocols to ensure comparability across sites
- Cautions: relationships between bat populations and environmental change are limited by data granularity; linking ECN data to broader monitoring can mitigate

## Access, attribution, and provenance

- Data origin and stewardship are clearly tracked; datasets should be cited with acknowledgment to ECN
- Users are encouraged to consult the accompanying documentation (ECN_BA2.csv, ECN_BA3.csv, ECN_BA_qtext.csv) and the detailed site/species/habitat code lists
- Contact ECN for further information or clarifications on field codes or site-specific details