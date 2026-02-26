# Collection/generation methods: Study sites

## Overview
- Monitoring an approximately 35 km urban–non-urban gradient from Glasgow city centre to Loch Lomond National Park, Scotland.
- Annual monitoring conducted 2014–2022 with 5–20 sites per year.
- Focus on blue tit (Cyanistes caeruleus) and great tit (Parus major) nestbox populations; productivity assessed via breeding attempts.

## Study design and sites
- Gradient extremes: Glasgow city centre and Loch Lomond National Park.
- Sites varied yearly (5–20) to cover the gradient; data linked to a central long-term database and deposited with EIDC.

## Species and sampling period
- Nestbox monitoring during the breeding season: 1 April to 20 June (2014–2022).
- Productivity measured through breeding attempts, first-egg date, and clutch size.
- Opportunistic mist netting outside the breeding season supplements mark-recapture data and bycatch data for other passerines.

## Field procedures and measurements
- Nestbox monitoring:
  - Weekly checks from 1 April until incubation begins; incubation date and clutch size recorded.
  - After incubation starts, avoid disturbance; return inspections 14 days after incubation begins; then every other day until chicks are observed.
  - Adults captured on the nest around 13 days after hatching; marked with a unique metal ring or recorded ring number from prior years.
  - Nestlings marked within broods around 13 days post-hatching.
- Mist netting:
  - Conducted outside the breeding season at both study sites; provides mark-recapture data and bycatch information for other passerines.
- Measurements and data collected:
  - Morphology: Wing length (mm), Weight (g), Tarsus length (mm).
  - Ringing and tagging: Ring details (BTO), RFID and radio tagging status and identifiers.
  - Additional fields: Date, time, site, nestbox number, sex (based on brood patch/cloacal protrusion during breeding; plumage outside breeding), moult, fat score, Ces visit number, notes on rings and colours, parental IDs, and chick counts (alive/ringed).

## Data management and quality control
- End-of-year data are checked and uploaded to a central long-term Access database enabling linking between reproductive attempts and mark-recapture data.
- Datasets and records are deposited with the EIDC.
- Quality control: annual data verification and upload to the central database; explicit data-structure documentation to ensure consistency.

## Data structure and variables
- Table 1 (capture events):
  - Key fields: ID, year, retrap code (N/R/C/X/U), ring_number, species code, age code (BTO), sex, date, time, site, wing, weight, initial, moult, tarsus, fat, chicks_alive, chicks_ringed, nestbox_number, notes, chick_age, father_ring, mother_ring, RFID_fitted, RFID_number, radio_tag_fitted, radio_tag_ID, colour_left_up/down, colour_right_up/down, CES_visit_num, notes_colour, old_greater_coverts, muscle score, etc.
- Table 2: BTO age codes
  - Definitions for ages 0–6 and variants (e.g., 1J, 3J) with notes on accuracy and plumage stage.
- Fat score references:
  - Codes describing fat reserves from no fat to full fat using BWG/ESF standards; linked to Redfern & Clark fat score descriptions and figure references.

## Data standards and references
- Fat score and age coding follow BTO and BWG/ESF equivalence guidelines.
- Primary references: Redfern, C.P.F. & Clark, J.A. (2001) Ringers' Manual; related fat-score documentation and figure/code references.
- Data provenance documented via links to ringing records and standardized coding (BTO species and age codes).

## Relevance to environmental monitoring
- Enables linking reproductive success, individual life histories, and population dynamics across an urban–rural gradient.
- Standardized data collection and long-term storage support analysis of environmental health, habitat effects, and population trends.
- Facilitates sharing underlying data (ringing, morphometrics, capture histories) for broader environmental and policy assessments.