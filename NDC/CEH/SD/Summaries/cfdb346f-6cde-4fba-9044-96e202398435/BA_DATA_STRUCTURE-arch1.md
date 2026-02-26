# UK Environmental Change Network (http://www.ecn.ac.uk) Bats (BA)

## Overview
- Observational dataset of bat species along transects as part of the UK Environmental Change Network (ECN).
- Bat species mapped using bat detectors; bat behaviour recorded on transects.
- Methodology based on the Bats and Habitats survey (University of Bristol, JNCC) and linked to ECN monitoring programs.
- Transects are walked four times per year (in four three-week windows) with surveys avoided during heavy rain or strong winds.
- Acknowledges limitations in relating population levels to environmental change; data are enhanced by linking to other monitoring programs.
- Accompanied by quality information to inform data use.

## Data Origin, Ownership, and Acknowledgement
- Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology.
- Dataset Owners: ECN program funded by a consortium of UK government departments/agencies (list includes Defra, Natural England, Environment Agency, NERC, Scottish Government, Welsh Government, etc.).
- Acknowledgement: Users should acknowledge ECN data and send one reprint of any publication citing the data.
- Protocol Reference: ECN Measures for terrestrial bats (BA) protocol URL provided.

## Survey Protocol and Limitations
- Survey approach: Bat species detected/heard along transects; behavior recorded.
- Four surveys per year across specified periods; surveys not conducted in heavy rain or strong winds.
- Limitations: limited detail on precise population-environment relationships; mitigation via integration with broader monitoring programs.
- Data users should consult accompanying quality information for proper use.

## Data Structure (Core Observation Data)
- Stored in Oracle database as 10 tables per site (D1BA_xxx; site code xxx).
- D1BA_xxx (Core observations) fields include:
  - SITECODE, SDATE (sampling date), TRANSECT (transect), BATLOC_ID (location of bat sighting/hearing), FIELDNAME (bat species code), VALUE (count), ACTS (bat seen), ACTH (bat heard), ACTF (bat feeding buzz heard).
- Data are organized by site codes (example site tables: D1BA_T01, D1BA_T02, etc.).

## Data Structure (Survey Metadata)
- D2BA_xxx (Survey metadata) fields include:
  - BATDETECTORTYPE (detector used), KEPTPROTOCOLFREQUENCY, ADJUSTFREQUENCY, USEREFERENCECD, USESONOGRAMANALYSIS (whether sonogram analysis was used), plus related indicators.
- These describe how the survey was conducted and equipment/protocol choices.

## Data Structure (Habitat Observations)
- D3BA_xxx (Habitat data) fields include:
  - SITECODE, SDATE, TRANSECT, BATLOC_ID, HAB1/HAB2/HAB3 (habitat types observed near sighting), FIELDNAME (habitat code), VALUE (habitat code value).
- Habitat codes and descriptions are provided in the VALUE field for HAB1–HAB3.

## Site Codes and Dataset Range
- T01 Drayton; location coordinates and date range: 29-JUN-1993 to 05-SEP-2006.
- T02 Glensaugh; coordinates and date range: 07-JUL-1994 to 30-AUG-2012.
- T03 Hillsborough; coordinates and date range: 12-AUG-1994 to 05-SEP-2002.
- T04 Moor House - Upper Teesdale; coordinates and date range: 16-JUN-1993 to 28-AUG-2012.
- T05 North Wyke; coordinates and date range: 04-JUL-1993 to 30-AUG-2012.
- T07 Sourhope; coordinates and date range: 12-JUL-1994 to 03-SEP-2012.
- T08 Wytham; coordinates and date range: 05-JUL-1993 to 21-AUG-2012.
- T09 Alice Holt; coordinates and date range: 29-JUN-1994 to 05-SEP-2012.
- T10 Porton Down; coordinates and date range: 04-JUL-1994 to 03-SEP-2006.
- T11 Y Wyddfa – Snowdon; coordinates and date range: 16-JUL-1996 to 31-AUG-2011.

## Bat Species Codes (Fieldname in D1BA_xxx)
- Bb Barbastella barbastellus
- Es Eptesicus serotinus
- M Myotis (Myotis spp.)
- Ms Myotis bechsteinii
- Mb Myotis brandtii
- Md Myotis daubentonii
- Mm Myotis myotis
- Mw Myotis mystacinus
- Mn Myotis nattereri
- XX No bats found
- Nl Nyctalus leisleri
- Nn Nyctalus noctula
- Pp Pipistrellus (Pipistrellus spp.)
- Ppl Pipistrellus pipistrellus (Common pipistrelle)
- Ppg Pipistrellus pygmaeus (Soprano pipistrelle)
- P Plecotus (Long-eared spp.)
- Pa Plecotus auritus
- Pg Plecotus austriacus
- Rf Rhinolophus ferrumequinum
- Rh Rhinolophus hipposideros
- UU Unidentified bat

- Up to three habitat types recorded per sighting:
  - HAB1, HAB2, HAB3 (described below)

## Habitat Types (Codes in Habitat VALUE)
- 1: Hedgerows
- 2: Treelines
- 3: Treelines (discontinuous/spread)
- 4: Stone walls
- 5: Footpaths
- 6: Tracks/bridleways
- 7: Roads
- 8: Ditches
- 9: Streams
- 10: Fast-flowing rivers
- 11: Slow-flowing rivers
- 12: Canals
- 13: Semi-natural broadleaved woodland
- 14: Broadleaved plantations/orchards
- 15: Semi-natural coniferous woodland
- 16: Coniferous plantations
- 17: Semi-natural mixed woodland
- 18: Mixed plantation
- 19: Young plantation
- 20: Recently felled woodland
- 21: Parkland
- 22: Tall scrub
- 23: Low scrub
- 24: Beach (dunes, flats, shingle)
- 25: Lowland heaths
- 26: Heather moorland
- 27: Bog
- 28: Wet ground
- 29: Ponds
- 30: Lakes
- 31: Standing man-made water
- 33: Upland unimproved grassland
- 34: Lowland unimproved grassland
- 35: Semi-improved grassland
- 36: Improved grassland
- 37: Arable
- 38: Amenity grassland
- 39: Rock surfaces
- 40: Quarries/open-cast mines
- 41: Bare soil/unvegetated ground
- 42: Built land
- 43: Others (unspecified)

## Data Access, Quality, and Use
- Data are stored in an Oracle database with site-specific tables and accompanied by core metadata and quality information.
- The ECN encourages linking the bat data with broader monitoring programs to mitigate method limitations.
- Data and metadata are intended to be discoverable via portals with descriptive metadata.

## Practical Takeaways for Analysts
- The BA dataset provides time-series bat detections/hearings and behaviors across multiple UK sites from 1993–2012.
- Observations are coupled with detector type and survey protocol, enabling reproducibility and method-consistency checks.
- Species-level counts are encoded by field names (FIELDNAME) with standardized bat codes; habitat context is captured via HAB1–HAB3 codes.
- Researchers can model correlations between bat activity, detector settings, habitat types, transect location, and temporal factors, while controlling for survey conditions recorded in D2BA_xxx.
- Data provenance and usage constraints (acknowledgement and publication reprint) are explicitly specified.