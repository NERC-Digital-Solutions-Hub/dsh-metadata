# Collection/generation methods: Study sites

- Overview
  - Longitudinal monitoring of an approximately 35 km urban–non-urban gradient from Glasgow city centre to Loch Lomond National Park, Scotland.
  - Years monitored: 2014–2022; 5–20 sites per year.
  - Target species: blue tit (Cyanistes caeruleus) and great tit (Parus major).
  - Productivity measured via breeding attempts recorded in nestboxes.

- Study design and sampling
  - Nestboxes monitored annually from 1 April to 20 June.
  - Key breeding data collected: date of first egg, clutch size; incubation status used to time checks to minimize disturbance.
  - Post-hatching: intensified checks 2–10 days after hatch; attempts to catch breeding adults on the nest 13 days after hatching.
  - Off-season data: opportunistic mist netting at both study sites to supplement mark–recapture data and bycatch data for other passerines.

- Data collection protocol
  - Morphometrics collected: wing length, weight, tarsus length, fat score, and other measurements.
  - Ringing and marking: adults marked with metal rings (or ring number noted); nestlings marked at 13 days old.
  - RFID and radio tagging: records include whether RFID or radio tags were fitted, and their identifiers.
  - Data capture details: includes observer initials, date, time, nestbox location, and nestling/egg details where applicable.
  - Data linkage: annual data are uploaded to a central long-term Access database enabling linkage between reproductive attempts and individual birds; data deposited with the EIDC.

- Data management and quality control
  - Year-end quality control: data checked and uploaded to a central database.
  - Central repository structure: supports linking of reproductive attempts to individual mark–recapture records.

- Data structure and content (Table 1 and Table 2)
  - Table 1: Capture event records with fields such as
    - ID (unique record number), year, retrap status (N for new, R for retrapped, C for known, X for found dead, U for unknown)
    - ring_number (BTO ring), species (5-letter codes; e.g. bluti for blue tit, greti for great tit), age (BTO code with X added for certain nestling deaths), sex (U/M/F), date and time of capture
    - site (multiple site names or grid reference), wing (mm), weight (g), initial (processor initials), moult code, tarsus (mm), fat score
    - chicks_alive and chicks_ringed (only if age code = 1), nestbox_number, notes
    - chick_age, father_ring, mother_ring, RFID_fitted, RFID_number, radio_tag_fitted, radio_tag_ID
    - colour_left_up/colour_left_down/colour_right_up/colour_right_down (colour ring codes)
    - CES_visit_number (week number of Constant Effort Site visit), notes on colour rings, old_greater_coverts (count), muscle score, and other related fields
    - Additional fields capture nestling details, parent information, and various tags/observations
  - Table 2: BTO age codes with definitions and coding nuances
    - Codes 0–6 with explicit meanings (e.g., 0 = age unknown; 1 = pullus; 2 = fully grown with unknown hatch year; 3 = definitely hatched in current year; 4–6 = progressively older categories)
    - Special codes for passerines (1J, 3J*, 5J) indicating fledging status or juvenile plumage
    - Notes on crosswalk to BWG and ESF scales (e.g., ESF equivalents for BWG scores)
  - Fat score references
    - Descriptions and natural language mappings for no visible fat to fully fat reserves, with BWG/ESF equivalents
    - Includes notes on how fat scores relate to muscle and other body condition indicators
  - Data standards and references
    - Data terminology and coding follow standards from the Ringers’ Manual (Redfern & Clark, 2001) and BTO guidelines
    - Species codes and age codes linked to BTO resources and documentation

- Accessibility and storage
  - Data linked within a central long-term Access database for longitudinal tracking
  - Deposited with the Endangered and Invasive Species Data Centre (EIDC) for broader access and archiving

- Bibliography
  - Redfern, C.P.F. & Clark, J.A. (2001) Ringers’ Manual. British Trust for Ornithology.